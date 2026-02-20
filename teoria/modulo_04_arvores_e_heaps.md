# Módulo 04: Árvores e Heaps

## Sumário
- [1. Introdução](#1-introdução-ao-módulo)
- [2. Árvores Binárias](#2-árvores-binárias)
- [3. Árvores Binárias de Busca (BST)](#3-árvores-binárias-de-busca-bst)
- [4. Heaps Binários](#4-heaps-binários)
- [5. Union-Find](#5-union-find)
- [6. Exercícios de Fixação](#6-exercícios-de-fixação)
- [7. Conclusão](#7-conclusão)

---

## 1. Introdução ao Módulo

Diferente das estruturas lineares que vimos antes, as **Árvores** organizam dados de forma hierárquica - como uma árvore genealógica ou a estrutura de pastas do seu computador. Elas são fundamentais para representar estruturas como sistemas de arquivos, HTML (DOM) e para algoritmos de busca e ordenação super eficientes.

---

## 2. Árvores Binárias

### Estrutura
- **Raiz (Root):** O nó superior.
- **Nó Filho (Child):** Nó conectado abaixo de outro.
- **Folha (Leaf):** Nó sem filhos.

Em uma Árvore Binária, cada nó tem no máximo **dois** filhos: Esquerda e Direita.

![Anatomia da Árvore Binária](../imagens/imagem_arvore_binaria.png)

### Travessias (Traversals)

Como percorrer todos os nós de uma árvore? Existem três formas principais, dependendo da ordem em que você visita os nós:

1.  **Pré-ordem:** Visita a raiz primeiro, depois a subárvore esquerda, depois a direita (Raiz -> Esquerda -> Direita)
2.  **In-ordem:** Visita a subárvore esquerda, depois a raiz, depois a direita (Esquerda -> Raiz -> Direita). **Dica:** Em uma BST, isso visita os nós em ordem crescente!
3.  **Pós-ordem:** Visita as subárvores primeiro, depois a raiz (Esquerda -> Direita -> Raiz)

---

## 3. Árvores Binárias de Busca (BST)

Uma BST é uma árvore binária com uma propriedade especial que torna a busca super eficiente:

- Todos os valores na subárvore à **Esquerda** são **menores** que a raiz.
- Todos os valores na subárvore à **Direita** são **maiores** que a raiz.

Por que isso é útil? Porque quando você busca um valor, você sempre sabe para qual lado ir! Se o valor que você procura é menor que a raiz, vai para a esquerda. Se é maior, vai para a direita. Isso permite busca rápida em O(log n) em média - muito melhor que O(n) de uma lista!

![Propriedade BST](../imagens/imagem_bst_propriedade.png)

---

## 4. Heaps Binários

Heaps são árvores binárias especiais usadas para implementar **Filas de Prioridade** - estruturas onde você sempre quer pegar o elemento com maior (ou menor) prioridade rapidamente.

Existem dois tipos principais:

- **Max-Heap:** O pai é sempre maior ou igual aos filhos. O maior elemento está sempre na raiz, então você pode acessá-lo em O(1)!
- **Min-Heap:** O pai é sempre menor ou igual aos filhos. O menor elemento está sempre na raiz.

**Curiosidade:** Mesmo sendo árvores conceitualmente, heaps são geralmente implementados usando **Arrays** para economizar memória (sem precisar de ponteiros). É uma forma inteligente de representar uma árvore em um array!

[IMAGEM_HEAP_ESTRUTURA]

---

## 5. Union-Find

Union-Find (também chamado de Disjoint Set) é uma estrutura de dados para gerenciar grupos separados de elementos. É muito usada em algoritmos de grafos, especialmente no algoritmo de Kruskal para encontrar árvores geradoras mínimas.

As operações principais são bem intuitivas:
- **Find:** Descobre a qual grupo um elemento pertence. "Esse elemento está no grupo A ou B?"
- **Union:** Une dois grupos em um só. "Vamos juntar o grupo A com o grupo B."

Pense nisso como gerenciar grupos de amigos: você quer saber rapidamente se duas pessoas estão no mesmo grupo, e às vezes quer juntar grupos diferentes.

---

## 6. Exercícios de Fixação

**Exercício 1:** Em uma BST balanceada contendo `n` elementos, qual a complexidade da busca?
a) O(1)

b) O(n)

c) O(log n)

d) O(n²)

<details>
<summary>Ver Resposta</summary>

**Resposta:** c) O(log n)

**Explicação:** Como a cada passo eliminamos metade da árvore (esquerda ou direita), a busca é logarítmica, similar à busca binária em um array ordenado.
</details>

**Exercício 2:** Em um Max-Heap, onde está garantidamente o **segundo** maior elemento?
a) No filho esquerdo da raiz

b) No filho direito da raiz

c) Em um dos filhos da raiz (esquerdo ou direito)

d) Na última folha

<details>
<summary>Ver Resposta</summary>

**Resposta:** c) Em um dos filhos da raiz (esquerdo ou direito)

**Explicação:** O maior elemento está na Raiz. O segundo maior deve ser obrigatoriamente um filho direto da raiz, pois se estivesse mais abaixo, violaria a propriedade de que pais são maiores que filhos.
</details>

---

## 7. Conclusão

Árvores podem parecer mais complexas que estruturas lineares, mas elas trazem muito poder! BSTs aceleram buscas de forma incrível, e Heaps são perfeitos para gerenciar prioridades. Quando você precisar de busca rápida ou de sempre pegar o elemento mais importante, pense em árvores!

[Próximo módulo →](../teoria/modulo_05_grafos_e_algoritmos_de_busca.md)

[Voltar aos Links Rápidos](../README.md#links-rapidos)
