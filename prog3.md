#include<iostream>
#include<fstream>
using namespace std;

int ArraySum(int s,int min,int max)
{ int *a;
  int sum=0;
  a=new int[s];
  ifstream in("data.txt");
  if(!in)      //�򿪲��ɹ�
{  cout<<"�ļ���ʧ��\n";
	   return 0;}
  for(int i=min;in>>a[i],i<max;i++)
  sum+=a[i];
  in.close();
  return sum;
}

int main(void)
{  int s,min,max;
   int Sum;
   cout<<"����������ĳ���:";
   cin>>s;
   cout<<"�뷶Χ������:";
   cin>>min;
   cout<<"�����뷶Χ������:";
   cin>>max;
   Sum=ArraySum(s,min,max);
   cout<<"����ĺ�Ϊ:"<<Sum;
   return 0;
}