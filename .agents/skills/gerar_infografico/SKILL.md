---
name: gerar-infografico
description: Use this skill ALWAYS when the user requests generating technical or educational illustrations, diagrams, or infographics. This skill ensures visual consistency, prevents English words, and enforces strict Brazilian Portuguese (pt-BR) labels.
---

# Gerar Infográfico Educacional (pt-BR)

Esta habilidade define as diretrizes rigorosas e o padrão de prompt para gerar infográficos educacionais com estilo *flat vector*, garantindo que o texto presente na imagem seja exclusivamente em Português do Brasil (pt-BR) e que não contenha expressões em inglês ou a própria sigla do idioma. 

## Quando usar esta habilidade
Sempre que a tarefa envolver a chamada da ferramenta (tool) `generate_image` para fins de ilustração, diagramas de estrutura de dados ou explicações visuais de engenharia de software no contexto do projeto.

## Diretrizes de Construção do Prompt

O AI agent (você) deve seguir as seguintes regras de *progressive disclosure* e prompting ao gerar a imagem:

1. **Idioma Principal:** O prompt DEVE ser escrito inteiramente em **Inglês** (para garantir melhor alinhamento estético da IA geradora).
2. **Proibições Estritas:**
   - **NÃO** peça para escrever o nome do idioma ou siglas como "pt-BR" ou "Português" dentro da imagem.
   - **NÃO** permita rótulos ou qualquer palavra em inglês na imagem final.
3. **Especificação Exata de Rótulos:** Você deve listar *apenas* as opções precisas de rótulos em Português do Brasil de que precisa.
4. **Sufixo Estético Obrigatório:** O final do prompt deve sempre conter:
   `Minimalist design, technical aesthetic, clear and educational, flat vector style, software engineering infographic.`

## Template Oficial do Prompt

Copie e preencha este modelo de prompt cada vez que a ferramenta `generate_image` precisar ser chamada:

```text
A clean and informative infographic illustrating [CONCEITO GERAL]. 
[DESCRIÇÃO VISUAL DETALHADA: posições, cores, setas, estrutura]. 
Use ONLY the following words for labels: '[Palavra 1]', '[Palavra 2]', '[Palavra 3]'. 
DO NOT use English words. DO NOT write 'pt-BR' anywhere in the image. 
Minimalist design, technical aesthetic, clear and educational, flat vector style, software engineering infographic.
```

## Fluxo de Execução Recomendado

1. **Identificação:** Leia o conceito que será ilustrado através das orientações ou pedido ativo.
2. **Planejamento de Rótulos:** Decida exatamente quais palavras curtas em pt-BR aparecerão como legenda (ex: 'Ponteiro', 'Memória', 'Esquerda', 'Direita').
3. **Preenchimento:** Substitua os espaços "[ ]" do **Template Oficial** mantendo o restante fixo.
4. **Execução:** Chame `generate_image` com o `ImageName` em fomato snace_case descritivo e forneça o prompt.
5. **Automação:** Se o usuário solicitou uma substituição na base de código, emita imediatamente o comando (usando CMD ou PowerShell) para copiar o recém-gerado PNG para a pasta correspondente.
