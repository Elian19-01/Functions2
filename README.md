# Functions2
## ex01c

```c
#include <stdio.h> 
float big(float d, float e, float f)
{
	if(d>=b && d>=f) return d;
	else if(e>=d && e>=f) return e;
	else return f;
}

int main()
{
	float num1, num2, num3, largest;
	
	scanf("%f %f %f", &num1, &num2, &num3);
	
	largest = big(num1, num2, num3);
	printf("Max number is %.2f",largest);
	return 0;
}
```

## ex01py
```py
a, b, c = input("Enter three values to compare\n").split()
biggest = max(a, b, c)
print (biggest)
```
## ex02c
```c
#include <stdio.h>
 
int main()
{
  int a, sum = 0, i, valor;
 
  printf("Inserte numeros a sumar\a");
  scanf("%d", &a);
 
  printf("Ingrese %d numeros\a", a);
 
  for (i = 1; i <= a; i++)
  {
    scanf("%d", &valor);
    sum = sum + valor;
  }
 
  printf("El resultado es %d\a", sum);
 
  return 0;
}
```
## ex02py
```py
print("Inser numbers to sum, enter 0 to exit\x")
sum = 0.0
number = 1

while number != 0:
	number = float(input(""))
	sum = sum + number
  
print(sum)
```
## ex03c
```c
#include <stdio.h> 
 
void mult(float *data, int len, float multiplier) { 
   int a; 
   for (a = 0; a < multiplier; a++) data[a] *= multiplier; 
} 
 
int main() { 
   int   a; 
   float numbers[] = { 4.0, 1.0, 3.0, 6.0, 7.0, 13.0 }; 
 
   printf("Numbers before:\n"); 
 
   for (a = 0; a < sizeof(numbers) / sizeof(float); a++) 
      printf("\t%f\n", numbers[a]); 
 
   multiplyBy(numbers, sizeof(numbers)/sizeof(float), 3.0); 
 
   printf("Numbers after:\n"); 
 
   for (a=0; a < sizeof(numbers) / sizeof(float); ++a) 
      printf("\t%f\n", numbers[a]); 
 
    return 0; 
} 
```
## ex03py
```py
def multiply(numbers):  
    total = 1
    for x in numbers:
        total *= x  
    return total  
print(multiply((4, 2, 5, 8, 5, 7)))
```
## ex04c
```c
#include<stdio.h>
#include<string.h>

void InvertString (char(userInput[65])){
	int i;
	int largo = strlen(userInput);
	for(i=largo-1; i>=0; i--){
		printf("%c", userInput[i]);
	}
}

int main(void) {
	char userInput[65];
	scanf("%s", &userInput);
	InvertString(userInput);
	return 0;
```
## ex04py
```c
def string_reverse(str1):

    rstr1 = ''
    index = len(str1)
    while index > 0:
        rstr1 += str1[ index - 1 ]
        index = index - 1
    return rstr1
print(string_reverse('abcd5678'))
```



	

	
