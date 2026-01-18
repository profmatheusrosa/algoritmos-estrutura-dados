# Cheatsheet: Algoritmos e Complexidade

Um guia rápido para relembrar complexidades e operações comuns.

## Complexidade de Tempo (Big-O)

| Estrutura de Dados | Acesso | Busca | Inserção | Remoção |
|:-------------------|:------:|:-----:|:--------:|:-------:|
| Array / Lista (Python) | O(1) | O(n) | O(n)* | O(n)* |
| Pilha (Stack) | O(n) | O(n) | O(1) | O(1) |
| Fila (Queue) | O(n) | O(n) | O(1) | O(1) |
| Lista Encadeada | O(n) | O(n) | O(1) | O(1) |
| Hash Map / Dict | N/A | O(1) | O(1) | O(1) |
| BST (Balanceada) | O(log n)| O(log n)| O(log n)| O(log n)|
| BST (Pior Caso) | O(n) | O(n) | O(n) | O(n) |

*\* Inserção no final é O(1) amortizado.*

## Algoritmos de Ordenação

| Algoritmo | Complexidade (Médio) | Complexidade (Pior) | Espaço | Estável? |
|:----------|:--------------------:|:-------------------:|:------:|:--------:|
| Bubble Sort | O(n²) | O(n²) | O(1) | Sim |
| Merge Sort | O(n log n) | O(n log n) | O(n) | Sim |
| Quick Sort | O(n log n) | O(n²) | O(log n)| Não |
| Heap Sort | O(n log n) | O(n log n) | O(1) | Não |

## Algoritmos de Grafos

- **BFS (Busca em Largura):** O(V + E). Usa Fila. Caminho mais curto (sem peso).
- **DFS (Busca em Profundidade):** O(V + E). Usa Pilha. Ciclos, Labirintos.
- **Dijkstra:** O(E log V). Caminho mais curto (com peso positivo).
- **Bellman-Ford:** O(VE). Caminho mais curto (pesos negativos).

## Fórmulas Úteis

- **Soma de 1 a N:** `n * (n + 1) / 2`
- **Profundidade Árvore Binária Cheia:** `log2(N)`
- **Número de Folhas:** `(N + 1) / 2`

[Voltar aos Links Rápidos](../README.md#links-rapidos)
