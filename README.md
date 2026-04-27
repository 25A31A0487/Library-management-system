# Library-management-system
#include <stdio.h>
struct Track {
    char Bname[30];
    char authorname[30]; 
    int id;
};

int main() {
    int n;
    struct Track T[10];
    printf("Enter how many book records you want: ");
    scanf("%d", &n);

    for(int i = 0; i < n; i++) {
        printf("\nEnter details for record %d:\n", i + 1);
        
        printf("Book Name: ");
        scanf("%s", T[i].Bname); 
        printf("Author Name: ");
        scanf("%s", T[i].authorname);
        printf("Student ID: ");
        scanf("%d", &T[i].id); 
    }

    printf("\n--- RECORD ---\n");
    for(int i = 0; i < n; i++) {
        printf("\nDetails for Record %d:\n", i + 1);
        printf("Book Name: %s \n", T[i].Bname);
        printf("Author: %s \n", T[i].authorname);
        printf("Student ID: %d \n", T[i].id);
        printf("Student %d has taken the book: %s\n", T[i].id, T[i].Bname);
    }

    return 0;
}
