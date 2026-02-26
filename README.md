//Bubble-sort
#include <stdio.h>
void swap(int arr[],int i,int j)
{
int temp;
temp=arr[i];
arr[i]=arr[j];
arr[j]=temp;
}
void bubble(int arr[],int n)
{
int i,j;
for(i=0;i<n-1;i++)
{
for(j=0;j<n-i-1;j++)
{
if(arr[j]>arr[j+1])
{
swap(arr,j,j+1);
}
}
}
}

int main()
{
int arr[100];
int n,i;
printf("Enter number of terms ");
scanf("%d",&n);
printf("Enter elements in array ");
for(i=0;i<n;i++)
{
scanf("%d",&arr[i]);
}
bubble(arr,n);
printf("Sorted array ");
for(i=0;i<n;i++)
{
printf("%d ,",arr[i]);
printf("\n");
}
return 0;
}

