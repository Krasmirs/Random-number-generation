///////////////////////////////////////////////////////////////////////////////////////////

/* Генерациия 10 уникальных рандомных чсел в диапазоне от 1 до 1000!*/


#include<iostream>
#include<ctime>
using namespace std;
int main()
{
	srand(time(NULL));
	const int size = 10;
	int arr[size];
	bool proverca;

	for (int i = 0; i < size; )
	{
		proverca = false;
		int randomnum = rand()% 1000;
		for (int j = 0; j <i ; j++)
		{
			if(arr[j]==randomnum)
			{
				proverca = true;
				break;
			}
			
			
		}
		if (!proverca)
		{
			arr[i] = randomnum;
			i++;
		}
		
	}
	
	
	int minvalue = arr[0];
	
	for (int i = 1; i < size; i++)
	{
		if (arr[i] < minvalue)
			minvalue = arr[i];

	}
	cout << minvalue << endl;
}


///////////////////////////////////////////////////////////////////////////////////////////////////////////////////

/* Сгенерировано 10 уникальных чисел выведено в консоле и выведено минимальное число из этого массива!*/



#include<iostream>
#include<ctime>

using namespace std;

int main() {

	srand(time(NULL));
	const int size = 10;
	int arr[size];
	int randnumer;
	bool proverka;
	for (int i = 0; i < size;)
	{
		randnumer = rand() % 20;
		proverka = false;
		
		for (int j = 0; j < i; j++)
		{
			if (arr[j]==randnumer)
			{
				proverka = true;
				break;
			}
			
		}
		
		
			if (!proverka)
			{
				arr[i] = randnumer;
				i++;
			}
		
		
	}
	for (int i = 0; i < size; i++)
	{
		cout << arr[i] << endl;
	}

	int minvalue=arr[0];
	for (int i = 0; i < size; i++)
	{
		if(minvalue>arr[i])
		{
			minvalue = arr[i];
		
		}
		
	}
	cout << endl << "Minimal numer - (" <<  minvalue<< ")";
}
////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

/* С помощю вызова функции в которой было сгенерированно уникальне ранндомное число. Выведено на консоль 10 ранндомных чисел! */



#include<iostream>
#include<ctime>
using namespace std;

void set(int arr[], const int size)
{
	srand(time(NULL));
	bool proverka;
	int randnumer;
	for (int i = 0; i < size;)
	{
		proverka = false;
		randnumer = rand() % 10;
		for (int j = 0; j < i; j++)
		{
			if (arr[j]==randnumer)
			{
				proverka = true;
			}
		}
		if (!proverka)
		{
			arr[i] = randnumer;
			i++;
		}
	}
	

}

void setcout(int arr[], const int size)
{
	for (int i = 0; i < size; i++)
	{
		cout << arr[i] << endl;
	}
	

}



void main() 
{
	const int size = 10;
	int arr1[size];
	set( arr1, size);
	setcout(arr1, size);

}
