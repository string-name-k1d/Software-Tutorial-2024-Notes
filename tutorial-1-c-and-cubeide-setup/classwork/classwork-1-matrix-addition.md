#include <stdio.h>

void display_matrix(int matrix[][2], int num_row) {
  for (int r = 0; r < num_row; r++) {
    for (int c = 0; c < 2; c++) {
      printf("\t%d", matrix[r][c]);
    }
    printf("\n");
  }
}

int main() {
  int matrix_A[3][2] = {
    {0, 1},
    {2, 3},
    {4, 5}
  };
  
  int matrix_B[3][2] = {
    {0, 1},
    {2, 3},
    {4, 5}
  };
  
  int result[3][2] = {0};
  
  // your code starts here
  void add(int mat_a[][2], int mat_b[][2], int result[][2]){
    for (int i = 0; i < 3; i++)
        for (int j = 0; j < 2; j++)
            result[i][j] = mat_a[i][j] + mat_b[i][j];
  }
  add(matrix_A, matrix_B, result);
  
  // your code ends here
  
  printf("A = \n");
  display_matrix(matrix_A, 3);
  printf("\nB = \n");
  display_matrix(matrix_B, 3);
  printf("\nA + B = \n");
  display_matrix(result, 3);
  return 0;
}
