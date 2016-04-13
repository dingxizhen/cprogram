#include<iostream>
#include<iomanip>
using namespace std;
int main()
{
	char a[500];
	int z=0,i=0,m=0;
	int b;
	cin.getline(a,500);
	while(a[m]!='\0')
	{
		if((a[m]>='A'&&a[m]<='Z')||(a[m]>='a'&&a[m]<='z'))
			z++;
		else
			if((a[m]==' '||a[m]=='.')&&z>i)
			{
				i=z;
				
				b=m;
			}
		if(a[m]==' ')
			z=0;

			m++;
	}
	for(int j=b-i;j<b;j++)
	{
		cout<<a[j];
	}
	
	return 0;
}