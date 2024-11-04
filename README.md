Steps:
1.Define the matrices: Define two matrices A and 𝐵 of the same size.
2.Input matrix elements: Take input for each element of matrices A and 𝐵
3.Add the matrices: Calculate each element of matrix 𝐶 by adding corresponding elements of 
A and 𝐵
4.Display the result: Output the resulting matrix 𝐶


C Program Implementation:

#include <stdio.h>

#define SIZE 3  // Define the size of the matrices

int main() {
    
    int A[SIZE][SIZE], B[SIZE][SIZE], C[SIZE][SIZE];
    int i, j;

    // Input elements for matrix A
    printf("Enter elements of matrix A (%dx%d):\n", SIZE, SIZE);
    for (i = 0; i < SIZE; i++) {
        for (j = 0; j < SIZE; j++) {
            printf("A[%d][%d]: ", i, j);
            scanf("%d", &A[i][j]);
        }
    }

    // Input elements for matrix B
    printf("Enter elements of matrix B (%dx%d):\n", SIZE, SIZE);
    for (i = 0; i < SIZE; i++) {
        for (j = 0; j < SIZE; j++) {
            printf("B[%d][%d]: ", i, j);
            scanf("%d", &B[i][j]);
        }
    }

    // Perform matrix addition
    for (i = 0; i < SIZE; i++) {
        for (j = 0; j < SIZE; j++) {
            C[i][j] = A[i][j] + B[i][j];
        }
    }

    // Display the result matrix C
    printf("\nResultant Matrix C after addition:\n");
    for (i = 0; i < SIZE; i++) {
        for (j = 0; j < SIZE; j++) {
            printf("%d ", C[i][j]);
        }
        printf("\n");
    }

    return 0;
}

Explanation:

1.Matrix Declaration: We define three 3x3 matrices: A and B for the input matrices, and C for the result matrix.
2.Input Elements for A and B: We prompt the user to enter elements for each matrix.
3.Matrix Addition: Using nested loops, we add corresponding elements of A and B, storing the result in C.
4.Output Result: The result matrix C is displayed, which is the sum of A and B.
