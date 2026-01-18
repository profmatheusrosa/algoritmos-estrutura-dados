# Módulo 01: Projeto - Profiler de Algoritmos

## Objetivo
Criar uma ferramenta simples de "profiling" (análise de desempenho) em Python que possa medir o tempo de execução de diferentes funções e plotar ou exibir os resultados comparativos.

## Cenário
Você é um engenheiro de software e precisa provar para sua equipe que um determinado algoritmo é mais lento que outro conforme os dados crescem. Você deve criar uma classe utilitária que automatize esse teste.

## Requisitos

1.  Crie uma classe `Profiler` em Python.
2.  Ela deve ter um método `run_test(funcao, entrada)` que executa a função com a entrada fornecida e retorna o tempo gasto.
3.  Implemente duas funções para teste:
    - `soma_linear(n)`: Soma números de 0 a n usando um loop.
    - `soma_constante(n)`: Soma números usando a fórmula da soma aritmética (fórmula de Gauss).
4.  Execute ambas as funções com valores de `n` crescentes (100, 1000, 10000, 100000, 1000000).
5.  Exiba uma tabela no console comparando os tempos.

## Estrutura Sugerida

```python
import time

class Profiler:
    def __init__(self):
        pass
        
    def measure(self, func, *args):
        # Implementar medição de tempo
        pass

# Implementar funções de teste
# Rodar testes
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
