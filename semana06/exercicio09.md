##Ponteiros

```c
#include <stdio.h>
#include <string.h>
#include <stdlib.h>

    int main(void) {
    int  x  = 10;
    int *p  = &x;        /* p guarda o endereço de x; tipo: int* */
    *p = 20;             /* derreferência: acessa/modifica o objeto apontado */

/* Ponteiro nulo — "não aponta para nada" */
  int *q = NULL;        /* ou: int *q = 0; */
  if (q == NULL) { }    /* sempre verificar antes de derreferênciar */

/* const e ponteiros — quatro combinações */
  const int *p1 = &x;         /* ponteiro para int constante: *p1 não pode mudar */
  int *const p2 = &x;         /* ponteiro constante para int: p2 não pode apontar para outro lugar */
  const int *const p3 = &x;   /* ambos constantes */
  int *p4 = &x;               /* nenhum constante */

/* Ponteiro void — tipo genérico */
  void *vp = &x;               /* aceita qualquer tipo */
  int  *ip = (int*)vp;         /* cast necessário para derreferênciar */
```
