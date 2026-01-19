# Módulo 03: Exercícios - HashMaps e Dicionários

## Exercício Prático 1: Encontrar Duplicatas

Escreva uma função `encontrar_duplicados(lista)` que recebe uma lista de números e retorna uma lista contendo apenas os números que aparecem mais de uma vez.
**Restrição:** Tente fazer isso em O(n) de tempo usando um conjunto (`set`) ou dicionário.

```python
def encontrar_duplicados(lista):
    pass

# Teste: [1, 2, 3, 2, 4, 5, 5] -> [2, 5]
```

## Exercício Prático 2: Soma de Dois (Two Sum)

Dado um array de inteiros `nums` e um inteiro `alvo`, retorne os **índices** dos dois números que somados resultam no `alvo`.
Você pode assumir que cada entrada terá exatamente uma solução.

**Exemplo:**
`nums = [2, 7, 11, 15]`, `alvo = 9`
Saída: `[0, 1]` (pois nums[0] + nums[1] == 9)

**Dica:** Use um dicionário para armazenar os números que você já viu e seus índices enquanto percorre a lista. Isso permite verificar se o complemento (`alvo - atual`) já existe em O(1).

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
