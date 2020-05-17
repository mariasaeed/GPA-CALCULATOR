# GPA-CALCULATOR

#include <stdio.h>

double function_grade(double x);
int main(void)
{
	double gpa_old;
	int i,w;
	
	printf("Old GPA information:\n");
	printf("\n");
	
	
	
	printf("Enter your current CGPA: ");
	scanf("%lf",&gpa_old);
	
	printf("Enter the number of courses used to calculate the CGPA: ");
	scanf("%d",&w);
	double old_points;
	
	old_points=gpa_old*w;
	
	i=0;
	double percent=0;
	double grade1;
	double total=0;
	
	printf("\n");
	printf("New GPA information:\n");
	printf("\n");
	printf("Enter -1 to finish");
	printf("\n\n");
	
	do
	{
		printf("Enter grade percentage: ");
		scanf("%lf",&percent);
		
		grade1=function_grade(percent);
		i++;
		total+=grade1;	
	}while(percent!=-1);
	
	printf("\n\n");
	
	double tgpa;
	
	i=i-1;
	
	tgpa=total/i;
	
	printf ("Your TGPA for this semester is %.2lf\n\n",tgpa);
	
	double a,cgpa;
	int b;
	
	a=old_points+total;
	b=i+w;
	
	cgpa=a/b;
	
	printf ("Your CGPA is %.2lf\n",cgpa);
	
	
	return 0;
}

double function_grade(double x)
{
	double point;
	
	if(x<=100 && x>=90)
			point=4.33;
		else
			if(x<=89 && x>=85)
				point=4.00;
			else
				if(x<=84 && x>=80)
					point=3.67;
				else
					if(x<=79 && x>=77)
						point=3.33;
					else
						if(x<=76 && x>=73)
							point=3.00;
						else
							if(x<=72 && x>=70)
								point=2.67;
							else
								if(x<=69 && x>=67)
									point=2.33;
								else
									if(x<=66 && x>=63)
										point=2.00;
									else
										if(x<=62 && x>=60)
											point=1.67;
										else
											if(x<=59 && x>=57)
												point=1.33;
											else
												if(x<=56 && x>=53)
													point=1.00;
												else
													if(x<=52 && x>=50)
														point=0.67;
													else
														if(x<=49 && x>=0)
															point=0.00;
	return(point);
}

	
	
	
