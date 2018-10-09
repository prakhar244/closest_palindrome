# closest_palindrome





import java.io.*;
import java.util.*;
class palindrome
{
    public static void main(String args[])
    {
        Scanner sc=new Scanner(System.in);
        int i,j=0,k,l=0,n;
        int p;
        n=sc.nextInt();
        k=n;
        if (n<10)
        { System.out.println(n);
        }
        else
       { 
            p=pali(n);
            l=p;
        if(l==1)
        {
            System.out.println(n);
        }
        else
        {
        j=fun(n);
     
        System.out.println(j);
        }}  
    }
    public static int  pali(int n)
    {
        int m;
        m=n;
        int s=0,r,d;
        while(n>0)
        {
            r=n%10;
            s=(s*10)+r;
            n=n/10;
        }
        if(s==m)
        return 1;
        else
        return 0;
    }
    public static int fun(int n)
    {
        int v=n;
        int i,j,p,q,s1=0,s2=0;
        for(i=n+1;i<(n+2000);i++)
        {
          p=pali(i);
          if(p==1)
          {
              s1=i;
              break;
          }
          
        }
               for(j=n-1;j>=n-2000;j--)
        {
          q=pali(j);
          if(q==1)
          {
              s2=j;
              break;
          }
        }
        int m,n1;
        m=s1-v;
        n1=v-s2;
        if(m>n1)
        return s2;
        else
        return s1;
    }
    }
