
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
//以下为简化算法后的代码
#include<stdio.h>
#include<math.h>
int main() {
	int i, j;
	int k = 0;
	for (i = 101; i < 996; i+=2) //结尾是质数的才有可能是质数，能极大降低检测的质数数量
	{
		for (j = 2; j < sqrt(i); j++) //只需要小于被除数的开方即可，约数是成对出现的，比开方都大的数据也进行计算就无意义了
		{
			if (i % j == 0) 
			{
				break;
			}
		}if (j > sqrt(i)) 
		{
			k++;
		}
	}
	printf("%d\n", k+1);
	return 0;
}
