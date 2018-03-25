#include<iostream.h>
#include<fstream.h>
#include<stdio.h>
#include<ctype.h>
#include<conio.h>
#include<process.h>
#include<dos.h>
#include<string.h>
#include<stdlib.h>
#include<graphics.h>
#include<math.h>
void start()
{  int midx,midy;
int gdriver = DETECT,gmode;
	initgraph(&gdriver,&gmode,"C:\\Turboc3\\BGI");
	setcolor(11);  setbkcolor(8);
			 midx = getmaxx() / 2;
		 midy = getmaxy() / 2;
				  settextjustify(CENTER_TEXT, CENTER_TEXT);
		settextstyle(4, HORIZ_DIR,7);
		outtextxy(midx,midy-130,"BANKING SYSTEM");
		outtextxy(midx,midy-70,"APPLICATION");
		setcolor(WHITE);
		settextstyle(0, HORIZ_DIR,1);
		outtextxy(midx,midy+95,"DESIGNED AND PROGRAMMED BY:");
		outtextxy(midx,midy+130,"KUSH RAJ RIMAL");
		outtextxy(midx,midy+155,"ROLL NO: 690348");
		outtextxy(midx,midy+170,"KHWOPA ENGINEERING COLLEGE");
		delay(5000);
		cleardevice();
		closegraph();
		}

class admin
{private:
char name[30],password[30];
public:
void set();
int check();
void change();
};
void admin::set()
{char ch;int i;
 ss:
 gotoxy(25,7); textbackground(1);textcolor(3+BLINK);
cprintf("\n****Create a new user account****");
gotoxy(25,9);   textbackground(0);textcolor(3);
cprintf("\n\nEnter your user name: ");
gets(name);
abcd:
char paw[30]={0};
gotoxy(25,11);
cprintf("\n\nEnter your password: ");
	    int ij=0;
	do
		{
			ch=getch();
				if(isprint(ch))
				{
				paw[ij]=ch;
				printf("*");
					     }
		       else if(ch==8)
			{
			for(i=25;i>=11;i--)
			{delline();}
			  goto abcd;
			}
			ij++;
		}
		while(ch!=13);
		abc:
		char pa[30]={0};
		textcolor(3);
		 gotoxy(25,13);
		 cprintf("\n\nRe-enter your password: ");
int in=0;
	do
		{
			ch=getch();
				if(isprint(ch))
				{
				pa[in]=ch;
				printf("*");
					     }
		       else if(ch==8)
			{
			for(i=25;i>=13;i--)
			{delline();}
			  goto abc;
			}
			in++;
		}
		while(ch!=13);textcolor(3);
if(strcmp(paw,pa)!=0)
{ gotoxy(25,15);textcolor(GREEN);
cprintf("\n\nPasswords not matching");textcolor(3);
sound(1000);delay(700);nosound();
clrscr();
goto ss;}
strcpy(password,paw);
delay(200);
}

int admin::check()
{char nam[30]={0},ch;int i; static int l=3;
 fstream oo;
gotoxy(25,7); textbackground(1);textcolor(3+BLINK);
cprintf("\n****Please authenticate yourself****");
gotoxy(25,9);  textbackground(0);textcolor(3);
cprintf("\n");cout<<l;
cprintf(" attempts remaining");   l--;
gotoxy(25,11);
cprintf("\nEnter your user name: ");
textcolor(GREEN);
cin>>nam;
ab:
gotoxy(25,13);
char pas[30]={0};
textcolor(3);
cprintf("\nEnter your password: ");

textcolor(GREEN);
int inc=0;
	do
		{
			ch=getch();
				if(isprint(ch))
				{
				pas[inc]=ch;
				printf("*");
					     }
		       else if(ch==8)
			{
			for(i=25;i>=13;i--)
			{delline();}
			  goto ab;
			}
			inc++;
		}
		while(ch!=13);textcolor(3);
	      oo.open("adm.dat",ios::in);
oo.seekg(0,ios::beg);
while(oo.read((char*)this,sizeof(*this)))
{
 if((strcmp(nam,name)==0)&&(strcmp(pas,password)==0))
{l=3; return(1);
}
oo.close();
} return(0); }


void admin::change()
{int d,b,i;admin ad;
 clrscr();
fstream io;
io.open("adm.dat",ios::out);
io.close();
ad.set();
io.open("adm.dat",ios::out|ios::binary);
io.seekp(0,ios::beg);
io.write((char*)&ad,sizeof(ad));
io.close();
}

void fun()
{int d,b,i;admin admi;int j=1;
 clrscr();
fstream io;
io.open("adm.dat",ios::ate|ios::out|ios::binary);
io.seekp(0,ios::end);
b=io.tellp()/sizeof(admi);
io.close();
if(b==0)
{ io.open("adm.dat",ios::out|ios::binary);
  admi.set();
  io.write((char*)&admi,sizeof(admi));
  io.close();
  }
else
{cc:
clrscr();
i=admi.check();
if(i!=1)
{clrscr(); gotoxy(27,9);textcolor(RED);
		printf(" Match not found");textcolor(3);
		sound(1000);delay(700);nosound();
j++;
if(j==4)
{exit(0);}
else
{goto cc;}
}
}
  }

class bank
{public:
char name[50],address[50],g,type,status,contact[20],citi[20];
double balance, amt,acc,leak;float r,t,dd,mm,yy,time;
public:
double getdata(double c);
double loan(double k,double kk);
void showdata();
void show();
void deposit();
void withdraw();
void payloan();
void display();
void loandisplay();
float tim(int d,int m,int y,int dd,int mm,int yy);
double findloan(char n[50],char cit[20]);
double find(char n[50],char cit[20]);
double check(char cit[20]);
double count();
double loancount();
};

 void bank::loandisplay()
{fstream io; int i=2,j=2;
io.open("loanfile.dat",ios::in);
io.seekg(0,ios::end);
if(io.tellg()!=0)
{
io.seekg(0,ios::beg);
yy:
gotoxy(7,2);cprintf("\nAccount no");gotoxy(27,2);cprintf("\nName of Account holder");gotoxy(55,2);cprintf("\nAccount status");
while(io.read((char*)this,sizeof(*this)))
{ j=j+i;
gotoxy(7,j);textcolor(GREEN); cprintf(" ");cout<<acc;gotoxy(27,j);textcolor(GREEN);cprintf(" ");puts(name);gotoxy(55,j);cprintf("     ");cout<<status;
if(j==18)
{gotoxy(7,20);cprintf("\nPress any key to view more(Press E to exit)");
char ck=getch();
if(ck=='e'||ck=='E')
goto to;
else
{j=2;clrscr();goto yy;
}
}
}
	}
gotoxy(7,j+i);  getch();
to:
 }

void bank::display()
{fstream io; int i=2,j=2;
io.open("file.dat",ios::in);
io.seekg(0,ios::end);
if(io.tellg()!=0)
{
io.seekg(0,ios::beg);
yy:
gotoxy(7,2);cprintf("\nAccount no");gotoxy(27,2);cprintf("\nName of Account holder");gotoxy(55,2);cprintf("\nAccount status");
while(io.read((char*)this,sizeof(*this)))
{ j=j+i;
gotoxy(7,j);textcolor(GREEN); cprintf(" ");cout<<acc;gotoxy(27,j);textcolor(GREEN);cprintf(" ");puts(name);gotoxy(55,j);cprintf("     ");cout<<status;
if(j==18)
{gotoxy(7,20);cprintf("\nPress any key to view more(Press E to exit)");
char ck=getch();
if(ck=='e'||ck=='E')
goto to;
else
{j=2;clrscr();goto yy;
}
}
}
	}
gotoxy(7,j+i);  getch();
to:
 }

double bank::findloan(char n[],char cit[])
{fstream io;
io.open("loanfile.dat",ios::in);
io.seekg(0,ios::beg);
double kkk=0;
while(io.read((char*)this,sizeof(*this)))
{ kkk++;
 if(strcmp(n,name)==0&&strcmp(cit,citi)==0)
  break;
}
 io.seekg((sizeof(*this)),ios::end);
 io.read((char*)this,sizeof(*this));
 if(strcmp(n,name)!=0||strcmp(cit,citi)!=0)
 {gotoxy(27,17);textcolor(GREEN); cprintf("\nThis account doesn't exist");textcolor(3);sound(1000);delay(700);nosound();kkk=0;}
io.close();
return(kkk);
}

double bank::find(char n[],char cit[])
{fstream io;
io.open("file.dat",ios::in);
io.seekg(0,ios::beg);
double kkk=0;
while(io.read((char*)this,sizeof(*this)))
{ kkk++;
 if(strcmp(n,name)==0&&strcmp(cit,citi)==0)
  break;
}
 io.seekg((sizeof(*this)),ios::end);
 io.read((char*)this,sizeof(*this));
 if(strcmp(n,name)!=0||strcmp(cit,citi)!=0)
 {gotoxy(27,17);textcolor(GREEN); cprintf("\nThis account doesn't exist");textcolor(3);sound(1000);delay(700);nosound();kkk=0;}
io.close();
return(kkk);
}

double bank::check(char cit[])
{fstream io;
io.open("file.dat",ios::in);
io.seekg(0,ios::end);
double a=0;
if(io.tellg()==0)
{return(-1);}
io.seekg(0,ios::beg);
while(io.read((char*)this,sizeof(*this)))
  {a++;
 if(strcmp(cit,citi)==0)
   break;
  }
    io.seekg((sizeof(*this)),ios::end);
 io.read((char*)this,sizeof(*this));
 if(strcmp(cit,citi)==0)
 {clrscr(); gotoxy(10,9);
  cprintf("\nYou already have an account here and your account no is ");
  cout<<a;
    delay(2000);a=0;}
io.close();
double b=io.tellg()/sizeof(*this);
if(a==b&&a!=0)
 { clrscr(); gotoxy(10,9);
 cprintf("\nYou already have an account here and your account no is ");
 cout<<a;
  delay(2000);a=0;}
return(a);
}

double bank::loancount()
{   float t;
double amts;
float d,m,y;
struct date ddd;
getdate(&ddd);
d=ddd.da_day;
m=ddd.da_mon;
y=ddd.da_year;
fstream io;
io.open("loanfile.dat",ios::in);
io.seekg(0,ios::end);
double kkk=0;
if(io.tellg()==0)
{return(kkk);}
io.seekg(0,ios::beg);
while(io.read((char*)this,sizeof(*this)))
{  t=tim(d,m,y,dd,mm,yy);
   balance=amt*pow((1+(r/200)),2*t);
   kkk=kkk+balance;
  }
return(kkk);
}
double bank::count()
{ float d,m,y;
struct date ddd;
getdate(&ddd);
d=ddd.da_day;
m=ddd.da_mon;
y=ddd.da_year;
fstream io;
io.open("file.dat",ios::in);
io.seekg(0,ios::end);
double kkk=0;
if(io.tellg()==0)
{return(kkk);}
io.seekg(0,ios::beg);
while(io.read((char*)this,sizeof(*this)))
{ t=tim(d,m,y,dd,mm,yy);
   balance=amt*pow((1+(r/200)),2*t);
   amt=balance;
 kkk=kkk+amt+leak;
  }
return(kkk);
}

double bank::loan(double c,double kk)
{ char eg[30];
acc=c;
gotoxy(25,2);
textbackground(1);textcolor(3+BLINK);
cprintf("Create new loan account");
textbackground(0);textcolor(3);
gotoxy(20,3);
cprintf("\nYour assigned loan account no. is: ");cout<<acc;
gotoxy(20,5);textcolor(GREEN);cprintf("\nEnter your personal details");
textcolor(3);
a:
gotoxy(20,7);
cprintf("\nCitizenship no: ");
cin>>citi;
//double ab=_atold(citi);
//if(ab==0)
//{gotoxy(10,6);cprintf("\nCitizenship no. must start numeric"); delay(1500);
//for(int i=25;i>=4;i--)
//{ gotoxy(10,i);delline(); }
//goto a;}
gotoxy(20,9);
cprintf("\nName: ");
gets(name);
strcpy(name,strupr(name));
b:
gotoxy(20,11);
cprintf("\nGender(M/F): ");
g=getche();
if(g!='m'&g!='M'&g!='f'&g!='F')
{ gotoxy(20,13);
cprintf("\nPress either M or F");
delay(1500);
for(int i=25;i>=11;i--)
{ gotoxy(10,i);delline(); }
goto b;}
if(g=='m'||g=='M')
{g='M';}
if(g=='f'||g=='F')
{g='F';}
gotoxy(20,13);
cprintf("\nAddress: ");
gets(address);
strcpy(address,strupr(address));
c:
gotoxy(20,15);
cprintf("\nContact no: ");
gets(contact);
//double abc=_atold(contact);
//if(abc==0)
//{cprintf("\nContact no. must be numeric"); delay(1500);
//for(int i=25;i>=12;i--)
//{ gotoxy(10,i);delline(); }
//goto c;}
n:
gotoxy(20,17);
cprintf("\nEnter the loan amount to be issued ( > Nrs.10,000) : ");
char bal[20];
cin>>bal;
balance=_atold(bal);
if(balance<10000||balance>kk)
{ gotoxy(20,19);
cprintf("\nThis loan is not issuable");
 sound(1000);delay(700);nosound();
 for(int i=25;i>=17;i--)
{ gotoxy(10,i);delline(); }
 goto n;}
amt=balance;
r=15.5;type='L'; status='O';
o:
gotoxy(20,19);
cprintf("\nEnter the loan period(in years): ");
char lo[10];
cin>>lo;
time=_atold(lo);
if(time<0.5)
{ gotoxy(20,19);
cprintf("\nThis loan is not issuable");
 sound(1000);delay(700);nosound();
 for(int i=25;i>=18;i--)
{ gotoxy(10,i);delline(); }
 goto o;}
 amt=balance;//*pow(1+(r/200),2*time);
struct date ddd;
getdate(&ddd);
dd=ddd.da_day;
mm=ddd.da_mon;
yy=ddd.da_year;
leak=0;
return balance;
}

double bank::getdata(double c)
{ char eg[20];
acc=c;
gotoxy(25,2);
textbackground(1);textcolor(3+BLINK);
cprintf("Create new account");
textbackground(0);textcolor(3);
gotoxy(20,3);
cprintf("\nYour assigned account no. is: ");cout<<acc;
d:
gotoxy(20,5);textcolor(GREEN);
cprintf("\nEnter your personal details");textcolor(3);
gotoxy(20,7);
cprintf("\nCitizenship no: ");
gets(citi);
//double ab=_atold(cit);
//if(ab==0)
//{gotoxy(10,8);cprintf("\nCitizenship no. must be numeric"); delay(1500);
// for(int i=25;i>=6;i--)
// {
// gotoxy(10,i);delline();}
// goto d;}
// strcpy(citi,cit);
strcpy(eg,citi);
double re=check(eg);
if(re!=0)
{
strcpy(citi,eg);
acc=c;
gotoxy(20,9);
cprintf("\nName: ");
gets(name);
strcpy(name,strupr(name));
e:
gotoxy(20,11);
cprintf("\nGender(M/F): ");
g=getche();
if(g!='m'&g!='M'&g!='f'&g!='F')
{ gotoxy(20,13);
cprintf("\nPress either M or F");
delay(1500);
for(int i=25;i>10;i--)
{ gotoxy(10,i);delline(); }
goto e;}
if(g=='m'||g=='M')
{g='M';}
if(g=='f'||g=='F')
{g='F';}
gotoxy(20,13);
cprintf("\nAddress: ");
gets(address);
strcpy(address,strupr(address));
f:
gotoxy(20,15);
cprintf("\nContact no: ");
cin>>contact;
//double abc=_atold(con);
//if(abc==0)
//{gotoxy(10,16);cprintf("\nContact no. can't start with such character");delay(1500);
//for(int i=25;i>=14;i--)
//{ gotoxy(10,i);delline(); }
//goto f;}

there:
gotoxy(20,17);
cprintf("\nOpening Balance (>Nrs 500): ");
char bal[20];
cin>>bal;
balance=_atold(bal);
 if(balance<500)
{ for(int i=25;i>=16;i--)
{ gotoxy(10,i);delline(); }
goto there; }
amt=balance;
g:
gotoxy(20,19);
cprintf("\nPlease choose an account type");
gotoxy(20,21);
cprintf("\nSavings->(S)");cout<<" Rate->6.5%";
gotoxy(50,21);
cprintf("\nCurrent->(C)");cout<<" Rate->3.5%";
gotoxy(20,24);
type=getche();
if(type!='S'&type!='s'&type!='C'&type!='c')
{ gotoxy(20,24);
cprintf("Invalid data entry"); textcolor(WHITE);
sound(1000);delay(700);nosound();
for(int i=25;i>=18;i--)
{ gotoxy(10,i);delline(); }
goto g; }
if(type=='S'||type=='s')
{r=6.5;type='S';}
if(type=='C'||type=='c')
{r=3.5;type='C';}
status='O';
struct date ddd;
getdate(&ddd);
dd=ddd.da_day;
mm=ddd.da_mon;
yy=ddd.da_year;
leak=0;
t=0;
}
return(re);
  }

void bank::show()
{float d,m,y;
struct date ddd;
getdate(&ddd);
d=ddd.da_day;
m=ddd.da_mon;
y=ddd.da_year;
float t=tim(d,m,y,dd,mm,yy);
balance=balance*pow((1+(r/200)),2*t);
//int gh;
//if(t>0.5)
//{gh=t/0.5; gh=gh/2;
//amt=amt*pow((1+(r/100)),2*t);}
dd=d; mm=m; yy=y;
clrscr();
gotoxy(29,2); textbackground(1);textcolor(3+BLINK);
cprintf("LOAN ACCOUNT DETAILS");
textbackground(0);textcolor(3);
gotoxy(15,6);
cprintf("\nName:  ");puts(name);
gotoxy(15,4);
cprintf("\nAccount no:  ");cout<<acc;
gotoxy(45,4);
cprintf("\nCitizenship no:  ");puts(citi);
gotoxy(45,6);
cprintf("\nGender:  ");cout<<g;
gotoxy(45,8);
cprintf("\nAddress:  ");puts(address);
gotoxy(15,8);
cprintf("\nContact:  ");puts(contact);
gotoxy(15,14);
cprintf("\nAmount Payable(till date):NRs. ");cout<<balance;
gotoxy(45,10);
cprintf("\nAccount type:  ");cout<<type;
gotoxy(15,10);
cprintf("\nInterest rate:  "); cout<<r;
cout<<" % p.a.";
gotoxy(15,12);
cprintf("\nAccount status:  "); cout<<status;
gotoxy(15,16);
cprintf("\nLoan Amount initially issued Nrs. ");cout<<amt;
getch();
}

void bank::showdata()
{ float d,m,y;char de;
gotoxy(45,18);
//cout<<dd<<mm<<yy;getch();
struct date ddd;
getdate(&ddd);
d=ddd.da_day;
m=ddd.da_mon;
y=ddd.da_year;
float t=tim(d,m,y,dd,mm,yy);
int gh;
balance=amt*pow((1+(r/200)),2*t);
//if(t>0.5)
//{gh=t/0.5; gh=gh/2;
amt=amt*pow((1+(r/200)),2*t);//}
dd=d; mm=m; yy=y;
clrscr();
gotoxy(33,2); textbackground(1);textcolor(3+BLINK);
cprintf("ACCOUNT DETAILS");
textbackground(0);textcolor(3);
gotoxy(15,8);
cprintf("\nName:  ");puts(name);
gotoxy(15,6);
cprintf("\nAccount no:  ");cout<<acc;
gotoxy(45,6);
cprintf("\nCitizenship no:  ");puts(citi);
gotoxy(45,8);
cprintf("\nGender:  ");cout<<g;
gotoxy(45,10);
cprintf("\nAddress:  ");puts(address);
gotoxy(15,10);
cprintf("\nContact:  ");puts(contact);
gotoxy(15,12);
cprintf("\nBalance:Nrs ");cout<<balance;
gotoxy(45,12);
cprintf("\nAccount type:  ");cout<<type;
gotoxy(15,14);
cprintf("\nInterest rate:  "); cout<<r;
cout<<" % p.a.";
gotoxy(45,14);
cprintf("\nAccount status:  "); cout<<status;
}

void bank::payloan()
{ if(status!='C')
{
float t,tt;
double amts;
float d,m,y;
struct date ddd;
getdate(&ddd);
d=ddd.da_day;
m=ddd.da_mon;
y=ddd.da_year;
int gh;
t=tim(d,m,y,dd,mm,yy);
//amt=balance*pow((1+r/200),2*(time-t));
balance=balance*pow((1+(r/200)),2*t);
//if(t>0.5)
//{gh=t/0.5; gh=gh/2;
//amt=amt*pow((1+(r/200)),2*gh);//}
dd=d; mm=m; yy=y;
gotoxy(22,9);
cprintf("\nEnter amount to pay at this installment\n");
gotoxy(22,11);
char bal[20];
cin>>bal;
amts=_atold(bal);
balance=balance-amts;
//amt=amt-amts;
if(balance<1)
{status='C';
balance=0;
amt=0;}
getch();
 }
 else if(status=='C')
 {gotoxy(25,10);
 cprintf("\nThis loan has already been paid");
 getch();
 }
 }
void bank::deposit()
{char t,tt;
if(status=='C')
{showdata();
cout<<"\n\n\t\tDo you want to re-open this account(Y/N)";
t=getche();
if(t=='Y'||t=='y')
status='O';
clrscr();
gotoxy(20,10);
cprintf("Do you want to change the account type(Y/N)");
tt=getch();
if(tt=='y'||tt=='Y')
{if(type=='C')
{type='S';
r=6.5;
}
else
{type='C';
r=3.5;
}
}
}
 if(status!='C')
{
float t;
double amts;
float d,m,y;
struct date ddd;
getdate(&ddd);
d=ddd.da_day;
m=ddd.da_mon;
y=ddd.da_year;
t=tim(d,m,y,dd,mm,yy);
balance=amt*pow((1+(r/200)),2*t);
//int gh;
//if(t>0.5)
//{gh=t/0.5; gh=gh/2;
amt=amt*pow((1+(r/200)),2*t);//}
//amt=balance*pow((1+(r/100)),2*t);
dd=d; mm=m; yy=y;
showdata();cout<<"\n\n\t\tPress any key to proceed";getche();clrscr();
gotoxy(27,9);
cprintf("\nEnter amount to deposit(Nrs): ");
char bal[20];
cin>>bal;
amts=_atold(bal);
balance=balance+amts;
amt=amt+amts;
  }
  }

void bank::withdraw()
{ if(status!='C')
{
float t;
double amts;
float d,m,y;
struct date ddd;
getdate(&ddd);
d=ddd.da_day;
m=ddd.da_mon;
y=ddd.da_year;
t=tim(d,m,y,dd,mm,yy);
balance=amt*pow((1+(r/200)),2*t);
//int gh;
//if(t>0.5)
//{gh=t/0.5; gh=gh/2;
amt=amt*pow((1+(r/200)),2*t);//}
//amt=balance*pow((1+(r/100)),2*t);
dd=d; mm=m; yy=y;
double bv=balance-500;
showdata();cout<<"\n\n\t\tPress any key to proceed";getche();clrscr();
gotoxy(10,9);
cprintf("\nEnter amount to withdraw (Max value withdrawable is Nrs ");cout<<bv<<")";
gotoxy(35,12);
char bal[20];
cin>>bal;
amts=_atold(bal);
if(amts>bv)
{clrscr(); gotoxy(15,11);
cprintf("\nTransaction not possible");
sound(1000);delay(700);nosound();
}
else
{
balance=balance-amts;
amt=amt-amts;
}
char tt;
if(balance<=501)
{gotoxy(15,13);
cprintf("\nDo you want to close the account as well?(Y/N)");
gotoxy(15,15);
tt=getch();
if(tt=='Y'||tt=='y')
{status='C';
leak=leak+balance;
balance=0; amt=0;}  }
 } }

float bank::tim(int d,int m,int y,int dd,int mm,int yy)
{float t;
if((d-dd)<0.0)
{d=d+30.0;m=m-1.0;}
if((m-mm)<0.0)
{m=m+12.0;y=y-1.0;}
t=((y-yy)/1.0)+((m-mm)/12.0)+((d-dd)/365.0);
return(t);
}
void funs()
{bank ba,ban;
int a,b,c,d,n;
//ba.autopsy();
xxx:
clrscr();
struct date ddd;
getdate(&ddd);
float dddd=ddd.da_day;
float mmmm=ddd.da_mon;
float yyyy=ddd.da_year;
gotoxy(33,2); textbackground(1);textcolor(3+BLINK);
cprintf("Banking System");
textbackground(0);textcolor(3);
gotoxy(63,3);
cout<<"DATE:"<<dddd<<"/"<<mmmm<<"/"<<yyyy;
gotoxy(12,5);
cprintf("\n1.Create new account");
gotoxy(40,5);
cprintf("\n2.See Account details");
gotoxy(12,7);
cprintf("\n3.Perform a transaction");
gotoxy(40,7);
cprintf("\n4.See Account-holders list");
gotoxy(12,9);
cprintf("\n5.Loan Issual");
gotoxy(40,9);
cprintf("\n6.Loan status");
gotoxy(12,11);
cprintf("\n7.Pay loan");
gotoxy(40,11);
cprintf("\n8.Change username and password");
gotoxy(12,13);
cprintf("\n9.Log out");
gotoxy(40,13);
cprintf("\n10.Bank's financial state");
gotoxy(12,15);
textcolor(WHITE);
cprintf("\nPress 0 to Exit\n"); textcolor(3);
gotoxy(12,17); char *cha;
cin>>cha;
a=atoi(cha);
clrscr();
switch(a)
{	case 1:
{fstream io;
io.open("file.dat",ios::ate|ios::in|ios::out|ios::binary);
io.seekp(0,ios::end);
b=io.tellp()/sizeof(ba);
c=b+1;
hey:
double re=ba.getdata(c);
if(re!=0)
{
ba.showdata();
gotoxy(12,17);
cprintf("\nAre all the information correct?");
gotoxy(12,19);
cprintf("\nAre you sure that you want to create this account(Y/N)");
char ii=getche();
if(ii=='Y'||ii=='y')
{
io.write((char*)&ba,sizeof(ba));
io.close();
    gotoxy(12,21);
    textcolor(GREEN);
cprintf("\nRecord added successfully");
textcolor(3);
delay(2000);
}
else {gotoxy(12,21);
textcolor(RED);
cprintf("\nRecord not added");
textcolor(3);
delay(2000);} }
goto xxx;
}
case 2:
 {
   char nam[50],cit[20];int i;
fstream io;
io.open("file.dat",ios::ate|ios::in|ios::binary);
io.seekg(0,ios::end);
if(io.tellg()<1)
{
gotoxy(27,9);textcolor(RED);cprintf("\nNo account exists.");
sound(1000);delay(700);nosound();
goto xxx;
}
b=io.tellg()/sizeof(ba);
ag:
clrscr();
gotoxy(27,4);
textbackground(1);textcolor(3+BLINK);
cprintf("Search account"); textbackground(0);textcolor(3);
gotoxy(27,9);
cprintf("1.Search by account no.");gotoxy(27,11);cprintf("\n2.Search by name\n");gotoxy(27,14);cprintf("\n3.Main menu\n");
gotoxy(27,16); char *cha;
cin>>cha;
i=atoi(cha);
switch(i)
{case 2:
{ clrscr();
gotoxy(27,9);
cprintf("\nEnter the name");
gotoxy(27,11);
gets(nam);
strcpy(nam,strupr(nam));
k:
gotoxy(27,13);
cprintf("\nEnter your citizenship no.");
gotoxy(27,15);
gets(cit);
//double abc;
//abc=_atold(cit);
/*if(abc==0)
{cprintf("\nCitizenship no. must be numeric");
 delay(3000);
 for(int i=25;i>=13;i--)
{ gotoxy(10,i);delline(); }
goto k;
 }*/
n=ba.find(nam,cit);
if(n==0)
{goto xxx;}
gotoxy(27,17);
cprintf("\nYour account no. is "); cout<<n;
getch();
break;
}
case 1:
{
clrscr();gotoxy(27,9); cprintf("\nEnter the account no.");
cin>>n;
 if(n>b||n<1)
{clrscr();gotoxy(27,9);cprintf("\nThis account doesn't exist.");sound(1500);delay(1500);nosound();goto xxx;}
break; }
case 3:
{goto xxx;}
default:
 {gotoxy(27,15);
 cprintf("\nEnter a valid value");
  sound(1500);delay(2000);nosound();
 goto ag; }
 }
c=(n-1)*sizeof(ba);
io.seekg(c);
io.read((char*)&ba,sizeof(ba));
ba.showdata();
io.close();
getch();goto xxx;
 }
case 3:

{ fstream io;
io.open("file.dat",ios::ate|ios::in|ios::out|ios::binary);
io.seekp(0,ios::end);
if(io.tellp()<1)
{clrscr();gotoxy(27,9);
cprintf("\nNo account exists"); io.close();
    sound(1500);delay(2000);nosound();
goto xxx;}
gotoxy(29,4);textbackground(1);textcolor(3+BLINK); cprintf("Perform transaction");
textbackground(0);textcolor(3);
gotoxy(20,11); cprintf("1.Deposit");
gotoxy(45,11);cprintf("2.Withdraw");
gotoxy(20,13);char *cha; int a;
cin>>cha;
a=atoi(cha);
switch(a)
{case 1:
{fstream io;
io.open("file.dat",ios::ate|ios::in|ios::out|ios::binary);
io.seekp(0,ios::end);
if(io.tellp()<1)
{clrscr();gotoxy(27,9);
cprintf("\nNo account exists");
    sound(1000);delay(700);nosound();
goto xxx;}
b=io.tellp()/sizeof(ba);
clrscr();gotoxy(27,9);
cprintf("\nEnter your account no: ");
cin>>n;
if(n>b||n<1)
{  clrscr();
gotoxy(27,9);
cprintf("\nThis account doesn't exist.");
 sound(1000);delay(700);nosound();
goto xxx;}
c=(n-1)*sizeof(ba);
io.seekp(c);
io.seekg(c);
io.read((char*)&ba,sizeof(ba));
ban=ba;
ban.deposit();
ban.showdata();
io.close();
 fstream oo;
oo.open("file.dat",ios::ate|ios::out|ios::binary);
oo.seekp(c);
oo.write((char*)&ban,sizeof(ban));
oo.close();
getch();
goto xxx;
}
case 2:
{
fstream io;
io.open("file.dat",ios::ate|ios::in|ios::out|ios::binary);
io.seekp(0,ios::end);
if(io.tellp()<1)
{   clrscr();gotoxy(27,9);
cprintf("\nNo account exists");
 sound(1000);delay(700);nosound();
 goto xxx;}
b=io.tellp()/sizeof(ba);
clrscr();
gotoxy(27,9);
cprintf("\nEnter your account no: ");
char bal[20];
cin>>bal;
n=_atold(bal);
if(n>b||n<1)
{clrscr();gotoxy(27,9);
cprintf("\nThis account doesn't exist.");
  sound(1000);delay(700);nosound();
goto xxx;}
c=(n-1)*sizeof(ba);
io.seekp(c);
io.seekg(c);
io.read((char*)&ba,sizeof(ba));
ban=ba;
ban.withdraw();
ban.showdata();
io.close();
 fstream oo;
oo.open("file.dat",ios::ate|ios::out|ios::binary);
oo.seekp(c);
oo.write((char*)&ban,sizeof(ban));
oo.close();
getch();
goto xxx;
}
default:
{goto xxx;}
}
}
case 4:
{fstream io;
io.open("file.dat",ios::ate|ios::in|ios::out|ios::binary);
io.seekp(0,ios::end);
if(io.tellp()<1)
{clrscr();gotoxy(27,9);
cprintf("\nNo account exists"); io.close();
    sound(1500);delay(2000);nosound();
goto xxx;}
ba.display();
goto xxx;}

case 5:
{ double kk,kkk;char ch;
fstream io;
io.open("loanfile.dat",ios::ate|ios::in|ios::out|ios::binary);
io.seekp(0,ios::end);
b=io.tellp()/sizeof(ba);
kk=ba.count(); kkk=ba.loancount();
kk=0.95*kk;
kk=kk-kkk;
if(kk<10000)
{gotoxy(23,9);
cprintf("\nBank cannot issue loan currently"); delay(1500);
goto xxx;}
gotoxy(12,2);
cprintf("\nThe maximum loan issuable is Nrs. ");cout<<kk;
gotoxy(12,4);
cprintf("\nDo you want to proceed? (Y/N) ");
ch=getche();
if(ch!='y'&&ch!='Y')
{goto xxx;}
clrscr();
c=b+1;
ba.loan(c,kk);
ba.show();
gotoxy(15,17);
cprintf("\nAre all the information correct?");
gotoxy(15,19);
cprintf("\nAre you sure that you want the loan to be issued?(Y/N)");
char ii=getche();
if(ii=='Y'||ii=='y')
{
io.write((char*)&ba,sizeof(ba));
io.close();
    gotoxy(15,21);
    textcolor(GREEN);
cprintf("\nRecord added successfully");
textcolor(3);
delay(2000);
}
else {gotoxy(15,21);
textcolor(RED);
cprintf("\nRecord not added");
textcolor(3);
delay(2000);}
goto xxx;
}

case 8:{admin admi;
admi.change();goto xxx;
}

case 9:
{break;}

case 10:
{
double sp,ps,psa;
sp=ba.count();ps=ba.loancount();psa=sp;
gotoxy(20,4);
textbackground(1);textcolor(3+BLINK);
cprintf("Bank's Financial State");
textbackground(0);textcolor(3);
gotoxy(20,8); cprintf("Bank's total capital:Nrs ");cout<<sp;
gotoxy(20,10); cprintf("Total loan issued:Nrs ");cout<<ps;
sp=sp-ps;
gotoxy(20,12); cprintf("Liquid available:Nrs ");cout<<sp;
sp=0.95*psa; sp=sp-ps;
gotoxy(20,14); cprintf("Loan issuable amount:Nrs ");cout<<sp;
getch();
goto xxx;
}
case 0:
{ gotoxy(35,9);
exit(0);}

case 6:
{ int i;char nam[50],cit[20];
fstream io;
io.open("loanfile.dat",ios::ate|ios::in|ios::out|ios::binary);
io.seekg(0,ios::end);
if(io.tellg()<1)
{clrscr();gotoxy(27,9); cprintf("\nNo loan has been issued.");
  sound(1000);delay(700);nosound();
goto xxx;}
b=io.tellg()/sizeof(ba);
agl:
clrscr();
gotoxy(27,3);
textbackground(1);textcolor(3+BLINK);
cprintf("Search loan account");
textbackground(0);textcolor(3);
gotoxy(27,9);
cprintf("1.Search by account no.");gotoxy(27,11);cprintf("\n2.Search by name\n");gotoxy(27,17);cprintf("\n4.Main menu\n");gotoxy(27,14);cprintf("\n3.See all loan accounts\n");
gotoxy(27,19);  char *cha;
cin>>cha;
i=atoi(cha);
switch(i)
{case 2:
{ clrscr();
gotoxy(27,9);
cprintf("\nEnter the name");
gotoxy(27,11);
gets(nam);
strcpy(nam,strupr(nam));
kk:
gotoxy(27,13);
cprintf("\nEnter the citizenship no.");
/*gotoxy(27,15);
double abc;
abc=_atold(cit);
if(abc==0)
{cprintf("\nCitizenship no. must be numeric");
 delay(700);
 for(int i=25;i>=13;i--)
{ gotoxy(10,i);delline(); }
goto kk;
 } */
gets(cit);
n=ba.findloan(nam,cit);
if(n==0)
{goto xxx;}
gotoxy(27,17);
cprintf("\nYour account no. is "); cout<<n;
getch();
break;
}
case 1:
{
clrscr();gotoxy(27,9); cprintf("\nEnter the account no.");
char bal[20];
cin>>bal;
n=_atold(bal);
 if(n>b||n<1)
{clrscr();gotoxy(27,9);cprintf("\nThis account doesn't exist.");
 sound(1000);delay(700);nosound();
goto xxx;}
break; }
case 4:
{goto xxx;}
default:
 {gotoxy(27,15);
 cprintf("\nEnter a valid value");
  sound(1000);delay(700);nosound();
 goto agl; }
 case 3:
 {clrscr(); ba.loandisplay(); goto xxx;}
 }
c=(n-1)*sizeof(ba);
io.seekg(c);
io.read((char*)&ba,sizeof(ba));
ba.show();
io.close();
goto xxx;
 }
  case 7:
 {
fstream io;
io.open("loanfile.dat",ios::ate|ios::in|ios::out|ios::binary);
io.seekp(0,ios::end);
if(io.tellp()<1)
{clrscr();gotoxy(27,9);cprintf("\nNo loan has been issued");
 sound(1000);delay(700);nosound();
 goto xxx;}
b=io.tellp()/sizeof(ba);
gotoxy(27,9);
cprintf("\nEnter your loan account no:");
char bal[20];
cin>>bal;
n=_atold(bal);
if(n>b||n<1)
{clrscr();gotoxy(27,9);cprintf("\nThis loan account doesn't exist");
 sound(1000);delay(700);nosound();
 goto xxx;
 }
c=(n-1)*sizeof(ba);
io.seekp(c);
io.seekg(c);
io.read((char*)&ba,sizeof(ba));
ban=ba;
ban.show();
gotoxy(27,18);
cprintf("\n\nPress any key to proceed "); getche();clrscr();
ban.payloan();
ban.show();
io.close();
 fstream oo;
oo.open("loanfile.dat",ios::ate|ios::out|ios::binary);
oo.seekp(c);
oo.write((char*)&ban,sizeof(ban));
oo.close();

goto xxx;
}
default:
{clrscr();
gotoxy(27,9);
cprintf("\nPlease make a valid choice");
 sound(1000);
  delay(700);
  nosound();
goto xxx;}
}
}
void main()
{char ch;int a;
//start();
clrscr();
 gotoxy(25,10);textcolor(3);
cprintf("\n\t\t\tPress any key to continue.\t\t\t");
getche();
while(1)
{
fun();
funs();
}
}