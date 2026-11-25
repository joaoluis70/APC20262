```python
maior = float('-inf')
lista = []
for i in range(5):
    num = int(input())
    lista.append(num)
    if num > maior:
        maior = num

print(maior)
print(max(lista))
```
