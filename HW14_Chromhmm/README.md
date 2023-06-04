# hse_hw3_chromhmm

Клеточная линия - K562

Файл контроля - wgEncodeBroadHistoneK562ControlStdAlnRep1.bam

## Список 10-ти гистоновых меток

|   Номер   | Название | Файл |
|:---------:|:--------:|:----:|
|1          |H3k27me3  |wgEncodeBroadHistoneK562H3k27me3StdAlnRep1.bam|
|2          |H3k9me1   |wgEncodeBroadHistoneK562H3k9me1StdAlnRep1.bam |
|3          |H3k36me3  |wgEncodeBroadHistoneK562H3k36me3StdAlnRep1.bam|
|4          |H3k4me2   |wgEncodeBroadHistoneK562H3k4me2StdAlnRep1.bam |
|5          |H3k4me1   |wgEncodeBroadHistoneK562H3k4me1StdAlnRep1.bam |
|6          |H3k4me3   |wgEncodeBroadHistoneK562H3k4me3StdAlnRep1.bam |
|7          |H3k9ac    |wgEncodeBroadHistoneK562H3k9acStdAlnRep1.bam  |
|8          |H3k27ac   |wgEncodeBroadHistoneK562H3k27acStdAlnRep1.bam |
|9          |H3k79me2  |wgEncodeBroadHistoneK562H3k79me2StdAlnRep1.bam|
|10         |H2az      |wgEncodeBroadHistoneK562H2azStdAlnRep1.bam    |

## Файл cellmarkfiletable.txt

|   Клеточная линия   | Гистоновая метка | Файл метки*| Файл контроля*|
|:-------------------:|:----------------:|:----------:|:-------------:|
|K562	                |H3k27me3	         |H3k27me3.bam|Control.bam    |
|K562	                |H3k9me1	         |H3k9me1.bam	|Control.bam    |
|K562	                |H3k36me3	         |H3k36me3.bam|Control.bam    |
|K562	                |H3k4me2	         |H3k4me2.bam	|Control.bam    |
|K562	                |H3k4me1	         |H3k4me1.bam	|Control.bam    |
|K562	                |H3k4me3	         |H3k4me3.bam	|Control.bam    |
|K562	                |H3k9ac	           |H3k9ac.bam	|Control.bam    |
|K562	                |H3k27ac	         |H3k27ac.bam	|Control.bam    |
|K562	                |H3k79me2	         |H3k79me2.bam|Control.bam    |
|K562	                |H2az	             |H2az.bam	  |Control.bam    |

*Имена файлов, которые использовались в коде

## ChromHMM

|   |   |   |   |   |
|:-:|:-:|:-:|:-:|:-:|
|![image](https://user-images.githubusercontent.com/77894393/230181661-1639eddf-305b-4952-9a7b-fae4eca75087.png)|![image](https://user-images.githubusercontent.com/77894393/230181799-82c8a017-295c-4e9a-be12-ecd0f9636885.png)|![image](https://user-images.githubusercontent.com/77894393/230181915-2079e2aa-bb02-42e5-b5b7-6776d9a8b2ba.png)|![image](https://user-images.githubusercontent.com/77894393/230181930-d4d4b970-e7f3-4bcf-a738-78bfb7222338.png)|![image](https://user-images.githubusercontent.com/77894393/230181948-4e732c06-bd09-495d-b972-fe6544474bb5.png)|

## Табличка эпигенетических типов

|Название типа                         |Гистоновые метки |Типичное расположение |
|:------------------------------------:|:---------------:|:--------------------:|
|1 Active Promoter                     | H3k27me3 (не сильно), H2az	(не сильно), H3k9me1 (не сильно)|Genome, RefSeqExon, RefSeqGene, RefSeqTES, RefSeqTSS2kb, laminB1lads|
|2 Weak Promoter                       | - |Genome, laminB1lads|
|3 Inactive/poised Promoter            | H3k9me1 (не сильно), H3k36me3 (не сильно), H3k79me2 (не сильно)|Genome, RefSeqExon, RefSeqGene, RefSeqTES, RefSeqTSS2kb, laminB1lads|
|4 Strong enhancer                     | H3k27ac (не сильно), H3k9me1 (не сильно), H3k36me3 (не сильно), H3k79me2 (не сильно)|RefSeqExon, RefSeqGene, RefSeqTES|
|5 Strong enhancer                     | H3k4me1 (не сильно), H3k9me1 (не сильно), H3k36me3 (не сильно), H3k79me2|Genome, RefSeqExon, RefSeqGene, RefSeqTES, RefSeqTSS2kb|
|6 Weak/poised enhancer                | H2az	(не сильно), H3k4me2, H3k4me3, H3k9ac, H3k27ac, H3k4me1, H3k9me1, H3k36me3 (не сильно), H3k79me2|RefSeqExon, RefSeqGene, RefSeqTES, RefSeqTSS2kb|
|7 Weak/poised enhancer                | H2az	(не сильно), H3k27ac (не сильно), H3k4me1, H3k9me1 (не сильно), H3k36me3 (не сильно), H3k79me2 (не сильно)|RefSeqExon, RefSeqGene, RefSeqTES, RefSeqTSS2kb, laminB1lads|
|8 Insulator                           | H2az, H3k4me2, H3k4me3, H3k9ac, H3k27ac, H3k4me1, H3k9me1 (не сильно), H3k36me3 (не сильно), H3k79me2 (не сильно)|RefSeqExon, RefSeqGene, RefSeqTES, RefSeqTSS, RefSeqTSS2kb, laminB1lads|
|9 Transcriptional transition          | H2az, H3k4me1, H3k9me1 (не сильно)|Genome, RefSeqExon, RefSeqTES, RefSeqTSS2kb, laminB1lads|
|10 Transcriptional elongation         | H3k27me3 (не сильно), H2az, H3k4me2, H3k4me3, H3k9ac, H3k27ac, H3k4me1, H3k9me1 (не сильно), H3k79me2 (не сильно)|CpGIsland, RefSeqExon, RefSeqGene, RefSeqTES, RefSeqTSS, RefSeqTSS2kb, laminB1lads|
|11 Weak transcribed                   | H2az, H3k4me2, H3k4me3, H3k9ac, H3k27ac, H3k4me1, H3k9me1 (не сильно), H3k79me2 (не сильно)|CpGIsland, RefSeqExon, RefSeqGene, RefSeqTES, RefSeqTSS, RefSeqTSS2kb, laminB1lads|
|12 Polycomb-repressed                 | H2az, H3k4me2, H3k4me3, H3k9ac, H3k27ac, H3k4me1, H3k9me1 (не сильно), H3k36me3 (не сильно), H3k79me2|CpGIsland, RefSeqExon, RefSeqGene, RefSeqTES, RefSeqTSS, RefSeqTSS2kb|

## Скрины UCSC GenomeBrowser

|   |   |   |   |
|:-:|:-:|:-:|:-:|
|![image](https://user-images.githubusercontent.com/77894393/230203396-b3db150e-e9d6-409e-973b-09fd0935e1bb.png)|![image](https://user-images.githubusercontent.com/77894393/230203739-793a60ee-a90d-4bee-90c3-e2c1f1f87ef9.png)|![image](https://user-images.githubusercontent.com/77894393/230203903-f2a85e8f-d5e8-4fd7-aa43-601d6239516b.png)|![image](https://user-images.githubusercontent.com/77894393/230204018-b5dc76af-a216-40ad-909d-a77108bf7546.png)|

## Список всех запущенных команд

Все команды можно посмотреть в файле гугл колаба
