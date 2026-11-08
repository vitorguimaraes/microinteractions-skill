# Checklist de auditoria e "conserto"

## Auditoria rápida (responder sim/não e corrigir os "não")
**Gatilho**
- Visibilidade proporcional à frequência de uso?
- Mesma ação em todo disparo? Sem affordance falsa?
- Mostra um dado útil antes do clique (bring the data forward)?
- Label só onde há ambiguidade, específico e consistente?
- Gatilho do sistema pode ser ajustado/desligado e tem versão manual?

**Regras**
- Objetivo = estado final do usuário, escrito em uma frase?
- Regras explicáveis em poucas linhas?
- Usa contexto e histórico (não começa do zero)?
- Poucas opções, padrão inteligente e visível?
- Erros evitados por desenho; mensagens só para falhas do sistema?
- Estados de cada objeto definidos (padrão, ativo, atualizado)?

**Feedback**
- Toda ação do usuário confirmada, perto do ponto de ação?
- Mínimo de canais para a importância da mensagem?
- Animação com propósito, curta, suave, coerente com o modelo espacial?
- Erro diz o que houve e como corrigir, sem acusar?
- Som passa no teste da buzina e pode ser desligado?

**Loops e modos**
- Zero ou um modo? Se há modo, tem tela/transição própria?
- Spring-loaded ou one-off quando possível?
- Nenhum loop sem fim ou sem saída? Timeouts definidos?
- Há memória/adaptação para a 2ª e a 100ª vez?

## Como consertar uma microinteração sem graça
1. Deve ser um momento marcante? (quanto mais, mais rico o controle e o feedback)
2. O que já sei do usuário/contexto?
3. Qual o dado mais importante e dá para trazê-lo à frente?
4. Um controle customizado ajudaria?
5. Que erros humanos posso prevenir automaticamente?
6. Que elementos "esquecidos" da interface podem comunicar mais?
7. Há gatilho invisível (gesto/atalho) para usuários avançados?
8. O texto soa como uma pessoa falaria? Cabe um toque de humor?
9. Uma animação discreta daria sentido e continuidade?
10. Som ou háptico adicionam ênfase sem incomodar?
11. O que acontece na segunda e na centésima vez (long loop)?
