# Módulo 03: Projeto - Banco de Dados em Memória (Key-Value Store)

## Objetivo
Criar um sistema de banco de dados simples em memória (como um mini Redis) que suporte operações básicas e transações simples.

## Cenário
Você precisa de um armazenamento rápido para configurações de aplicação que não precise de persistência em disco, mas que suporte comandos de linha.

## Requisitos

1.  Crie uma classe `BancoEmMemoria`.
2.  Métodos necessários:
    - `set(chave, valor)`: Salva um valor.
    - `get(chave)`: Retorna o valor ou `None`.
    - `delete(chave)`: Remove a chave.
    - `exist(chave)`: Retorna `True` ou `False`.
    - `count(valor)`: Retorna quantas chaves possuem exatamente esse valor (simulando uma indexação reversa simples).

3.  **Desafio Extra (Opcional):** Implemente um método `rollback` simples? (Isso exigiria uma pilha de estados, conectando com o Módulo 2!).

## Exemplo de Uso

```python
db = BancoEmMemoria()
db.set("usuario", "admin")
db.set("tema", "escuro")
print(db.get("usuario"))  # admin
print(db.count("escuro")) # 1

db.delete("tema")
print(db.get("tema"))     # None
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
