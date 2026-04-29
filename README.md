#include <stdio.h>

int main() {
    int units = 893;
    float bill = 0;

    printf("Units Consumed: %d\n", units);

    if (units <= 100) {
        bill = units * 5;
    } else if (units <= 200) {
        bill = (100 * 5) + ((units - 100) * 7);
    } else {
        bill = (100 * 5) + (100 * 7) + ((units - 200) * 10);
    }

    printf("\n--- Electricity Bill Breakdown ---\n");

    if (units <= 100) {
        printf("First %d units  x  5 = %.2f\n", units, (float)(units * 5));
    } else if (units <= 200) {
        printf("First 100 units  x  5 = 500.00\n");
        printf("Next  %d units  x  7 = %.2f\n", units - 100, (float)((units - 100) * 7));
    } else {
        printf("First 100 units  x  5 =  500.00\n");
        printf("Next  100 units  x  7 =  700.00\n");
        printf("Above %d units  x 10 = %.2f\n", 200, (float)((units - 200) * 10));
    }

    printf("----------------------------------\n");
    printf("Total Bill = %.2f Taka\n", bill);

    return 0;
}
