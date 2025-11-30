# Домашнее задание к работе 9
## Условие задачи

Написать программу, выводящую на экран заданную
геометрическую фигуру, нарисованную с помощью заданного с клавиатуры
символа, условие заполнения фигуры и задаваемые параметры фигуры в
таблице (остальные можно взять константные)
- Равносторонний треугольник
- Высота h
- Только контур

## 1. Алгоритм и блок-схема
### Алгоритм
1. **Начало**
2. Ввод значения:
   - `h` -высота
   - `ch` - символа  для рисования
3. цикл **for**
   - `i = 1` -  цикл   до `r`
   - `h - i` - пробелы  слева
   - `2*i-1` - только контур
4. Вывести результат на экран.
5. **Конец**
   
### Блок-схема
<img width="669" height="711" alt="{1D312FEB-878E-43A6-9BAD-CD0FAEDD2C9F}" src="https://github.com/user-attachments/assets/015343c0-3363-4414-b564-3069e482c9d9" />


## 2. Реализация программы
```
#define _CRT_SECURE_NO_WARNINGS 
#define _USE_MATH_DEFINES 
#include <locale.h> 
#include <stdio.h> 
#include <stdlib.h> 
#include <conio.h> 
#include <math.h> 

int main() {

    setlocale(LC_ALL, "RUS");

    char sim;
    char cont = 'y';
    int h;

    while (cont == 'y' || cont == 'Y') {

        printf("Введите символ: ");
        scanf(" %c", &sim);

        printf("Введите высоту треугольника: ");
        scanf("%d", &h);

       
        for (int i = 1; i <= h; i++) {

           
            for (int s = 0; s < h - i; s++) {
                printf(" ");
            }

            if (i == 1) {                 
                printf("%c\n", sim);
                continue;
            }

            if (i == h) {                
                for (int k = 0; k < 2 * h - 1; k++) {
                    printf("%c", sim);
                }
                printf("\n");
                continue;
            }


            printf("%c", ch);          

            for (int k = 0; k < 2 * i - 3; k++) {
                printf(" ");              
            }

            printf("%c\n", sim);          
        }

    
        printf("\nПродолжить? (Да - y, Нет - n): ");
        scanf(" %c", &cont);
        printf("\n");
    }
    return 0;
}
```
## 3. Результаты работы программы
```
Введите символ: *
Введите высоту треугольника: 10
         *
        * *
       *   *
      *     *
     *       *
    *         *
   *           *
  *             *
 *               *
*******************

Продолжить? (Да - y, Нет - n): Y

Введите символ:

```

<img width="1190" height="378" alt="{02DB0E77-7075-4A7A-9BC8-0221A9C6CC69}" src="https://github.com/user-attachments/assets/6b245355-f00c-4328-920b-6197fbe5efa4" />

