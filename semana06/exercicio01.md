## Exercício 1 — Pilha de chamadas
Nesse exercício, o compilador começa no `main`. A variável `resultado` recebeu uma função `soma_mult` com três parâmetros.
Em seguida, vamos para a linha da função `soma_mult`, que vai retornar `1` multiplicado por outra função, `mult`.
Agora vamos para a função `mult`, que vai retornar a multiplicação de dois parâmetros, no caso, `5` e `3`. O resultado dá `16`.
Por fim, o código segue para o `printf`, mostrando o resultado, e o código termina.

```c
#include <stdio.h>

int mult(int a, int b){
    return a * b;
}

int soma_mult(int a, int b, int c){
    return a + mult(b, c);
}

int main(void){
    int resultado = soma_mult(1, 5, 3);
    printf("%d\n", resultado);
    return 0;
}
```
