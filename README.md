#include<iostream>
using namespace std;
int print(int start, int last)
{
	int flag = 0;
	for (int i = start; i <= last; i++)
	{
		flag = 0;
		for (int j = 2; (j <= i / 2) && (flag == 0); j++)
		{
			if (i%j == 0)
			{
				flag = 1;
			}
		}
		if (flag == 0)
		{
			cout << i << endl;
		}
	}
	return 0;
}
int main()
{
	int start = 0;
	int last = 0;
	int prime = 0;
	int choice;
	
	while(1)
	{
		cout << "Enter starting number and number should be equal to 2 or greater " << endl;
		cin >> start;
	
		cout << "Enter last number the number should be greater than starting " << endl;
		cin >> last;
	
		if(start==last)
		{
			cout<<"Wrong input !!!  "<<endl;
		}
		else
		print(start, last);
		
		cout<<"Do you want to continue Press 1 OR Do you want to quit Press 0" <<endl;
		cin>>choice;
		
		if(choice==0)
		{
			break;
		}
	}
}
