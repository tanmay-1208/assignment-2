# assignment-2
#include<stdio.h>

int main(void)
{
int deposit,withdraw,kbalance;
int option;
int decash,wicash;
int balance;
int wibal;

printf("Welcome to bank\n");
printf("Enter your current Balance\n");
scanf_s("%d", &balance);
printf("Press 1 to deposit cash\n");
printf("Press 2 to Withdraw Cash\n");
printf("Press 3 to Know Your Balance\n");
printf("Press 4 to Quit\n");
while((option=getchar())!=4){
scanf("%d", &option);
switch(option)
   {
    case 1:
        printf("Enter the amount you want to deposit\n");
        scanf_s("%d", &decash);
        printf("Thank You\n");
        printf("%d have been deposited in your account\n", decash);
        balance=balance+decash;
        printf("Your balance is Rs.%d\n",balance);
        break;
    case 2:
        printf("Enter the amount you want to withdraw\n");
        scanf_s("%d", &wicash);
        wibal=balance-wicash;
        if(wicash<balance){
            printf("Thank You\n");
            printf("%d have been withdrawed from your account\n", wicash);
            printf("Your balance is Rs.%d\n", wibal);}
        else{
            printf("Sorry. You have insufficient balance to conduct         this transaction!\n");}
        balance=balance-wicash;
        break;
    case 3:
        printf("Your balance is Rs.%d\n", balance);
        break;
    case 4:
        exit();
        break;
    default:
        printf("Invalid Input\n");
        break;
    }
}
_getch();
}
