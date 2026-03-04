# Módulo 05: Exercícios - Grafos e Algoritmos de Busca

## Exercício Prático 1: Implementar Grafos

Crie uma classe `Grafo` que use **Lista de Adjacência** (dicionário de listas em Python).
Métodos:
- `adicionar_vertice(v)`
- `adicionar_aresta(u, v)` (lembre-se se é direcionado ou não)
- `imprimir_grafo()`

```python
class Grafo:
    def __init__(self, direcionado=False):
        self.adj = {}
        self.direcionado = direcionado

    # Implemente os métodos
```

## Exercício Prático 2: Tem Caminho? (BFS/DFS)

Adicione um método `tem_caminho(origem, destino)` à sua classe. Ele deve retornar `True` se for possível chegar ao destino a partir da origem, e `False` caso contrário.
Tente usar BFS ou DFS.

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
