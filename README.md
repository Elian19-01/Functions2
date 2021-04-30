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
#include <string.h>

int usarr[] = {92, 237, 2311, 18340};
int len = sizeof(usarr) / sizeof(usarr[0]);

int addition(int usarr[], int len)
{
    int sumno = 0;
 
    for (int i = 0; i < len; i++)
    {sumno += usarr[i];}
 
    return sumno;
}
 
int main()
{
    printf("Sum of the list is %d", addition(usarr, len));
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
def inrange(user, lownum, maxnum):
    if user in range(lownum, maxnum):
        print( " %s is in the range"%str(user))
    else :
        print("The number is outside the given range.")

lownum = int(input("Write a number for the lower number of the range: "))
maxnum = int(input("Write a number for the max number of the range: "))
user = int(input("Write a number and lets see if it is in a range: "))

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
## ex08py
```py
def unique_list(y):
  z = []
  for x in y:
    if x not in z:
      z.append(x)
  return z

print(unique_list(input(""))) 
```
## ex09c
```c
#include <stdio.h>
#include <stdlib.h>
int main()
{
    int number=0;
    int dividers=0;
    int prime=0; 
    do
    {
        scanf(" %d",&number);
        if(number!=-1 && number>0)
        {
            prime=0;
            dividers=2;
            while(dividers<number  && prime!=1)
            {
                if(numero%dividers==0) prime=1;
                dividers++;
            }
            if (prime==0)
            {
                printf("It is prime");
            }
            else
            {
                printf("It is not primo");
            }
        }
    } while(numero!=-1);
    return 0;
}
```
## ex09py
```py
def prime-test(a):
    if (a==1):
        return False
    elif (a==2):
        return True;
             for s in range(2,a):
            if(a % s==0):
                return False
        return True            
print(prime-test(3))
```
## ex10c
```c
#include<stdio.h>

int no, arr[20];

void evennumbers()
{
  printf("Enter the size of the array: ");
  scanf("%d", &no);

  printf("Write array numbers: \n");
  for(int i = 0; i < no; i++)
   {
      scanf("%d",&arr[i]);
   }

  printf("Even numbers in the array are: \n");
  for(int i = 0; i < no; i++)
   {
    if(arr[i] % 2 == 0)
    printf("%d ", arr[i]);
   }
}

int main()
{
  evennumbers();
  return 0;
}
```
## ex10py
```py
def evennums(user):
    no = []
    for a in user:
        if a % 2 == 0:
            no.append(a)
    return no

print(evennums([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 432, 234234, 234243234, 24, 43553, 21, 41,]))
```
## ex11c
```c
# include <stdio.h>   

int main()   
{   
 int i, Number, Sum = 0 ;   
  
 printf("\n Please Enter any number \n") ;   
 scanf("%d", &Number) ;   
 
 for(i = 1 ; i < Number ; i++)   
  {   
   if(Number % i == 0)   
     Sum = Sum + i ;   
  }    

 if (Sum == Number)   
    printf("\n %d is a Perfect Number", Number) ;   
 else   
    printf("\n%d is not the Perfect Number", Number) ;   

return 0 ;   
}
```
## ex11py
```py
def perfect_number(s):
    sum = 0
    for i in range(1, s):
        if s % i == 0:
            sum += i
    return sum == s
print(perfect_number(int(input())))

```

## ex12c
```c
#include<stdio.h>
#include<string.h>

int length, pos1, pos2;
char user[20];

void palindrome()
{
  printf("Write a word and lets see if its a palindrome: ");
  scanf("%s", user);
  length = strlen(user);

  pos1 = 0;
  pos2 = length - 1;
  while (pos2 > pos1)
  {
    if (user[pos1] != user[pos2])
    {
      printf("0");
    }
    else if (user[pos1] == user[pos2])
    {
      printf("1");
    }
    pos1 += 1;
    pos2 -= 1;
  } 
}
```
## ex12py
```py
def palindrome(user):
	pos1 = 0
	pos2 = len(user) - 1	
	while pos2 >= pos1:
		if not user[pos1] == user[pos2]:
			return False
		pos1 += 1
		pos2 -= 1
	return True

user = input("Write a word and lets see if its a palindrome: ")
print(palindrome(user))
```
