#include <stdio.h>


#include <stdlib.h>





#define MAX_SIZE 100





int top = -1, n;


int a[MAX_SIZE]; // Global array





void push() {


    if (top == n - 1) {


        printf("Stack is Full.\n");


    } else {


        int element;


        printf("Enter the element: ");


        scanf("%d", &element);


        a[++top] = element; // Increment and insert


    }


}





void pop() {


    if (top == -1) {


        printf("Stack is Empty.\n");


    } else {


        printf("Element popped: %d\n", a[top--]); // Print and decrement top


    }


}





void display() {


    if (top == -1) {


        printf("Stack is Empty.\n");


    } else {


        printf("Stack elements: ");


        for (int i = top; i >= 0; i--) {


            printf("%d ", a[i]);


        }


        printf("\n");


    }


}





int main() {


    int ch;


    printf("Enter array size: ");


    scanf("%d", &n);


    if (n <= 0 || n > MAX_SIZE) {


        printf("Invalid size!\n");


        return 1;


    }





    while (1) {


        printf("\nStack Operations:\n");


        printf("1. Push\n2. Pop\n3. Display\n4. Exit\n");


        printf("Enter your choice: ");


        scanf("%d", &ch);





        switch (ch) {


            case 1:


                push();


                break;


            case 2:


                pop();


                break;


            case 3:


                display();


                break;


            case 4:


                exit(0);


            default:


                printf("Invalid Choice!\n");


        }


    }


    return 0;


}
