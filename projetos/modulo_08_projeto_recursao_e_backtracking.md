# Módulo 08: Projeto - Resolvedor de Sudoku

## Objetivo
Criar um programa que resolva automaticamente um tabuleiro de Sudoku incompleto usando Backtracking.

## Cenário
Você quer impressionar seus amigos ou criar um app de "ajuda" para passatempos de jornal.

## Requisitos

1.  Crie uma classe ou função `SudokuSolver`.
2.  Represente o tabuleiro como uma matriz 9x9 (lista de listas). 0 representa vazio.
3.  Método principal: `resolver(tabuleiro)`.
    - Encontre uma célula vazia.
    - Tente colocar números de 1 a 9.
    - Verifique se é válido (não repete na linha, coluna ou bloco 3x3).
    - Se válido, chame recursivamente `resolver`.
    - Se a chamada recursiva retornar True, terminou!
    - Se não, zere a célula (backtrack) e tente o próximo número.
4.  Retorne o tabuleiro resolvido ou imprima uma mensagem se não houver solução.

## Exemplo de Tabuleiro

```python
board = [
    [5, 3, 0, 0, 7, 0, 0, 0, 0],
    [6, 0, 0, 1, 9, 5, 0, 0, 0],
    [0, 9, 8, 0, 0, 0, 0, 6, 0],
    ...
]
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
