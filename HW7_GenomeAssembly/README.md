# hse22_hw1

Полыгалов Богдан, 2 группа

Содержание:
1. Результаты основной части
   - Все команды
   - Скриншоты и статистика
   - Код анализа данных
   - Вывод
2. Результаты бонусной части
   - Все команды
   - Скриншоты и статистика
   - Код анализа данных
   - Вывод
3. Сравнение

# Результаты основной части:

## Все команды: 

### 1. Создание ссылок
```
ln -s /usr/share/data-minor-bioinf/assembly/oil_R1.fastq
ln -s /usr/share/data-minor-bioinf/assembly/oil_R2.fastq
ln -s /usr/share/data-minor-bioinf/assembly/oilMP_S4_L001_R1_001.fastq
ln -s /usr/share/data-minor-bioinf/assembly/oilMP_S4_L001_R2_001.fastq
```

### 2. Выбор случайных чтений
```
//сид 706
seqtk sample -s706 oil_R1.fastq 5000000 > sub1.fastq
seqtk sample -s706 oil_R2.fastq 5000000 > sub2.fastq
seqtk sample -s706 oilMP_S4_L001_R1_001.fastq 1500000 > mp1.fastq
seqtk sample -s706 oilMP_S4_L001_R2_001.fastq 1500000 > mp2.fastq
```

### 3. Оценка качества fastQC и multiQC
```
mkdir fastqc
ls sub* mp* | xargs -tI{} fastqc -o fastqc {}
mkdir multiqc
multiqc -o multiqc fastqc
```

### 4. Подрезание чтений
```
//согласно документации первая команда работает только paired-end чтениями, а вторая с mate-pairs
platanus_trim sub*
platanus_internal_trim mp*
```

### 5. Удаление изначальных файлов
```
rm sub1.fastq 
rm sub2.fastq
rm mp1.fastq
rm mp2.fastq
```

### 6. Оценка качества fastQC и multiQC подрезанных чтений
```
mkdir fastqc_trimmed
ls sub* mp*| xargs -tI{} fastqc -o fastqc_trimmed {}
mkdir multiqc_trimmed
multiqc -o multiqc_trimmed fastqc_trimmed
```

### 7. Сбор контигов, используя platanus assemble
```
//c mate-pairs не делаем, согласно документации
time platanus assemble -o Poil -f sub1.fastq.trimmed sub2.fastq.trimmed 2> assemble.log
```

### 8. Сбор скаффолдов, используя platanus scaffold
```
time platanus scaffold -o Poil -c Poil_contig.fa -IP1 sub1.fastq.trimmed sub2.fastq.trimmed -OP2 mp1.fastq.int_trimmed mp2.fastq.int_trimmed 2> scaffold.log
```

### 9. Уменьшение числа гэпов, используя platanus gap_close
```
time platanus gap_close -o Poil -c Poil_scaffold.fa -IP1 sub1.fastq.trimmed sub2.fastq.trimmed -OP2 mp1.fastq.int_trimmed mp2.fastq.int_trimmed 2> gapclose.log
```

### 10. Удаление подрезанных чтений
```
rm sub1.fastq.trimmed
rm sub2.fastq.trimmed
rm mp1.fastq.int_trimmed
rm mp2.fastq.int_trimmed
```

## Скриншоты и статистика:

### Изначальные чтения:
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428598-8f0f331d-0bc1-4dc4-a1fe-ad91e47e2b05.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428612-2d6dd1bd-619c-4d38-b353-f0d45123a987.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428620-c4f7c6ef-488c-4aa3-ae37-0b5c0a894395.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428658-da1b4068-f0ad-4ecf-8836-edc6bb4dd54e.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428675-a8068f4e-53a7-43ce-bc03-39cfba47e403.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428686-156610c5-9ef6-4429-bec3-c3ea66813148.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428700-c03f5f61-3267-4ca1-b9ef-db7573353526.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428727-59b4e0e9-9af8-4626-bb77-f7d33f4c0209.png">
<img width="1161" alt="image" src="https://user-images.githubusercontent.com/77894393/193428829-22ec2ca4-c1f2-4d55-a030-153354858985.png">
<img width="1161" alt="image" src="https://user-images.githubusercontent.com/77894393/193428837-737f15b3-316c-48ff-bdf0-24e1419506e9.png">

### Подрезанные чтения:
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428889-469c87d8-785c-4131-b561-ed663c0564da.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428894-81206916-6053-4bad-8bd1-db7361ef3ad1.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428906-998ed7bc-2d76-4bc1-b764-2ca3bae7e800.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428911-66ea9366-bdae-4bf1-9ab6-6f07474aa359.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428915-99915ee7-6bfe-4113-a2eb-878754554706.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428924-b91b3bf2-8a6e-440a-b8d1-1dd406d180de.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428932-19206fbc-23b8-49c9-9772-6c80432937bb.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428952-ab0ac8aa-239c-4575-b04d-8e47f42bde8e.png">
<img width="1105" alt="image" src="https://user-images.githubusercontent.com/77894393/193428958-9afc5fb7-495e-419d-9add-bcb7cac89841.png">
<img width="1160" alt="image" src="https://user-images.githubusercontent.com/77894393/193428978-fe0457d4-7113-4904-b0d6-05434c78cb71.png">
<img width="1160" alt="image" src="https://user-images.githubusercontent.com/77894393/193428982-4ce9a199-3fa5-4ea4-a1d4-3bc31592b7c7.png">

## Код анализа данных:

Файл google colab'a находится в папке src

## Вывод:

Качество сборки хорошее, поскольку 
  - контигов малое количество - 599, 
  - N50 скаффолда большое - 3.834.350, близкое к общей длине, что говорит о большом покрытии
  - общая длина - 3.873.895, ожидаемая примерно 4.500.000 (в интернете пишут, что это средняя длина у бактерий), следовательно, довольно близко к ожидаемой

# Результаты бонусной части:

## Все команды:

Команды использовались такие же, как в основной части, но для второй команды количество чтений было уменьшено в два раза

```
//сид 706
seqtk sample -s706 oil_R1.fastq 2500000 > sub1.fastq
seqtk sample -s706 oil_R2.fastq 2500000 > sub2.fastq
seqtk sample -s706 oilMP_S4_L001_R1_001.fastq 750000 > mp1.fastq
seqtk sample -s706 oilMP_S4_L001_R2_001.fastq 750000 > mp2.fastq
```

## Скриншоты:

### Изначальные чтения:
<img width="1116" alt="image" src="https://user-images.githubusercontent.com/77894393/193456079-d58f38e0-aa84-4816-a89d-2a6ba6bfc3d7.png">
<img width="1116" alt="image" src="https://user-images.githubusercontent.com/77894393/193456103-bd679745-5f92-4280-8f03-c243dd1d127f.png">
<img width="1116" alt="image" src="https://user-images.githubusercontent.com/77894393/193456118-3709a294-e501-4e5d-8513-651ef7dfad00.png">
<img width="1116" alt="image" src="https://user-images.githubusercontent.com/77894393/193456133-18524a49-3a60-4277-84a3-105966181687.png">
<img width="1116" alt="image" src="https://user-images.githubusercontent.com/77894393/193456145-e77217b4-4847-4ebb-8898-7cff5bc929cd.png">
<img width="1116" alt="image" src="https://user-images.githubusercontent.com/77894393/193456298-e514b197-bcf4-476b-b66e-db47167c8868.png">
<img width="1116" alt="image" src="https://user-images.githubusercontent.com/77894393/193456310-e43ccf17-f98d-4d13-aa67-21cb19f23566.png">
<img width="1116" alt="image" src="https://user-images.githubusercontent.com/77894393/193456326-95978fde-2da3-4e91-a226-3ca2f9bda92e.png">
<img width="1172" alt="image" src="https://user-images.githubusercontent.com/77894393/193456354-6c02b9a4-b556-42b0-b5d1-ee6abdbe9ae3.png">
<img width="1172" alt="image" src="https://user-images.githubusercontent.com/77894393/193456387-dfc31fe0-3546-4f4e-b633-5f48df4291f0.png">

### Подрезанные чтения:
<img width="1109" alt="image" src="https://user-images.githubusercontent.com/77894393/193456474-0bdbbcd2-ad0f-4c82-966f-e815378005bc.png">
<img width="1109" alt="image" src="https://user-images.githubusercontent.com/77894393/193456505-abfbf65f-2cae-410f-a155-19c4d70b07d8.png">
<img width="1109" alt="image" src="https://user-images.githubusercontent.com/77894393/193456527-20046029-dd1a-4db1-95bc-678e247c310f.png">
<img width="1109" alt="image" src="https://user-images.githubusercontent.com/77894393/193456536-18405e70-6fc1-47d1-80f9-8db9d7c9800a.png">
<img width="1109" alt="image" src="https://user-images.githubusercontent.com/77894393/193456543-e87aca67-7c25-4eaa-a553-9e293bb50888.png">
<img width="1109" alt="image" src="https://user-images.githubusercontent.com/77894393/193456556-83e0af56-aca6-407c-acf2-4232b068730f.png">
<img width="1109" alt="image" src="https://user-images.githubusercontent.com/77894393/193456568-6c3a10e5-fc00-4cbd-bf33-e21b9fa01b6b.png">
<img width="1109" alt="image" src="https://user-images.githubusercontent.com/77894393/193456583-76e307b1-5861-4eb4-b110-b61522fde34f.png">
<img width="1109" alt="image" src="https://user-images.githubusercontent.com/77894393/193456592-e122c0ce-6cb1-484e-8b40-a85a761f4749.png">
<img width="1159" alt="image" src="https://user-images.githubusercontent.com/77894393/193456721-5ad50e27-469e-4aa4-924a-902bfbe05f04.png">
<img width="1159" alt="image" src="https://user-images.githubusercontent.com/77894393/193456689-34c59554-7d12-4463-b9e3-87ac172108d1.png">

## Код анализа данных:

Файл google colab'a находится в папке src

## Вывод:

Качество сборки хорошее, поскольку 
  - контигов малое количество - 702, 
  - N50 скаффолда большое - 3.829.580, близкое к общей длине, что говорит о большом покрытии
  - общая длина - 3.869.455, ожидаемая примерно 4.500.000 (в интернете пишут, что это средняя длина у бактерий), следовательно, довольно близко к ожидаемой
  
# Сравнение:

Уменьшив количество чтений в два раза, качество сборки ухудшилось: количество контигов увеличилось, общая длина и N50 скаффолдов уменьшились. Но при этом качество осталось хорошим, поскольку значение параметров отклонилось на небольшое число и имеет, в общем, хорошие показатели.
