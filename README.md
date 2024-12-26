# project
#include <stdio.h>

void main() {
    int choice;
    float amount, converted_amount;
    
    float usd_to_inr = 83.0;   
    float eur_to_inr = 90.0;   
    float gbp_to_inr = 102.0;  
    
    printf("=== Currency Converter ===\n");
    printf("Choose the currency to convert from:\n");
    printf("1. USD to INR\n");
    printf("2. EUR to INR\n");
    printf("3. GBP to INR\n");
    printf("Enter your choice (1-3): ");
    scanf("%d", &choice);
    
    if (choice < 1 || choice > 3) {
        printf("Invalid choice! Please run the program again.\n");
        return;
    }
    
    printf("Enter the amount to convert: ");
    scanf("%f", &amount);
    
    switch (choice) {
        case 1:
            converted_amount = amount * usd_to_inr;
            printf("%f USD is %f INR\n", amount, converted_amount);
            break;
        case 2:
            converted_amount = amount * eur_to_inr;
            printf("%f EUR is %f INR\n", amount, converted_amount);
            break;
        case 3:
            converted_amount = amount * gbp_to_inr;
            printf("%f GBP is %f INR\n", amount, converted_amount);
            break;
    }
    
    printf("Thank you for using the Currency Converter!\n");
}
