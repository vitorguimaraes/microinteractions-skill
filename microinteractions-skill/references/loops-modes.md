# Loops e modos

## Modos
- Modo = bifurcação nas regras em que a mesma ação faz outra coisa. Usar com extrema parcimônia: no máximo um por microinteração, idealmente zero.
- Bom motivo: ação rara que poluiria o fluxo principal (ex.: configurações, adicionar cidade).
- Se necessário: dar ao modo **sua própria tela**, com transição de ida e volta; ao voltar, o modo original deve estar como foi deixado, já refletindo mudanças.
- Alternativas que evitam o usuário "preso":
  - **Spring-loaded (quasimodo)**: ativo só enquanto há ação física (segurar Shift; segurar Iniciar para reiniciar).
  - **One-off**: dura uma única ação e desliga sozinho (menu contextual de formatação; ferramenta que volta ao ponteiro; comando de voz após palavra de ativação, com timeout).

## Loops
Ciclo que se repete, define ritmo e vida útil da microinteração. Sinais nas regras: "buscar dados a cada 30 s", "rodar 3 min e parar", "lembrar em 10 dias".

Estilos:
- **Por contagem (for)**: N vezes (tentar conexão 10 vezes antes de erro).
- **Por condição (while)**: enquanto condição vale.
- **Por coleção**: percorre todos os itens e termina (cada e-mail não lido soma 1).
- **Infinito**: evitar; só quando faz sentido (luz acesa até desligar). Cuidado com loops sem saída (caso do rover Spirit: reinicialização repetida por falta de espaço).

Tipos: **aberto** (não reage a feedback) e **fechado** (se ajusta, como volume do som seguindo ruído do motor).
Parâmetros importam: ciclos curtos demais = intrusivo; longos demais = lento.

Usos: limitar duração (logout por inatividade, com cuidado), limitar abuso (alerta se adiciona amigos rápido demais), detectar hesitação e oferecer ajuda (vídeo travado oferece baixar).

## Long loops (loops longos)
Fazem a microinteração melhorar na 2ª, 10ª, 10.000ª vez: memória, dados, adaptação.
- **Long Wow**: entregar novidades aos poucos, de modo que pareça novo ao longo do tempo.
- Lembrar preferências (volume, último ciclo) e retomar de onde parou.
- Lembretes periódicos (lista de desejos semanal), pausas ("pausar durante feriados").
- **Divulgação progressiva**: com o uso, mostrar atalhos e recursos avançados.
- **Redução progressiva**: com a proficiência, a interface simplifica (label some, botão perde ênfase); se o usuário fica longe, voltar a ficar mais explícita.
- Falhas comuns: "Lembrar de mim" que não lembra (loop quebrado).
