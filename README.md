#include<stdio.h> 
#include<stdlib.h> 
 
int top=-1,a[5]; 
int push(int); 
int pop(); 
int display(); 
 void main() 
 { 
    int ch,ele; 
    while(1){ 
 
        printf("\n enter your choice of operation on stack:");
        printf("\n1 push\n 2 pop\n 3 display\n" ) ;
        scanf("%d",&ch); 
       
        switch(ch){ 
            
            case 1: 
                   push(ele); 
                   break; 
             case 2:pop(); 
                   break; 
            case 3:display(); 
                  break; 
          default:exit(0); 
        } 
    } 
} 
 
int push(int ele) 
{ 
    ++top; 
  
    if(top<5) 
    { 
         printf("\n enter the pushed element into stack:"); 
         scanf("%d",&ele); 
        a[top]=ele; 
    } 
    else 
    { 
        printf("\n stack is over flow"); 
        top--; 
    } 
    return(0); 
} 
 
int pop(){ 
    if(top==-1) 
    { 
        printf("\n stack is under flow"); 
    } 
    else{ 
        printf("\n poped elements is %d",a[top]); 
        top--; 
    } 
} 
 
int display(){ 
    if(top==-1) 
    { 
        printf("stack is empty"); 
    } 
    else{ 
        printf("\n stack element are:"); 
        for (int i = top; i >=0; i--) 
        { 
            printf("%d ",a[i]); 
 
        } 
        printf("\n"); 
    } 
}
