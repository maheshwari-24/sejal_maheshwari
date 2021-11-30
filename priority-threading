#include <pthread.h>
#include<stdio.h>
#include<time.h>
clock_t start,end;

unsigned long sum[4];

void *thread_fn(void *arg)
{
    long id = (long)arg;
    int s =id * 2500000;
    int i=0;
    while(i<2500000)
    {
        sum[id] += (i+s);
        i++;
    }
    return NULL;
}
int main()
{   start=clock();
    pthread_t t1, t2, t3, t4;
    
    pthread_create(&t1,NULL,thread_fn, (void *)0);
    pthread_create(&t2,NULL,thread_fn, (void *)1);
    pthread_create(&t3,NULL,thread_fn, (void *)2);
    pthread_create(&t4,NULL,thread_fn, (void *)3);

    pthread_join(t1,NULL);
    pthread_join(t2,NULL);
    pthread_join(t3,NULL);
    pthread_join(t4,NULL);

    printf("%lu\n",sum[0]+sum[1]+sum[2]+sum[3]);
    
    end=clock();
    double timeused=((double)(end-start))/CLOCKS_PER_SEC;
    printf("\nTime used=%f",timeused);
    return 0;
}
