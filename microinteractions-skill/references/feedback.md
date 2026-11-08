# Feedback

## Conteúdo
- Função do feedback
- Quando dar feedback
- Princípios
- Personalidade
- Visual e animação
- Mensagens
- Áudio
- Háptico
- Regras do feedback

## Função
Feedback ilumina as regras: confirma que a ação ocorreu e o que resultou. Basta o suficiente para um modelo mental funcional. Aviso: feedback pode ser usado para enganar (caça-níqueis: quase-vitórias, luzes e sons desproporcionais, reforço intermitente). Em produto, buscar **previsibilidade e reforço consistente** do comportamento desejado.

## Deve ocorrer
- Imediatamente após gatilho manual ou ajuste de regra (todo ato do usuário recebe reconhecimento).
- Em gatilhos do sistema que mudem significativamente o estado.
- Ao chegar à borda de uma regra (erro iminente, fim da lista).
- Quando o sistema não consegue executar (offline), podendo esperar algumas tentativas antes de avisar.
- Em progresso de processos críticos/longos (estimar duração).

## Pode ocorrer
No início/fim de processo, na entrada/saída de modo. Também vale indicar o que **não** aconteceu quando isso tranquiliza.

## Mensagens que o feedback comunica
Algo aconteceu · você fez algo · processo iniciou · terminou · está em andamento · você não pode fazer isso.

## Princípios
1. Não sobrecarregar: qual o mínimo de feedback que comunica o necessário?
2. Nunca arbitrário: ligação clara entre ação e feedback (clique mecânico ou som que sobe ao ligar, em vez de um bipe qualquer).
3. Transmitir o máximo com o mínimo: mais canais (animação + som + vibração) = mais intrusivo; quanto mais importante, mais proeminente.
4. Usar o negligenciado: cursor, barra de rolagem, barra de progresso, tooltip, ícone do app, aba do navegador, para dar feedback sem adicionar elementos.
5. Feedback é para humanos: rostos, tom humano; a "penalidade" por interpretar mal um sinal deve ser nenhuma.

## Personalidade
Feedback é o lugar para humor e identidade, principalmente em erros e esperas. Dose: "um verniz" de personalidade; não repetir piada em ação frequente, não ser acusatório, não parecer humano demais (expectativa alta, "vale da estranheza"). Evitar sorrisos aleatórios em mensagens que não são alegres. Não deixar a coleta de dados evidente demais (parece invasivo).

## Visual e animação
- Padrão é visual para toda ação do usuário (exceto ações impossíveis); do sistema, só o que exige intervenção ou informa algo acionável.
- Sem feedback redundante (tooltip repetindo o label). Não piscar sem necessidade.
- Perto do ponto de entrada; se longe, usar movimento (fade-in) para atrair.
- **Animação**: usar com moderação; cada animação deve revelar o modelo de comportamento (um painel que entra pela esquerda sai pela esquerda). Deve ser:
  rápida, suave, natural (inércia/gravidade), simples, com propósito.
- Funções legítimas: manter contexto na troca de visão, explicar o que acabou de acontecer, mostrar relação entre objetos, focar atenção, melhorar desempenho percebido, criar ilusão de espaço, convidar à interação.
- Duração: faça a animação com metade do tempo que parece certo, e talvez reduza de novo.

## Mensagens (texto)
- Precisas, curtas, sem "erro"/"aviso" vazios; dizer **o que houve e como corrigir**, idealmente com o controle de correção ao lado.
- Evitar "você"/"eu": "Senha incorreta" soa menos acusatório que "Você digitou a senha errada".
- Verbos de ação: "Digite a senha novamente".

## Áudio
- Dois usos: **ênfase** (confirma ação) e **alerta** (evento do sistema). Combinado com visual é mais eficaz que só visual.
- Teste da buzina (foghorn test): vale o usuário saber disso quando não está olhando? Oferecer como desligar.
- Considerar contexto (ruído, hora, presença) e o "caso de não uso" (som alto em sala vazia à noite).
- **Earcons**: curtos (menos de 1 s), distintos por ação, coerentes com a emoção (urgente x utilitário); evitar muito agudos ou fracos; nunca em loop. Assinatura sonora: 2 a 4 notas, no máximo uma por microinteração.
- Fala: breve, opções sim/não, ação no fim da frase; gravada (mais humana) x TTS (dinâmico).

## Háptico
Útil para reforçar ação física, para alerta sem som e, raramente, para simular textura. Humanos distinguem poucos níveis (3–4): usar para comunicação sutil/ambiente ou alerta disruptivo; mensagens complexas não cabem.

## Regras do próprio feedback
Definir: mudanças por contexto, duração (e o que dispensa), intensidade (e se cresce), repetição.
