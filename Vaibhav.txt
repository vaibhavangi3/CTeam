#include<iostream>
#include<conio.h>
#include<ctype.h>
#include<string.h>
#include<stdio.h>
using namespace std;
#define Welcome cout<<"Welcome to the wonderful world of C++ Programmimg\n"
#define Vaibhav cout<<" by-> Vaibhav \n"
int length = 0;
int length1=0;
int length2=0;
struct date
{
 int dd,mm,yy;
};
struct player
{
int age,worldrank;
char name[20],nation[10],hand[10];
int weight;
date DOB;
};

struct date1
{
 int dd,mm,yy;
};
struct bolwer
{
int age,worldrank;
char name[20],nation[10],hand[10];
int weight;
date DOB;
};

struct date2
{
 int dd,mm,yy;
};
struct all
{
int age,worldrank;
char name[20],nation[10],hand[10];
int weight;
date DOB;
};

void Add(player p[]);
void Add(bolwer b[]);
void Add(all a[]);
void Search(player p[]);
void Search(bolwer b[]);
void Search(all a[]);
void Display(player p[]);
void Display(bolwer b[]);
void Display(all a[]);
void Edit(player p[]);
void Edit(bolwer b[]);
void Edit(all a[]);

 int main()
 {
  player P[10];
  bolwer B[10];
  all A[10];
  int choice;
  char contin;
  Welcome;
  Manohar;
  do
  {
  cout<<"\n_____Menu______";
  cout<<"\n1. BATSMEN";
  cout<<"\n2. BOWLER";
  cout<<"\n3. ALL ROUNDER";
  cout<<"\nEnter your choice-> ";
  std::cin>>choice;
  if(choice == 1)
  {

    char name1[4][20]={"Bruce","Man","Matt","Wayne"};
    char hand1[4][10]={"Left","Right","Left","Right"};
    char nation1[4][10]={"India","Russia","Brazil","Norway"};
    for(int i=0;i<4;i++)
    {
     strcpy(P[i].name, name1[i]);
     P[i].age = 20 + i;
     P[i].worldrank = 1 + i;
     P[i].weight = 50 + i;
     strcpy(P[i].hand, hand1[i]);
     strcpy(P[i].nation, nation1[i]);
     P[i].DOB.dd = 22 + i;
     P[i].DOB.mm = 6 + i;
     P[i].DOB.yy = 80 + i;
     length++;
    }

   do
   {
    cout<<"\n_____Menu______";
    cout<<"\n1. Add New Player";
    cout<<"\n2. Search Player";
    cout<<"\n3. Show all Players";
    cout<<"\n4. Edit Player Info";
    cout<<"\nEnter your choice: ";
    cin>>choice;
    if(choice == 1)
    {
     Add(P);
    }
     else if(choice == 2)
    {
     Search(P);
    }
     else if(choice == 3)
    {
     Display(P);
    }
    else if(choice == 4)
   {
    Edit(P);
   }
    else
   {
    cout<<"Wrong choice!! Please enter correct choice.";
    break;
   }
    cout<<"\n\nDo you want to continue?? If yes then press Y or y key\n";
    cin>>contin;
   }while(contin == 'y' || contin == 'Y');
 }
  else if(choice == 2)
  {
  char name3[10][20]={"Nehra","Abhi","Manu","Yashika"};
  char hand3[4][10]={"Left","Right","Left","Right"};
  char nation3[4][10]={"India","India","Brazil","West.I"};
  for(int i=0;i<4;i++)
  {
    strcpy(B[i].name, name3[i]);
    B[i].age = 20 + i;
    B[i].worldrank = 1 + i;
    B[i].weight = 50 + i;
    strcpy(B[i].hand, hand3[i]);
    strcpy(B[i].nation, nation3[i]);
    B[i].DOB.dd = 2 + i;
    B[i].DOB.mm = 1 + i;
    B[i].DOB.yy = 80 + i;
    length1++;
  }

  do
  {
  cout<<"\n_____Menu______";
  cout<<"\n1. Add New Player";
  cout<<"\n2. Search Player";
  cout<<"\n3. Show all Players";
  cout<<"\n4. Edit Player Info";
  cout<<"\nEnter your choice: ";
  cin>>choice;
  if(choice == 1)
  {
    Add(B);
  }
  else if(choice == 2)
  {
    Search(B);
  }
  else if(choice == 3)
  {
    Display(B);
  }
  else if(choice == 4)
  {
    Edit(B);
  }
  else
  {
    cout<<"Wrong choice!! Please enter correct choice.";
    break;
  }
  cout<<"\n\nDo you want to continue?? If yes then press Y or y key\n";
  cin>>contin;
  }while(contin == 'y' || contin == 'Y');

  }
  else if(choice == 3)
  {
    char name2[4][20]={"Sankara","Dhoni","Decok","A.B.D"};
  char hand2[4][10]={"Left","Right","Left","Right"};
  char nation2[4][10]={"W.indies","India","S.Africa","S.Africa"};
  for(int i=0;i<4;i++)
  {
    strcpy(A[i].name, name2[i]);
    A[i].age = 20 + i;
    A[i].worldrank = 1 + i;
    A[i].weight = 50 + i;
    strcpy(A[i].hand, hand2[i]);
    strcpy(A[i].nation, nation2[i]);
    A[i].DOB.dd = 22 + i;
    A[i].DOB.mm = 6 + i;
    A[i].DOB.yy = 80 + i;
    length2++;
  }

  do
  {
  cout<<"\n_____Menu______";
  cout<<"\n1. Add New Player";
  cout<<"\n2. Search Player";
  cout<<"\n3. Show all Players";
  cout<<"\n4. Edit Player Info";
  cout<<"\nEnter your choice: ";
  cin>>choice;
  if(choice == 1)
  {
    Add(A);
  }
  else if(choice == 2)
  {
    Search(A);
  }
  else if(choice == 3)
  {
    Display(A);
  }
  else if(choice == 4)
  {
    Edit(A);
  }
  else
  {
    cout<<"Wrong choice!! Please enter correct choice.";
    break;
  }
  cout<<"\n\nDo you want to continue?? If yes then press Y or y key\n";
  cin>>contin;
  }while(contin == 'y' || contin == 'Y');

  }
  else
  {
    cout<<"Wrong choice!! Please enter correct choice.";
  }
  cout<<"\n\nDo you want to continue?? If yes then press Y or y key\n";
  cin>>contin;
  }while(contin == 'y' || contin == 'Y');
 getch();
}

void Add(player p[])
{
 for(int i=length;i<length+1;i++)
 {
  cout<<"\nEnter the name of Player "<<i+1<<" ->";
  cin>>p[i].name;
  cout<<"\nEnter the age of Player "<<i+1<<" ->";
  cin>>p[i].age;
  cout<<"\nEnter the world rank of Player "<<i+1<<" ->";
  cin>>p[i].worldrank;
  cout<<"\nEnter the weight of Player "<<i+1<<" ->" ;
  cin>>p[i].weight;
  cout<<"\nEnter the nation of Player "<<i+1<<" ->";
  cin>>p[i].nation;
  cout<<"\nEnter the hand of Player "<<i+1<<" ->";
  cin>>p[i].hand;
  cout<<"\nEnter the DOB of Player "<<i+1<<" ->";
  cin>>p[i].DOB.dd>>p[i].DOB.mm>>p[i].DOB.yy;
 }
 length++;
}
void Add(bolwer b[])
{
 for(int i=length;i<length+1;i++)
 {
  cout<<"\nEnter the name of Player "<<i+1<<" ->";
  cin>>b[i].name;
  cout<<"\nEnter the age of Player "<<i+1<<" ->";
  cin>>b[i].age;
  cout<<"\nEnter the world rank of Player "<<i+1<<" ->";
  cin>>b[i].worldrank;
  cout<<"\nEnter the weight of Player "<<i+1<<" ->" ;
  cin>>b[i].weight;
  cout<<"\nEnter the nation of Player "<<i+1<<" ->";
  cin>>b[i].nation;
  cout<<"\nEnter the hand of Player "<<i+1<<" ->";
  cin>>b[i].hand;
  cout<<"\nEnter the DOB of Player "<<i+1<<" ->";
  cin>>b[i].DOB.dd>>b[i].DOB.mm>>b[i].DOB.yy;
 }
 length1++;
}
void Add(all a[])
{
 for(int i=length;i<length+1;i++)
 {
  cout<<"\nEnter the name of Player "<<i+1<<" ->";
  cin>>a[i].name;
  cout<<"\nEnter the age of Player "<<i+1<<" ->";
  cin>>a[i].age;
  cout<<"\nEnter the world rank of Player "<<i+1<<" ->";
  cin>>a[i].worldrank;
  cout<<"\nEnter the weight of Player "<<i+1<<" ->" ;
  cin>>a[i].weight;
  cout<<"\nEnter the nation of Player "<<i+1<<" ->";
  cin>>a[i].nation;
  cout<<"\nEnter the hand of Player "<<i+1<<" ->";
  cin>>a[i].hand;
  cout<<"\nEnter the DOB of Player "<<i+1<<" ->";
  cin>>a[i].DOB.dd>>a[i].DOB.mm>>a[i].DOB.yy;
 }
 length2++;
}


void Search(player p[])
{
 char pname[30];
 int flag=0;
 cout<<"\nEnter the player name u wish to search->";
 gets(pname);
 if(length == 0)
 {
   cout<<"No Record in Database!!";
 }
 else
 {
  for( int i=0;i<length;i++)
  {
   if(strcmp(p[i].name,pname)==0)
   {
    cout<<"\nRecord of player is:\n";
    cout<<"\n Name:"<<p[i].name;
    cout<<"\n Nation:"<<p[i].nation;
    cout<<"\n Hand:"<<p[i].hand;
    cout<<"\n Age:"<<p[i].age;
    cout<<"\n World Rank:"<<p[i].worldrank;
    cout<<"\n Weight:"<<p[i].weight;
    cout<<"\n DOB:"<<p[i].DOB.dd<<"/"<<p[i].DOB.mm<<"/"<<p[i].DOB.yy;
    flag=0;
    break;
   }
   else
   {
    flag=1;
   }
  }
  if(flag==1)
  {
   cout<<"No Record found for "<<pname;
  }
 }
}
void Search(bolwer b[])
{
 char pname[30];
 int flag=0;
 cout<<"\nEnter the player name u wish to search->";
 gets(pname);
 if(length1 == 0)
 {
   cout<<"No Record in Database!!";
 }
 else
 {
  for( int i=0;i<length1;i++)
  {
   if(strcmp(b[i].name,pname)==0)
   {
    cout<<"\nRecord of player is:\n";
    cout<<"\n Name:"<<b[i].name;
    cout<<"\n Nation:"<<b[i].nation;
    cout<<"\n Hand:"<<b[i].hand;
    cout<<"\n Age:"<<b[i].age;
    cout<<"\n World Rank:"<<b[i].worldrank;
    cout<<"\n Weight:"<<b[i].weight;
    cout<<"\n DOB:"<<b[i].DOB.dd<<"/"<<b[i].DOB.mm<<"/"<<b[i].DOB.yy;
    flag=0;
    break;
   }
   else
   {
    flag=1;
   }
  }
  if(flag==1)
  {
   cout<<"No Record found for "<<pname;
  }
 }
}
void Search(all a[])
{
 char pname[30];
 int flag=0;
 cout<<"\nEnter the player name u wish to search->";
 gets(pname);
 if(length2 == 0)
 {
   cout<<"No Record in Database!!";
 }
 else
 {
  for( int i=0;i<length2;i++)
  {
   if(strcmp(a[i].name,pname)==0)
   {
    cout<<"\nRecord of player is:\n";
    cout<<"\n Name:"<<a[i].name;
    cout<<"\n Nation:"<<a[i].nation;
    cout<<"\n Hand:"<<a[i].hand;
    cout<<"\n Age:"<<a[i].age;
    cout<<"\n World Rank:"<<a[i].worldrank;
    cout<<"\n Weight:"<<a[i].weight;
    cout<<"\n DOB:"<<a[i].DOB.dd<<"/"<<a[i].DOB.mm<<"/"<<a[i].DOB.yy;
    flag=0;
    break;
   }
   else
   {
    flag=1;
   }
  }
  if(flag==1)
  {
   cout<<"No Record found for "<<pname;
  }
 }
}



void Display(player p[])
{
 if(length == 0)
 {
    cout<<"No Record in Database!!";
 }
 else
 {
  cout<<"Name \t\t Age \t World rank \tWeight \tHand \t Nation \t DOB";
  for(int i=0;i<length;i++)
  {
   cout<<"\n"<<p[i].name<<"\t\t"<<p[i].age<<"\t";
   cout<<p[i].worldrank<<"\t\t"<<p[i].weight;
   cout<<"\t"<<p[i].hand<<"\t"<<p[i].nation;
   cout<<"\t    "<<p[i].DOB.dd<<"/"<<p[i].DOB.mm<<"/"<<p[i].DOB.yy;
  }
 }
}

void Display(bolwer b[])
{
 if(length1 == 0)
 {
    cout<<"No Record in Database!!";
 }
 else
 {
  cout<<"Name \t\t Age \t World rank \tWeight \tHand \t Nation \t DOB";
  for(int i=0;i<length1;i++)
  {
   cout<<"\n"<<b[i].name<<"\t\t"<<b[i].age<<"\t";
   cout<<b[i].worldrank<<"\t\t"<<b[i].weight;
   cout<<"\t"<<b[i].hand<<"\t"<<b[i].nation;
   cout<<"\t    "<<b[i].DOB.dd<<"/"<<b[i].DOB.mm<<"/"<<b[i].DOB.yy;
  }
 }
}

void Display(all a[])
{
 if(length2 == 0)
 {
    cout<<"No Record in Database!!";
 }
 else
 {
  cout<<"Name \t\t Age \t World rank \tWeight \tHand \t Nation \t DOB";
  for(int i=0;i<length2;i++)
  {
   cout<<"\n"<<a[i].name<<"\t\t"<<a[i].age<<"\t";
   cout<<a[i].worldrank<<"\t\t"<<a[i].weight;
   cout<<"\t"<<a[i].hand<<"\t"<<a[i].nation;
   cout<<"\t    "<<a[i].DOB.dd<<"/"<<a[i].DOB.mm<<"/"<<a[i].DOB.yy;
  }
 }
}


void Edit(player p[])
{
 char pname[30];
 int ch, flag=0;
 cout<<"Enter the name of player you wish to edit: ";
 gets(pname);
 for( int i=0;i<length;i++)
  {
   if(strcmp(p[i].name,pname)==0)
   {
    cout<<"\nWhat do you want to edit in player info : ";
    cout<<"\n1. Name ";
    cout<<"\n2. Nation ";
    cout<<"\n3. Hand ";
    cout<<"\n4. Age ";
    cout<<"\n5. World Rank ";
    cout<<"\n6. Weight ";
    cout<<"\n7. DOB ";
    cout<<"\n Please enter your choice : ";
    cin>>ch;
    switch(ch)
    {
     case 1 : cout<<"\nEnter new name: ";
		cin>>p[i].name;
		break;
     case 2 : cout<<"\nEnter new nation: ";
		cin>>p[i].nation;
		break;
     case 3 : cout<<"\nEnter new hand: ";
		cin>>p[i].hand;
		break;
     case 4 : cout<<"\nEnter new age: ";
		cin>>p[i].age;
		break;
     case 5 : cout<<"\nEnter new world rank: ";
		cin>>p[i].worldrank;
		break;
     case 6 : cout<<"\nEnter new weight: ";
		cin>>p[i].weight;
		break;
     case 7 : cout<<"\nEnter new date of birth: ";
		cin>>p[i].DOB.dd>>p[i].DOB.mm>>p[i].DOB.yy;
		break;
     default : cout<<"WRONG CHOICE!!";
		break;
    }

    flag=0;
    break;
   }
   else
   {
    flag=1;
   }
  }
  if(flag==1)
  {
   cout<<"No Record found for "<<pname;
  }
}
void Edit(bolwer b[])
{
 char pname[30];
 int ch, flag=0;
 cout<<"Enter the name of player you wish to edit: ";
 gets(pname);
 for( int i=0;i<length1;i++)
  {
   if(strcmp(b[i].name,pname)==0)
   {
    cout<<"\nWhat do you want to edit in player info : ";
    cout<<"\n1. Name ";
    cout<<"\n2. Nation ";
    cout<<"\n3. Hand ";
    cout<<"\n4. Age ";
    cout<<"\n5. World Rank ";
    cout<<"\n6. Weight ";
    cout<<"\n7. DOB ";
    cout<<"\n Please enter your choice : ";
    cin>>ch;
    switch(ch)
    {
     case 1 : cout<<"\nEnter new name: ";
		cin>>b[i].name;
		break;
     case 2 : cout<<"\nEnter new nation: ";
		cin>>b[i].nation;
		break;
     case 3 : cout<<"\nEnter new hand: ";
		cin>>b[i].hand;
		break;
     case 4 : cout<<"\nEnter new age: ";
		cin>>b[i].age;
		break;
     case 5 : cout<<"\nEnter new world rank: ";
		cin>>b[i].worldrank;
		break;
     case 6 : cout<<"\nEnter new weight: ";
		cin>>b[i].weight;
		break;
     case 7 : cout<<"\nEnter new date of birth: ";
		cin>>b[i].DOB.dd>>b[i].DOB.mm>>b[i].DOB.yy;
		break;
     default : cout<<"WRONG CHOICE!!";
		break;
    }

    flag=0;
    break;
   }
   else
   {
    flag=1;
   }
  }
  if(flag==1)
  {
   cout<<"No Record found for "<<pname;
  }
}
void Edit(all a[])
{
 char pname[30];
 int ch, flag=0;
 cout<<"Enter the name of player you wish to edit: ";
 gets(pname);
 for( int i=0;i<length2;i++)
  {
   if(strcmp(a[i].name,pname)==0)
   {
    cout<<"\nWhat do you want to edit in player info : ";
    cout<<"\n1. Name ";
    cout<<"\n2. Nation ";
    cout<<"\n3. Hand ";
    cout<<"\n4. Age ";
    cout<<"\n5. World Rank ";
    cout<<"\n6. Weight ";
    cout<<"\n7. DOB ";
    cout<<"\n Please enter your choice : ";
    cin>>ch;
    switch(ch)
    {
     case 1 : cout<<"\nEnter new name: ";
		cin>>a[i].name;
		break;
     case 2 : cout<<"\nEnter new nation: ";
		cin>>a[i].nation;
		break;
     case 3 : cout<<"\nEnter new hand: ";
		cin>>a[i].hand;
		break;
     case 4 : cout<<"\nEnter new age: ";
		cin>>a[i].age;
		break;
     case 5 : cout<<"\nEnter new world rank: ";
		cin>>a[i].worldrank;
		break;
     case 6 : cout<<"\nEnter new weight: ";
		cin>>a[i].weight;
		break;
     case 7 : cout<<"\nEnter new date of birth: ";
		cin>>a[i].DOB.dd>>a[i].DOB.mm>>a[i].DOB.yy;
		break;
     default : cout<<"WRONG CHOICE!!";
		break;
    }

    flag=0;
    break;
   }
   else
   {
    flag=1;
   }
  }
  if(flag==1)
  {
   cout<<"No Record found for "<<pname;
  }
}
