# HSE-BI-ProjectIndividualPart

## Общая информация
**Ген:** HR
<br>**Эпигенетическая функция:** Histone modification erase
<br>**Эпигенетическая группа:** H3K9me


**Статьи:** 
<br>[We performed a series of in vitro demethylation assays, which demonstrated that HR can demethylate monomethylated or dimethylated histone H3 lysine 9 (H3K9me1 or me2).](https://pubmed.ncbi.nlm.nih.gov/24334705/)

[For example, the reported intrinsic histone H3K9 demethylase activity of HR may activate dormant genes to contribute to carcinogenesis.](https://pubmed.ncbi.nlm.nih.gov/28543886/)

## Выравнивание гистонов
|Название | Скрин | Вывод |
|:-:|:-:|:-:|
|H2A|![image](https://github.com/miamib34ch/HSE-BI-ProjectIndividualPart/assets/77894393/8f6fe524-08f4-4423-96ac-e7cb1fcf43db)|Между последовательностями есть различия, но не особо сильные, скорее всего, это связано с мутациями и полиморфизмом|
|H2B|![image](https://github.com/miamib34ch/HSE-BI-ProjectIndividualPart/assets/77894393/c3121703-4f5e-4a78-803d-0f85c260c9cd)|Между последовательностями есть различия, но не особо сильные, скорее всего, это связано с мутациями и полиморфизмом|
|H3|![image](https://github.com/miamib34ch/HSE-BI-ProjectIndividualPart/assets/77894393/1b733314-46f4-4d13-8284-64d7d244a4b2)|Между последовательностями практически нет различий (чуть-чуть полиформизм есть), гены являются копиями|
|H4|![image](https://github.com/miamib34ch/HSE-BI-ProjectIndividualPart/assets/77894393/cf5417e4-0fe0-404d-856a-faa24d8d9ca2)|Между последовательностями практически нет различий (чуть-чуть полиформизм есть), гены являются копиями|

## e-value
![image](https://github.com/miamib34ch/HSE-BI-ProjectIndividualPart/assets/77894393/b9d3ad01-bee9-457f-87a2-b75f449032a8)

## Тепловая карта

![image](https://github.com/miamib34ch/HSE-BI-ProjectIndividualPart/assets/77894393/7686a889-09a5-4b30-ad13-9758c9e2f7a8)

## Код

**На сервере для выравнивания использовал:** blastp -query *protein*.fasta -db /mnt/storage/project_2023/proteomes/*proteome*.faa -out *proteome*.blast -outfmt 7

**Для построения тепловой карты использовал python** *(файл heatmap.ipynb)*

## Вывод 

Выбранный белок гена HR эволюционно появился у многоклеточных позвоночных организмов.