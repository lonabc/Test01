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

------------------------------------------------------------------------------------------------------------------------------------
#define  _CRT_SECURE_NO_WARNINGS

#include<stdio.h>
#include<string.h>

int main()
{
	char password[] = { 0 };
	for (int mbcc = 1; mbcc <= 3; mbcc++)
	{
		scanf("%s", password);
		if (strcmp(password,"23456") == 0)
		{
			printf("您好殷传国先生");
			break;


		}
		else
		{
			printf("您好，您的密码错误，请在次输入");
		}
		if (mbcc== 3)
		{
			printf("您的账户已被冻结");
			break;
		}
	}
	return 0;
}
--------------------------------------------------------------------------------------
#include<stdio.h>
#include<math.h>

int Suoi_w(int g)
{
	int hg = 1;
	for (int r = 2; r < g; r++)
	{
		int bv = g % r;
		if (bv == 0)
		{
			hg = 0;
			return 0;
		}
		return 1;
	}
}
int main()
{
	int hgd = 0;
	for (int y = 100; y <= 200; y++)
	{
		int h = Suoi_w(y);
		if (h == 1)
		{
			
			printf("%d ",y);
			hgd++;
			if (hgd == 8)
			{
				hgd = 0;
				printf("\n");
			}
		}
	}
}
----------------------------------------------------------------------------------------------------------------------------------
#include<stdio.h>

int bvc(int arr[], int j ,int sz)
{
	 
	int right = sz - 1;
	int left = 0;

	while (right >= left)
	{

		int mid = (right + left) / 2;
		if (arr[mid] > j)
		{
			right = mid - 1;
		}
		else if (arr[mid] < j)
		{
			left = mid + 1;
		}
		else
		{
			return mid;
			break;
		}
	
	}
	if (right < left)
	{
		return -1;
	}
}
int main()
{
	int arr[] = {1,2,3,4,5,6,7,8,9,10};
	 
	 
	int j = 8;
	int sz = sizeof(arr) / sizeof(arr[0]);
	int k = bvc(arr, j,sz);
	if (k == -1)
	{
		printf("找不到指定数值\n");
	}
	else {
		printf("该数值的下标为%d\n",k);
	}
	 
} 
--------------------------------------------------------------------------------------------------
#include<stdio.h>

int main()
{
 int n,m,sum;
 scanf("%d",&n);
  for(int i =1;i<=n;i++)
  {
    int m=1;
    for(int j=1;j<=i;j++)
    {
      m=m*j;
    }
    sum =sum+m;
  }
  printf("%d\n",sum);
  return 0;
}
------
#define  _CRT_SECURE_NO_WARNINGS 
#include<stdio.h>


int main()
{
	int  a, b,add;
	b = 1;
	add = 0;
	scanf("%d",&a);
	for (int i = 1; i <= a; i++)
	{
		b = b * i;
			add = add + b;

	}
	printf("%d",add);
	return 0;
}
-----------------------------------------------------------------------------------------
#define    _CRT_SECURE_NO_WARNINGS 1

#include<stdio.h>
#include<math.h>
#include<string.h>
#include<windows.h>

void main()
{
	 
	int i = 0;
	char password[20] = { 0 };
	 
	for (int i = 0; i < 3; i++)
	{
		printf("请输入密码：\n");
	    scanf("%s",&password);
		 
		if (strcmp(password , "123456b") == 0)
		{
			printf("登入成功\n");
			break;
		}
		else
		{
			printf("登录失败\n");
		}
	}
	if (i == 3)
	{
		return 0;
	}
}
---------------------------------------------------------------------------------------------------
int Ying(char* e)
{
	int m = 0;
	while (*e != '\0')
	{
		m++;
		e++;

	}
	return m;

}


int main()
{
	int c = 0;
	char  e[] = "hello sir";
	 
	c = Ying(e);
	printf("%d",c);
	return 0;

}
-------------------------------------
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
 

int Fib(int h)
{
	 
	if (h > 1)
	{
		return  h * Fib(h - 1);
	}
	else
	{
		return  1;
	}

}
int main()
{
	int m = 0;
	scanf("%d",&m);
	int b = Fib(m);
	printf("%d\n",b);
	return 0;
} 
----------------------------------------
#define _CRT_SECURE_NO_WARNINGS
#include<stdio.h>
 
int main()
{
	printf("请输入三个浮点型数据，每一个数据换行确认；");
	float m, n, v;
	scanf("%f %f %f",&m,&n,&v);
	if (n > v)
	{

		if (v > m)
		{
			printf("从大到小为：%2.6f %4.6f %4.6f", n, v, m);
		}
		else if (n > m)
		{
			printf("从大到小为：%2.6f %4.6f %4.6f", n, m, v);
		}
		else
		{
			printf("从大到小为：%2.6f %4.6f %4.6f", m, n, v);
		}
	}
	else
	{
		if (n > m)
		{
			printf("从大到小为：%2.6f %4.6f %4.6f", v, n, m);
		}
		else if (m > v)
		{
			printf("从大到小为：%2.6f %4.6f %4.6f", m, v, n);
		}
		else
		{
			printf("从大到小为：%2.6f %4.6f %4.6f", v, m, n);
		}

	}

	return 0;
}
------------------------------
#define _CRT_SECURE_NO_WARNINGS 
#include<stdio.h>

int main()
{
	int arr[3][4] = { { 1,2,3,4 },{5} };
	for (int i = 0; i <3; i++)
	{
		for (int j = 0; j < 4; j++)
		{
			printf("%d ",arr[i][j] );
			 
		}
		printf("\n");
	}
	return 0；
----------------------------------------------
#include<stdio.h>
struct Book
{
	char name[20];
	short price;
};
int main()
{
	struct  Book b1 = {"c语言程序设计",55};
	printf("%s\n",b1.name);
	printf("%d\n",b1.price);
	return 0;
}
--------------------------

#include<stdio.h>

void Add0(int arr[], int count)
{
	for (int i =0;i<count-1;i++)
	{
		
		for ( int j = 0; j < count-1-i; j++)
		{
			if (arr[j]<arr[j+1])
			{
				int temp = arr[j+1];
				arr[j + 1] = arr[j];
				arr[j] = temp;
			}
		}

	}
}

int main()
{
	int arr[10] = { 0,1,2,3,4,5,6,7,8,9 };
	int count = sizeof(arr) / sizeof(arr[0]);
	Add0(arr,count);
	printf("arr[10]= ");
	for (int i = 0; i < count; i++)
	{
		printf("%d ",arr[i]);
	}
	 
	return 0;

}
-------------------------
#define _CRT_SECURE_NO_WARNINGS 1
#include <stdio.h>
#include<string.h>
  int main()
{ 
	  for (int i = 1; i <= 4; i++)
	  {
		  for (int m = 1; m <= 4 - i; m++)
		  {
			  printf(" ");
		  }

		  for (int j = 1; j <= 2 * i - 1; j++)
		  {
			  printf("%c", '*');
		  }
		  printf("\t");
		  for (int m = 1; m <= 4 - i; m++)
		  {
			  printf(" ");
		  }
		  for (int j = 1; j <= 2 * i - 1; j++)
		  {
			  printf("%c", '*');
		  }

		  printf("\n");
	  }

	  for (int i = 1; i <= 7; i++)
	  {
		  for (int j = 1; j <= i; j++)
		  {
			  printf(" ");
		  }
		  for(int m=1;m<=15-i*2;m++)
		  {
			  printf("*");
           }
		  printf("\n");
	  }
 	printf("\n殷传国");
	return 0;
}
---------------------------------------
int main()
{ 
	  int arr[3][4] = { {1,2,3,4},{5,6,7,8},{9,10,11,12} };
	  int arr1[4][3];
	  for (int i = 0; i <3; i++)
	  {
		  for (int j = 0; j < 4; j++)
		  {
			  printf("%d ",arr[i][j]);
		  }
		  printf("\n");
	  }
	  for (int i = 0; i < 3; i++)
	  {
		  for(int j=0;j<4;j++)
		  {
			 arr1[j][i] = arr[i][j];
		  }
	  }
	  for (int i = 0; i < 4; i++)
	  {
		  for (int j = 0; j < 3; j++)
		  {
			  printf("%d ",arr1[i][j]);
		  }
		  printf("\n");
	  }
 	printf("\n殷传国");
	return 0;
}
-----------------------------------------
#define _CRT_SECURE_NO_WARNINGS 1
#include <stdio.h>
#include<string.h>
#include<math.h>
#include<Windows.h>
int binary(int* arr ,int key, int low, int high)
{
	int mid = 0;
	while (low <= high)
	{
		mid =( high + low)/2;
		if (key <= arr[mid])
		{
			high = mid - 1;
		}
		else {
			low = mid + 1;
		}

	}
	return low;
}
void bin(int* arr,int sz)
{
	for (int i = 1; i < sz; i++)
	{
		int key = arr[i];
		int loc = binary(arr,key,0,i);
		if (loc !=i)
		{
			for (int j = i - 1; j >= loc; j--)
			{
				arr[j + 1] = arr[j];
			}
			arr[loc] = key;
		}
	}
}

int main()
{
	int arr[5] = {2,3,1,5,4};
	int sz = sizeof(arr) /sizeof( arr[0]);
	bin(arr,sz);
	int left = 0;
	int right = sz - 1;
	for (int i = 0; i < 5; i++)
	{
		printf("%d ",arr[i]);
	}
	printf("\n殷传国");
	return 0;
}
