# GenomeAnnotation

## Статистика:
* Предсказанно генов всего - 3602
* Удалось аннотировать с помощью сравнения с бактерией MIL-1 - 3323
* Удалось аннотировать с помощью БД SwissProt - 53
* Количество белков, которые остались без аннотации функции - 226 (если учитывать аннотацию SwissProt)
* Количество белков, которые остались без аннотации функции - 279 (если не учитывать аннотацию SwissProt)

## Бонус
Процент сходства между соответствующими рРНК находится в колонке "% identity"
``` 
# BLASTN 2.6.0+
# Query: rRNA_341494...343033
# Database: User specified sequence set (Input: scaffolds.fa)
# Fields: query acc.ver, subject acc.ver, % identity, alignment length, mismatches, gap opens, q. start, q. end, s. start, s. end, evalue, bit score
# 4 hits found
rRNA_341494...343033	scaffold1_cov231	100.000	1539	0	0	1	1539	2527358	2528896	0.0	2843
rRNA_341494...343033	scaffold1_cov231	99.935	1539	1	0	1	1539	846845	845307	0.0	2837
rRNA_341494...343033	scaffold1_cov231	100.000	64	0	0	1	64	1673342	1673405	7.22e-27	119
rRNA_341494...343033	scaffold32_cov590	100.000	1399	0	0	134	1532	1399	1	0.0	2584
# BLASTN 2.6.0+
# Query: rRNA_343487...346374
# Database: User specified sequence set (Input: scaffolds.fa)
# Fields: query acc.ver, subject acc.ver, % identity, alignment length, mismatches, gap opens, q. start, q. end, s. start, s. end, evalue, bit score
# 5 hits found
rRNA_343487...346374	scaffold1_cov231	100.000	2887	0	0	1	2887	2529147	2532033	0.0	5332
rRNA_343487...346374	scaffold1_cov231	99.965	2887	1	0	1	2887	845056	842170	0.0	5326
rRNA_343487...346374	scaffold35_cov590	100.000	1535	0	0	1353	2887	1815	281	0.0	2835
rRNA_343487...346374	scaffold41_cov598	100.000	1051	0	0	215	1265	1051	1	0.0	1941
rRNA_343487...346374	scaffold49_cov624	100.000	127	0	0	1	127	127	1	1.30e-61	235
# BLASTN 2.6.0+
# Query: rRNA_346568...346684
# Database: User specified sequence set (Input: scaffolds.fa)
# Fields: query acc.ver, subject acc.ver, % identity, alignment length, mismatches, gap opens, q. start, q. end, s. start, s. end, evalue, bit score
# 4 hits found
rRNA_346568...346684	scaffold1_cov231	100.000	116	0	0	1	116	841988	841873	5.67e-57	215
rRNA_346568...346684	scaffold1_cov231	100.000	116	0	0	1	116	2532215	2532330	5.67e-57	215
rRNA_346568...346684	scaffold1_cov231	100.000	60	0	0	57	116	1673623	1673682	7.65e-26	111
rRNA_346568...346684	scaffold35_cov590	100.000	99	0	0	1	99	99	1	1.60e-47	183
# BLASTN 2.6.0+
# Query: rRNA_2580484...2580600
# Database: User specified sequence set (Input: scaffolds.fa)
# Fields: query acc.ver, subject acc.ver, % identity, alignment length, mismatches, gap opens, q. start, q. end, s. start, s. end, evalue, bit score
# 4 hits found
rRNA_2580484...2580600	scaffold1_cov231	98.276	116	2	0	1	116	841873	841988	1.23e-53	204
rRNA_2580484...2580600	scaffold1_cov231	98.276	116	2	0	1	116	2532330	2532215	1.23e-53	204
rRNA_2580484...2580600	scaffold1_cov231	96.667	60	2	0	1	60	1673682	1673623	1.66e-22	100
rRNA_2580484...2580600	scaffold35_cov590	98.990	99	1	0	18	116	1	99	7.44e-46	178
# BLASTN 2.6.0+
# Query: rRNA_2580781...2583668
# Database: User specified sequence set (Input: scaffolds.fa)
# Fields: query acc.ver, subject acc.ver, % identity, alignment length, mismatches, gap opens, q. start, q. end, s. start, s. end, evalue, bit score
# 5 hits found
rRNA_2580781...2583668	scaffold1_cov231	100.000	2887	0	0	1	2887	2532033	2529147	0.0	5332
rRNA_2580781...2583668	scaffold1_cov231	99.965	2887	1	0	1	2887	842170	845056	0.0	5326
rRNA_2580781...2583668	scaffold35_cov590	100.000	1535	0	0	1	1535	281	1815	0.0	2835
rRNA_2580781...2583668	scaffold41_cov598	100.000	1051	0	0	1623	2673	1	1051	0.0	1941
rRNA_2580781...2583668	scaffold49_cov624	100.000	127	0	0	2761	2887	1	127	1.30e-61	235
# BLASTN 2.6.0+
# Query: rRNA_2583918...2585457
# Database: User specified sequence set (Input: scaffolds.fa)
# Fields: query acc.ver, subject acc.ver, % identity, alignment length, mismatches, gap opens, q. start, q. end, s. start, s. end, evalue, bit score
# 4 hits found
rRNA_2583918...2585457	scaffold1_cov231	99.935	1539	1	0	1	1539	845307	846845	0.0	2837
rRNA_2583918...2585457	scaffold1_cov231	99.870	1539	2	0	1	1539	2528896	2527358	0.0	2832
rRNA_2583918...2585457	scaffold1_cov231	100.000	64	0	0	1476	1539	1673405	1673342	7.22e-27	119
rRNA_2583918...2585457	scaffold32_cov590	99.929	1399	1	0	8	1406	1	1399	0.0	2579
# BLASTN 2.6.0+
# Query: rRNA_3418645...3418761
# Database: User specified sequence set (Input: scaffolds.fa)
# Fields: query acc.ver, subject acc.ver, % identity, alignment length, mismatches, gap opens, q. start, q. end, s. start, s. end, evalue, bit score
# 4 hits found
rRNA_3418645...3418761	scaffold1_cov231	100.000	116	0	0	1	116	841873	841988	5.67e-57	215
rRNA_3418645...3418761	scaffold1_cov231	100.000	116	0	0	1	116	2532330	2532215	5.67e-57	215
rRNA_3418645...3418761	scaffold1_cov231	100.000	60	0	0	1	60	1673682	1673623	7.65e-26	111
rRNA_3418645...3418761	scaffold35_cov590	100.000	99	0	0	18	116	1	99	1.60e-47	183
# BLASTN 2.6.0+
# Query: rRNA_3418942...3421829
# Database: User specified sequence set (Input: scaffolds.fa)
# Fields: query acc.ver, subject acc.ver, % identity, alignment length, mismatches, gap opens, q. start, q. end, s. start, s. end, evalue, bit score
# 5 hits found
rRNA_3418942...3421829	scaffold1_cov231	100.000	2887	0	0	1	2887	2532033	2529147	0.0	5332
rRNA_3418942...3421829	scaffold1_cov231	99.965	2887	1	0	1	2887	842170	845056	0.0	5326
rRNA_3418942...3421829	scaffold35_cov590	100.000	1535	0	0	1	1535	281	1815	0.0	2835
rRNA_3418942...3421829	scaffold41_cov598	100.000	1051	0	0	1623	2673	1	1051	0.0	1941
rRNA_3418942...3421829	scaffold49_cov624	100.000	127	0	0	2761	2887	1	127	1.30e-61	235
# BLASTN 2.6.0+
# Query: rRNA_3422079...3423618
# Database: User specified sequence set (Input: scaffolds.fa)
# Fields: query acc.ver, subject acc.ver, % identity, alignment length, mismatches, gap opens, q. start, q. end, s. start, s. end, evalue, bit score
# 4 hits found
rRNA_3422079...3423618	scaffold1_cov231	99.935	1539	1	0	1	1539	845307	846845	0.0	2837
rRNA_3422079...3423618	scaffold1_cov231	99.870	1539	2	0	1	1539	2528896	2527358	0.0	2832
rRNA_3422079...3423618	scaffold1_cov231	100.000	64	0	0	1476	1539	1673405	1673342	7.22e-27	119
rRNA_3422079...3423618	scaffold32_cov590	99.929	1399	1	0	8	1406	1	1399	0.0	2579
# BLASTN 2.6.0+
# Query: rRNA_3423993...3424109
# Database: User specified sequence set (Input: scaffolds.fa)
# Fields: query acc.ver, subject acc.ver, % identity, alignment length, mismatches, gap opens, q. start, q. end, s. start, s. end, evalue, bit score
# 4 hits found
rRNA_3423993...3424109	scaffold1_cov231	100.000	116	0	0	1	116	841873	841988	5.67e-57	215
rRNA_3423993...3424109	scaffold1_cov231	100.000	116	0	0	1	116	2532330	2532215	5.67e-57	215
rRNA_3423993...3424109	scaffold1_cov231	100.000	60	0	0	1	60	1673682	1673623	7.65e-26	111
rRNA_3423993...3424109	scaffold35_cov590	100.000	99	0	0	18	116	1	99	1.60e-47	183
# BLASTN 2.6.0+
# Query: rRNA_3424290...3427177
# Database: User specified sequence set (Input: scaffolds.fa)
# Fields: query acc.ver, subject acc.ver, % identity, alignment length, mismatches, gap opens, q. start, q. end, s. start, s. end, evalue, bit score
# 5 hits found
rRNA_3424290...3427177	scaffold1_cov231	100.000	2887	0	0	1	2887	2532033	2529147	0.0	5332
rRNA_3424290...3427177	scaffold1_cov231	99.965	2887	1	0	1	2887	842170	845056	0.0	5326
rRNA_3424290...3427177	scaffold35_cov590	100.000	1535	0	0	1	1535	281	1815	0.0	2835
rRNA_3424290...3427177	scaffold41_cov598	100.000	1051	0	0	1623	2673	1	1051	0.0	1941
rRNA_3424290...3427177	scaffold49_cov624	100.000	127	0	0	2761	2887	1	127	1.30e-61	235
# BLASTN 2.6.0+
# Query: rRNA_3427427...3428966
# Database: User specified sequence set (Input: scaffolds.fa)
# Fields: query acc.ver, subject acc.ver, % identity, alignment length, mismatches, gap opens, q. start, q. end, s. start, s. end, evalue, bit score
# 4 hits found
rRNA_3427427...3428966	scaffold1_cov231	99.935	1539	1	0	1	1539	845307	846845	0.0	2837
rRNA_3427427...3428966	scaffold1_cov231	99.870	1539	2	0	1	1539	2528896	2527358	0.0	2832
rRNA_3427427...3428966	scaffold1_cov231	100.000	64	0	0	1476	1539	1673405	1673342	7.22e-27	119
rRNA_3427427...3428966	scaffold32_cov590	99.929	1399	1	0	8	1406	1	1399	0.0	2579
# BLAST processed 12 queries
``` 
Или после обработки
<br> <img width="527" alt="image" src="https://user-images.githubusercontent.com/77894393/196786861-9f10c988-3938-4176-8ac6-870d80dc03b4.png">
