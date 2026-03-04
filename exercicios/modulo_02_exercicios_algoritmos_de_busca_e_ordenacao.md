# Exercícios: Módulo 02 - Algoritmos de Busca e Ordenação

Neste módulo, focamos na prática de localizar e ordenar dados. Os exercícios a seguir exigem que você aplique os conceitos vistos na teoria através de implementações clássicas e problemas aplicados.

## Exercício 1: Busca Binária

Implemente a busca binária em Python (construa tanto a versão iterativa quanto a recursiva). Teste com o array `[10, 20, 30, 40, 50, 60, 70, 80]` buscando os números `20` e `90`.

## Exercício 2: First Bad Version

(Problema clássico). Você tem `n` versões de um software `[1, 2, ..., n]` e quer descobrir a primeira versão ruim, pois todas as versões seguintes a uma versão ruim também serão ruins.

Você tem à disposição uma função (API simulada) `isBadVersion(version)` que retorna um booleano `True` ou `False`.
Implemente uma solução inteligente com complexidade **O(log n)** para encontrar o primeiro *True*, minimizando o número de chamadas à API.

```python
# API mock para testes
def isBadVersion(version):
    return version >= 4  # Supondo que a versão 4 foi a primeira ruim

# Implemente sua função abaixo
def firstBadVersion(n):
    pass
```

## Exercício 3: Insertion Sort na Prática

Implemente o algoritmo Insertion Sort.
Em seguida, modifique sua implementação original para que a função **retorne um número inteiro** representando quantas "trocas/deslocamentos" (swaps/shifts) de fato ocorreram durante o processo de ordenação do array providenciado.

## Exercício 4: Comparativo de Pior Caso (Desafio Prático)

Crie um pequeno script para medir tempo de execução na prática usando a biblioteca `time` do Python.

1. Construa um array de tamanho `10.000` invertido (de `10000` caindo até `1`).
2. Meça e imprima o tempo de execução exato do seu **Bubble Sort**.
3. Meça e imprima o tempo de execução exato do seu **Selection Sort**.

*(Cuidado: se você testar com tamanhos muito maiores que 10 mil em O(n²), seu computador pode demorar minutos para finalizar).*

## Exercício 5: Merge O(n) (Introdução ao Dividir e Conquistar)

Construir completamente o Merge Sort pode ser complexo, mas sua engrenagem principal é a etapa do `merge`.
Dados dois arrays numéricos já previamente ordenados `A` e `B`, escreva uma função `merge_arrays(A, B)` que retorne um novo array ordenado contendo a junção de todos os elementos.

**Restrição obrigatória:** Seu loop deve ser capaz de fazer a junção em O(n), iterando por ambos os arrays simultaneamente usando ponteiros, sem utilizar funções embutidas de sort num array concatenado como `(A + B).sort()`.

---
[Voltar aos Links Rápidos](../README.md#links-rapidos)
