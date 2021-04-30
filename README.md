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
}
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

## ex05c
```c
#include <stdio.h>
int main() {
    int i, a;
    unsigned long long fact = 1;
    printf("Inserte numero: ");
    scanf("%d", &i);

    // shows error if the user enters a negative integer
    if (i < 0)
        printf("numero no valido");
    else {
        for (a = 1; a <= n; ++a) {
            fact *= a;
        }
        printf("El factorial es %llu", fact);
    }

    return 0; 
}
```
## ex05py
```py
def factorial(a):
    if a == 0:
        return 1
    else:
        return a * factorial(a-1)
a=int(input("Input a number to compute the factiorial : "))
print(factorial(a))
```
## ex06c
```c
#include<stdio.h>
 
int main() {
    int num, min, max;
     
    printf("write a number\n");
    scanf("%d", &num);
    printf("Enter the numbers that define the range\n");
    scanf("%d %d", &min, &max);
     
    if((num-min)*(num-max) <= 0){
        printf("Dentro del rango");
    } else {
     printf("outside the range");
    }
 
    return 0;
    }
```
## ex06py
```py
def test_range(a):
    if a in range(13,34):
        print( " %s is in the range"(a))
    else :
        print("The number is outside the range.")
 return(0)
```
## ex07c
```c
#include <stdio.h>

int main(void)
{
    int mayus = 0, minus = 0;
    char ch[80];
    int i = 0;
    printf("\nwrite a word: \n");
    fgets(ch, sizeof(ch), stdin);
    while (ch[i] != '\0')
    {
        if (ch[i] >= 'A' && ch[i] <= 'Z')
            mayus++;
        if (ch[i] >= 'a' && ch[i] <= 'z')
            minus++;
        i++;
    }
    printf("no. of Upper: %d \n no.of lower: %d", mayus, minus);
    return 0;
}
```
## ex07py
```python
def string_test(a):
    d={"upper":0, "lower":0}
    for b in a:
        if b.isupper():
           d["upper"]+=1
        elif c.islower():
           d["lower"]+=1
        else:
           pass
    print ("Original String is  : ", a)
    print ("Upper characters : ", d["upper"])
    print ("Lower Characters : ", d["lower"])
```
## ex08c
```c
#include <stdio.h>
 
int main()
{
	int arr[10], FreqArr[10], i, j, Count, Size;
	
	printf("\n Ingrese numero de elementos a comparar: \n");
	scanf("%d", &Size);
	
	printf("Ingrese los elementos\n");
	for (i = 0; i < Size; i++)
	{
    	scanf("%d", &arr[i]);
    	FreqArr[i] = -1;
   	}     
 
	for (i = 0; i < Size; i++)
	{
		Count = 1;
		for(j = i + 1; j < Size; j++)
		{
    		if(arr[i] == arr[j])
    		{
    			Count++;
    			FreqArr[j] = 0;
    		}
    	}
    	if(FreqArr[i] != 0)
    	{
    		FreqArr[i] = Count;
		}
	}

 	printf("Lista de elementos diferentes: ");
 	for (i = 0; i < Size; i++)
  	{
  		if(FreqArr[i] == 1)
  		{
  			printf("%d\n", arr[i]);
		}		
  	}	     
 	return 0;
}
```
ex08py
```py
def unique_list(y):
  z = []
  for x in y:
    if x not in z:
      z.append(x)
  return z

print(unique_list(input(""))) 
```

	
