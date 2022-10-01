# Test01
初学者的随手练习档案
#include<stdio.h>
int main()
{
	int count = 0;
	
	for (int i = 2; i <= 10; i++)
	{
		char op = 'q';
		for (int g = 2; g < i; g++)
		{
			int m = i % g;
			if (m == 0)
			{
				op = 'a';
				break;
			}
		}
		if (op == 'q')
		{
			
				printf("i=%d",i );
				printf(" ");
				count++;
				if (count == 8)
				{
					printf("\n");
					count = 0;
				}
		}
	}
}
