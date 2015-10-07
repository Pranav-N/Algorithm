# Algorithm
Pub-Sub architecture

#include<iostrem.h>
class pub
{
  public:
  char publish()
  {
   char a[50];
   cout<<"\nEnter the Message that you want to publish:";
   cin>>a;
   return a;
  }
};

class sub
{
 public:
 void subscibe(char a[])
 {
  cout<<"\nMessage:\n"<<a;
 } 
};

main()
{
 int x,y;
 cout<<"\nEnter the total number of subscribers(<10):";
 cin>>y;
 cout<<"\nEnter the total number of publishers(<10):";
 cin>>x;
 pub obj[10];
 sub obj1[10];
 int i,j;
 char p[50];
 for(i=0;i<=x;i++)
 {
  p=obj[i].publish();
  for(j=0;j<=y;j++)
  {
   obj1[j].subscribe(p);
  }
 }
} 
   
 
