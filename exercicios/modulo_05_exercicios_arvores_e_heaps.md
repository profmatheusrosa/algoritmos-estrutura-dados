# Módulo 04: Exercícios - Árvores e Heaps

## Exercício Prático 1: Validar BST

Escreva uma função `eh_bst(raiz)` que recebe a raiz de uma árvore binária e retorna `True` se ela for uma Árvore Binária de Busca válida, e `False` caso contrário.

**Dica:** Lembre-se que TODOS os nós à esquerda devem ser menores, não apenas o filho imediato. Pode ser útil passar limites (min, max) recursivamente.

```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right

def eh_bst(raiz):
    # Implemente aqui
    pass
```

## Exercício Prático 2: K-ésimo Maior Elemento

Dado um array de inteiros (não ordenado) e um número `k`, encontre o k-ésimo maior elemento.
**Desafio:** Tente usar um **Min-Heap** de tamanho `k` para resolver isso em O(n log k).

Use `heapq` do Python.

```python
import heapq

def k_esimo_maior(nums, k):
    pass
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
