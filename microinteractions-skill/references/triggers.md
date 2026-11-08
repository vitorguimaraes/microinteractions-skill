# Gatilhos

## Conteúdo
- Princípios do gatilho manual
- Controles
- Descobribilidade
- Gatilhos invisíveis
- Estados do controle
- Labels
- Gatilhos do sistema

## Princípios do gatilho manual
1. Fazer o gatilho ser reconhecível como tal no contexto.
2. Disparar **sempre a mesma ação**, para formar modelo mental correto.
3. **Trazer os dados à frente** (bring the data forward): o próprio gatilho mostra informação útil (badge, progresso no ícone, prévia no hover).
4. Não quebrar a affordance visual: se parece botão, é botão. Sem affordance falsa.
5. Quanto mais frequente o uso, mais visível o gatilho. Esconder em menu é o mínimo de visibilidade.
6. Preferir formas geométricas simples e controles padrão (inovar por último).
7. Label só quando o gatilho sozinho for ambíguo.

## Escolha do controle
| Necessidade | Controle |
|---|---|
| Ação única | botão ou gesto simples |
| Dois estados (liga/desliga) | toggle/switch; botão comum só se o estado for evidente |
| Vários estados definidos | dial, ou conjunto de botões |
| Valor contínuo com faixa | slider ou dial; sem faixa: par de botões +/- |
| Entrada composta | campos de formulário, **pré-preenchidos** com padrões |

## Descobribilidade (regra de ouro)
- O que a maioria faz com frequência: muito descobrível.
- O que alguns fazem às vezes: fácil de achar.
- O que poucos fazem raramente: pode exigir busca.

Ordem do mais ao menos descobrível: objeto em movimento → objeto com affordance e label → objeto com label → objeto sozinho (ícone) → só label (item de menu) → invisível.
Movimento e som capturam atenção involuntária: reservar para prioridade alta (erros, alertas).

## Gatilhos invisíveis
- Baseados em sensor/gesto/atalho/voz (sempre ouvindo, diálogo, ou voz combinada com controle físico).
- Usar quando não há espaço para controle visível ou para reduzir ruído, nunca como objetivo em si.
- Devem ser aprendíveis (disponíveis de forma previsível) e, se possível, descobertos por acaso durante outra ação (ex.: puxar a lista para baixo revela atualizar).
- Nunca invisível para ação de alta prioridade; oferecer ao menos um caminho visível (menu, atalho listado).

## Estados do controle
Considerar: padrão, ativo (processo em segundo plano), hover, rollover, ao clicar/tocar/em processo, toggle, valor/setting.
- Indicadores de estado ficam junto ao gatilho; se o gatilho expande, expandir no lugar (não abrir janela distante).
- Hover é bom lugar para antecipar um dado interno.

## Labels
- Curtos, específicos, em linguagem do usuário; o mesmo nome em toda a microinteração (não alternar "alerta"/"aviso").
- Dar **feedforward**: o rótulo antecipa o que vai acontecer ("Enviar relatório" > "Enviar").
- Labels são utilitários: humor só se a clareza se mantiver.
- Testar rótulos com o público-alvo; rotulagem ruim causa a maior parte dos problemas de usabilidade.

## Gatilhos do sistema
Condições típicas: erros, localização, dados que chegam, dados internos (hora, recursos), outras microinterações, outras pessoas.
- Todo gatilho do sistema precisa de forma manual de ajustar/desativar (idealmente no ponto em que aparece: "não mostrar mais"; no mínimo nas configurações).
- Oferecer também controle manual do mesmo processo (ex.: sincronizar agora) como garantia quando o automático falha.
- Definir regras do gatilho: frequência, dados já conhecidos, indicador visível de que disparou, o que fazer em erro (tentar de novo? após quanto tempo?).
