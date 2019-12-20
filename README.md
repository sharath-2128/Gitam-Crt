# Gitam-Crt

#include<stdio.h>
int isPalindrome(int x)
{
	int rev=0,buffer=x;
	while(x!=0){
		rev = rev*10 + (x%10);
		x /= 10;
	}
	if(buffer==rev){
		return 1;
	}
	else{
		return 0;
	}
}
int main()
{
	int i,x1,x2,n,res,cnt=0;
	scanf("%d%d",&x1,&x2);
	scanf("%d",&n);
	for(i=x1;i<=x2;i++)
	{
		res = isPalindrome(i);
		if(res==1)
		{
			cnt++;
			if(cnt==n){
				printf("%d",i);
				break;
			}
		}
	}
	return 0;
}
