// C program to create dynamic array using malloc() function 
  
#include <stdio.h> 
#include <stdlib.h> 
  
int main() 
{ 
  
    // address of the block created hold by this pointer 
    int* ptr; 
    int size; 
  
    // Size of the array 
    printf("Enter size of elements:"); 
    scanf("%d", &size); 
  
    //  Memory allocates dynamically using malloc() 
    ptr = (int*)malloc(size * sizeof(int)); 
  
    // Checking for memory allocation 
    if (ptr == NULL) { 
        printf("Memory not allocated.\n"); 
    } 
    else { 
  
        // Memory allocated 
        printf("Memory successfully allocated using "
               "malloc.\n"); 
  
        // Get the elements of the array 
        for (int j = 0; j < size; ++j) { 
            ptr[j] = j + 1; 
        } 
  
        // Print the elements of the array 
        printf("The elements of the array are: "); 
        for (int k = 0; k < size; ++k) { 
            printf("%d, ", ptr[k]); 
        } 
    } 
  
    return 0; 
}
