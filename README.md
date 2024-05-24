#include<stdio.h>
#include<stdlib.h>  
int search(int arr[], int n, int x)  
{  
    for (int i = 0; i < n; i++)  
        if (arr[i] == x)  
            return i;  
    return -1;  
}  
int binarySearch(int arr[], int l, int r, int x)  
{  
    while (l <= r) {  
        int m = l + (r - l) / 2;  
        if (arr[m] == x)  
          {  
            return m;  
          }    
  
        if (arr[m] < x)  
        {  
            l = m + 1;  
        }   
        else{  
            r = m - 1;  
        }  
    }  
    return -1;  
}  
void bubbleSort(int a[], int n)  
{ 
    for (int i = 0; i < n; i++)  
    { 
        for (int j = i + 1; j < n; j++)  
        { 
            if (a[i] > a[j]) { 
                int temp = a[i]; 
                a[i] = a[j]; 
                a[j] = temp; 
            } 
        } 
    } 
} 
int main()  
{  
    int n,x;  
    int result;
    printf("enter the n number:-");  
    scanf("%d",&n);  

    int arr[n];  
   printf("enter the array values:-");  
    for(int i=0;i<n;i++){  
        scanf("%d",&arr[i]);  
    }  

    printf("enter the searching element:-");  
    scanf("%d",&x);  

    printf(" 1 linear \n 2 binary\n 3 exit\n");
    int op;
    scanf("%d",&op);
    switch(op){
        while(1){
            case 1:
            result=search(arr, n, x); 
            break;
            case 2:
             bubbleSort(arr, n); 
            printf("Sorted Order: \n"); 
            for (int i = 0; i < n; i++) {
            
            printf("%d\n", arr[i]); }
           result= binarySearch(arr, 0, n-1, x); 
            break;
            case 3:
            exit(0);
            break;
            default:
            printf("invalid input ");


        }

    }

     if(result == -1)  
    {  
     printf("Element is not present in array");  
    }  
  else{  
 printf("Element is present at index %d", result);  
  }  
    return 0;  
} 
