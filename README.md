# ADA program
This is my first git repository
'''
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int n,*array;
void input()
{
printf("Enter the total number:");
scnf("%d",&n);
array=(int*)malloc(n*sizeof(int));
for(int i=0;i<n;i++)
{
array[i]=rand()%1000;
}
printf("Unsorted array:\n");
for(int i=0;i<n;i++)
{
    printf("%d",array[i])
}
printf("\n");
}
void selectionsort()
{
    for(int i=0;i<n-1;i++)
    {
        int min=i;
        for(int j=i+1;j<n;j++)
        {
            if(array[j]<array[min])
            {
                min=j;
            }
        }
            int temp=array[j];
            array[j]=array[i];
            array[i]=temp;
    }
    
}
int main()
{
    int i;
    clock_t start=clock();
    selectionsort();
    clock_t end=clock();
    double duration=((double)(end-start))CLOCKS_PER_SEC*%1000000000;
    printf("Time taken to sort array is %.2f nano seconds",duration)
    printf("sorted array:\n");
for(int i=1;i<=n;i++)
{
    printf("%d",array[i])
}
printf("\n");
free(array);
return 0;
}
