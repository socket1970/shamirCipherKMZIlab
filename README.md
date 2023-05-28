# Шифр Шамира. Лабораторная работа по предмету КМЗИ.
![C](https://img.shields.io/badge/c-%2300599C.svg?style=for-the-badge&logo=c&logoColor=white)
[![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/funny_m4n)
***
## Описание
Алгоритм реализован на Си с использованием библиотеки GMP.

Схема шифра:
```
    1. Alice -> Bob:    x1 = m^Ca mod p;
    2. Bob -> Alice:    x2 = x1^Cb mod p;
    3. Alice -> Bob:    x3 = x2^Da mod p;
    4. Bob:         m = x4 = x3^Db mod p;
```
***
### Задание 1.
Заданы параметры шифра:
* Ca - ключ Алисы;
* Cb - ключ Боба;
* m - исходное сообщение;
* p - параметр шифра, для расчета ключей;

Производится расчет недостающих ключей и переписки. Переписка выводится на экран.

### Задание 2.
Заданы параметры шифра:
* m - исходное сообщение;
* p - параметр шифра, для расчета ключей;

Производится расчет всех ключей и переписки. Переписка выводится на экран.

### Задание 3.
Заданы параметры шифра:
* m - исходное сообщение;
* p - параметр шифра, для расчета ключей;

Производится расчет ключей Боба и переписки. Переписка выводится на экран.

*** 
### Компиляция.
Проверена работоспособность под wsl и дистрибутивами Linux (Debian 11, Ubuntu 20.04, Kali 2022.4).

В файле bash.install прописаны все пакеты, необходимые для сборки.
Для запуска
```
    chmod +x bash.install
    ./bash.install
```
Для сборки
```
    cmake .
    make
    ./shamirCipher
```
***