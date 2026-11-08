#include <stdio.h>

float add(float a, float b) { return a + b; }
float sub(float a, float b) { return a - b; }
float mul(float a, float b) { return a * b; }
float divide(float a, float b) { return a / b; }

int main() {
    float a, b;
    char op;
    printf("Enter two numbers: ");
    scanf("%f %f", &a, &b);
    printf("Enter operator (+ - * /): ");
    scanf(" %c", &op);

    switch (op) {
        case '+': printf("Result = %.2f\n", add(a, b)); break;
        case '-': printf("Result = %.2f\n", sub(a, b)); break;
        case '*': printf("Result = %.2f\n", mul(a, b)); break;
        case '/':
            if (b == 0)
                printf("Error: division by zero\n");
            else
                printf("Result = %.2f\n", divide(a, b));
            break;
        default: printf("Invalid operator\n");
    }
    return 0;
}
