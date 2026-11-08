# Prática: exemplos, orquestração, documentação e teste

## Conteúdo
- Exemplos aplicados
- Orquestração
- Documentar e prototipar
- Testar

## Exemplos aplicados (padrão de raciocínio)
Para cada um, seguir: objetivo → regras básicas → gatilho → não começar do zero → controles → feedback → loops/modos.

1. **App de alarme (mobile)**: objetivo = ser avisado no horário (não "configurar alarme"). Trazer à frente o dado disponível na plataforma (nº de alarmes ativos no badge). Contexto: se o mesmo alarme foi definido 3 dias seguidos, sugerir na abertura; mostrar "faltam 8 h" para evitar erro AM/PM; soneca decrescente (5 min, 4, 3...) virando 1 min; remover soneca se nunca usada em uma semana; desligar sozinho após ~10 min. Controle customizado (flip de minutos de 5 em 5) só se for momento marcante; sem tela de configurações na primeira versão.
2. **Playlist compartilhada (web)**: gatilho manual (arrastar para o slot "Solte uma música aqui", item de menu para músicas internas, atalho) e do sistema (amigo adiciona). Feedback: lista desce e a nova entra por cima com som; ícone na aba do navegador; loader com personagem que "procura" a música. Algoritmo de correspondência: até 3 opções, priorizar artista, mais 3 sob demanda, estado "triste" sem resultado. Long loop: lembrar quando o usuário contribuiu pela última vez. Limite de 30 músicas.
3. **Painel de lava-louças (sem tela)**: botões por ciclo + Iniciar; faixa de LEDs mostra tempo restante (dado que o usuário quer); estados do Iniciar: Desligado, "Aperte-me" (pulsando), Em operação (vermelho), Limpo (verde/azul, acessível a daltônicos); reset por pressão longa (spring-loaded) com rótulo "Segure para reiniciar"; porta aberta pausa e retoma; reset automático após 1 h aberta; som de fim só se o contexto permitir.

## Orquestração
- Microinteração raramente vive sozinha: definir sua relação com o recurso (inicia, controla, aparece dentro, encerra) e sua persistência.
- Raramente deve ser marcante; velocidade e ausência de esforço vencem, principalmente se está no caminho (login).
- Encadear: o fim de uma é o gatilho da próxima (efeito dominó), como em wizard ou "bem-vindo de volta".
- Criar uma lista mestre e um **mapa de microinterações**; cuidar das passagens (handoffs) para que o conjunto pareça um todo. Antes de projetar uma, anotar quais outras ela toca (ex.: lista x rolagem).

## Documentar e prototipar
Melhor para comunicar fluxo e tempo: protótipo na plataforma, filme/animação, storyboard quadro a quadro. Pior: capturas estáticas soltas. Se só houver estáticos, incluir **quadros-chave**: gatilho, momento essencial das regras, fim. Combinar métodos (protótipo para tempo, storyboard para contexto, wireframes com chamadas para regras complexas). A documentação deve contar o que acontece e por quê.

## Testar
- Ciclo Construir > Medir > Aprender; protótipo de **alta fidelidade** (gatilho, regras, feedback e loops são inseparáveis).
- Quantitativo é o caminho para nuances pequenas: exige amostras grandes (mínimo ~20; ideal centenas ou milhares); eventos de analytics em web; A/B. Qualitativo detecta o terrível ou o ótimo.
- Cuidado com erros de cenário causados pelo próprio teste (pausar para perguntar faz perder feedback).
- Validar: objetivo real entendido, dados que importam, microcopy necessária e clara, tempo e fluxo.
- Sinais observáveis e causa provável: "O que acabou de acontecer?" (feedback pouco claro) · "Aconteceu algo?" (feedback ausente/sutil) · "Não acho" (rótulo/ausência) · "Onde estou?" (transição/modo) · "Não vi o botão" (hierarquia visual) · "Não sabia que dava" (gatilho escondido) · "O que faço agora?" (próximo passo pouco claro).
- Métricas: taxa de conclusão, duração total e por passo (média geométrica reduz o efeito de outliers), nº de passos/cliques, erros do sistema, erros humanos (deslizes x equívocos), notas de satisfação/dificuldade/confiança/utilidade.
- Dados informam, não decidem: precisam de interpretação em contexto.
- Roteiro sugerido: perguntar expectativa antes; uso sem ajuda (coletar métricas); passo a passo falando em voz alta; "o que gostaria que lembrasse amanhã?"; "o que consertar?". Rodar ao menos duas rodadas com grupos diferentes.
