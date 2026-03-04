# Módulo 02: Projeto - Simulador de Navegador Web

## Objetivo
Criar um sistema simples que simule o histórico de navegação de um browser (Navegador Web) utilizando Pilhas.

## Cenário
Você está construindo o núcleo de um novo navegador. O usuário precisa ser capaz de:
1.  Visitar uma nova página.
2.  Clicar no botão "Voltar" para ir à página anterior.
3.  Clicar no botão "Avançar" para ir à página que ele acabou de voltar.

## Requisitos

1.  Crie uma classe `Navegador`.
2.  Use duas pilhas: `historico_voltar` e `historico_avancar`.
3.  Implemente os métodos:
    - `visitar(url)`: Abre uma página e limpa o histórico de avançar.
    - `voltar()`: Retorna a última URL visitada e a move para a pilha de avançar.
    - `avancar()`: Retorna a URL do topo da pilha de avançar e a move de volta para o histórico principal.

## Exemplo de Uso

```python
nav = Navegador()
nav.visitar("google.com")
nav.visitar("github.com")
nav.visitar("stackoverflow.com")

print(nav.voltar()) # Deve retornar "github.com"
print(nav.voltar()) # Deve retornar "google.com"
print(nav.avancar()) # Deve retornar "github.com"
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
