# Módulo 01: Exercícios - Introdução e Complexidade

Este arquivo contém exercícios práticos para fixar os conceitos de complexidade de tempo e espaço.

---

## Exercício Prático 1: Análise de Algoritmos

Dado os seguintes trechos de código em Python, determine a complexidade Big-O de cada função e justifique sua resposta nos comentários.

### Código A
```python
def contagem_regressiva(n):
    while n > 0:
        print(n)
        n -= 1
```

### Código B
```python
def soma_matriz(matriz):
    soma = 0
    linhas = len(matriz)
    colunas = len(matriz[0])
    for i in range(linhas):
        for j in range(colunas):
            soma += matriz[i][j]
    return soma
```

### Código C
```python
def potencia_de_dois(n):
    if n == 0:
        return 0
    k = 1
    while k < n:
        k = k * 2
        print(k)
```

---

## Exercício Prático 2: Comparação de Desempenho

Escreva um script Python que compare o tempo de execução de duas abordagens para verificar se um número existe em uma lista:
1.  Busca linear (usando `in` operator em uma lista).
2.  Busca rápida (usando `in` operator em um `set`).

**Dica:** Use o módulo `time` ou `timeit` para medir o tempo com uma entrada grande (ex: 1.000.000 elementos).

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
