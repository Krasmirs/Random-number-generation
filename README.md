//By calling a function in which a uniquely random number was generated. Displayed 10 random numbers on the console

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
