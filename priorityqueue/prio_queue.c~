#include <stdio.h>
#include <stdlib.h>
#include "boolean.h"
#include "prio_queue.h"

void init_queue(queue *q){
   (*q)= (queue) malloc (sizeof(struct endpointer));
   (*q)-> front=NULL;
   (*q)-> back=NULL;
}

boolean is_full(void){
   node_pointer temp;
   temp= (node_pointer) malloc (sizeof(struct queuenode));
   if (temp == NULL)
      return TRUE;
   else
      return FALSE;
}

boolean is_empty(queue q){
   if ((q->front ==NULL) && (q->back==NULL))
      return TRUE;
   else
      return FALSE;
}
  
void add( queue *q, int x , int y){
   node_pointer temp, newpo;
   newpo=(node_pointer) malloc (sizeof(struct queuenode));
   newpo->data=x;
   newpo->prior=y;
   if(((*q)->front==NULL) && ((*q)->back==NULL)){
      newpo->next=NULL;
      (*q)->front=newpo;
      (*q)->back=newpo;
   }
   else if(newpo-> prior <= (*q)->back->prior){
      newpo-> next= NULL;
      (*q)->back->next=newpo;
   }
   else if(newpo->prior>(*q)->front->prior){
      newpo->next=(*q)->front;
      (*q)-> front=newpo;
   }
   else{
      temp=(*q)->front;
      while (newpo->prior <= temp->next->prior){
         temp=temp->next;
      }
         newpo->next=temp->next;
         temp->next=newpo;
   }
}

int fetch(queue *q){
   node_pointer temp;
   int prio_data;
   int data_removed;
   temp=(*q)-> front;
   data_removed=temp->data;
   prio_data= temp->data;
   if((*q)->front==(*q)->back){
      (*q)->front=NULL;
      (*q)->back=NULL;
   }
   else{
      (*q)->front=temp->next;
   }
   free (temp);
   printf("%d  priority: %d is deleted from the queue\n",data_removed,prio_data);
}

void print_queue(queue q){
   node_pointer temp;
   temp=q->front;
   while(temp!=NULL){
     printf("%d priority:",temp->data);
     temp= temp->next;
   }
}

   

