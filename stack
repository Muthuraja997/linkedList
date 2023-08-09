//STACK IMPLEMENTATION USING LIKEDLIST 
#include<stdio.h>
#include<stdlib.h>
struct node
{
    int data;
    struct node* next;
}* top;
void push(int ele)
{
    struct node* newNode=(struct node*)malloc((sizeof(struct node)));
    newNode->data=ele;
    newNode->next=top;
    top=newNode;
}
void pop()
{
    struct node* temp=top;
    printf("%d this element was delet \n",temp->data);
    top=temp->next;
    free(temp);
}
void display()
{
    struct node* temp=top;
    while(temp!=NULL)
    {
        printf("%d ",temp->data);
        temp=temp->next;
    }
}
void peek()
{
    if(top==NULL)
    {
        printf("List is empty");
    }
    else
    {
    printf("\nlast element is%d",top->data);
    }
}
void isempty()
{
    if(top==NULL)
    {
        printf("underflow");
    }
    else
    {
        printf("\nNo");
    }
}
int main()
{
    int n=1,choise,ele;
    while(n!=0)
    {
        printf("\n0-exit\n1-push\n2-pop\n3-isempty-4display\n");
        printf("Enter the choise :");
        scanf("%d",&choise);
        switch(choise)
        {
            case 1:
            printf("***PUSH OPERATION***\n");
            printf("Enter the value :");
            scanf("%d",&ele);
            push(ele);
            printf("\n***FINISHED***\n");
            break;
            case 2:
            printf("***POP OPERATION***\n");
            pop();
            printf("\n***FINISHED***\n");
            break;
            case 3:
            printf("***ISEMPTY OPERATION***\n");
            isempty();
            printf("\n***FINISHED***\n");
            break;
            case 4:
            printf("***DISPLAY***\n");
            display();
            printf("\n***FINISHED***\n");
            break;
            case 0:
            printf("EXIT\n");
            printf("FINSHED\n");
            return 0;
            default:
            printf("Invalid choise ");
        }
    } 
}

