# 1228
#include<stdio.h>
int main()
{ int a;
  int b;
  int x;                   //a*b x*y
  int y;
  scanf("%d%d%d%d",&a,&b,&x,&y);
  
  
  int i;
  int j;
  int c;
  int loop;
 
 
  int first[a][b];
  for(i=0;i<a;i++)
  for(j=0;j<b;j++) 
  scanf("%d",&first[i][j]);
   
     int second[x][y];
     for(i=0;i<x;i++)
     for(j=0;j<y;j++) 
    scanf("%d",&second[i][j]);
	
	if(b!=x)
  printf("error\n");
  else{ 
	int result[a][y];
	for(i=0;i<a;i++)
    for(j=0;j<y;j++)                           // first[i][0]*second[0][j]+...+first[i][b-1]*second[x-1][j]
     { int temp=0;                               //b==x;
         for(c=0;c<b;c++)
        temp=temp+first[i][c]*second[c][j];
		result[i][j]=temp;                          
	 }
	 
	 for(i=0;i<a;i++)
    {
	for(j=0;j<y;j++)  
    printf("%d ",result[i][j]);
    printf("\n");}
  	
  



} return 0;}
