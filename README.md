#include<stdio.h>
#include <conio.h>
int Sum_Number(int a[], int n)
{
    int i, sum=0;
    for(i=0;i<n;i++)
    {
        sum+=a[i];
    }
    return sum;

}

int main()
{
    int a[10],i,n,sum;
    double average;

    printf("Enter the size of array : ");
    scanf("%d",&n);
    printf("Enter elements in array: ");
    for(i=0; i<n; i++)
    {
        scanf("%d", &a[i]);
    }
    sum= Sum_Number(a,n);
    printf("sum of array is :%d\n",sum);
    average= sum/n;
    printf("average: %.2lf", average);

}
