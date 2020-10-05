# Zadacha-6

#include <iostream>
using namespace std;
int main()
{
	int n, n1;
	int min = 0, min1 = 0,max=0,max1=0;
	int arr[100], arr1[100];
	cin >> n >> n1;
	for (int i = 1; i <= n; i++)
	{
		cin >> arr[i];
	}
	for (int j = 1; j <= n1; j++)
	{
		cin >> arr1[j];
	}
	for (int i = 1; i <= n; i++)
	{
		if (arr[i] >arr[0])
		{
			arr[0] = arr[i];
		}
		max = arr[0];
	}
	for (int i = 1; i <= n; i++)
	{
		if (arr[i] < arr[0])
		{
			arr[0] = arr[i];
		}
		min = arr[0];
	}


	cout << "First Commission" << endl << "Max: " << max << endl << "Min: " << min << endl;
	for (int j = 1; j <= n1; j++)
	{
		if (arr1[j] > arr1[0])
		{
			arr1[0] = arr1[j];
		}
		max1 = arr1[0];
	}
	for (int j = 1; j <= n1; j++)
	{
		if (arr1[j] < arr1[0])
		{
			arr1[0] = arr1[j];
		}
		min1 = arr1[0];
	}
	cout << "Second Commission" << endl << "Max: " << max1 << endl << "Min: " << min1 << endl;
	if (max1 > max)
	{
		cout << "Highest score: " << max1 << endl;
	}
	else
	{
		cout << "Highest score: " << max << endl;
	}
	if (min1 < min)
	{
		cout << "Lowest result: " << min1 << endl;
	}
	else
	{
		cout << "Lowest result: " << min << endl;
	}
}


