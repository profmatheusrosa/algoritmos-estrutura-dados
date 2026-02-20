# Módulo 02: Estruturas Lineares

## Sumário
- [1. Introdução](#1-introdução-ao-módulo)
- [2. Listas e Arrays](#2-listas-e-arrays)
- [3. Pilhas (Stacks)](#3-pilhas-stacks)
- [4. Filas (Queues)](#4-filas-queues)
- [5. Exercícios de Fixação](#5-exercícios-de-fixação)
- [6. Conclusão](#6-conclusão)

---

## 1. Introdução ao Módulo

Neste módulo, vamos explorar as estruturas de dados lineares - aquelas onde os elementos são organizados um após o outro, em sequência. Pense nelas como uma fila de pessoas ou uma pilha de livros. Elas são a base para estruturas mais complexas que vamos ver depois e são fundamentais para manipular dados na memória de forma eficiente.

---

## 2. Listas e Arrays

### Conceitos

Vamos entender dois conceitos importantes:

- **Array:** É uma coleção de elementos que ficam guardados um do lado do outro na memória. Pode ter tamanho fixo (em linguagens como C) ou dinâmico (como em Python). A grande vantagem é que você consegue acessar qualquer elemento rapidamente - O(1) - porque você sabe exatamente onde ele está na memória.

- **Lista Encadeada:** É como uma corrente de elos. Cada elemento (nó) sabe onde está o próximo, mas eles não precisam ficar lado a lado na memória. Isso permite inserir e remover elementos facilmente - O(1) se você já souber onde está -, mas para encontrar um elemento específico, você precisa percorrer a lista inteira - O(n).

**Em Python**, a estrutura `list` que você usa todo dia é implementada como um **Array Dinâmico** por baixo dos panos. Isso significa que ela tem acesso rápido, mas algumas operações podem ser mais lentas do que você imagina!

```python
# Exemplo de Lista em Python
frutas = ["Maçã", "Banana", "Laranja"]

# Acesso O(1)
print(frutas[0]) 

# Inserção no final O(1) (amortizado)
frutas.append("Uva")

# Inserção no meio O(n) (precisa deslocar elementos)
frutas.insert(1, "Morango")
```

![Array vs Linked List](../imagens/imagem_array_vs_linkedlist.png)

---

## 3. Pilhas (Stacks)

### O que são Pilhas?

Pilhas seguem a regra LIFO (Last-In, First-Out), que significa "o último a entrar é o primeiro a sair". A melhor analogia é uma pilha de pratos: você só pode pegar o prato de cima, e quando coloca um novo prato, ele vai para o topo.

### Operações Básicas
- **Push:** Adicionar ao topo.
- **Pop:** Remover do topo.
- **Peek:** Olhar o topo sem remover.

### Implementação em Python

A boa notícia é que podemos usar a própria `list` do Python para implementar uma pilha! É bem simples:

```python
pilha = []
pilha.append(10) # Push
pilha.append(20)
topo = pilha.pop() # Pop (retorna 20)
```

[IMAGEM_CONCEITO_PILHA]

---

## 4. Filas (Queues)

### O que são Filas?

Filas seguem a regra FIFO (First In, First Out), que significa "o primeiro a entrar é o primeiro a sair". É exatamente como uma fila de banco ou supermercado: quem chega primeiro é atendido primeiro.

### Operações Básicas
- **Enqueue:** Adicionar ao final.
- **Dequeue:** Remover do início.

### Implementação em Python

Aqui está um ponto importante: usar uma `list` comum para filas é **ineficiente** quando você precisa remover do início (dequeue), porque isso tem complexidade O(n) - todos os elementos precisam ser deslocados! 

A solução é usar `collections.deque` (double-ended queue), que permite adicionar e remover dos dois lados em O(1):

```python
from collections import deque

fila = deque()
fila.append("Cliente A") # Enqueue
fila.append("Cliente B")
proximo = fila.popleft() # Dequeue ("Cliente A") - O(1)
```

[IMAGEM_CONCEITO_FILA]

---

## 5. Exercícios de Fixação

**Exercício 1:** Qual estrutura de dados é mais adequada para implementar a funcionalidade "Desfazer" (Undo) de um editor de texto?
a) Fila (Queue)

b) Array

c) Pilha (Stack)

d) Árvore Binária

<details>
<summary>Ver Resposta</summary>

**Resposta:** c) Pilha (Stack)

**Explicação:** A ação de desfazer reverte a operação mais recente. Isso segue a lógica LIFO (Last In, First Out), perfeitamente modelada por uma Pilha.
</details>

**Exercício 2:** Qual a complexidade de tempo para remover o **primeiro** elemento de uma lista padrão do Python (`list.pop(0)`)?
a) O(1)

b) O(log n)

c) O(n)

d) O(n²)

<details>
<summary>Ver Resposta</summary>

**Resposta:** c) O(n)

**Explicação:** Como as listas em Python são arrays dinâmicos, remover o primeiro elemento exige que todos os elementos subsequentes sejam deslocados uma posição para a esquerda na memória para preencher o vazio.
</details>

---

## 6. Conclusão

Arrays, Pilhas e Filas são ferramentas essenciais que você vai usar constantemente na programação. Saber quando usar `deque` em vez de `list`, ou quando uma Pilha resolve seu problema de "histórico" (como o botão de desfazer), é o que diferencia programadores iniciantes de avançados. 

Lembre-se: escolher a estrutura certa pode fazer seu código ficar muito mais rápido e eficiente!

[Próximo módulo →](../teoria/modulo_03_hashmaps_e_sets.md)

[Voltar aos Links Rápidos](../README.md#links-rapidos)
