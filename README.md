# CTest01
c语言初学者的随手练习档案


//输出100以内的素数
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

------------------------------------------------------------------------------------------------------------------------
 int main() 
{
	int arr[] = { 1,2,3,4,5,6,7,8,9,10 };
	int left = 0;
	int right = 0;
	int yyds = sizeof(arr) / sizeof(arr[0]);
	right = yyds - 1;
	int bb = 9;

       while (left <= right)
	{ 
		int mid =(left + right)/ 2;
		if (arr[mid] > bb)
		{
			right = mid - 1;
		}
		else if (arr[mid] < bb)
		{
			left = mid + 1;
		}
		else  if (arr[mid]=bb)
		{
			printf("该数下标为 ;%d\n", mid);
			break;
		}
		 
		 

	}
	if (left > right)
	{
		printf("该数不存在");

	}
	return 0;
	
	
}
--------------------------------------------------------------------------------------------------------------
#include<stdio.h>

struct Movie
{
	char name[20];
	float time;

};
int main()
{
	struct Movie nv = { "月球陨落" ,2.2 };
	printf("该电影的名称是；%s\n",nv.name);
	printf("该电影电影的时长是；%0.3f", nv.time);
	return 0;
}
-----------------------------------------------------------------------------------------------
#include<stdio.h>
#include<string.h>
#include<stdlib.h>
#include<windows.h>
int main()
{
	char m[] = "Welcome to chaohu ";
	char n [] = "******************";
	int rightm = sizeof(m) / sizeof(m[0]);
	rightm = rightm - 2;
	int left = 0;
	 
	while (left <= rightm)
	{
		 
		n[rightm] = m[rightm];
		n[left] = m[left];
		printf("%s\n",n);
		Sleep (1000);//单位毫秒
		left++;
		rightm--;
	}
	system("cls");
	return 0;
}
----------------------------------------------------------------------------------------------------------------------------
#include<stdio.h>

void Swap(int* bn, int* bh)
{
	int temp = 2;
	temp = *bh;
	*bh = *bn;
	*bn = temp;
}
int main()
{
	int a = 12;
	int b = 21;
	printf("a=%d\n,b=%d\n",a,b);
	Swap(&a, &b);
		printf("a=%d\n ,b=%d\n",a,b);
}
