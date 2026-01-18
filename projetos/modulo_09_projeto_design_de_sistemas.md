# Módulo 09: Projeto - Arquitetura de Encurtador de URL

## Objetivo
Implementar a lógica central de um Encurtador de URLs, focando na eficiência da geração de chaves e na estrutura de dados simulada.

## Requisitos

1.  Crie uma classe `EncurtadorURL`.
2.  **Gerador de ID Único:** Em um sistema distribuído, não podemos depender apenas de um auto-incremento de banco simples. Implemente uma lógica de conversão de ID numérico (ex: do banco) para Base62 (a-z, A-Z, 0-9).
    - Ex: ID 1000 -> "g8" (exemplo hipotético).
3.  Simule o banco de dados com dois dicionários:
    - `url_para_id`: Para evitar duplicatas (mesma URL longa gerando novas curtas).
    - `id_para_url`: Para o redirecionamento rápido.
4.  Métodos:
    - `encurtar(url_longa)`: Retorna a string curta (ex: "http://meu.site/Ab3").
    - `restaurar(url_curta)`: Retorna a URL original.

## Exemplo de Lógica Base62

```python
CARACTERES = "0123456789abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ"

def encode(num):
    # Converte inteiro para base62
    pass

def decode(string):
    # Converte base62 para inteiro
    pass
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
