# Projeto Módulo 02: Motor de Catálogo E-commerce

Neste projeto de consolidação, você construirá o motor de ordenação e busca por baixo do catálogo de um e-commerce simplificado. Este é um cenário real enfrentado por engenheiros backend diariamente ao lidar com devolução e organização de recursos manipulados na memória antes de despachá-los para um frontend.

## O Cenário

Seu e-commerce precisa ser capaz de:
1. Buscar rapidamente os detalhes de um produto dado o seu ID.
2. Fornecer ao usuário funcionalidades de ordenação dos produtos dependendo do filtro selecionado na interface web.

## Requisitos do Projeto

Para simular o banco de dados, você criará e consumirá uma lista (array) de dicionários em Python simulando os produtos. Exemplo:

```python
catalogo = [
    {"id": 102, "nome": "SmartphoneX", "preco": 2999.00, "vendas": 500},
    {"id": 54,  "nome": "Fone Bluetooth", "preco": 150.00, "vendas": 1200},
    {"id": 87,  "nome": "Notebook Pro", "preco": 7500.00, "vendas": 30},
    # adicione mais dezenas de itens com IDs variados...
]
```

### Tarefa 1: Busca do Catálogo
* Para a busca ser eficiente, uma exigência técnica do projeto é que sua estrutura de catálogo seja **mantida sempre ordenada ordenado pelo `id` do produto na memória** primária.
* Implemente uma **Busca Binária** encapsulada em uma função `buscar_produto(id)`. A função deve lidar debaixo dos panos com o fato do array estar preenchido de dicionários, e retornar o dicionário correspondente ao ID procurado (ou aviso visual caso não encontre).

### Tarefa 2: Múltiplas Visões de Ordenação
O usuário aplicou filtros na UI do e-commerce. Implemente funções distintas (ou uma mesma função parametrizada) que seja capaz de devolver uma cópia visual da lista ordenada pelos seguintes critérios:
- Filtro 1: **"Menor Preço"** (Crescente no campo `preco`)
- Filtro 2: **"Maior Preço"** (Decrescente no campo `preco`)
- Filtro 3: **"Mais Vendidos"** (Decrescente no campo `vendas`)
- Filtro 4: **"Alfabética (A-Z)"** (Crescente no campo `nome`)

Você pode escolher qualquer um dos classificadores abordados na aula `O(n²)` se sua base de testes for pequena, mas tente utilizar métodos de ordenação eficientes na prática.

### Desafios Extras Pós-Conclusão
1. Consegue implementar as ordenações usando puramente um *Insertion Sort* ligeiramente modificado para aceitar o campo e tipo de ordenação como chave?
2. Em um E-commerce real teríamos milhares de produtos. Como você modificaria sua função de ordenação visual para implementar uma **Paginação de Resultados**, retornando apenas os "10 primeiros elementos" ordenados em vez de ordenar tudo e enviar a lista inteira?

---
[Voltar aos Links Rápidos](../README.md#links-rapidos)
