#include <stdio.h>

#define N 3

int main() {
    int matrix[N][N] = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    int primary_sum = 0, secondary_sum = 0;

    for (int i = 0; i < N; i++) {
        primary_sum += matrix[i][i];           // Primary diagonal
        secondary_sum += matrix[i][N - i - 1]; // Secondary diagonal
    }

    printf("Primary diagonal sum: %d\n", primary_sum);
    printf("Secondary diagonal sum: %d\n", secondary_sum);
    printf("Total diagonal sum: %d\n", primary_sum + secondary_sum);

    return 0;
}
PYTHON
# Function to calculate sum of both diagonals
def sum_of_diagonals(mat):
    n = len(mat)
    primary_sum = 0
    secondary_sum = 0

    for i in range(n):
        primary_sum += mat[i][i]           # Primary diagonal
        secondary_sum += mat[i][n - i - 1] # Secondary diagonal

    return primary_sum, secondary_sum

# Example
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

p_sum, s_sum = sum_of_diagonals(matrix)

print("Primary diagonal sum:", p_sum)
print("Secondary diagonal sum:", s_sum)
print("Total diagonal sum:", p_sum + s_sum)
OUTPUT
Primary diagonal sum: 15
Secondary diagonal sum: 15
Total diagonal sum: 30

# Sum-of-diagonals
