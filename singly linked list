#include<stdio.h>
#include<stdlib.h>
struct node
{
    int data;
    struct node* next;
}*head=NULL;
struct node* create(int ele)
{
    struct node*node=malloc(sizeof(struct node*));
    node->data=ele;
    node->next=NULL;
    return node;
}
void add(int ele)
{
    struct node* newNode=create(ele);
    if(head==NULL)
    {
        head=newNode;
    }
    else
    {
        struct node*temp=head;
        while(temp->next!=NULL)
        {
            temp=temp->next;
        }
        temp->next=newNode;
    }
}
void insertfirst(int ele)
{
    struct node* newNode=create(ele);
    if(head==NULL)
    {
        head=newNode;
    }
    else
    {
        newNode->next=head;
        head=newNode;
    }
    
}
void display()
{
    struct node* temp=head;
    if(head==NULL)
    {
        printf("List is empty");
    }
    else
    {
    while(temp!=NULL)
    {
        printf("%d ",temp->data);
        temp=temp->next;
    }
    }
}
void insertlast(int ele)
{
    struct node* newNode=create(ele);
    if(head==NULL)
    {
        printf("List is empty");
    }
    else{
        struct node* temp=head;
        while(temp->next!=NULL)
        {
            temp = temp->next;
        }
        temp->next=newNode;
    }
}
void insertat(int pos,int ele)
{
    struct node* newNode=create(ele);
    struct node* temp=head;
    if(head==NULL)
    {
        printf("List is empty\n");
    }
    else if(pos==0)
    {
        insertfirst(ele);
    }
    else if(pos>0)
    {
        for(int i=0;i<pos-1;i++)
        {
            if(temp->next==NULL)
            {
                printf("Invalid pos\n");
                break;
            }
            else
            {
            temp=temp->next;
            }
        }
        newNode->next=temp->next;
        temp->next=newNode;
    }
}
void insertafter(int search,int ele)
{
    struct node* newNode=create(ele);
    if(head==NULL)
    {
        printf("List is empty");
    }
    else
    {
        struct node* temp=head;
        while(temp!=NULL)
        {
            if(temp->data==search)
            {
                newNode->next=temp->next;
                temp->next=newNode;
                break;
            }
            else
            {
                temp=temp->next;
            }
        }
    }
}
void delfirst()
{
    if(head==NULL)
    {
        printf("List is empty");
    }
    else
    {
        struct node* temp=head;
        head=head->next;
        free(temp);
    }
}
void dellast()
{
    if(head==NULL)
    {
        printf("List is empty");
    }
    else
    {
    struct node* temp = head;
    struct node* prev=temp;
    while(temp->next!=NULL)
    {
        prev=temp;
        temp=temp->next;
    }
    prev->next=NULL;
    free(temp);
    }
}
void delat(int pos)
{
    if(pos==0)
    {
        delfirst();
    }
    else
    {
        struct node* temp=head;
        struct node* prev=temp;
        for(int i=0;i<=pos-1;i++)
        {
            if(temp->next==NULL)
            {
                printf("Invalid pos\n");
                break;
            }
            else
            {
            prev=temp;
            temp=temp->next;
            }
        }
        prev->next=temp->next;
        free(temp);
    }
}
void delele(int ele)
{
    struct node* temp=head;
    struct node* prev=temp;
    int flog=0;
    if(head==NULL)
    {
        printf("List is empty\n");
    }
    else if(head->data==ele)
    {
        delfirst();
    }
  
    else
    {
    while(temp!=NULL)
    {
        if(temp->data==ele)
        {
            flog=1;
            prev->next=temp->next;
            free(temp);
            break;
        }
        else
        {
            prev=temp;
            temp=temp->next;
        }
     
    }
    if(flog==0)
    {
        printf("Element not found\n");
    }
    
}
}
void delafter(int ele)
{
    struct node* temp=head;
    struct node* prev=temp;
    if(head==NULL)
    {
        printf("List is empty");
    }
    else
    {
        while(temp!=NULL)
        {
            if(temp->data==ele)
            {
                prev=temp;
                temp=temp->next;
                prev->next=temp->next;
                free(temp);
                break;
                
                
            }
            else
            {
                temp=temp->next;
            }
        }
    }
}
 int main()
{
     int choice,ele,pos,search,option;
     int n=1;
     //printf("00-exit,1-add,2-insertfirst,3-insertlast,4-insertat,5-insertafter,6-delfirst,7-dellast,8-delat,9-delafter,10-delele,11-display\n");
      while(n!=0)
     {
         printf("0-exit,1-add,2-insertfirst,3-insertlast,4-insertat,5-insertafter,6-delfirst,7-dellast,8-delat,9-delafter,10-delele,11-display\n");
         printf("Enter the choice :");
          scanf("%d",&choice);
 
     
    
 
     switch(choice)
     {
         case 1:
         //int ele;
         printf("****added******\n");
         printf("enter the value for add :");
         scanf("%d",&ele);
         add(ele);
         printf("****Finished*****\n");
         printf("choice :");
         break;
         case 2:
         //int ele;
         printf("***insert first****\n");
         printf("enter the value for insert :");
         scanf("%d",&ele);
         insertfirst(ele);
         printf("*****finished****\n");
         printf("choice :");
         break;
         case 3:
         printf("*****insertlast*****\n");
         printf("enter the value for insert :");
         scanf("%d",&ele);
         insertlast(ele);
         printf("*****finished*****\n");
         printf("choice :");
         break;
         case 4:
         printf("*****insertat*****\n");
         printf("enter the value of pos and ele :");
         scanf("%d %d",&pos,&ele);
         insertat(pos,ele);
         printf("***finished***\n");
         printf("choice :");
         break;
         case 5:
         printf("***insertafter***\n");
         printf("enter the value of search ele and ele :");
         scanf("%d %d",&search,&ele);
         insertafter(search,ele);
         printf("***finished***\n");
         printf("choice :");
         break;
         case 6:
         printf("***delfirst***\n");
         delfirst();
         printf("**finished***\n");
         printf("choice :");
         break;
         case 7:
         printf("***dellast***\n");
         dellast();
         printf("***finished***\n");
         printf("choice :");
         break;
         case 8:
         printf("***delat***\n");
         printf("enter the pos :");
         scanf("%d",&pos);
         delat(pos);
         printf("***finished***\n");
         printf("choice :");
         break;
         case 9:
         printf("***delafter***\n");
         printf("enter the ele :");
         scanf("%d",&ele);
         delafter(ele);
         printf("***finished***\n");
         printf("choice :");
         break;
         case 10:
         printf("***delele***\n");
         printf("enter the ele :");
         scanf("%d",&ele);
         delele(ele);
         printf("***finished***\n");
         printf("choice :");
         break;
         case 11:
         printf("***display***\n");
         display();
         printf("\n***finished***\n");
         printf("choice :");
         break;
         case 0:
         printf("***exit***");
         return 0;
         default:
         printf("Invalid choice\n");
         printf("choice :");
         break;
     }
     
     
     }
 
  
    
    // add(10);
    // add(20);
    // add(30);
    // insertfirst(5);
    // insertlast(100);
    // insertat(3,25);
    // insertafter(30,35);
    // delfirst();
    // dellast();
    // delat(2);
    // delele(10);
    // display();
}





