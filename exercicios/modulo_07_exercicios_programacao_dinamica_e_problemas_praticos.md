# Módulo 07: Exercícios - Programação Dinâmica

## Exercício Prático 1: Fibonacci com Memoization

Escreva uma função `fib(n, memo={})` que calcule o n-ésimo número de Fibonacci de forma eficiente.

```python
def fib(n, memo={}):
    # Se n estiver em memo, retorne memo[n]
    # Se n <= 1, retorne n
    # Calcule, salve em memo e retorne
    pass
```

## Exercício Prático 2: Subindo Escadas (Climbing Stairs)

Você está subindo uma escada. Ela tem `n` degraus. A cada passo, você pode subir 1 ou 2 degraus.
De quantas maneiras distintas você pode chegar ao topo?

Exemplo: n=3
1. 1+1+1
2. 1+2
3. 2+1
Total: 3 maneiras.

Dica: Isso se parece muito com Fibonacci!

```python
def contar_maneiras(n):
    # Use DP (Tabela ou Memo)
    pass
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
