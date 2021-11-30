#include <stdio.h>
#include<time.h>
clock_t start,end;

int main(void) {
     start=clock();
	unsigned long i=0;
	unsigned long sum=0;
	for(i=0;i<10000000;i++)
	{
	    sum+=i;
	}
	printf("sum=%lu",sum);
	end=clock();
    double time=((double)(end-start))/CLOCKS_PER_SEC;
    printf("\nTime used=%f",time);
	return 0;
}
