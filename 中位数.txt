#include<iostream>
using namespace std;
int main()
{
	int a[15000];
	int N,m;
	while((cin>>N)&&N!=0)
	{
		for(int i=0;i<N;i++)
		{
			cin>>a[i];
		}
		for(int x=0;x<N;x++)
		{
			for(int y=0;y<N-1;y++)
			{
				if(a[y]>a[y+1])
				{	
					int t=a[y+1];
					a[y+1]=a[y];
					a[y]=t;
				}
			}
		}
		if(N%2==1)
			m=a[N/2];
		else
			m=(a[N/2]+a[N/2-1])/2;
	
		cout<<m<<endl;
	}
		return 0;
	}