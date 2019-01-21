# Matrix Algebra

Simple template matrix algebra library.

Features:
- Save matrix to text file.
- Load matrix from text file.
- Use(in theory) any type that overloads *, +, -, /, == operators.
- Convert matrix to human readable string.
- You can create matrix using initialize list.
- Matrix multiplication, sum, substract dot product are implemented.

**How do I use this?**  
Simple!  
```c++
MatAlg::Matrix<double> first = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
std::cout << MatAlg::toString(first) << std::endl;

MatAlg::Matrix<double> second = {{7, 8, 9}, {4, 5, 6}, {1, 2, 3}};
std::cout << MatAlg::toString(second) << std::endl;

MatAlg::Matrix<double> result = first*second;
std::cout << MatAlg::toString(result) << std::endl;
```
Output:  
```
[ 1.000000 2.000000 3.000000 ]
[ 4.000000 5.000000 6.000000 ]
[ 7.000000 8.000000 9.000000 ]

[ 7.000000 8.000000 9.000000 ]
[ 4.000000 5.000000 6.000000 ]
[ 1.000000 2.000000 3.000000 ]

[ 18.000000 24.000000 30.000000 ]
[ 54.000000 69.000000 84.000000 ]
[ 90.000000 114.000000 138.000000 ]
```
**What about saving and loading?**  
As simple as previous example:  

```c++
MatAlg::Matrix<double> matrix = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
MatAlg::saveMatrix<double>("./test.txt", matrix);
MatAlg::Matrix<double> loaded = MatAlg::loadMatrix<double>("./test.txt");
std::cout << MatAlg::toString(loaded) << std::endl;
```
