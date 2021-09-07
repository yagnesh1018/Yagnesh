//Program to Explore Stack Operations
#include<stdio.h>
#define size 5

void main()
{
    int stk[size];
int top=-1;

//PUSH operations
void push(int val)
{
if(top>=size-1)
{
printf("STACK OVERFLOW\n");
}
else
{
top++;
stk[top]=val;
}
}

//POP operations
void pop()
{
if(top==-1)
{
printf("STACK UNDERFLOW\n");
}
else
{
printf("Popped Value %d \n",stk[top]);
top--;
}
}

//TOP OF STACK operations
void top_of_stack()
{
if(top==-1)
{
printf("\nStack is Empty\n\n");
}
else
{
printf("\nTop of Stack %d \n\n",stk[top]);
}
}

//choose your option
int choice,val,ans;
do{
printf("Enter your Choice\n1->PUSH\n2->POP\n3->PEEK\n4->Exit\n\n");
scanf("%d",&choice);
printf("Enter the value\n");
scanf("%d",&val);
switch(choice)
{
case 1: push(val);top_of_stack();
break;
case 2: pop(val);top_of_stack();
break;
case 3:top_of_stack();
break;
case 4:
break;
default:printf("Invalid Entry\n");
}
  printf("\n Do you want to Continue? \n");
  printf("\n Enter 1->continue \n 2->Exit \n");
    scanf("%d",&ans);
}while(ans!=2);
}
