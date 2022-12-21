# hse22_hw5

# Нормализация данных 

Статья про нормализацию: https://translational-medicine.biomedcentral.com/articles/10.1186/s12967-021-02936-w

Я решил делать TPM, потому что его можно преобразовать в FPKM, согласно статье

В TPM нормализации используется следующая формула: 
<img width="451" alt="Снимок экрана 2022-12-17 в 23 17 29" src="https://user-images.githubusercontent.com/77894393/208266621-438a33b9-4865-4eb0-822f-be87c4c5805f.png">

Где <img width="42" alt="image" src="https://user-images.githubusercontent.com/77894393/208266691-3e03c5f4-4862-414a-8e61-f09548377c99.png"> - риды попавшие на транскрипцию, а <img width="26" alt="image" src="https://user-images.githubusercontent.com/77894393/208266703-7894e7a4-eebc-42c8-ba29-c5d53a4335a5.png"> - длина транскрипции

Но мы работаем с файлами из статьи: "2018 Single-cell mapping of the thymic stroma identifies IL-25-producing tuft epithelial cells" (можно найти в папке other); и у нас нет длины, поэтому используется следующая формула: 

<img width="451" alt="Снимок экрана 2022-12-17 в 23 20 26" src="https://user-images.githubusercontent.com/77894393/208266746-fe2306b4-36ae-44b8-867a-0ea084ce73fe.png">

# Heatmap для экспрессии маркерных генов

В результате работы получена следующая тепловая карта: 

![Unknown](https://user-images.githubusercontent.com/77894393/208266913-27b64a93-61df-4826-a45c-c0da9615a4a3.png)

Видно, что всего пять групп по типу клеток. Также, что экспрессия внутри групп одинакова и есть характерные для групп гены.

# Полученные визуализации UMAP и PCA

Была понижена размерность:

![Unknown](https://user-images.githubusercontent.com/77894393/208267134-303b529f-a1c3-4f1a-aab1-c237b2763870.png)

![Unknown-2](https://user-images.githubusercontent.com/77894393/208267137-77c43dc6-9323-47d4-8f6b-b3855af8a81e.png)

Лучше справился UMAP, поскольку в PCA группы cTEC и mTEC-III лежат на других группах.

