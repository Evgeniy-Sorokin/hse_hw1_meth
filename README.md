# hse_hw1_meth

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

Количество ридов, пришедшихся на каждый целевой регион:

| Образец | 11347700-11367700 | 40185800-40195800 | Дедупликация, % |
| epiblast | 2328 | 1062 | 97.08 |
| ICM | 1456 | 630 | 90.92 |
| 8 cell | 1090 | 464 | 81.69 |
