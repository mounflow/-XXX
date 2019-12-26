### 选择排序
```c
#include<stdio.h>  // 选择排序 每一次找出 最小值 
void swap(int *a,int *b)
{
	int T;
	T=*a;
	*a=*b;
	*b=T;
}

void chioce_sort(int *Arry,int len)
{
	for(int i=0;i<len-1;i++)
	{
		int min=i;
		for(int j=i+1;j<len;j++)
			if(Arry[j]<Arry[min])
				min=j;
		swap(&Arry[i],&Arry[min]);
	}

}

int main()
{
	int Arry[]={12,34,56,23,5,433,324,45,23,45,3,4,234,354};
	int len = (int)sizeof(Arry)/sizeof(*Arry);
	chioce_sort(Arry,len);
	for(int i=0;i<len;i++)
	printf("%d\t",Arry[i]);
	printf("\n");
	return 0;
	
}
```
