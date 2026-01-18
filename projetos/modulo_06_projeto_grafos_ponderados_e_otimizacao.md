# Módulo 06: Projeto - Sistema de Navegação GPS

## Objetivo
Simular um GPS que encontra a rota mais rápida entre duas cidades, considerando distâncias (pesos).

## Cenário
Você tem um mapa de cidades conectadas por estradas, e cada estrada tem uma distância em km. O usuário quer ir da cidade A para a cidade B percorrendo a menor distância possível.

## Requisitos

1.  Crie uma classe `Mapa`.
2.  Use um grafo ponderado para representar as cidades e estradas.
3.  Implemente o algoritmo de **Dijkstra**.
4.  O método `rota_mais_curta(origem, destino)` deve retornar:
    - A distância total.
    - A lista de cidades da rota (ex: ["São Paulo", "Campinas", "Ribeirão Preto"]).
    
    *Dica: Para reconstruir a rota, você precisará armazenar de onde você veio (`parent pointer`) ao atualizar as distâncias no Dijkstra.*

## Dados Exemplo

```python
mapa = Mapa()
mapa.adicionar_estrada("A", "B", 10)
mapa.adicionar_estrada("B", "C", 15)
mapa.adicionar_estrada("A", "C", 30) # Caminho direto é mais longo que via B (10+15=25)

# rota_mais_curta("A", "C") -> (25, ["A", "B", "C"])
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
