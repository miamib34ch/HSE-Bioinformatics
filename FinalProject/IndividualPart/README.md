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
|:-:|:-:|:-|
|H2A|![image](https://github.com/miamib34ch/HSE-Bioinformatics/assets/77894393/445da4a2-51cf-4cb6-b701-2390028b1484)|Между последовательностями есть различия, но не особо сильные, скорее всего, это связано с мутациями и полиморфизмом|
|H2B|![image](https://github.com/miamib34ch/HSE-Bioinformatics/assets/77894393/6c72ba23-3544-4f7c-8a65-2f53b8bffef2)|Между последовательностями есть различия, но не особо сильные, скорее всего, это связано с мутациями и полиморфизмом|
|H3|![image](https://github.com/miamib34ch/HSE-Bioinformatics/assets/77894393/2415e7c3-78a5-4a3e-954b-e42cbcd2d07c)|Между последовательностями практически нет различий (чуть-чуть полиформизм есть), гены являются копиями|
|H4|![image](https://github.com/miamib34ch/HSE-Bioinformatics/assets/77894393/1de068b8-7c0c-4bab-b642-e9bc19d3b9e9)|Между последовательностями практически нет различий (чуть-чуть полиформизм есть), гены являются копиями|

## e-value
![image](https://github.com/miamib34ch/HSE-Bioinformatics/assets/77894393/f24e47df-d34d-4dfb-b0e1-1ac5a12c4448)

## Тепловая карта
![image](https://github.com/miamib34ch/HSE-Bioinformatics/assets/77894393/5f9d24c1-94d7-4938-8804-b566398e510c)

*Чем светлее цвет, тем более значимый результат*

## Код

**На сервере для выравнивания использовал:** blastp -query *protein*.fasta -db /mnt/storage/project_2023/proteomes/*proteome*.faa -out *proteome*.blast -outfmt 7

**Для построения тепловой карты использовал python** *(файл heatmap.ipynb)*

## Вывод 

Выбранный белок гена HR эволюционно начал появляться у многоклеточных беспозвоночных организмов (drosophila). И есть уже у всех исследуемых многоклеточных позвоночных (human, mouse, zebrafish). 
<br>Также подтверждается связь с H3 семейством гистонов.

*Вывод делал по значению -log(e-value) > 10* 
