Chapter 2 : Array

1. Write a Program for the transpose matrix.
   
Input :

#include<stdio.h>int

main(){

int matrix[2][2];int i,j;

printf("Enter elements of 2 X 2 matrix :\n");

for(i=0;i<2;i++){

for(j=0;j<2;j++){

printf("Element [%d][%d]:",i,j);

scanf("%d",&matrix[i][j]);

}

}

printf("\nOriginal Matrix :\n");

for(i=0;i<2;i++){

for(j=0;j<2;j++){

printf("%d\t",matrix[i][j]);

}

printf("\n");

}

printf("\nTranspose Matrix :\n");

for(i=0;i<2;i++){

for(j=0;j<2;j++){

printf("%d\t",matrix[j][i]);

}

printf("\n");

}

return 0;

}

OUTPUT:



3. Write a program to multiply two polynomials. (1 dimensional)

Input:

#include<stdio.h>

void mult(int poly1[],int poly2[],int res[],int n1,int n2){int i,j;

for(i=0;i<n1;i++){

for(j=0;j<n2;j++){

res[i+j] += poly1[i]*poly2[j];

}

}

}

void disp(int poly[], int n){int I;

for(i=0;i<n;i++){

printf("%d",poly[I]);

if(i!=n-1)

printf("x^%d",I);

if(i!=n-1)

printf("+");

}

printf("\n");

}


int main(){

int n1, n2, poly1[100], poly2[100], I;

printf("Enter number of terms in 1st Polynomial : ");

scanf("%d",&n1);

printf("Enter coefficients of 1st polynomial : ");

for(i=0;i<n1;i++){

printf("Coefficient of x^%d :",I);

scanf("%d",&poly1[I]);

}

printf("Enter number of terms in 2nd Polynomial : ");

scanf("%d",&n2);

printf("Enter coefficients of 2nd polynomial : ");

for(i=0;i<n2;i++){

printf("Coefficient of x^%d :",I);

scanf("%d",&poly2[I]);

}

int res[200]={0};

mult(poly1, poly2, res, n1, n2);

printf("First Polynomial : ");

disp(poly1,n1);

printf("Second Polynomial : ");

disp(poly2,n2);

printf("After Multiplication : ");

disp(res, n1+n2-1);
return 0;

}

OUTPUT:

4. Write a program to addition two polynomials.(2 dimensional)

Input:

#include<stdio.h>

void add(int poly1[][2],int poly2[][2],int res[][2],int n){int i,j;

for(i=0;i<n;i++){

res[i][0]=poly1[i][0]+poly2[i][0];

}

}

void disp(int poly[][2], int n){int I;

for(i=0;i<n;i++){

printf("%d",poly[i][0]);

if(i!=0)

printf("x^%d",I);

if(i!=n-1)

printf("+");

}

printf("\n");

}

int main(){

int n, poly1[100][2], poly2[100][2], res[100][2], i; printf("Enter

number of terms in the Polynomials : ");scanf("%d",&n);

printf("Enter coefficients of 1st polynomial : ");

for(i=0;i<n;i++){

printf("Coefficient of x^%d :",I);

scanf("%d",&poly1[i][0]);

}

printf("Enter coefficients of 2nd polynomial : ");

for(i=0;i<n;i++){

printf("Coefficient of x^%d :",I);

scanf("%d",&poly2[i][0]);

}

add(poly1, poly2, res, n);

printf("First Polynomial : ");

disp(poly1,n);

printf("Second Polynomial : ");

disp(poly2,n);

printf("After Additipn : ");

disp(res, n);

return 0;

}

OUTPUT:

5. Write a program to addition subtraction polynomials.(2 dimensional)

Input:

#include<stdio.h>

void add(int poly1[][2],int poly2[][2],int res1[][2],int n){int i,j;

for(i=0;i<n;i++){

res1[i][0]=poly1[i][0]+poly2[i][0];

}

}

void subs(int poly1[][2],int poly2[][2],int res2[][2],int n){int i,j;

for(i=0;i<n;i++){

res2[i][0]=poly1[i][0]-poly2[i][0];

}

}

void disp(int poly[][2], int n){int I;

for(i=0;i<n;i++){

printf("%d",poly[i][0]);

if(i!=0)

printf("x^%d",I);

if(i!=n-1)

printf("+");

}

printf("\n");

}

int main(){

int n, poly1[100][2], poly2[100][2], res1[100][2], res2[100][2], I;

printf("Enter number of terms in the Polynomials : "); scanf("%d",&n);

printf("Enter coefficients of 1st polynomial : ");

for(i=0;i<n;i++){

printf("Coefficient of x^%d :",I);

scanf("%d",&poly1[i][0]);

}

printf("Enter coefficients of 2nd polynomial : ");

for(i=0;i<n;i++){

printf("Coefficient of x^%d :",I);

scanf("%d",&poly2[i][0]);

}

add(poly1, poly2, res1, n);

subs(poly1, poly2, res2, n);

printf("First Polynomial : ");

disp(poly1,n);

printf("Second Polynomial : ");

disp(poly2,n);

printf("After Additipn : ");

disp(res1, n);

printf("After Substraction : ");

disp(res2, n);

return 0;

}

OUTPUT:

Chapter 3 : Stack

5. Write a Program for Implementation of stack.

Input:

#include<stdio.h>

#define max 100 int

top=-1;

int stack[max]; void

push(int val){

if(top==max-1){

printf("Cannot Push %d\n",val);

}

else{

}

}

stack[++top]=val;

printf("%d pushed to stack\n",val);

void pop(){

if(top==-1){

printf("Cannot Pop\n");

}
else{
}

}

printf("%d popped from stack\n",stack[top--]);

void peek(){

if(top==-1){

printf("\nStack is Empty\n");

}

else{
}


}

printf("Top element is %d\n",stack[top]);

int isEmpty(){

return top==-1;

}

int isFull(){

return top==max-1;

}

int main(){

push(10);

push(20);

push(30);

peek();

pop();

pop();

peek();

if(isEmpty()){

printf("\nStack is Empty");

}

else{

}

printf("\nStack is not Empty");

if(isFull()){

printf("\nStack is Full");

}

else{

}

printf("\nStack is not Full");

return 0;

}

OUTPUT:

6. Write a Program to Checking of balanced parenthesis using stack

Input:

#include<stdio.h>

#include<string.h>

#define max 100 char

stack[max]; int top;

void initStack(){

top=-1;

}

void push(char item){

if(top==max-1){

printf("Stack is Full\n");

}

else{

stack[++top]=item;

}

}

void pop(){

if(top==-1){

printf("Stack is Empty\n");

}

else{

}

}

--top;

int isEmpty(){

return top==-1;

}

int isFull(){

return top==max-1;
}

char peek(){

if(!isEmpty()){

return stack[top];

}

return '\0';

}

int balancedParenthesis(char expression[]){

initStack();

int i; for(i=0;i<strlen(expression);i++){

char ch=expression[I];

switch(ch){

case '(':

case '{':

case '[':

push(ch);

break;

case ')':

if(isEmpty()||peek()!='(')

return 0;

pop();

break;

case '}':

if(isEmpty()||peek()!='{')

return 0;

pop();

break;

case ']':

if(isEmpty()||peek()!='[')

return 0;

pop();

break;

}

}

return isEmpty();

}

int main(){

char expression[max]; printf("Enter

an expression : ");

scanf("%s",&expression);

if(balancedParenthesis(expression)){

printf("Parenthesis are balanced.\n");

}

else{

}

printf("Parenthesis are not balanced.\n");

return 0;

}

OUTPUT:

7. Write a Program to reverse a string using stack.

Input:

#include<stdio.h>

#include<string.h>

#define max 100

int top=-1, stack[max];

void push(char x){

if(top==max-1){

printf("Stack is Full\n");

}

else{

}

}

stack[++top]=x;

void pop(){

if(top==-1){

printf("Stack is Empty\n");

}

else{

}

}

printf("%c",stack[top--]);

int main(){

char str[max]; printf("Enter

the string : ");scanf("%s", &str);

int len=strlen(str); int

i; for(i=0;i<len;i++){

push(str[i]);

}

printf("Reversed String : ");

for(i=0;i<len;i++){

pop();

}

return 0;

}

OUTPUT:

8. Write a function for Dynamic Implementation of stack.

Input:

#include<stdio.h>

#define max 100 int

top=-1;

int stack[max]; void

push(int val){

if(top==max-1){

printf("Cannot Push %d\n",val);

}

else{

}

stack[++top]=val;

printf("%d pushed to stack\n",val);

}

void pop(){

if(top==-1){

printf("Cannot Pop\n");

}

else{

}

}

printf("%d popped from stack\n",stack[top--]);

void peek(){

if(top==-1){

printf("\nStack is Empty\n");

}

else{

}

}

printf("Top element is %d\n",stack[top]);

int isEmpty(){

return top==-1;

}

int isFull(){

return top==max-1;

}

int main(){

int ch, val;

while(1){

printf("Stack Operations : \n");

printf("1.Push\n");

printf("2.Pop\n");

printf("3.Peek\n");

printf("4.Exit\n");

printf("Enter Choice : ");

scanf("%d",&ch); switch(ch){

case 1:

printf("Enter element to insert : ");

scanf("%d",&val);

push(val);

break;

case 2:

pop();

break;

case 3:

peek();

break;

case 4:

exit(0);

default:

printf("Enter the valid choice!");

}

}

return 0;

}

OUTPUT:

9. Write a program to Evaluation of a postfix expression

Input:

#include<stdio.h>

#include<ctype.h>

#include<string.h>

#define max 100 int

stack[max];

int top=-1;

void push(int x){

if(top==max-1){

printf("Stack is full\n");

}

else{

}

}

stack[++top]=x;

int pop(){

if(top==-1){

printf("Stack is empty\n");

return -1;

}


else{

}

}

return stack[top--];

int performOperation(int op1, int op2, char operation){

switch(operation){

case '+':

return op1+op2;

case '-':

return op1-op2;

case '*':

return op1*op2;


case '/':

return op1/op2;

default:

return 0;

}

}


int evalPostfixExp(char *expression){int

l=strlen(expression);

int i;

for(i=0;i<l;i++){

char c=expression[i];

if(isdigit(c)){

push(c-'0');

}

else{

}

}

int op2=pop();

int op1=pop();

int res=performOperation(op1,op2,c);

push(res);

return pop();

}

int main(){

char expression[max];

printf("Enter a postfix Expression : ");

scanf("%s",expression);

int res=evalPostfixExp(expression); printf("Result of

Postfix Expression : %d\n",res);return 0;

}

OUTPUT:

10. Write a program to Evaluation of a prefix expression

Input:

#include<stdio.h>

#include<ctype.h>

#include<string.h>

#define max 100 int

stack[max];

int top=-1;

void push(int x){

if(top==max-1){

printf("Stack is full\n");

}

else{

}

}

top++;

stack[top]=x;

int pop(){

if(top==-1){

printf("Stack is empty\n");

return -1;

}

else{

}

}

int x=stack[top];

top--;

return x;

int performOperation(int op1, int op2, char operation){

switch(operation){

case '+':

return op1+op2;

case '-':

return op1-op2;

case '*':

return op1*op2;

case '/':

if(op2!=0){

return op1/op2;

}

else{

}

default:

printf("Error:Division by zero.\n");return

0;

return 0;

}

}

int evalPrefixExp(char *expression){int

l=strlen(expression);

int i;

for(i=l-1;i>=0;i--){

char c=expression[i];

if(isdigit(c)){

push(c-'0');

}

else{

}

}

int op1=pop();

int op2=pop();

int res=performOperation(op1,op2,c);

push(res);

return pop();

}

int main(){

char expression[max];

printf("Enter a prefix Expression : ");

scanf("%s",expression);

int res=evalPrefixExp(expression); printf("Result of

Prefix Expression : %d\n",res);return 0;

}

OUTPUT:

11. Write a program to convert infix to postfix using stack

Input:

#include<stdio.h>

#include<ctype.h>

#include<string.h>

#include<limits.h>

#include<stdlib.h>

#define max 100 char

stack[100]; int top=-

1;

int isEmpty(){

return top==-1;

}

int isFull(){

return top==max-1;

}

char peek(){

return stack[top];

}

char pop(){

if(isEmpty()){

return -1;

}

return stack[top--];

}

void push(char op){

if(isFull()){

printf("Satck is Full");

}

else{

}

}

stack[++top]=op;

int checkifoperand(char ch){

return(ch>='a'&&ch<='z')||(ch>='A'&&ch<='Z')||(ch>='0'&&ch<='

9');

}

int precedence(char ch){

switch(ch){

case '+':

case '-':

return 1;

case '*':

case '/':

return 2;

case '^':

return 3;

default:

return -1;

}

}

int convertintopost(char *expression){int

i,j=-1;

char postfix[max];

for(i=0;expression[i];++i){

char c=expression[I];

if(checkifoperand(c)){

postfix[++j]=c;

}

else if(c=='('){

push(c);

}

else if(c==')'){

while(!isEmpty() && peek()!='('){

postfix[++j]=pop();

}

if(!isEmpty() && peek()!='('){

printf("Invalid Expression\n");

return -1;

}

else{

}

else{

}

pop();

while(!isEmpty()&&precedence(c)<=precedence(peek())){

postfix[++j]=pop();

}

push(c);

}

}

while(!isEmpty()){

postfix[++j]=pop();

}

postfix[++j]='\0';

printf("%s",postfix);

}

int main(){

char expression[max];

printf("Enter an infix Expression : "); fgets(expression,

max, stdin); expression[strcspn(expression,"\n")]='\0';

convertintopost(expression);

return 0;

}

OUTPUT:

12. Write a program to convert infix to prefix using stack

Input:

#include<stdio.h>

#include<string.h>

#include<limits.h>

#include<stdlib.h>

#define max 100 char

stack[100]; int top=-

1;

int isEmpty(){

return top==-1;

}

int isFull(){

return top==max-1;

}

char peek(){

return stack[top];

}

char pop(){

if(isEmpty()){

return -1;

}

return stack[top--];

}


void push(char op){

if(isFull()){


}

else{

}

}

printf("Satck is Full");


stack[++top]=op;

int checkifoperand(char ch){


return(ch>='a'&&ch<='z')||(ch>='A'&&ch<='Z')||(ch>='0'&&ch<='

9');

}

int precedence(char ch){

switch(ch){

case '+':

case '-':

return 1;

case '*':

case '/':

return 2;

case '^':
return 3;

default:

return -1;

}

}

void reverse(char *expression){int

n=strlen(expression); int I;

for(i=0;i<n/2;i++){

char temp=expression[I];

expression[i]=expression[n-i-1];

expression[n-i-1]=temp;

}

}

int convertintopre(char *expression){

reverse(expression);

int i, j=0;

int n=strlen(expression);

char res[max];

memset(res, 0, sizeof(res));

for(i=0;expression[i];++i){char

c=expression[i];

if(c=='('){

c=')';


}

else if(c==')'){

c='(';

}

if(checkifoperand(c)){

res[j++]=c;

}

else if(c=='('){

push(c);

}

else if (c == ')') {

while (!isEmpty() && peek() != '(') {res[j++]

= pop();


}

pop();
}

else{

while (!isEmpty() && precedence(peek()) >= precedence(c)) {res[j++] =

pop();


}

push(c);

}

}

while (!isEmpty()) {

res[j++] = pop();


}

res[j] = '\0';

reverse(res);

printf("Prefix Expression: %s\n", res);

}


int main(){

char expression[max];

printf("Enter an infix Expression : "); fgets(expression,

max, stdin); expression[strcspn(expression,"\n")]='\0';

convertintopre(expression);

return 0;

}

OUTPUT:

Chapter 4 : Queue

13. Write a program to implement the queue and display the no.of

elements.

Input:


#include<stdio.h>

#define size 5

int queue[size], front=-1, rear=-1;void

enqueue(int val){

if(rear==size-1){

printf("Queue is Full!\n");

}

else{

if(front==-1){

front=0;

}

rear++;

queue[rear]=val;

printf("Inserted %d\n",val);

}

}

void dequeue(){int

I;

if(front==-1){

printf("Queue is Empty!\n");

}

else{

}

}

printf("\nDeleted %d\n",queue[front]);

front++;

void display(){

int i; if(front==-

1){

printf("Queue is Empty!\n");

}

else{

printf("Queue elements are : \n");

for(i=front;i<=rear;i++){

printf("%d\t",queue[I]);

}

}

}

int main(){

enqueue(10);

enqueue(20);

enqueue(30);

display();

dequeue();

display();

return 0;

}

OUTPUT:

14. Write a program of circular queue.

Input:

#include<stdio.h>

#define size 5

int cqueue[size], front=-1, rear=-1;void

enqueue(int val){

if((rear+1)%size==front){

printf("Circular Queue is empty!\n");

}

else{

if(front==-1){

front=0;

}

rear=(rear+1)%size;

cqueue[rear]=val; printf("Inserted

%d\n",val);

}

}

void dequeue(){

if(front==-1){

printf("Circular Queue is Empty.\n");

}

else{

printf("Deleted %d\n",cqueue[front]);

if(front==rear){

}

else{

}

}

}

front=-1;

rear=-1;

front=(front+1)%size;

void display(){

int i; if(front==-

1){

printf("Circular Queue is Empty.\n");

}

else{

printf("Circular Queue Elements are : ");

for(i=front;i!=rear;i=(i+1)%size){

printf("%d\t",cqueue[i]);

}

printf("%d\n",cqueue[rear]);

}

}

int main(){
enqueue(10);

enqueue(20);

enqueue(30);

display();

dequeue();


display();

return 0;

}

OUTPUT:

Chapter 7 : Searching and Sorting

15. Write a program to insertion Sort

Input:

#include<stdio.h>int

main(){

int A[6]={18,7,22,3,14,2};

int i,j,key;

printf("Before Sorting : ");

for(i=0;i<6;i++){

printf("%d\t",A[I]);

}

printf("\n");

for(i=1;i<6;i++){

key=A[I];

for(j=i-1;A[j]>key;j--){

A[j+1]=A[j];

}

A[j+1]=key;

}

printf("After Sorting : ");

for(i=0;i<6;i++){

printf("%d\t",A[I]);

}

printf("\n");

return 0;

}

OUTPUT:

16. Write a Program to Bubble Sort .

Input:

#include<stdio.h>int

main(){

int A[5]={64,34,25,12,22};

int i, j, x;

printf("Before Sorting : ");

for(i=0;i<5;i++){

printf("%d\t",A[I]);

}

printf("\n");

for(i=0;i<4;i++){

for(j=0;j<4-i;j++){

if(A[j]>A[j+1]){

x=A[j];

A[j]=A[j+1];

A[j+1]=x;

}

}

}

printf("After Sorting : ");

for(i=0;i<5;i++){

printf("%d\t",A[I]);

}

printf("\n");

return 0;

}
OUTPUT:

17. Write a program to Selection Sort
Input:

#include<stdio.h>int

main(){

int A[5]={12,11,13,5,6};

int i, j, x;

printf("Before Sorting : ");

for(i=0; i<5;i++){

printf("%d\t",A[I]);

}

printf("\n");

for(i=0;i<5;i++){

for(j=i+1;j<5;j++){

if(A[i]>A[j]){

x=A[i];

A[i]=A[j];

A[j]=x;

}

}

}

printf("After Sorting : ");

for(i=0; i<5;i++){

printf("%d\t",A[I]);

}

printf("\n");

return 0;

}

OUTPUT:

18. Write a Program Linear Search

Input:

#include<stdio.h>

int linearsearch(int arr[], int target){int I;

for(i=0; i<5; i++){

if(arr[i]==target){

return I;

}

}

return -1;
}

int main(){

int arr[5]={10,2,8,5,17};

int target;

printf("Enter the value to search : ");

scanf("%d", &target);

int res=linearsearch(arr, target);

if(res==-1){

printf("Element not found in the array.\n");

}

else{

}

printf("Element %d found at index %d.\n",target,res);

return 0;

}

OUTPUT:

19. Write a Program Binary Search

Input:

#include<stdio.h>

#define size 8

int binarysearch(int arr[], int target){int

low=0, high=size-1;

while(low<=high){

int mid=low+(high-low)/2;

if(arr[mid]==target){

return mid;
}

else if(arr[mid]<target){

low=mid+1;

}
else{

}

}

high=mid-1;

return -1;

}

int main(){

int arr[size]={1,3,5,7,9,11,13,15};

int target;

printf("Enter the target value : ");

scanf("%d",&target);

int result=binarysearch(arr, target);

if(result!=-1){

printf("Element %d found at index %d\n",target,result);

}

else{

}

printf("Element %d not found\n",target);

return 0;

}

OUTPUT:

20. Write a Program Linear search on sorted data .

Input:

#include<stdio.h>

#define size 5

int main(){

int A[size];

int x, I;

printf("Enter %d elements in sorted order : \n",size);

for(i=0;i<size;i++){

printf("Element %d : ",i+1);

scanf("%d",&A[I]);

}

while(getchar()!='\n'); printf("Enter

value to search : ");scanf("%d",&x);

for(i=0;i<size;i++){


if(A[i]==x){



printf("Value found at the index %d\n",i);return

0;

}

else if(A[i]>x){

break;

}

}

printf("Value not found\n");

return 0;

}

OUTPUT:

21. Write a Program Linear search on unsorted data

Input:

#include<stdio.h>

#define size 5

int main(){

int A[size];

int x, I;

printf("Enter %d elements in unsorted order : \n",size);

for(i=0;i<size;i++){

printf("Element %d : ",i+1);

scanf("%d",&A[I]);

}

while(getchar()!='\n'); printf("Enter

value to search : ");scanf("%d",&x);

for(i=0;i<size;i++){

if(A[i]==x){

break;

}

}

if(i==10){

printf("Value not found\n");

}

else{

}

printf("Value found");

return 0;

}

OUTPUT:

Chapter 6 : Tree

22. Write a Program Implementation of a BST ,Add,Search ,Min,Max

Input:

#include <stdio.h>

#include <stdlib.h>

struct Node {

int key;

struct Node* left;

struct Node* right;

};

struct Node* createNode(int key) {

struct Node* newNode = (struct Node*)malloc(sizeof(struct Node));newNode-

>key = key;

newNode->left = NULL;

newNode->right = NULL;

return newNode;

}

struct Node* add(struct Node* root, int key) {if (root

== NULL) {

return createNode(key);

}

if (key < root->key) {

root->left = add(root->left, key);

} else if (key > root->key) {

root->right = add(root->right, key);

}

return root;

}

int search(struct Node* root, int key) {if

(root == NULL) {

return 0;

}

if (root->key == key) {

return 1;

}

if (key < root->key) {

return search(root->left, key);

} else {

return search(root->right, key);

}

}

struct Node* Min(struct Node* root) {

while (root->left != NULL) {root =

root->left;

}

return root;

}

struct Node* Max(struct Node* root) {while

(root->right != NULL) {

root = root->right;

}

return root;

}

int main() {

struct Node *root=NULL;int

ch, val;

while(1){

printf("\n\n1.Add\n2.Search\n3.Min\n4.Max\n5.Exit\n");printf("Enter

your Choice : ");

scanf("%d", &ch);

switch(ch){

case 1:

printf("Enter value to add : ");

scanf("%d",&val); root=add(root,

val);

break;

case 2:

printf("Enter value to search : ");int

value;

scanf("%d",&value); if

(search(root, value)) {

printf("Value %d found in the BST.\n", value);

} else {

printf("Value %d not found in the BST.\n",

value);

}

break;

case 3:{

struct Node* minNode = Min(root);if

(minNode != NULL) {

printf("Minimum value in the BST: %d\n", minNode->key);

} else {

printf("The tree is empty.\n");

}

break;

}

maxNode->key);

case 4:{

struct Node* maxNode = Max(root);if

(maxNode != NULL) {

printf("Maximum value in the BST: %d\n",

} else {

printf("The tree is empty.\n");

}

break;

}

case 5:

exit(0);

default:

printf("Invalid Choice");

}

}

return 0;

}

OUTPUT:

23. Write a Program Implementation of a BST create insert, countleaf,

countnodes, depth.

Input:

#include<stdio.h>

#include<stdlib.h>

struct Node{

int data;

struct Node *left; struct

Node *right;

};


struct Node *createNode(int val){

struct Node *newNode=(struct Node*)malloc(sizeof(struct Node));newNode-

>data=val;

newNode->left=NULL;

newNode->right=NULL;


return newNode;

}

struct Node *insert(struct Node *root, int val){

if(root==NULL){

return createNode(val);

}

if(val<root->data){

root->left=insert(root->left,val);

}

else if(val>root->data){

root->right=insert(root->right,val);

}

return root;

}

int countNodes(struct Node *root){

if(root==NULL){

return 0;

}

return 1+countNodes(root->left)+countNodes(root->right);

}

int countLeaf(struct Node *root){

if(root==NULL){

return 0;

}

if(root->left==NULL && root->right==NULL){return 1;

}

return countLeaf(root->left)+countLeaf(root->right);

}

int depth(struct Node *root){

if(root==NULL){

return 0;

}

int leftDepth=depth(root->left); int

rightDepth=depth(root->right);

return 1+(leftDepth>rightDepth?leftDepth:rightDepth);

}

void inorder(struct Node *root){

if(root!=NULL){

inorder(root->left);

printf("%d\t",root->data);

inorder(root->right);

}

}

int main(){

struct Node *root=NULL;int

ch, val;

while(1){

printf("\n\n1.Insert\n2.Display(Inorder)\n3.Count

Nodes\n4.Count Leaf Nodes\n5.Depth\n6.Exit\n");

printf("Enter your Choice : ");

scanf("%d", &ch); switch(ch){

case 1:

printf("Enter value to insert : ");

scanf("%d",&val); root=insert(root,
val);

break;

case 2:

printf("Inorder Traversal : ");

inorder(root);

printf("\n");

break;

case 3:

printf("Total no. of

Nodes : %d\n",countNodes(root));

break;

case 4:

printf("Total no. of leaf

Nodes : %d\n",countLeaf(root));

break;

case 5:

printf("Depth(Height) : %d\n",depth(root));break;

case 6:

exit(0);

default:

printf("Invalid Choice");

}

}

return 0;

}

OUTPUT:

Advance Scripting html Css.

Q1.How to repeat background image?

Input

<html >

 <head>
 
  <meta charset="UTF-8">
 <meta name="viewport" content="width=device-width, initial-scale=1.0">
 
 <title>Background Image Repeat</title>
 
 <style>
 
  body {

   background-image: url('your-image.jpg'); /* Replace with your image path */

   background-repeat: repeat;

   background-size: auto; /* Optional: use cover or contain for different effects */
 
  }
 </style>

</head>

<body>

 <h1>Repeated Background Image</h1>


 <p>This page has a background image that repeats both horizontally and

  vertically.</p>

</body>

</html>

Output.

Q2. How to set the background image will be repeated only horizontally.

Input

<html lang="en">

 <head>

  <meta charset="UTF-8">

 <meta name="viewport" content="width=device-width, initial-scale=1.0">

 <title>Background Image Repeat Horizontally</title>

 <style>

  body {

   background-image: url('your-image.jpg'); /* Replace with your image path */

   background-repeat: repeat-x; /* Repeats image only horizontally */

   background-size: auto;

  }

 </style>

</head>

<body>

 <h1>Background Image Repeating Horizontally</h1>

 <p>This page has a background image that repeats only horizontally across the

  screen.</p>

</body>

</html>

Output.

Q3. How to set different background colors of different elements.

<html lang="en">

 <head>

  <title>Background Colors Example</title>

 <style>
 /* Set background color for the entire body */

  body {

   background-color: #f0f8ff; /* Light blue */

  }
 /* Header background color */

  header {

   background-color: #4CAF50; /* Green */

   color: white;

   padding: 20px;

   text-align: center;

  }
 /* Section background color */
 section {

  background-color: #ffebcd; /* Blanched Almond */

  padding: 20px;

  margin: 10px 0;

 }
 /* Article background color */

  article {

   background-color: #ffe4e1; /* Misty Rose */

   padding: 15px;

   border-radius: 8px;

  }
 /* Footer background color */

  footer {

   background-color: #333; /* Dark Gray */

   color: white;

   text-align: center;

   padding: 10px;

  }

 </style>

</head>

<body>

 <header>

  <h1>Header with Green Background</h1>

 </header>

 <section>

  <h2>Section with Almond Background</h2>

 <p>This section has a different background color from the header and footer.</p>

 </section>

 <article>

  <h3>Article with Misty Rose Background</h3>

 <p>This article has a unique background color for emphasis.</p>

 </article>

 <footer>
 
  <p>Footer with Dark Background</p>

 </footer>

</body>

</html>

Q5. How the Background image will not be repeated.

Input

<!DOCTYPE HTML>

<html lang="en">

 <head>

  <meta charset="UTF-8">

 <meta name="viewport" content="width=device-width, initial-scale=1.0">

 <title>Background Image No Repeat</title>
 
 <style>

  body {

   background-image: url('your-image.jpg'); /* Replace with your image path */

   background-repeat: no-repeat; /* Prevents the image from repeating */

  }

 </style>

</head>

<body>

 <h1>Background Image Without Repetition</h1>

 <p>This page has a background image that does not repeat across the screen.</p>

</body>

</html>

Output.

Q6. HOW TO SET THE RIGHT MARGIN FOR A PARAGRAPH ELEMENT.

INPUT.

<html lang="en">

 <head>

  <title>Right Margin for Paragraph</title>

 <style>

  p {

   margin-right: 50px; /* Adjust the value as needed */

   background-color: #f0f0f0; /* Optional: adds background color to visualize
margin */

   padding: 10px; /* Optional: adds padding inside the paragraph */

  }

 </style>

</head>

<body>

 <p>This paragraph has a right margin of 50 pixels.</p>

</body>

</html>

Q7. How to set the maximum width of the paragraph element.

Input.

<html lang="en">

 <head>

  <title>Maximum Width for Paragraph</title>

 <style>

  p {

   max-width: 600px; /* Adjust the maximum width as needed */

   padding: 10px; /* Optional: adds padding inside the paragraph */

  }

 </style>

</head>

<body>

 <p>This paragraph has a maximum width of 600 pixels. If the screen or container is

  wider, the paragraph will not exceed this width. On smaller screens, it will adapt to fit

within the screen size.</p>

</body>

</html>

OUTPUT.

Q8. How to set the text decoration for heading elements.

Input.

<html lang="en">

 <head>

  <title>Text Decoration for Headings</title>

 <style>

  h1 {

   text-decoration: underline;
 }

  h2 {
 text-decoration: overline;
 }

  h3 {
 text-decoration: line-through;
 }

 h4, h5, h6 {
 text-decoration: none;
 }

 </style>

</head>

<body>

 <h1>This is an underlined heading</h1>

 <h2>This is a heading with an overline</h2>

 <h3>This is a heading with a line-through</h3>

 <h4>This heading has no decoration</h4>

</body>

</html>

Q9. How to set the rounded border to an element.

Input.

<html lang="en">

 <head>

  <title>Rounded Border Example</title>

 <style>

  div {

   border: 2px solid black; /* Set a solid black border */

   border-radius: 15px; /* Apply rounded corners with a radius of 15px */

   padding: 20px;

   width: 300px;

  }

 </style>

</head>

<body>

 <div>This div has a rounded border</div>

</body>

</html>

Output.

Q10. How to display different type of cursor.

Input.

<html lang="en">

 <head>

  <title>Rounded Border Example</title>

 <style>

  div {

   border: 2px solid black; /* Set a solid black border */

   border-radius: 15px; /* Apply rounded corners with a radius of 15px */

   padding: 20px;

   width: 300px;

   text-align: center;

  }

 </style>

</head>

<body>

 <div>This div has a rounded border</div>

</body>

</html>

Q11. How to set indent of the first line of all paragraphs elements.

Input

<html lang="en">

 <head>

  <title>Text Indent Example</title>

 <style>
 /* Indent the first line of all paragraphs */

  p {

   text-indent: 30px; /* Indent the first line of each paragraph by 30px */

  }

 </style>

</head>

<body>

 <p>This is the first paragraph. The first line will be indented.</p>

 <p>This is the second paragraph. It will also have the first line indented.</p>

 <p>The same will apply to any paragraph in this document.</p>

</body>

</html>

Q12.How to set the line height in percent.

Input.

<html lang="en">

 <head>
 
  <title>Line Height Example</title>
 
 <style>
 
  p {
 
   font-size: 18px; /* Set font size */
 
   line-height: 140%; /* Set line height to 140% of the font size */
 
  }
 
 </style>

</head>

<body>

 <p>This is a paragraph with the line height set to 140% of the font size.</p>
 
 <p>Adjusting the line height can improve readability by giving more space between

  lines of text.</p>

</body>

</html>

Q13. How to demonstrate the z-index in html CSS

Input.

<html lang="en">

 <head>
 
  <title>z-index Demonstration</title>
 
 <style>
 /* Set the size of the container */
 
  .container {
 
   position: relative;
 
   width: 300px;
 
   height: 300px;
 
   border: 1px solid black;
 
  }
 /* Create three overlapping elements */
 
  .box1, .box2, .box3 {
 
   position: absolute;
 
   width: 100px;
 
   height: 100px;
 
  }
 /* Style for the first box */
 
  .box1 {
 
   background-color: red;
 
   top: 50px;
 
   left: 50px;
 
   z-index: 1; /* This box will be in the back */
 
  }
 /* Style for the second box */
 
  .box2 {
 
   background-color: green;
 
   top: 80px;
 
   left: 80px;
 
   z-index: 2; /* This box will be in the middle */
 
  }
 /* Style for the third box */
 
  .box3 {
 
   background-color: blue;
 
   top: 110px;
 
   left: 110px;
 
   z-index: 3; /* This box will be in the front */
 
  }
 
 </style>

</head>

<body>

 <div class="container">
 
  <div class="box1"></div>
 
 <div class="box2"></div>
 
 <div class="box3"></div>
 
 </div>

</body>

</html>

Output.

Q14.How to rotate an element using CSS.

Input.

<html lang="en">

 <head>
 
  <title>CSS Rotation Example</title>
 
 <style>

  .rotate-box {
 
   width: 100px;
 
   height: 100px;
 
   background-color: blue;
 
   transition: transform 0.5s ease; /* Smooth transition */
 
  }
 /* Rotate on hover */
 
  .rotate-box:hover {
 
   transform: rotate(45deg); /* Rotate 45 degrees on hover */
 
  }

 </style>

</head>

<body>

 <div class="rotate-box"></div>

</body>

</html>

Q15.Demonstrate Client Side image mapping.

Input.

<html lang="en">

 <head>

  <title>Client-Side Mapping with Leaflet</title>
 <!-- Include Leaflet CSS -->
 
 <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
 
 <style>
 
  /* Set the map container size */
 
  #map {
 
   width: 100%;
 
   height: 500px;
 
  }
 
 </style>

</head>

<body>

 <h1>Client-Side Mapping Example with Leaflet.js</h1>

 <!-- The map container -->
 <div id="map"></div>
 <!-- Include Leaflet JS -->
 
 <script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>

 
 <script>
 // Initialize the map centered at a specific location (e.g., New York City)
 
  var map = L.map('map').setView([40.7128, -74.0060], 13); // Latitude, Longitude,

  Zoom level
 
  // Add OpenStreetMap tiles to the map
 
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
 
   attribution: '&copy; <a

    href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
 
  }).addTo(map);
 // Add a marker at a specific latitude and longitude
 
  var marker = L.marker([40.7128, -74.0060]).addTo(map);
 
  marker.bindPopup("<b>New York City!</b><br>This is NYC.").openPopup();
 // Add a circle around the marker
 var circle = L.circle([40.7128, -74.0060], {
 
  color: 'blue',
 
  fillColor: '#30a3e3',
 
  fillOpacity: 0.5,

 
  radius: 500

 }).addTo(map);
 
  circle.bindPopup("This is a 500-meter radius circle around the marker.");

  // Add a polygon (for example, a simple triangle)
 var polygon = L.polygon([

  [40.7118, -74.0070],

  [40.7138, -74.0080],

  [40.7158, -74.0050]

 ]).addTo(map);
  
  polygon.bindPopup("This is a triangle.");

 </script>

</body>

</html>
