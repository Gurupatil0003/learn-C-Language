```c
#include <stdio.h>

int main(){

    int qty;
    double price,subtotal,gst,total;

    scanf("%d %lf",&qty,&price);

    subtotal=qty*price;
    gst=subtotal*0.18;
    total=subtotal+gst;

    printf("SUBTOTAL: %.2f\n", subtotal);
    printf("GST@18%%: %.2f\n", gst);
    printf("TOTAL   : %.2f\n", total);

    return 0;

}

```

```c
#include <stdio.h>

int main(){
    int p,q;

    scanf("%d %d",&p, &q);

    int a=p && q;
    int or=p||q;
    int xo=p^q;
    int not=!p;

    printf("AND: %d\n",a);
    printf("OR : %d\n",or);
    printf("XOR: %d\n",xo);
    printf("NOT: %d\n",not);

    return 0;
}


```

```c
#include <stdio.h>

int main() {
    int S, add, sub, mul, divv, modd;
    
    // Read input
    scanf("%d %d %d %d %d %d", &S, &add, &sub, &mul, &divv, &modd);
    
    // Display initial score
    printf("START: %d\n", S);
    
    // Apply operations in sequence
    S += add;
    printf("ADD  : %d\n", S);
    
    S -= sub;
    printf("SUB  : %d\n", S);
    
    S *= mul;
    printf("MUL  : %d\n", S);
    
    S /= divv;  // integer division
    printf("DIV  : %d\n", S);
    
    S %= modd;
    printf("MOD  : %d\n", S);
    
    return 0;
}


```


```c
#include <stdio.h>

int main() {
    int x, y;

    // Read inputs
    scanf("%d %d", &x, &y);

    // Perform and print relational comparisons
    printf("LT : %d\n", x < y);
    printf("LE : %d\n", x <= y);
    printf("EQ : %d\n", x == y);
    printf("NE : %d\n", x != y);
    printf("GE : %d\n", x >= y);
    printf("GT : %d\n", x > y);

    return 0;
}


```

```c
#include <stdio.h>

int main() {
    int a;
    if (scanf("%d", &a) != 1) return 0;

    printf("INIT : %d\n", a);
    printf("PRE++: %d\n", ++a);
    printf("POST++: %d\n", a++);
    printf("PRE--: %d\n", --a);
    printf("POST--: %d\n", a--);
    printf("FINAL: %d\n", a);

    return 0;
}


```
