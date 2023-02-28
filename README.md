# Assembler-X86
<h2 >Лабораторная работа №1 - Система команд микропроцессора Х86 <br>
Цель - изучение системы команд и способов адресации 
микропроцессоров с архитектурой x86.</h2>

<strong>Индивидуальное задание выглядит следующим образом: </strong> <br>
Вычислить M=(Z’or X’ and Y)+(X’ / Z), где Z', X’ – получены 
в результате инверсии 4 старших бит X и Y соответственно

<strong>Исходные данные:</strong> <br>
X = 9, Y = 44, Z = 12

<strong> Дополнительные данные: </strong> <br>
D = 15, F = 240 числа, необходимые для инверсии старших 4 бит

1. Изначально необходимо вычислить Z' и X', для этого будет использована операция исключающее или (XOR). <br>
<strong> Для Z': </strong> Х = 9 (1001 в двоичном коде), для инверсии 4 старших бит будет использовано число 15 (1111 в двоичном коде) <br>
1001 XOR 1111 = 0110 (6 в десятичном коде). <br>
<strong> Для X': </strong> Y = 44 (00101100 в двоичном коде), для инверсии 4 старших бит будет использовано число 240 (11110000 в двоичном коде) <br>
00101100 XOR 11110000 = 11011100 (220 в десятичном коде).
2. Далее реализуется операция OR, 00000110 or 11011100 = 11011110 (222 в десятичном коде).
3. После реализуется операция AND, 11011110 and 00101100 = 00001100 (12 в десятичном коде).
4. Следующим шагом выполняется операция DIV, 11011100/1100 (220/12) = 18 (00010010 в двоичном коде) результат деления, остаток не учитывается
5. Последний шаг - операция ADD, 00010010 + 00001100 (18+12) = 30 (00011110 в двоичном коде)

Исходный код представлен в файле Code.txt <br>
Результат работы программы представлен на рисунке ниже
![image](https://user-images.githubusercontent.com/126500303/221666116-6f99f06e-25b4-403a-86f5-a4f890e26ee4.png)


