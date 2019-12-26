### 冒泡排序
```c
#include <stdio.h>        //冒泡排序 
void bubblu_sort(int *Arry,int len)
{
	for(int i=0;i<len-1;i++)
		for(int j=0;j<len-1-i;j++)
		if(Arry[j]>Arry[j+1]){
			int Temp= Arry[j];
			Arry[j]=Arry[j+1];
			Arry[j+1]=Temp;
		} 
}

int main()
{
	int Arry[10]={12,34,1,34,12,454,1,434,2,5};
	int len = (int) sizeof(Arry) / sizeof(*Arry);
	bubblu_sort(Arry,len);
	for(int i=0;i<len;i++)
	printf("%d\t",Arry[i]);
	return 0;
}

```
