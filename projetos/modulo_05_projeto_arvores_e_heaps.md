# Módulo 04: Projeto - Agendador de Tarefas Prioritárias

## Objetivo
Criar um sistema de gerenciamento de tarefas onde cada tarefa tem uma prioridade. O sistema deve sempre executar (remover) a tarefa de maior prioridade primeiro.

## Cenário
Em um sistema operacional ou servidor web, processos críticos (como responder ao mouse) devem ser processados antes de tarefas de fundo (como indexar arquivos). Você vai simular esse comportamento.

## Requisitos

1.  Crie uma classe `AgendadorTarefas`.
2.  Use o módulo `heapq` do Python. Nota: `heapq` implementa Min-Heap. Para simular Max-Heap (maior prioridade primeiro), você pode armazenar as prioridades como números negativos.
3.  Métodos:
    - `adicionar_tarefa(nome, prioridade)`: Adiciona uma tarefa. Prioridade 10 é maior que 1.
    - `pegar_proxima_tarefa()`: Retorna e remove a tarefa de maior prioridade.
    - `visualizar_tarefas()`: Mostra as tarefas pendentes (não precisa estar ordenado).

## Exemplo de Uso

```python
agendador = AgendadorTarefas()
agendador.adicionar_tarefa("Limpar Cache", 1)
agendador.adicionar_tarefa("Processar Pagamento", 10)
agendador.adicionar_tarefa("Enviar Email", 5)

print(agendador.pegar_proxima_tarefa()) # Deve ser "Processar Pagamento"
print(agendador.pegar_proxima_tarefa()) # Deve ser "Enviar Email"
```

---

[Voltar aos Links Rápidos](../README.md#links-rapidos)
