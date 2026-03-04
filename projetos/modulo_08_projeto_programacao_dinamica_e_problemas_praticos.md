# Módulo 07: Projeto - Otimizador de Investimentos

## Objetivo
Resolver o problema da "Mochila 0/1" aplicado a investimentos.

## Cenário
Você tem um capital fixo (ex: R$ 10.000) e uma lista de opções de investimento. Cada opção tem um custo e um retorno estimado (lucro). Você não pode investir parcialmente em uma opção (ou investe tudo ou nada). Quais opções escolher para maximizar o lucro sem estourar o orçamento?

## Requisitos

1.  Crie uma função `otimizar_investimento(capacidade, opcoes)`.
2.  `opcoes` será uma lista de dicionários/tuplas: `{"nome": "Ações X", "custo": 2000, "lucro": 500}`.
3.  Use a abordagem de Tabulação (Criar uma tabela 2D `dp[item][peso]`).
4.  Retorne o lucro máximo possível e, idealmente, quais investimentos foram escolhidos.

## Exemplo de Uso

```python
investimentos = [
    {"nome": "A", "custo": 1000, "lucro": 200},
    {"nome": "B", "custo": 3000, "lucro": 500},
    {"nome": "C", "custo": 5000, "lucro": 900}
]
capital = 6000

# Melhor combo: A + C (Custo 6000, Lucro 1100).
# A + B (Custo 4000, Lucro 700) é pior.
# B sozinha (500) é pior.
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
