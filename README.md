This program is designed to perform various kinds of data management tasks inside a book database on the computer. It contains the name of the book, the author name, the number of pages and the price of the book. It also keeps track of the number of books in the library database. The main practical tasks you could perform with this program would be of 4 kind. You can add a new book and it's information to the database, you can ask the computer to display that information, you can ask the system to produce a list of the books by the same author, and ofcourse, check the number of total books at a point in time.


#include <stdio.h>
#include <stdlib.h>
#include <string.h>
struct library 
{char name[40];
char writer[40];
int tot_pages;
float cost;};
int main()
{struct library lib[100];
char author[40], book[40];
int x,y,total;
x=y=total=0;
while (y!= 5) 
{printf("\n\n E - L I B R A R Y\n");
printf("\n1. Total number of books in the library\n");
printf("2. Add info\n");
printf("3. Display book info\n");
printf("4. Books of the writer\n");
printf("5. Exit\n");
printf("\n\nYour option: ");
scanf("%d",&y);
switch (y) 
{case 1:printf("\n No of books in library : %d",total);
break;
case 2:printf("Enter book name = ");
scanf("%s", lib[x].name);
printf("Enter writer= ");
scanf("%s", lib[x].writer);
printf("\nEnter pages = ");
scanf("%d", &lib[x].tot_pages);
printf("Enter price = ");
scanf("%f", &lib[x].cost);
total++;
break;
case 3:for(x=0;x<total;x++) 
{printf("book name = %s",lib[x].name);
printf("\t author name= %s",lib[x].writer);
printf("\t pages = %d",lib[x].tot_pages);
printf("\t price = %f",lib[x].cost);}
break;
case 4:printf("Enter Author: ");
scanf("%s", author);
for (x=0;x<total;x++) 
{if(strcmp(author,lib[x].writer)== 0)
printf("%s%s%d%f",lib[x].name,lib[x].writer,lib[x].tot_pages,lib[x].cost);}
break;

case 5:exit(0);
}}
return 0;}


