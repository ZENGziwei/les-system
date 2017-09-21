# les systems des étudiqnts
#include<stdio.h>
#include<malloc.h>
#include<stdlib.h>

typedef struct 
{
	char *name;
	int  num;
	char sex;
	struct student *next;
}student;




int main()
{
	char *name;
	char n[20];
	int  num;
	char sex;
	int i;
	int j=0;
	student *head,*p,*q,*r;
	head=(student*)malloc(sizeof(student));
	head->next= NULL;
	q=head;
	
	
	
	
	for(i=0;i<10;i++)
	{
		name=malloc(sizeof(n[20]));
		scanf("%s",name);
		if(name[0]!='#')
		{
			scanf("%d",&num);
			scanf("%c",&sex);
			scanf("%c",&sex);
			p= (student*)malloc(sizeof(student));
			p->name=name;
			p->num=num;
			p->sex=sex;
			q->next=p;
			q=p;
			p->next=NULL;
			
			
		}
		else
		{
			scanf("%d",&num);
			p=head->next;
			r=head->next;
			while(p!=NULL &&p->num!=num)
			{
				q=p;
				p=p->next;
				j++;
			}
			if(p==NULL)
			{
				printf("No\n");
				break;
			}
			else
			{
				if(j!=0 || r->next!=NULL)
				{
					if(p==head->next)
					{
						q=head;
					}
					
					q->next=p->next;
					p=head->next;
					while(p!=NULL)
					{
						printf("%s ",p->name);
						printf("%d ",p->num);
						printf("%c\n",p->sex);
						p=p->next;
					}
					break;
					
				

					
				}
				else
						break;
			
			}
		}
	}
	
	return 0;
	
}



