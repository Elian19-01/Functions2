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
x, y, z = input("Enter three values to compare\n").split()
biggest = max(x, y, z)
print (biggest)
```
