# Functions2
##ex01c

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

##ex01py
```py
a, b, c = input("Enter three values to compare\n").split()
biggest = max(a, b, c)
print (biggest)
```
##ex02c
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
##ex02py
```py
print("Inser numbers to sum, enter 0 to exit\x")
sum = 0.0
number = 1

while number != 0:
	number = float(input(""))
	sum = sum + number
  
print(sum)
```
