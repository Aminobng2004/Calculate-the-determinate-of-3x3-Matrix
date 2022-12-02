#include <stdio.h>
main()
{
	int tab[100][100],s[100][100];
	int k,i,l,j,o,c;
	float a,b,d,det;
	
	printf("lines?:");
	scanf("%d",&l);
	
	printf("coloms?:");
	scanf("%d",&c);
	
	/*declaration du tableau*/
	for(i=1;i<=l;i++)
		{
			for(k=1;k<=c;k++)
				{
					printf("tab1[%d][%d]=",i,k);
					scanf("%d",&tab[i][k]);				
				}
		}
		
	for(i=1;i<=l;i++)
		{
			for(k=1;k<=c;k++)
				{		
					printf("%d\t",tab[i][k]);				
				}
					printf("\n");
					
			printf("\n");			
		}
		
		
		
		printf("-----------------------------\n");
		printf("le determinant d'une matrice:\n\n");
		
		
		
		for(i=1;i<=l;i++)
		{
			
			for(j=1;j<=c+2;j++)
			{	   
				if(j<=3)
				{
				s[i][j]=tab[i][j];
				}
					else
					{
						s[i][j]=tab[i][j-3];			
					}		
						printf("%d\t",s[i][j]);
			}
			printf("\n\n");
	}
	

    	for(i=1;i<=l;i++)
        {
				for(j=i;j<=c;j++) 
				{
					a+=s[i][j]*s[i+1][j+1]*s[i+2][j+2];	
				}    
		}
		
		printf("%.0f\t",a);           		
            
			    		
        for(i=1;i<=l;i++)					
     	{
			for(j=5;j>=c;j--) 
			{
				b+=s[i][j]*s[i+1][j-1]*s[i+2][j-2];						
			}    
		}
		
			printf("%.0f\t",b); 
			
			det=a-b;
			printf("\nle determinant de cet matrice est:%.0f",det);         		
                		
}
		
