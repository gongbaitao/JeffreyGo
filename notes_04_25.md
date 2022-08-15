# CUDA Programming Model
1. Kernels  
CUDA C++ extends C++ by allowing the programmer to define **C++ functions**, called kernels, that, when called, are **executed N times in parallel by N different CUDA threads**, as opposed to only once like regular C++ functions.  
A kernel is defined using the \_\_global\_\_ declaration specifier and the number of CUDA threads that execute that kernel for a given kernel call is specified using a new <<<...>>>execution configuration syntax  
For convenience, threadIdx is a 3-component vector, so that threads can be identified using a one-dimensional, two-dimensional, or three-dimensional thread index, forming a one-dimensional, two-dimensional, or three-dimensional block of threads, called a thread block


**cuBLAS中关于矩阵的存储方式与fortran, MATLAB类似，是列优先， 而非C/C++中的行优先**