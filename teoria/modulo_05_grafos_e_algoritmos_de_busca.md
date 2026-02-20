# Módulo 05: Grafos e Algoritmos de Busca

## Sumário
- [1. Introdução](#1-introdução-ao-módulo)
- [2. Conceitos de Grafos](#2-conceitos-de-grafos)
- [3. Representação de Grafos](#3-representação-de-grafos)
- [4. Algoritmos de Busca](#4-algoritmos-de-busca)
- [5. Exercícios de Fixação](#5-exercícios-de-fixação)
- [6. Conclusão](#6-conclusão)

---

## 1. Introdução ao Módulo

Grafos são provavelmente a estrutura mais versátil da computação! Eles modelam praticamente tudo: redes sociais (pessoas conectadas a pessoas), mapas (cidades conectadas por estradas), conexões de internet, dependências de pacotes e muito mais. 

A regra é simples: se você tem "coisas" conectadas a outras "coisas", você tem um grafo. É uma forma poderosa de representar relacionamentos e conexões.

---

## 2. Conceitos de Grafos

### Terminologia Básica

Vamos entender os termos principais:

- **Vértice (Vertex/Node):** É o ponto ou objeto no grafo. Pode ser uma pessoa, uma cidade, uma página web - qualquer coisa que você queira representar.

- **Aresta (Edge):** É a conexão entre dois vértices. Pode ser uma amizade, uma estrada, um link, etc.

- **Direcionado vs Não Direcionado:**
  - **Direcionado (Digraph):** As arestas têm sentido, como uma seta (A -> B). Exemplo: seguir alguém no Twitter - você segue eles, mas eles não necessariamente te seguem de volta.
  - **Não Direcionado:** A conexão é mútua (A - B). Exemplo: amizade no Facebook - se você é amigo de alguém, vocês são amigos mutuamente.

[IMAGEM_GRAFO_CONCEITO]

---

## 3. Representação de Grafos

Como guardar um grafo na memória do computador? Existem duas formas principais, cada uma com suas vantagens:

### Lista de Adjacência

Cada vértice tem uma lista dos vértices aos quais está conectado. É como ter uma agenda onde cada pessoa tem uma lista de seus amigos.

**Vantagem:** Usa menos memória para grafos esparsos (aqueles com poucas conexões). É a representação mais comum e eficiente na maioria dos casos.
```python
grafo = {
    'A': ['B', 'C'],
    'B': ['D'],
    'C': [],
    'D': ['A']
}
```

### Matriz de Adjacência

É uma grade NxN (onde N é o número de vértices) onde 1 indica que há uma conexão e 0 indica que não há conexão. É como uma tabela onde você marca quais pessoas se conhecem.

**Vantagem:** Super rápido para verificar se A está conectado a B - apenas O(1)!

**Desvantagem:** Gasta muita memória - O(V²). Se você tem 1000 vértices, precisa de 1 milhão de células na matriz, mesmo que só tenha 100 conexões!

![Representação de Grafo](../imagens/imagem_grafo_representacao.png)

---

## 4. Algoritmos de Busca

### BFS (Breadth-First Search) - Busca em Largura

BFS explora o grafo nível por nível, como uma onda se espalhando na água. Primeiro visita todos os vizinhos diretos, depois os vizinhos dos vizinhos, e assim por diante.

**Quando usar:** 
- Encontrar o caminho mais curto em grafos não ponderados (onde você quer o menor número de arestas, não o menor peso)
- Verificar se dois pontos estão conectados
- Encontrar todos os nós a uma certa distância

**Estrutura usada:** Uma **Fila** (FIFO) - os primeiros descobertos são os primeiros explorados.

### DFS (Depth-First Search) - Busca em Profundidade

DFS explora o mais fundo possível em um ramo antes de voltar (backtrack). É como explorar um labirinto: você vai até o fim de um corredor antes de tentar outro.

**Quando usar:**
- Detectar ciclos no grafo
- Verificar conectividade
- Resolver labirintos
- Encontrar caminhos (não necessariamente o mais curto)

**Estrutura usada:** Uma **Pilha** (LIFO) ou simplesmente recursão - os últimos descobertos são os primeiros explorados.

![BFS vs DFS](../imagens/imagem_bfs_vs_dfs.png)

---

## 5. Exercícios de Fixação

**Exercício 1:** Qual algoritmo é garantido para encontrar o caminho com o menor número de arestas entre dois nós em um grafo não ponderado?
a) DFS

b) BFS

c) Busca Binária

d) Ordenação Topológica

<details>
<summary>Ver Resposta</summary>

**Resposta:** b) BFS

**Explicação:** O BFS explora o grafo em "camadas". Ele visita todos os vizinhos a uma distância 1, depois todos a distância 2, e assim por diante. Portanto, assim que encontra o alvo, garante-se que é o caminho mais curto em arestas.
</details>

**Exercício 2:** Em um grafo representando uma Rede Social onde as arestas são amizades, o que representa um vértice com muitas arestas (alto grau)?
a) Uma pessoa antissocial

b) Uma pessoa popular / influenciador

c) Um erro no banco de dados

d) Um ciclo infinito

<details>
<summary>Ver Resposta</summary>

**Resposta:** b) Uma pessoa popular / influenciador

**Explicação:** O "grau" de um vértice é o número de conexões que ele possui. Muitos amigos = alto grau.
</details>

---

## 6. Conclusão

Dominar BFS e DFS é essencial! Quase todos os problemas avançados de grafos (Dijkstra, Prim, etc.) são variações ou especializações dessas duas buscas fundamentais. Se você entender bem essas duas, vai conseguir resolver a maioria dos problemas de grafos que encontrar por aí.

[Próximo módulo →](../teoria/modulo_06_grafos_ponderados_e_otimizacao.md)

[Voltar aos Links Rápidos](../README.md#links-rapidos)
