#include<iostream>
#include<fstream>
using namespace std;

int ArraySum(int s)
{ int *a;
  int sum=0;
  a=new int[s];
  ifstream in("data.txt");
  if(!in)      //�򿪲��ɹ�
{ cout<<"�ļ���ʧ��\n";
	   return 0;}
  for(int i=0;in>>a[i],i<s;i++)
  sum+=a[i];
  in.close();
  return sum;
}

int main(void)
{  int s;
   int Sum;
   cout<<"����������ĳ���:";
   cin>>s;
   Sum=ArraySum(s);
   cout<<"��Ϊ:"<<Sum;
   return 0;
}