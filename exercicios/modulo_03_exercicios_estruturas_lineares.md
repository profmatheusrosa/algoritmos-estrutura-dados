# Módulo 02: Exercícios - Estruturas Lineares

## Exercício Prático 1: Verificador de Palíndromos com Pilha

Um palíndromo é uma palavra ou frase que se lê da mesma forma de trás para frente (desconsiderando espaços e pontuação).
Escreva uma função `is_palindrome(string)` que use uma **Pilha** para verificar se a string é um palíndromo.

**Exemplo:**
`is_palindrome("arara")` -> True
`is_palindrome("python")` -> False

**Dica:** Empilhe metade da string e compare desempilhando.

---

## Exercício Prático 2: Fila de Atendimento com Prioridade (Simples)

Implemente uma classe `FilaBanco`. Ela deve ter dois métodos:
- `entrar(nome, prioridade)`: Adiciona uma pessoa. Se prioridade for `True`, ela vai para o início da fila? Não, na verdade, tente implementar **duas filas internas**: uma para prioritários e uma para comuns.
- `proximo()`: Retorna o próximo a ser atendido (prioritários primeiro).

```python
class FilaBanco:
    def __init__(self):
        # Inicialize suas estruturas aqui
        pass

    def entrar(self, nome, prioritaria=False):
        pass

    def proximo(self):
        pass
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
