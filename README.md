# Matrix Addition Program

A C++ program that performs the addition of two matrices and displays the resultant matrix.

## Description

This program allows the user to input two matrices of the same dimensions and calculates their sum. It demonstrates basic matrix operations and input/output handling in C++.

### Key Features
- Matrix input from user
- Matrix addition operation
- Dynamic result calculation
- Console output of the resultant matrix

## Code Structure

```cpp
#include <iostream>
using namespace std;

int main() {
    int rows, cols;
    cout << "Enter the number of rows and columns: ";
    cin >> rows >> cols;
    int matrix1[10][10], matrix2[10][10], result[10][10];
    
    cout << "Enter elements of first matrix:\n";
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cin >> matrix1[i][j];
        }
    }
    
    cout << "Enter elements of second matrix:\n";
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cin >> matrix2[i][j];
        }
    }
    
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            result[i][j] = matrix1[i][j] + matrix2[i][j];
        }
    }
    
    cout << "Resultant matrix after addition:\n";
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cout << result[i][j] << " ";
        }
        cout << endl;
    }
    return 0;
}
