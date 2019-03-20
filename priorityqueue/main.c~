#include <stdio.h>
#include "boolean.h"
#include "prio_queue.h"
/*
Name: Suyanka Pokharel
Course: Computer Programming II
*/

int menu(void);

int main(void){
  queue q;
  int choice,data_item,prio_data;
  init_queue(&q);
  choice=menu();
  while(choice!= 4){
     switch(choice){
        case 1: if(!is_full()){
                  printf("Enter a data:\n");
                  scanf("%d",&data_item);
                  printf("Enter a priority data:\n");
                  scanf("%d",&prio_data);
                  add(&q,data_item,prio_data);
               }
               else{
                  printf("Error! Queue is full:\n");
               }
        break;
         
        case 2: if(!is_empty(q))
                  data_item=fetch(&q);
                else{
                  printf("Error! Queue is full:\n");
                }
        break;
        
        case 3: if(!is_empty(q))
                  print_queue(q);
                else{
                  printf("Queue is empty:\n");
                }
        break;
       
        default:
                  printf("%d is not a valid choice:\n",choice);
     }
  choice= menu();
  }
}

int menu(void){
   int selection;
     printf("\n");
     printf("1: Add\n");
     printf("2: Fetch\n");
     printf("3: List\n");
     printf("4: Quit\n");
     printf("Enter your selection:\n");
     scanf("%d", &selection);
     return selection;
}

   



    
 

        

