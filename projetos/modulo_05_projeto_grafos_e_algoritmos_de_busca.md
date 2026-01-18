# Módulo 05: Projeto - Recomendação de Amigos em Rede Social

## Objetivo
Simular uma pequena rede social e usar algoritmos de grafos para recomendar novos amigos.

## Cenário
"Pessoas que você talvez conheça". Essa funcionalidade sugere amigos de amigos. Se Alice é amiga de Bob, e Bob é amigo de Carol (mas Alice não conhece Carol), o sistema deve sugerir Carol para Alice.

## Requisitos

1.  Use sua classe `Grafo` ou crie uma nova estrutura. O grafo deve ser **não direcionado** (amizade é recíproca).
2.  Implemente a função `recomendar_amigos(usuario)`.
3.  Lógica de recomendação:
    - Encontre todos os amigos diretos do usuário (Distância 1).
    - Encontre todos os amigos desses amigos (Distância 2).
    - Exclua as pessoas que já são amigas do usuário e o próprio usuário.
    - Retorne a lista de sugestões.

## Exemplo de Uso

```python
rede = RedeSocial()
rede.conectar("Alice", "Bob")
rede.conectar("Bob", "Carol")
rede.conectar("Alice", "David")
rede.conectar("David", "Carol")

# Alice conhece Bob e David.
# Bob conhece Carol. David conhece Carol.
# Sugestão para Alice: Carol (amiga em comum de Bob e David)

print(rede.recomendar_amigos("Alice")) # Esperado: ["Carol"]
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
