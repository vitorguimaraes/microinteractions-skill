# Regras

## Conteúdo
- O que as regras definem
- Como gerar regras
- Verbos e substantivos
- Telas e estados
- Restrições
- Não começar do zero
- Absorver complexidade
- Opções limitadas e padrões inteligentes
- Controles e entrada
- Prevenção de erros
- Microcopy
- Algoritmos

## O que as regras definem
Resposta ao gatilho · controle do usuário durante o processo · sequência e tempo · dados usados e origem · parâmetros de algoritmos · quando há feedback · modo atual · se repete · o que acontece ao terminar.
As regras são invisíveis; só o feedback as revela. Objetivo: um modelo simples e não técnico, que pareça natural (fluxo), não uma lista a memorizar.

## Lições sobre expectativas
- Se não dá para escrever ou diagramar as regras, o usuário não formará um modelo mental.
- Usuários chegam com expectativas. Só quebre-as se o ganho for claro e imediato; senão parece gimmick. (Caso clássico: a remoção do "Salvar como" no macOS Lion quebrou um modelo de ~30 anos e foi revertida parcialmente.)

## Como gerar regras
Começar listando as regras óbvias em ordem; depois acrescentar nuances (ex.: botão "Adicionar" vira "Adicionar de novo" se já comprado). Usar diagrama lógico para ver complexidade e erros de lógica.

## Verbos e substantivos
- Pensar a microinteração como frase: verbos = o que o usuário pode fazer; substantivos = objetos/controles.
- Cada objeto tem características e estados definidos pelas regras.
- Cada substantivo deve ser único; objetos iguais agem igual; objetos que agem diferente parecem diferentes.
- Melhor desenho: muitos verbos com poucos substantivos.

## Telas e estados
Evitar transformar cada regra em uma tela (wizard) exceto para passos discretos e raros. Preferir mudança de estado e divulgação progressiva. Todo objeto interativo tem ao menos: estado de convite/padrão, ativado, atualizado. Projetar cada um (ex.: arrastar: parece arrastável → durante arrasto → ao soltar).

## Restrições
Considerar: métodos de entrada/saída disponíveis, tipo e faixa de entrada, o que é caro (dinheiro, servidor, bateria), dados disponíveis (sensores, APIs) e dados que podem ser coletados.

## Não começar do zero
Perguntar logo após o gatilho: o que sei do usuário e do contexto? Exemplos: plataforma, hora, ruído, tempo desde o último uso, reunião, bateria, localização, histórico. Combinar dados para prever (ex.: "todo dia às 10h faz X → oferecer X"). Dados do histórico viabilizam atalhos para usuários avançados. Cuidado com privacidade: se a informação pode constranger ou colocar o usuário em risco, não coletar.

## Absorver complexidade (Lei de Tesler)
A complexidade inerente não some: ou o sistema absorve ou o usuário. Em microinterações, favorecer o sistema decidir. Deixar com a máquina: cálculos, tarefas simultâneas, memória, padrões complexos, busca em grandes conjuntos. Dar controle só quando necessário e no momento certo.

## Opções limitadas e padrões inteligentes
- Cada opção cria uma regra. Ser rigoroso ao eliminar opções; ideal: nenhuma, só padrões bons.
- Enfatizar (ou executar) a próxima ação mais provável. Padrão mais proeminente = o que a maioria faz na maioria das vezes (OK maior que Cancelar; Enter executa o padrão).
- No máximo uma opção que altere radicalmente as regras (isso vira modo).
- Mostrar o que o padrão decide ("Adiar 15 min" em vez de "Adiar").
- Escolhas devem ser significativas (alteram o resultado/objetivo). Se não, remover.
- Eliminar opções elimina casos de borda; reformular regras para tornar casos de borda impossíveis (ano de nascimento como lista, não texto livre).
- Ordem das opções afeta a escolha: início/fim lembram mais; destacada é mais escolhida; ir do amplo ao detalhado.

## Controles e entrada
- Simplicidade operacional (um controle por comando) para uso raro; simplicidade percebida (um controle, várias ações) para uso repetido. Exceção: ações rápidas e críticas (mudo em teleconferência).
- Campos de texto devem ser tolerantes (telefone com ou sem máscara; colar "#" em hex; colar "Nome <email>") e normalizar em silêncio.
- Ordenar listas pensando no uso (mais comum no topo, mesmo que "ilógico").
- Atalhos redundantes são bem-vindos, mas toda ação importante precisa de caminho visível.

## Prevenção de erros (Poka-Yoke)
- Desenhar para que o erro seja impossível ou corrigido pelo sistema antes de avisar.
- Mensagem de erro só quando o sistema falha, não quando o usuário fez tudo certo. Alertas em pop-up são último recurso.
- Exemplos: avisar esquecimento de anexo antes de enviar; pausar upload com bateria baixa; ajustar busca sem resultados; mostrar duração ao escolher horário final.

## Microcopy
- Só o necessário; rótulo basta no lugar de instrução ("Próximo" dispensa "Toque em Próximo para continuar").
- Texto truncado precisa de forma de ver completo (hover/toque).
- Evitar rótulos ambíguos (Anterior/Próximo invertidos); evitar dupla negação.
- Melhor lugar do label: acima do campo; segundo: dentro/ao lado do objeto. Não depender de label que some ao digitar; usar exemplo no campo.
- Texto de instrução igual ao controle (verbo do texto = verbo do botão).
- Preferir tempo relacional ("há 3 horas") a data exata, salvo quando a exatidão importa.

## Algoritmos
Quatro partes: **sequência**, **decisões** (se...então), **repetições**, **variáveis** (número de resultados, passos, etc.). Definir variáveis permite ajustar sem reescrever. Designers devem participar para que valores humanos (não só eficiência) entrem na lógica. Quando útil, informar ao usuário quais variáveis agem para que ele possa ajustá-las.
