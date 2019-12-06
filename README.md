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

int minimum(int a[],int n,int i)
 {
 	static int min=0;;
 	   if(i<n)
       {
       	if(a[min]>a[i])
       	 {
			      min=i;
			      minimum(a,n,++i);

        }
	   }

        return min;

 }
 int maximum(int a[],int n,int i)
 {
 	   	static int max=0;;
 	   if(i<n)
       {
       	if(a[max]<a[i])
       	 {
			      max=i;
			      maximum(a,n,++i);

        }
	   }

        return max;
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
    printf("\nminimum of array is : %d",a[(minimum(a,n,1))]);

}
