#include<stdio.h>

int main()
{
    int a[100],n,i;
    scanf("%d",&n);
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    subset(a,i,n);
}
int subset(int b[],int c,int tot)
{
    int j,k;
    c=1<<tot;
    while(c>0)
    {
        printf("{");
        for(j=tot-1,k=0;j>=0;j--)
        {
            if(1<<j&c)
            {
                printf("%d",b[k]);
                
            }
            k++;
        }
        c--;
        printf("}\n");
    }
    
}
