# stacks-usingarray
#include<stdio.h>
#include<stdlib.h>
#define MAX 5
int a[MAX],top=-1;
void push(int x)
{
        if(top==MAX-1)
        {
                printf("stack overflowen");
        }
        else
        {
                a[++top]=x;
        }
}
int pop()
{
        int x;
        if(top==-1)
                return -1;
        else
        {
                x=a[top];
                top--;
                return x;
        }
}
int peek()
{
        return a[top];
}
int display()
{
        int i;
        if(top==-1)
        {
                printf("there are no elements to display");
        }
        else
        {
                for(i=top;i>=0;i--)
                {
       
                        printf("\n%d",a[i]);
                }
        }
}
void main()
{
        int x;
        while(1)
        {
        printf("\nenter your choice \n1.push \n2.pop \n3.peek \n4.display \n5.exit");
        scanf("%d",&x);
        switch(x)
        {
                case 1:
                        printf("enter element to insert");
                        scanf("%d",&x);
                        push(x);
                        break;
                case 2:
                        x=pop();
                        if(x==-1)
                        {
                                printf("stack underflown");
                        }
                        else
                        {
                                printf("the element deleted is=%d",x);
                        }
                        break;
                case 3:
                        x=peek();
                        printf("the element in the top of the stack is %d",x);
                        break;
                case 4:
                        printf("the elements in the stack are:");
                        display();
                        break;
                case 5:
                        exit(0);
}
}
}
