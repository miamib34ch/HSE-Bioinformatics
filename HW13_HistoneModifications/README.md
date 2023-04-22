# hse_hw2_chip

# FastQC

Необходимость фильтрации или подрезания чтений не увидел.

## ENCFF001FFI - файл контроля

![image](https://user-images.githubusercontent.com/77894393/222066491-5094c292-3046-4a22-b3a5-f9742a81f724.png)

![image](https://user-images.githubusercontent.com/77894393/222066403-fc750070-a986-4bdb-8b80-e3718a54eaca.png)

![image](https://user-images.githubusercontent.com/77894393/222066643-f2d0d513-c64c-40e5-ad42-aeef123c6042.png)

![image](https://user-images.githubusercontent.com/77894393/222066742-ee757191-d24b-4ea6-a1ea-29e06c645252.png)

![image](https://user-images.githubusercontent.com/77894393/222066807-a2d3d8c2-0793-491e-8c18-8da82d044dd7.png)

## ENCFF001FEG

![image](https://user-images.githubusercontent.com/77894393/222066942-c98ee3bc-d5ef-4f24-a6b0-cdedba031585.png)

![image](https://user-images.githubusercontent.com/77894393/222066989-9b3a17b3-149a-4a41-99d7-3167b9234bc6.png)

![image](https://user-images.githubusercontent.com/77894393/222067027-3e72c65a-7653-42c5-b6a4-52a1b3a31868.png)

![image](https://user-images.githubusercontent.com/77894393/222067083-8a5e55eb-1e86-4b2e-ba8d-90e3a82e19f9.png)

![image](https://user-images.githubusercontent.com/77894393/222067126-4497c414-f555-4533-8d86-5bc73a9b2277.png)

## ENCFF001FEF

![image](https://user-images.githubusercontent.com/77894393/222067234-beb78d80-3789-4bc2-aacc-7999923a0b4e.png)

![image](https://user-images.githubusercontent.com/77894393/222067271-d2f75f91-870a-4aef-83b8-50b9c7ee2a5f.png)

![image](https://user-images.githubusercontent.com/77894393/222067312-f72d35cd-9577-4cb2-a396-8ac453eb48e1.png)

![image](https://user-images.githubusercontent.com/77894393/222067342-dfa02e17-93f6-4a38-bb7b-a4fc68f4e108.png)

![image](https://user-images.githubusercontent.com/77894393/222067385-f8376515-946e-427d-a448-cac676962313.png)

# Выравнивание 

|   Образец   | Сколько ридов было в файле | Сколько ридов выравнилось уникально | Сколько ридов выравнилось НЕ-уникально | Сколько ридов НЕ выравнилось |
|:-----------:|:--------------------------:|:-----------------------------------:|:--------------------------------------:|:----------------------------:|
| ENCFF001FFI |           18390264         |            821433 (4.47%)           |            2280908 (12.40%)            |       15287923 (83.13%)      |
| ENCFF001FEG |           20906381         |            838912 (4.01%)           |            2795349 (13.37%)            |       17272120 (82.62%)      |
| ENCFF001FEF |           24113389         |            966182 (4.01%)           |            3110030 (12.90%)            |       20037177 (83.10%)      |

Процент выравниваний получился именно таким (маленьким), потому что мы выравнивали на одну хромосому. У человека их больше одной, и поэтому если бы выравнивали на большее количество, то и процент был бы выше. 

# Диаграммы Венна

По ниже представленным диаграммам Венна, можно заметить, что пересечений мало. Это связано, опять же, с тем, что мы выравнивали на одну хромосому, а в базе данных используются все. Также, можно заметить, что из-за порядка сравнения образцов различается количество пересечений для одних и тех же образцов. 

![image](https://user-images.githubusercontent.com/77894393/222071286-242e9b61-30c0-4699-86c3-2793ed1bf79a.png)

![image](https://user-images.githubusercontent.com/77894393/222071359-a187af26-312f-4905-a25e-0e96d8dbe529.png)

![image](https://user-images.githubusercontent.com/77894393/222071417-91232b8a-07a5-4049-a670-aa9cc0a71368.png)

![image](https://user-images.githubusercontent.com/77894393/222071487-46190c2d-ceb7-40c8-8169-90d3301ccf9f.png)
