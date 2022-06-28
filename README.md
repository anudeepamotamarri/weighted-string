# weighted-string 
#include<stdio.h>
#include<string.h>
int main()
{
int i,s=0;
int a[26]={0};
char *str="abc";
a[0]=1;
for(i=1;i<26;i++){
    a[i]=(i+1)+a[i-1];// as it takes 'a' alphabet value as 1 and b=2+a...like wise it goes
}
for(i=0;i<strlen(str);i++){
    s+=a[str[i]-'a'];
}
printf("%d",s);
}
