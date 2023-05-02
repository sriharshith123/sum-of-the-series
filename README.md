#include<stdio.h>

void calculateFactorial(int n, double *fact)
{
    if(n==0 || n==1) {
        *fact = 1;
        return;
    }
    calculateFactorial(n-1, fact);
    *fact *= n;
}

int main()
{
    int n, i;
    double fact, sum = 0.0;
    printf("Enter the value of n: ");
    scanf("%d", &n);

    for(i=1; i<=n; i++) {
        calculateFactorial(i, &fact);
        sum += fact/i;
    }

    printf("Sum of the series: %lf", sum);

    return 0;
}
