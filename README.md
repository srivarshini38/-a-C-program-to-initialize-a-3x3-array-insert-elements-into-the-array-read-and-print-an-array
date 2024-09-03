# -a-C-program-to-initialize-a-3x3-array-insert-elements-into-the-array-read-and-print-an-array
#include <stdio.h>

int main() {
    int matrix[3][3];
    int *ptr = &matrix[0][0];
    int sum_diagonal = 0;

    // Input elements in the matrix
    printf("Input elements in the matrix:\n");
    for(int i = 0; i < 3; i++) {
        for(int j = 0; j < 3; j++) {
            printf("element - [%d][%d]: ", i, j);
            scanf("%d", (ptr + i * 3 + j));
        }
    }

    // Print the matrix and calculate sum of diagonal elements
    printf("The matrix is:\n");
    for(int i = 0; i < 3; i++) {
        for(int j = 0; j < 3; j++) {
            printf("%d ", *(ptr + i * 3 + j));
            if(i == j || i + j == 2) {
                sum_diagonal += *(ptr + i * 3 + j);
            }
        }
        printf("\n");
    }

    // Print the sum of the diagonal elements
    printf("Sum of diagonal elements: %d\n", sum_diagonal);

    return 0;
}
