#include <stdio.h>

int countDigit(int n, int digit)
{
    if (n == 0)
        return 0;

    return (n % 10 == digit) + countDigit(n / 10, digit);
}

int main()
{
    int n, digit;
    scanf("%d %d", &n, &digit);

    printf("%d", countDigit(n, digit));

    return 0;
}
