# Módulo 03: Exercícios - HashMaps e Sets

Antes de começar, só uma curiosidade rápida: em alguns lugares você vai ver **set = conjunto** e **map = mapa/dicionário**. É a mesma ideia, só muda o “apelido” dependendo da linguagem.

## Exercício Prático 1: Encontrar Duplicatas

Escreva uma função `encontrar_duplicados(lista)` que recebe uma lista de números e retorna uma lista contendo apenas os números que aparecem mais de uma vez.

**Restrição:** Tente fazer isso em O(n) de tempo usando um conjunto (`set`) ou dicionário.

**Dica:** Você pode usar um dicionário para contar quantas vezes cada número aparece, ou usar um set para rastrear quais números você já viu.

```python
def encontrar_duplicados(lista):
    pass

# Teste: [1, 2, 3, 2, 4, 5, 5] -> [2, 5]
```

---

## Exercício Prático 2: Soma de Dois (Two Sum)

Dado um array de inteiros `nums` e um inteiro `alvo`, retorne os **índices** dos dois números que somados resultam no `alvo`.

Você pode assumir que cada entrada terá exatamente uma solução e não pode usar o mesmo elemento duas vezes.

**Exemplo:**
```python
nums = [2, 7, 11, 15]
alvo = 9
# Saída: [0, 1] (pois nums[0] + nums[1] == 9)
```

**Dica:** Use um dicionário para armazenar os números que você já viu e seus índices enquanto percorre a lista. Para cada número atual, verifique se o complemento (`alvo - atual`) já existe no dicionário. Isso permite fazer a verificação em O(1) em vez de O(n).

```python
def two_sum(nums, alvo):
    pass
```

---

## Exercício Prático 3: Verificar Anagramas

Duas palavras são anagramas se uma pode ser formada reorganizando as letras da outra. Por exemplo, "listen" e "silent" são anagramas.

Escreva uma função `sao_anagramas(palavra1, palavra2)` que retorna `True` se as duas palavras são anagramas, e `False` caso contrário.

**Dica:** Use um dicionário para contar a frequência de cada letra em ambas as palavras e compare os dicionários.

```python
def sao_anagramas(palavra1, palavra2):
    pass

# Teste: sao_anagramas("listen", "silent") -> True
# Teste: sao_anagramas("hello", "world") -> False
```

---

## Exercício Prático 4: Elementos Únicos

Dada uma lista que pode conter elementos duplicados, retorne uma nova lista contendo apenas os elementos únicos, mantendo a ordem de primeira aparição.

**Exemplo:**
```python
lista = [1, 2, 2, 3, 4, 4, 5]
# Saída: [1, 2, 3, 4, 5]
```

**Dica:** Use um set para rastrear quais elementos você já viu, mas mantenha uma lista para preservar a ordem.

```python
def elementos_unicos(lista):
    pass
```

---

## Exercício Prático 5: Interseção de Conjuntos

Dadas duas listas, encontre todos os elementos que aparecem em ambas (a interseção).

**Exemplo:**
```python
lista1 = [1, 2, 3, 4, 5]
lista2 = [4, 5, 6, 7, 8]
# Saída: [4, 5]
```

**Dica:** Converta as listas em sets e use a operação de interseção (`&`).

```python
def intersecao(lista1, lista2):
    pass
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
