# A-Book-Store-database-Program-in-C
#include <stdio.h>

struct Book {
    char id[10];          
    float price;     
    int quantity;    
};

void inputBooks(struct Book books[], int n) {
    for (int i = 0; i < n; i++) {
        printf("\nEnter details for Book %d:\n", i + 1);
        printf("Book ID: ");
        scanf("%s", &books[i].id);
        printf("Book Price: ");
        scanf("%f", &books[i].price);
        printf("Quantity Available: ");
        scanf("%d", &books[i].quantity);
    }
}

int main() {
    int n;

    printf("Enter the number of books: ");
    scanf("%d", &n);

    struct Book books[n];  

    inputBooks(books, n);

    printf("\nBook Details Entered:\n");
    printf("ID\t\tPrice\t\tQuantity\n");
    printf("_ _ _ _ _ _ _ _ _ _ _ _ _ _ _\n");
    for (int i = 0; i < n; i++) {
        printf("%s\t%.2f\t\t%d\n", books[i].id, books[i].price, books[i].quantity);
    }

    return 0;
}

