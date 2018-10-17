#include <stdio.h>
#include <conio.h>
void dummy (float a)
{
float *p=&a;
}
struct bill
{
char item[40];
float qty, price;
}b[10];

int main()
{
int i=0, c=1;
char ch;
float amt, total=0;
clrscr();
do
{
flushall();
printf("Enter Product Name  :");
gets(b[i].item);
printf("Enter Qty and Price :");
scanf("%f%f",&b[i].qty, &b[i].price);
flushall();
printf("Add More Items [y/n]");
scanf("%c",&ch);
if(ch=='y')
{i++;c++;};
}
while(ch=='y');
puts("\n=======================================================");
printf("\t\t SUPER MARKET\n");
puts("=======================================================");
printf("%-10s%15s%15s%15s\n", "Item", "Qty", "Price", "Amount");
puts("-------------------------------------------------------");
for(i=0;i<c;i++)
{
amt=b[i].qty*b[i].price;
total=total+amt;
printf("%-10s %15.2f\t%8.2f\t%7.2f\n",b[i].item, b[i].qty,b[i].price, amt);
}
puts("--------------------------------------------------------");
printf("Total Bill Amount :%2f\n",total);
printf("Happy Shopping");
getch();
}
