#  Пример кода C# #

Условия

```c#

int a = 5;

if (a > 3)
{
  Console.WriteLine("a больше трех"); //При a = 5 выполнится это действие
}
else
{
  Console.WriteLine("a меньше трех");
}

```

Циклы

```c#

for (int i = 0; i < 10; i++)
{
  Console.WriteLine(i);
}

```

Функции

```c#

int positionX = 0;
int positionY = 0;

//Функция принимает два аргумента(x, y). При выполнении функция прибавит к текущему значению переменной positionX значение аргумента x, а к positionY значение аргумента y
void Move(int x, int y)
{
  positionX += x;
  posirionY += y;
}

```

Массивы

```c#

int[] array = new int[4] { 15, 25, 35, 45 };

Console.WriteLine(nums[0]); // выведет в консоль 15

//цикл пройдется по каждому элементу массива и выведет его в консоль
foreach (int elem in array)
{
    Console.WriteLine(elem);
}

```

