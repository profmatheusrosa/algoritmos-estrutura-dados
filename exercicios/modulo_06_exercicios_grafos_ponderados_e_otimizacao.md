# Módulo 06: Exercícios - Grafos Ponderados

## Exercício Prático 1: Dijkstra Manual

Dado o grafo abaixo (descrito em lista de adjacência com pesos), execute manualmente o algoritmo de Dijkstra partindo de 'A' e determine a distância mínima para 'D'.

```python
grafo = {
    'A': {'B': 1, 'C': 4},
    'B': {'C': 2, 'D': 5},
    'C': {'D': 1},
    'D': {}
}
```
**Passos:**
1. Distâncias iniciais: A=0, B=Inf, C=Inf, D=Inf.
2. ... (continue o raciocínio)

## Exercício Prático 2: Kruskal com Union-Find

Se você implementou o Union-Find no Módulo 4, use-o para implementar o algoritmo de Kruskal.
Entrada: Lista de arestas `(peso, u, v)`.
Saída: Lista de arestas da MST.

```python
def kruskal(vertices, arestas):
    # arestas é uma lista de tuplas (peso, u, v)
    arestas.sort() # Ordenar por peso
    # ...
    pass
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
