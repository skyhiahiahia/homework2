#include<iostream>

#include<fstream>

using namespace std;

int ArraySum(int s,int min,int max)

{ int *a;
 
  int sum=0;
  
  a=new int[s];
 
  ifstream in("data.txt");
 
  if(!in)      //打开不成功

{  cout<<"文件打开失败\n";

	   return 0;}
  
  for(int i=min;in>>a[i],i<=max;i++)
 
  sum+=a[i];
 
  in.close();

  return sum;

}

int main(void)

{  int s,min,max;
 
   int Sum;
  
   cout<<"请输入数组的长度:";
   
   cin>>s;
   cout<<"请输入计算范围的下限:";
 
   cin>>min;
 
   cout<<"请输入计算范围的上限:";
   
   cin>>max;
   
   Sum=ArraySum(s,min,max);
   
   cout<<"数组的和为:"<<Sum;
  
   return 0;

}
