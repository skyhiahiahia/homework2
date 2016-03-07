#include<iostream>
#include<fstream>
using namespace std;

int ArraySum(int s)
{ int *a;
  int sum=0;
  a=new int[s];
  ifstream in("data.txt");
  if(!in)      //打开不成功
{ cout<<"文件打开失败\n";
	   return 0;}
  for(int i=0;in>>a[i],i<s;i++)
  sum+=a[i];
  in.close();
  return sum;
}

int main(void)
{  int s;
   int Sum;
   cout<<"请输入数组的长度:";
   cin>>s;
   Sum=ArraySum(s);
   cout<<"和为:"<<Sum;
   return 0;
}