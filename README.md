# hse_hw1_meth

__Ссылка на google-collab:__

https://colab.research.google.com/drive/1Vgv_MTvCrZyK0IIjkkjakdWtAORVXnXV#scrollTo=iNOwfIKdNLYa

## Часть №1

__"Какие особенности можно наблюдать по сравнению с секвенированием ДНК или РНК?"__

| SRR5836473_1 | SRR3414631 |
| :---: | :---: |
|![image](https://user-images.githubusercontent.com/71905847/154557992-bdbebdfb-93de-43e0-9262-f996e9d20456.png)|![image](https://user-images.githubusercontent.com/71905847/154557874-e4ad06aa-39ef-439c-ad5a-a418a37b9b90.png)|
|![image](https://user-images.githubusercontent.com/71905847/154558228-ddc55579-4b98-4fde-9fdd-bbe3435356ab.png)|![image](https://user-images.githubusercontent.com/71905847/154558190-85401726-0080-40e1-a3b6-4b2e22e2f0c3.png)|
|![image](https://user-images.githubusercontent.com/71905847/154558564-0645c795-f285-4e65-b31c-6c4ebc39cc82.png)|![image](https://user-images.githubusercontent.com/71905847/154558589-975b7c40-f5bc-488f-9b75-981892e16688.png)|

Опишем следующие ярко выраженные особенности:
- В Basic Statistics можно увидеть, что процент GC у РНК (SRR3414631), взятой из одного из прошлых домашних заданий, составляет 49%, в то время как у BS-Seq (SRR5836473_1) - 36%;
- Рассматривая Per base sequence content, заметим, что в случае РНК Цитозин, Гуанин, Аденин и Тимин находится примерно на одном уровне, в то время как у BS-Seq Цитозина меньше всего (10%), Гуанин и Аденин находятся примерно на одном уровне (25%), Цитозина же больше всего (40%);
- Обратив же внимание на GC distribution, отметим то, что в случае РНК наблюдается лишь совсем слабое отклонение от нормального распределения, а у BS-Seq - почти полное несоответствие и наличие двух колоколообразных пиков.

## Часть №2

__"Количество ридов, пришедшихся на каждый целевой регион:"__

| Образец | 11347700-11367700 | 40185800-40195800 | Дедупликация, % |
| :---: | :---: | :---: | :---: |
| epiblast | 2328 | 1062 | 97.08 |
| ICM | 1456 | 630 | 90.92 |
| cell8 | 1090 | 464 | 81.69 |

__bash-skript:__ ! ls -1 *1_bismark_bt2_pe* | xargs -tI{} deduplicate_bismark  --bam  --paired -o s_{} {}

__"Анализ M-bias plot:"__

| Название | Read 1 | Read 2 |
| :---: | :---: | :---: |
| epiblast | ![Bismark M-bias Read 1](https://user-images.githubusercontent.com/71905847/154702864-5da4923b-0c11-4739-b504-15739813ef9d.png) | ![Bismark M-bias Read 2](https://user-images.githubusercontent.com/71905847/154702890-8028bf9c-487f-4b66-a05e-ff53e0de4344.png) |
| ICM | ![Bismark M-bias Read 1 (1)](https://user-images.githubusercontent.com/71905847/154704950-836c5fd9-0b14-4f5c-9ebc-923391525106.png) | ![Bismark M-bias Read 2 (1)](https://user-images.githubusercontent.com/71905847/154704972-505ff363-baea-40f6-ae2f-404340ae0317.png)|
| cell8 | ![Bismark M-bias Read 1 (2)](https://user-images.githubusercontent.com/71905847/154705217-0301596a-793e-46b2-aa3e-cc59c6a57009.png) | ![Bismark M-bias Read 2 (2)](https://user-images.githubusercontent.com/71905847/154705239-ada35f72-918a-421f-8431-f67c67356a20.png)|

| Название | CpG context (Methylation, %) |
| :---: | :---: |
| epiblast | 77.0 |
| ICM | 25.2 |
| cell8 | 46.5 |

 Если же сравнивать CHG и CHH context, то для всех образцов они примено одинаковы.
 
__"Гистограмма распределения метилирования по хромосоме:"__

| Название | CpG context (Methylation, %) |
| :---: | :---: |
| epiblast | ![image](https://user-images.githubusercontent.com/71905847/154709162-a1b46c2e-7edb-455a-bf33-c40742c886b9.png) |
| ICM | ![image](https://user-images.githubusercontent.com/71905847/154709338-5deb5229-0047-4f9c-8ebb-d653a8967230.png) |
| cell8 | ![image](https://user-images.githubusercontent.com/71905847/154709291-21abce95-643d-4ced-a7bd-49c50e9a9b7d.png) |
