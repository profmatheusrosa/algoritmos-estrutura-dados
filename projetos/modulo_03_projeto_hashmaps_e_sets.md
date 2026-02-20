# Módulo 03: Projeto - Banco de Dados em Memória (Key-Value Store)

## Objetivo

Criar um sistema de banco de dados simples em memória (como um mini Redis) que suporte operações básicas usando HashMaps. Este projeto vai te ajudar a entender na prática como dicionários funcionam e como são usados em sistemas reais.

Curiosidade: dependendo da linguagem, você pode ver isso sendo chamado de **mapa (map)**, **dicionário (dictionary/dict)**, **hashmap** ou até **key-value store**. A ideia é sempre a mesma: **chave → valor**.

## Cenário

Você precisa de um armazenamento rápido para configurações de aplicação que não precise de persistência em disco, mas que suporte operações básicas de chave-valor. Pense nisso como um cache super rápido ou um sistema de configurações temporárias.

## Requisitos

### Parte 1: Operações Básicas

Crie uma classe `BancoEmMemoria` com os seguintes métodos:

1. **`set(chave, valor)`**: Salva um valor associado a uma chave. Se a chave já existir, atualiza o valor.
   - Complexidade esperada: O(1)

2. **`get(chave)`**: Retorna o valor associado à chave, ou `None` se a chave não existir.
   - Complexidade esperada: O(1)

3. **`delete(chave)`**: Remove a chave e seu valor do banco.
   - Complexidade esperada: O(1)

4. **`exists(chave)`**: Retorna `True` se a chave existe, `False` caso contrário.
   - Complexidade esperada: O(1)

5. **`keys()`**: Retorna uma lista com todas as chaves armazenadas.

6. **`values()`**: Retorna uma lista com todos os valores armazenados.

### Parte 2: Funcionalidades Avançadas

7. **`count(valor)`**: Retorna quantas chaves possuem exatamente esse valor (simulando uma indexação reversa simples).
   - **Dica:** Você pode precisar manter um dicionário adicional que mapeia valores para uma lista de chaves.

8. **`clear()`**: Remove todas as chaves e valores do banco.

### Parte 3: Desafio Extra (Opcional)

9. **`rollback()`**: Implemente um sistema simples de desfazer a última operação. Isso exigiria uma pilha de estados (conectando com o Módulo 2 sobre Pilhas!).
   - **Dica:** Use uma pilha para armazenar o histórico de operações. Cada operação pode ser representada como uma tupla: `('set', chave, valor_anterior)` ou `('delete', chave, valor)`.

## Exemplo de Uso

```python
db = BancoEmMemoria()

# Operações básicas
db.set("usuario", "admin")
db.set("tema", "escuro")
db.set("idioma", "pt-BR")

print(db.get("usuario"))   # "admin"
print(db.exists("tema"))   # True
print(db.exists("cor"))    # False

# Listar chaves e valores
print(db.keys())           # ["usuario", "tema", "idioma"]
print(db.values())         # ["admin", "escuro", "pt-BR"]

# Contar valores
db.set("tema2", "escuro")
print(db.count("escuro"))  # 2 (tema e tema2 têm o valor "escuro")

# Remover
db.delete("tema")
print(db.get("tema"))      # None
print(db.exists("tema"))   # False

# Limpar tudo
db.clear()
print(db.keys())           # []
```

## Dicas de Implementação

1. Use um dicionário Python (`dict`) como estrutura base para armazenar os pares chave-valor.

2. Para o método `count()`, considere manter um segundo dicionário que mapeia valores para um set de chaves. Isso permite contar em O(1) após a construção inicial.

3. Para o `rollback()`, você pode usar uma lista (pilha) do módulo `collections` ou simplesmente uma lista Python com `append()` e `pop()`.

4. Pense em casos extremos: o que acontece se tentar fazer `get()` de uma chave que não existe? E se tentar `delete()` de uma chave inexistente?

## Critérios de Avaliação

- ✅ Implementação correta de todas as operações básicas
- ✅ Complexidade O(1) para operações principais (set, get, delete, exists)
- ✅ Código limpo e bem documentado
- ✅ Tratamento adequado de casos extremos (chaves inexistentes, etc.)
- ✅ Implementação das funcionalidades avançadas (bonus)

## Extensão (Opcional)

Se você quiser ir além, tente implementar:

- **TTL (Time To Live)**: Adicionar um tempo de expiração para as chaves
- **Snapshot**: Salvar o estado atual do banco em um arquivo JSON
- **Load**: Carregar um estado salvo anteriormente

Boa sorte!

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
