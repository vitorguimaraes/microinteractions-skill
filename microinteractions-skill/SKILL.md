---
name: microinteractions
description: guia de design de microinterações baseado no modelo de Dan Saffer (gatilho, regras, feedback, loops e modos). use sempre que o usuário pedir para projetar, revisar, auditar ou melhorar um pequeno momento de interface (botão, toggle, copiar, salvar, login, formulário, notificação, alarme, loading, estados de erro, animação de resposta a clique, motion/transições), mesmo que não use a palavra "microinteração". também use para escrever microcopy (labels, mensagens de erro), definir feedback visual/sonoro/háptico, documentar ou testar microinterações, ou transformar um recurso complexo em momentos pequenos e encadeados.
---

# Microinterações (modelo Saffer)

Material de apoio baseado em *Microinteractions* (Dan Saffer, O'Reilly, 2013), reescrito de forma resumida e original. Não reproduza trechos do livro; cite no máximo frases curtas e sempre com atribuição.

## Modelo central

Microinteração = momento contido em torno de **um único caso de uso**. Toda microinteração tem 4 partes, sempre analisadas nesta ordem:

1. **Gatilho (trigger)** – o que inicia (manual ou do sistema).
2. **Regras (rules)** – o que acontece, em que ordem, com que dados.
3. **Feedback** – como o usuário percebe/entende as regras.
4. **Loops e modos** – o que muda com o tempo, repetição e desvios.

Princípio-guia: o objetivo é o **estado final desejado pelo usuário**, não um passo do processo (login = estar dentro do app, não digitar senha).

## Fluxo de trabalho

1. Identificar a microinteração e escrever o **objetivo** em uma frase.
2. Escrever as **regras** em linguagem simples (lista curta ou diagrama lógico). Se não dá para escrever, o usuário não vai entender.
3. Definir o **gatilho** (frequência de uso → visibilidade) e quais dados trazer à frente.
4. Definir o **feedback mínimo** necessário para o usuário formar o modelo mental.
5. Decidir **loops/modos**; evitar modos, preferir spring-loaded ou one-off.
6. Verificar com o checklist em [references/checklist.md](references/checklist.md).

## Onde ler mais (carregue só o necessário)

| Tarefa | Arquivo |
|---|---|
| Definir/avaliar gatilhos, controles, estados, labels, gatilhos invisíveis ou do sistema | [references/triggers.md](references/triggers.md) |
| Regras, padrões, limites de opções, prevenção de erro, microcopy, algoritmos | [references/rules.md](references/rules.md) |
| Feedback visual, animação/motion, áudio, háptico, tom de voz | [references/feedback.md](references/feedback.md) |
| Modos, loops, long loops, divulgação/redução progressiva | [references/loops-modes.md](references/loops-modes.md) |
| Exemplos aplicados, orquestração, documentação, teste e métricas | [references/practice.md](references/practice.md) |
| Auditar ou "consertar" uma microinteração sem graça | [references/checklist.md](references/checklist.md) |

## Formato de entrega (ao projetar ou revisar)

Responder com esta estrutura, adaptando o tamanho ao pedido:

```
Objetivo: <estado final do usuário>
Gatilho: <manual/sistema> · controle · estados · label
Regras: <lista numerada curta>
Feedback: <o que, em que canal, quando>
Loops/modos: <repetição, expiração, memória; ou "nenhum">
Riscos: <o que pode confundir ou quebrar o modelo mental>
```

Em revisões, listar primeiro as violações dos princípios (com a parte afetada: gatilho/regra/feedback/loop) e depois a correção proposta.

## Regras gerais de decisão

- Menos é mais: menos opções, menos feedback, menos texto, menos modos.
- Padrões inteligentes antes de perguntas; não começar do zero (usar contexto e histórico).
- Todo ato do usuário recebe reconhecimento imediato, perto do ponto de ação.
- Feedback nunca é arbitrário: deve ter relação direta com a ação e o resultado.
- Animação só se explica ou orienta algo; curta, suave, rápida.
- Se parecer botão, deve agir como botão. Mesmo gatilho, mesma ação, sempre.
- Privacidade: não coletar comportamento que possa envergonhar ou expor o usuário.
- Momento marcante (signature moment) só quando agrega identidade; a maioria das microinterações deve ser rápida e quase invisível.
