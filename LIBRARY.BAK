#include<stdio.h>
#include<conio.h>
#include<dos.h>
#include<string.h>


// SUTRUCTURE DESIGNING
typedef struct Book
{
char title[20];
char author[20];
}Book;




Book *book;  // This Is Global Book Type Pointer
int count =0; // This Is  Global Count Variable
int size;    // This Is  Global Variable For Dynamic Memory Allocation





// PASSWORD  PROTECTED
char mypassword[10]= {"mabx"};



// DECLARATIONS


void password();
void mainmenu();


// CASE 1 ADD BOOKS
void addbook()
{
clrscr();

printf("\n***** Add New Book Detail ******");
printf("\n Enter Book Title : ");
gets(book[count].title);
printf("\n Enter Book Author : ");
fflush(stdin);
gets(book[count].author);
count++;
}







//CASE 2 VIEW BOOKS 
void viewbooks()

{

int i;
clrscr();

printf("\n\n\t\t \xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB Books Details \xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB  ");

printf("\n\n\t\t Book Title \t\t\t Book Author  \t\n\n");

for (i=0;  i<count;  i++){
printf("\n\t\t%s", book[i].title);
printf("\t\t\t\t%s", book[i].author);
}

}










 

// CASE 4 : DELETE BOOK
void deletebook()
{
char btitle[10];
int i,j;
Book *temp;
printf("\n Enter Book Title You Want To Remove :   ");
gets(btitle);
for(i=0;i<count;i++)
{
if(stricmp(book[i].title,btitle)==0)
{
clrscr();

printf("\n\n\t\t\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB  Remove Books Details    \xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB");

gotoxy(20,4);
printf("\n\t\t\xDB\xDB\xDB\xDB\xDB Book Title    :     %s", book[i].title);

gotoxy(20,6);
printf("\n\t\t\xDB\xDB\xDB\xDB\xDB Book Author    :     %s", book[i].author);
for(j=i;j<count-1;j--)
	book = book+1;
count--;
return;
}
}
}




// CASE 3 SEARCH BOOK


void searchbook()
{
char btitle[10];
int i,j;
Book *temp;
printf("\n Enter Book Title You Want To be Search :   ");
gets(btitle);
for(i=0;i<count;i++)
{
if(stricmp(book[i].title,btitle)==0)
{
clrscr();

printf("\n\n\t\t\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB   Books Details    \xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB");

gotoxy(20,4);
printf("\n\t\t\xDB\xDB\xDB\xDB\xDB Book Title    :     %s", book[i].title);
gotoxy(20,6);
printf("\n\t\t\xDB\xDB\xDB\xDB\xDB Book Author    :     %s", book[i].author);
}
}
}





// MAIN FUNCTION

void main()
{
password();
getch();
}







// INITIALIZATION OF MAIN MENU

void mainmenu()
{
int choice;
printf("\n\n\n\n\t Enter Total No Of books You Want To add :   \t ");
scanf("%d", &size);
book = (Book*) malloc(sizeof(Book)*size);
do{
clrscr();
gotoxy(20,4);
printf("\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xB2 1 . Add Books");
gotoxy(20,6);
printf("\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xB2 2 . View Books");

gotoxy(20,8);
printf("\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xB2 3 . Search Books");


gotoxy(20,10);
printf("\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xB2 4 . Delete Books");

gotoxy(20,12);
printf("\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xDB\xB2 5 . Close Application ");

printf("\n\n\t\t\tChoose Your Choice :   ");
scanf("%d", &choice);
fflush(stdin);
switch(choice)
{
case 1:
addbook();
break;
case 2:
viewbooks();
break;
case 3:
searchbook();
break;
case 4:
deletebook();
break;
case 5:
clrscr();
gotoxy(15,3);
printf("Library Management System Mini Project In C Language");
gotoxy(15,4);
printf("Designed And Developed By Mabtoor Mabx ");
gotoxy(18,6);
printf("**********************************************");
gotoxy(20,17);
printf("__________Exiting in  2 Seconds_________");
delay(2000);
exit(0);
break;

case 6:
return;


}

getch();
}while(1);


}


















// INITIALIZATION OF WELCOME SCREEN AND  PASSWORD 




void password()
{
char str[50] = "Library Management Designed By Mabtoor Mabx";
char ch , pwd[10];
int i=0, j;
clrscr();
gotoxy(7,6);
for(j=0;j<8;j++)
{
delay(100);
printf("*");
}
for(j=0;j<strlen(str);j++)
{
delay(100);
printf("%c", str[j]);
}
for(j=0;j<8;j++)
{
delay(100);
printf("*");
}


gotoxy(15,7);
printf("Enter A Password\t");
while (ch!=13)
{
    ch=getch();

if (ch!=13&&ch!=8)
{
    printf("*");
    pwd[i]=ch;
    i++;
}

}

pwd[i] = '\0';
if (strcmp(pwd,mypassword)==0)
{
    gotoxy(15,8);
    printf("Congratulations! Password Match");
    gotoxy(16,10);
    printf("Press any Key To Continue");
    getch();
   mainmenu();
}

else
{
    gotoxy(13,8);
    printf("\a Warning!!  Your Password Is Incorrect");
    getch();
    password();
}


}
