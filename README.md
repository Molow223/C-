//Объявить три массива. Первые два заполнить случайными значениями  от 10 до 30.
//В элементы третьего массива записать сумму соответствующих элементов первых двух массивов. 

#include <iostream>

using namespace std;

int main()
{
	//Подключение русского языка
	setlocale(LC_ALL, "rus");
	//Инициализируем массивы и переменные
	const int size=10;
	int Arr[size] = {};
	int Arr2[size] = {};
	int Arr3[size] = {};
	//Заполняем первый массив
	cout << "Массив Arr:  ";
	for (int i = 0; i < size; i++)
	{
		Arr[i] = 10 + rand() % 21;
		cout << Arr[i] << " | ";
	}
	cout << endl << endl;
	//Заполняем второй массив
	cout << "Массив Arr2: ";
	for (int i = 0; i < size; i++)
	{
		Arr2[i] = 10 + rand() % 21;
		cout << Arr2[i] << " | ";
	}
	cout << endl << endl;

	// Заполняем третий массив
	cout << "Массив Arr3: ";
	for (int i = 0; i < size; i++)
	{
		Arr3[i] = Arr[i] + Arr2[i];
		cout << Arr3[i] << " | ";
	}
	cout << endl << endl;

	// Ищем среднее арифмитическое, минимум и максимум
	int averageValue = 0;
	int sum = 0;
	int minValue = Arr3[0];
	int maxValue = Arr3[0];
	for (int i = 0; i < size; i++)
	{
		sum += Arr3[i];

		if (Arr3[i] < minValue)
		{
			minValue = Arr3[i];
		}
		if (Arr3[i] > maxValue)
		{
			maxValue = Arr3[i];
		}
	}
	averageValue = sum / size;
	cout << "Среднеe арифметическое = " << averageValue << endl;
	cout << "Минимальное значение   = " << minValue << endl;
	cout << "Максимальное значение  = " << maxValue << endl;
	cout << endl << endl;


	
	return 0;
}
