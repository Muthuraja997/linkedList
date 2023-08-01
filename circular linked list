#include<stdio.h>
#include<stdlib.h>
struct node
{
    int data;
    struct node* next;
}* head,* tail;
struct node* create(int ele)
{
    struct node* node=(struct node*)malloc(sizeof(struct node));
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
        tail=newNode;
        newNode->next=head;
        
    }
    else
    {
        struct node* temp=head;
        while(temp->next!=head)
        {
            temp=temp->next;
        }
        temp->next=newNode;
        newNode->next=head;
        tail=newNode;
    }
}
void insertfirst(int ele)
{
    struct node* newNode=create(ele);
    if(head==NULL)
    {
        head=tail=newNode;
    }
    else
    {
        newNode->next=head;
        head=newNode;
        tail->next=head;
    }
}
void insertlast(int ele)
{
    struct node* newNode=create(ele);
    if(head==NULL)
    {
        printf("list is empty");
    }
    else
    {
        tail->next=newNode;
        newNode->next=head;
    }
}
void insertat(int pos,int ele)
{
    struct node* newNode=create(ele);
    if(pos==0)
    {
        insertfirst(ele);
    }
    else
    {
        struct node* temp=head;
        for(int i=0;i<pos-1;i++)
        {
            if(temp->next==head||temp==NULL)
            {
                printf("Invalid pos");
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
    struct node* temp=head;
    int flage=0;
    if(head==NULL)
    {
        printf("List is emply");
    }
    else
    {
        if(head->data==search)
        {
            insertat(1,ele);
           
        }
        else if(tail->data==search)
        {
            tail->next=newNode;
            newNode->next=head;
        }
        else
        {
            while(temp->next!=head)
            {
                if(temp->data==search)
                {
                    flage=1;
                    
                    newNode->next=temp->next;
                    temp->next=newNode;
                    break;
                    
                }
                else
                {
                    temp=temp->next;
                }
            }
            if(flage==0)
            {
                printf("Invalid search");
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
        head=temp->next;
        tail->next=head;
        free(temp);
    }
}
void dellast()
{
    struct node* temp=head;
    struct node* prev=temp;
    while(temp->next!=head)
    {
        prev=temp;
        temp=temp->next;
    }
    prev->next=head;
    free(temp);
}
void delat(int pos)
{
struct node* temp=head;
struct node* prev=temp;
for(int i=0;i<pos;i++)
{
    prev=temp;
    temp=temp->next;
}
prev->next=temp->next;
}
void delafter(int search)
{
    int flag=0;
    struct node* temp=head;
    struct node* prev=temp;
    if(head==NULL)
    {
        printf("List is empty");
    }
    while(temp->next!=head)
    {
        if(temp->data==search)
        {
            flag=1;
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
    if(flag==0)
    {
        printf("Invalid search");
    }
}
void delele(int ele)
{
    int flag=0;
    struct node* temp=head;
    struct node* prev=temp;
    if(head==NULL)
    {
        printf("List is Empty");
    }
    else
    {
    while(temp->next!=head)
    {
        if(temp->data==ele)
        {
            flag=1;
           
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
    }
    if(flag==0)
    {
        printf("Invalid ele");
    }
}
void display()
{
    struct node* temp=head;
    while(temp->next!=head)
    {
        printf("%d ",temp->data);
        temp=temp->next;
    }                      
    printf("%d ",temp->data);
}
int main()
{
    int n=1,m,ele,pos,search;
    while(n!=0)
    {
        printf("\n0-exit\n1-add\n2-insertfirst\n3-insertlast\n4-insertat\n5-insertafter\n6-delfirst\n7-dellast\n8-delat\n9-delele\n10-delafter\n11-display\n");
        printf("Enter the choise :");
        scanf("%d",&m);
        switch(m)
        {
            case 1:
            printf("*****ADD*****\n");
            printf("ENTER THE ELE :");
            scanf("%d",&ele);
            add(ele);
            printf("\n*****FINISHED*****");
            break;
            case 2:
            printf("*****INSERTFIRST*****\n");
            printf("ENETER THE ELE :");
            scanf("%d",&ele);
            insertfirst(ele);
            printf("\n*****FINISHED*****");
            break;
            case 3:
            printf("*****INSERTLAST*****\n");
            printf("ENTER THE ELE :");
            scanf("%d",&ele);
            insertlast(ele);
            printf("\n*****FINISHED*****");
            break;
            case 4:
            printf("*****INSERTAT*****\n");
            printf("ENTER THE POS AND ELE :");
            scanf("%d %d",&pos,&ele);
            insertat(pos,ele);
            printf("\n*****FINISHED*****");
            break;
            case 5:
            printf("*****INSERTAFTER*****\n");
            printf("ENTER THE SEARCH AND ELE :");
            scanf("%d %d",&search,&ele);
            insertafter(search,ele);
            printf("\n*****FINISHED*****");
            break;
            case 6:
            printf("*****DELFIRST*****\n");
            delfirst();
            printf("\n*****FINISHED*****");
            break;
            case 7:
            printf("*****DELLAST*****\n");
            dellast();
            printf("\n*****FINISHED*****");
            break;
            case 8:
            printf("*****DELAT*****\n");
            printf("ENTER THE POS : ");
            scanf("%d",&pos);
            delat(pos);;
            printf("\n*****FINISHED*****");
            break;
            case 9:
            printf("*****DELELE*****\n");
            printf("ENTER THE ELE :");
            scanf("%d",&ele);
            delele(ele);
            printf("\n*****FINISHED*****");
            break;
            case 10:
            printf("*****DELAFTER*****\n");
            printf("ENTER THE ELE :");
            scanf("%d",&ele);
            delafter(ele);
            printf("\n*****FINISHED*****");
            break;
            case 11:
            printf("*****DISPLAY*****\n");
            display();
            printf("\n*****FINISHED*****");
            break;
            case 0:
            printf("*****EXIT*****\n");
            return 0;
            break;
            
            
            
            
            
        }
    }
    // add(10);
    // add(15);
    // add(20);
    // add(30);
    // add(40);
    // insertfirst(5);
    // insertlast(50);
    // insertat(5,45);
    // insertafter(30,35);
    // delfirst();
    // dellast();
    // delat(2);
    // delafter(15);
    // delele(35);
    // display();
}










