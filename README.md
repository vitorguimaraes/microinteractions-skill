# Skill de Microinteractions

Skill para IA aplicar boas práticas de **microinteractions** em interfaces web, baseada no livro *Microinteractions: Designing with Details*, de Dan Saffer.

O objetivo é que a IA implemente feedback, estados e respostas a ações do usuário de forma consistente, **em qualquer stack frontend**.

## Origem

1. O livro (PDF) foi convertido para Markdown.
2. O Markdown foi usado como base no `skill-creator` para gerar a skill.
3. Um HTML+CSS autocontido resume as boas práticas do livro, com a descrição da prática em cada elemento.

## Estrutura do repositório

> Ajuste os nomes abaixo conforme os arquivos reais do repositório.

```
.
├── README.md
├── Microinteractions_Designing_with_Details.pdf   # livro original
├── Microinteractions.md                           # livro convertido para Markdown
├── boas-praticas.html                             # boas práticas resumidas (HTML+CSS)
└── microinteractions-skill/
    └── SKILL.md                                   # skill gerada pelo skill-creator
```

| Arquivo | Função |
|---|---|
| PDF | Fonte original, apenas para consulta |
| Markdown | Fonte textual usada para gerar a skill |
| HTML+CSS | Referência visual das boas práticas, para análise humana e apoio à IA |
| `SKILL.md` | Instruções que a IA carrega para implementar microinteractions |

## Escopo da skill

A skill cobre **microinteractions** segundo o livro: *trigger*, *rules*, *feedback* e *loops & modes*.

Ficam **fora do escopo** e devem ser tratados em skills separadas:

- **Motion/animação** (princípios, timing, easing, `prefers-reduced-motion`)
- **Acessibilidade de interação** (WAI-ARIA, foco, teclado)

Exemplo de microinteraction: ao clicar em "copiar", o botão cresce, muda de cor, exibe um ícone de confirmação e volta ao estado normal.

## Como usar

1. Instale/importe a pasta da skill na sua ferramenta de IA (Copilot, Claude etc.).
2. Peça a implementação normalmente, informando a stack desejada:

   ```
   Crie um botão "copiar" com feedback de sucesso, em React + Tailwind.
   ```

3. Use o HTML+CSS como referência complementar quando quiser conferir uma prática específica.

Os exemplos da skill são **agnósticos de stack** (HTML/CSS/JS puro como base), para que a IA os traduza para o framework do projeto.

## Validação: com vs. sem a skill

Para medir o impacto real, rode o mesmo prompt em dois chats novos, um com a skill e outro sem, **sem mencionar "microinteractions"** no pedido.

Critérios sugeridos:

- [ ] Trigger claro e com affordance
- [ ] Regras explícitas (o que acontece e quando termina)
- [ ] Feedback proporcional à ação
- [ ] Estados de loop/modo tratados (erro, carregando, repetição)
- [ ] Resultado consistente entre stacks diferentes

