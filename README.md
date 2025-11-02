# Домашнее задание к работе 9
## Условие задачи

Написать программу, выводящую на экран заданную геометрическую фигуру, нарисованную с помощью заданного с клавиатуры символа. Предусмотреть возможность изменения размеров фигуры путем задания ее размеров в количестве символов пользователем.
Дельтоид/Только контур/R

## 1. Алгоритм и блок-схема
### Алгоритм
1. **Начало**
2. Ввод значения:
   -  `r` - радиуса (высота половины дельтоида)
   - `ch` - символа  для рисования
3. цикл **for**
   - `i = 1` -  цикл   до `r`
   - `r - i` - пробелы  слева
   - `2*i-1` - только контур
4. Вывести результат на экран.
5. **Конец**
   
### Блок-схема
<img width="122" height="421" alt="Диаграмма без названия drawio" src="https://github.com/wyrtwwr/Lab8/blob/main/lab8_shema.jpg" />

## 2. Реализация программы

#define _CRT_SECURE_NO_WARNINGS 
#define _USE_MATH_DEFINES 
#include <locale.h> 
#include <stdio.h> 
#include <stdlib.h> 
#include <conio.h> 
#include <math.h> 
int main() {
    setlocale(LC_ALL, "RUS");
    int r;          
    char ch;        
    char a;        
    int i, j;
    while (1) {
        printf("Введите радиус (высоту половины дельтоида): ");
        scanf("%d", &r);
        printf("Введите символ для рисования: ");
        scanf(" %c", &ch);
        printf("\n");
        i = 1;
        while (i <= r) {
            j = 1;
            while (j <= r - i) {
                printf(" ");
                j++;
            }
            j = 1;
            while (j <= 2 * i - 1) {
                if (j == 1 || j == 2 * i - 1)
                    printf("%c", ch);
                else
                    printf(" ");
                j++;
            }
            printf("\n");
            i++;
        }
        i = r - 1;
        while (i >= 1) {
            j = 1;
            while (j <= r - i) {
                printf(" ");
                j++;
            }
            j = 1;
            while (j <= 2 * i - 1) {
                if (j == 1 || j == 2 * i - 1)
                    printf("%c", ch);
                else
                    printf(" ");
                j++;
            }
            printf("\n");
            i--;
        }
        printf("\nПродолжить? (Да - y, Нет - n): ");
        scanf(" %c", &a);
        if (a == 'n' || a == 'N') {
            printf("Программа завершена.\n");
            break;
        }
        printf("\n");
    }
}

## 3. Результаты работы программы

Введите радиус (высоту половины дельтоида): 8
Введите символ для рисования: +
       +
      + +
     +   +
    +     +
   +       +
  +         +
 +           +
+             +
 +           +
  +         +
   +       +
    +     +
     +   +
      + +
       +
Продолжить? (Да - y, Нет - n): Y
Введите радиус (высоту половины дельтоида):

<img src="https://github.com/wyrtwwr/Lab8/blob/main/lab8_code.jpg" width="981" height="266">
