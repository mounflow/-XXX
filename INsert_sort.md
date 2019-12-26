### 插入排序
```c
#include<stdio.h>
void inset_sort(int *Arry,int len)
{
	for(int i=0;i<len;i++)
	{
		int j;
		int Temp= Arry[i];
		for(j=i;j>0&&Arry[j-1]>Temp;j--)
			Arry[j]=Arry[j-1];
		Arry[j]=Temp; 
	}
	
}
int main()
{
	int Arry[]={12,34,23,345,234,34,52,34,345,234};
	int len = (int)sizeof(Arry) / sizeof(*Arry);
	inset_sort(Arry,len);
	for(int i=0;i<len;i++)
	printf("%d\t",Arry[i]);
	printf("\n");
	return 0;
} 
```
