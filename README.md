
#include<stdio.h>
int main()
{
	int i, j;
	int k = 0;
	for (i = 100; i < 1000; i++)//设定一个三位数 
	{
	  for (j = 2; j < i; j++) //设定一个小于被求出的除数，并不断增加这个除数
	{
		if (i % j == 0)//判断余数是否为零，如果为零，则跳出循环
		{
			break;
		}
	}if (j == i) //当所有的j都求不出来余数为零，则判读该数为指数，
	{
		k++;	
	}
}
printf("%d\n", k);
return 0;
}
