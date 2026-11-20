# Aldeburgo: mundo vivo

Jogo de vida e estratégia medieval-fantástico que roda no navegador, em um único arquivo (`index.html`).
Você começa como alguém comum numa vila, faz carreira, aprende energias e técnicas, funda instituições, convive com as grandes casas, e pode até derrubar o rei e comandar guerras num mapa de hexágonos. O mundo continua mudando mesmo quando você não faz nada.

> Este README descreve o que existe no jogo e como desbloquear cada coisa. Os números (preços, danos, chances) ainda não foram balanceados com muitas horas de jogo: se algo ficar forte, fraco ou chato demais, ajuste ou peça ajuste.

## Como jogar

- Abra o `index.html` no navegador (ou publique no GitHub Pages). Não precisa de servidor.
- Escolha uma **ação** na barra de categorias e clique no botão principal para **avançar a semana**. O botão "Tempo automático" avança sozinho.
- O jogo salva sozinho no navegador. Apagar os dados do site apaga o save.
- Só aparecem as ações que você já pode usar. Se uma ação sumiu, falta cumprir um requisito (veja as tabelas abaixo).
- Alguns eventos têm botões "Escolher e repetir automaticamente por 5 semanas". As escolhas automáticas ativas aparecem no painel "Mundo e metas" e podem ser canceladas ali.
- Quando você ganha uma habilidade (passiva, magia, técnica, relíquia, mestre, aptidão), aparece um **card dourado** no canto da tela.

## Tempo das ações

| Tipo | Tempo |
|---|---|
| Menus e escolhas: conversar, órfãos, Torre dos Magos, grandes casas, armas, edifícios, ensinar, pedir demissão, declarar guerra | **0 semanas** (não gasta tempo) |
| Viajar | tantas semanas quanto a distância do lugar (2 a 6) |
| Explorar além do mapa e explorar masmorra | 1 semana + 2 de caminhada |
| Caçar | 2 semanas |
| Plantar e colher | 3 semanas |
| Demais ações | 1 semana |

## Seu personagem

### Nascimento (só em partidas novas)

Ao começar um jogo novo, o jogo sorteia a origem. Chances aproximadas:

| Origem | Chance | O que você ganha |
|---|---|---|
| Família comum | ~68% | nada de especial |
| Família política | ~12% | cargo de Conselheiro, um pouco de dinheiro |
| Família nobre | ~12% | título de Cavaleiro, dinheiro e fama |
| **Grande casa** | ~7% | pertence a uma das 6 casas, herda uma técnica dela, boa relação e a raça da casa |
| **Filho do rei** | ~1% | título de Conde, cargo de Magistrado, dinheiro e fama, mas vira alvo |

Cada origem tem eventos próprios (ex.: o filho do rei pode sofrer **sequestro** ou **tentativa de assassinato**; quem é de uma grande casa enfrenta rivalidades; nobres sofrem intrigas; famílias políticas enfrentam escândalos).

**Predisposição:** com ~60% de chance você nasce com talento numa energia. Você pode descobrir sozinho depois de um tempo, a sua família pode ser conhecida por isso (você já começa treinado) ou a família pode contar. Quem tem predisposição treina mais rápido essa energia.

Saves antigos não ganham origem, só jogos novos.

### Status

Dinheiro, saúde, energia (fôlego), conhecimento, fama, "procurado" (atenção das autoridades), afeto das pessoas, título, cargo, ofício e influências (política, submundo, militar, acadêmica, econômica, religiosa).

### Comida

Pescar, caçar, plantar e fazer fazendas dão **porções de comida**. Cada porção guardada cobre 4 de ouro do custo semanal de vida, até 3 porções por semana. A comida guardada aparece no painel "Mundo e metas".

## Energias e níveis

Existem 4 energias: **Ki**, **Mana**, **Espiritual** e **Vital**.

O nível de uma energia (0 a 5) é o **menor** entre:
- treino ÷ 15;
- 1 + conhecimento ÷ 8;
- 3, a não ser que você tenha uma **fonte** (então o teto é 5).

**Fontes** que liberam os níveis 4 e 5: uma academia no nível 3 dessa energia, ter fundado uma guilda, decreto de academia, um artefato raro dessa energia, ou ter feito pelo menos 1 lição com um mestre dessa energia.

Como treinar: ação **Treinar uma energia**, **Estudar** (conhecimento), mestres, escolas e instituições.

### Vantagem e desvantagem de cada energia

| Energia | Estilo | Desvantagem em combate |
|---|---|---|
| Ki | físico | golpes de poder 28 ou mais deixam você exposto (inimigo acerta mais) |
| Mana | elementos variados | conjurar deixa você frágil (+15% de dano sofrido) |
| Espiritual | luz, cura, proteção | causar dano custa 3 de saúde |
| Vital | natureza | o dano chega aos poucos (60% agora, 40% depois) |

### Despertar (nível 3)

Ao chegar ao nível 3 de uma energia aparece o **Despertar**: você escolhe um **aspecto permanente** para ela. Há 3 por energia.

| Aspecto | Efeito |
|---|---|
| Ofensivo (Berserker, Elementalista, Inquisidor, Caçador) | +20% de dano nas técnicas dessa energia |
| Defensivo (Monge, Abjurador, Sacerdote, Druida) | +2 de saúde por semana |
| Sábio (Estrategista, Arcanista, Profeta, Herbalista) | +1 conhecimento a cada 4 semanas |

### Técnicas liberadas pelo nível

| Energia | Nível 2 | Nível 3 | Nível 4 |
|---|---|---|---|
| Ki | Punho Sísmico | Passo do Vento (esquiva) | Fúria Marcial |
| Mana | Bola de Fogo | Lança de Gelo | Tempestade Arcana |
| Espiritual | Toque Sagrado (cura) | Raio Divino | Julgamento |
| Vital | Garras Selvagens | Casca Protetora (defesa) | Fúria da Natureza |

### Ressonância (duas energias no nível 3)

Ter **duas energias no nível 3 ou mais** libera uma técnica híbrida:

| Combinação | Técnica |
|---|---|
| Ki + Mana | Lâmina Arcana |
| Mana + Espiritual | Luz Arcana |
| Ki + Vital | Fúria Bestial |
| Espiritual + Vital | Cura da Natureza |
| Ki + Espiritual | Punho Sagrado |
| Mana + Vital | Magia Selvagem |

Lembre que o nível 3 também depende de conhecimento (precisa de pelo menos 16).

## Combate

O combate abre em **tela cheia**: seu personagem à esquerda, o inimigo em **pixel art** à direita, barras de vida e energia, e números de dano flutuando. Cada golpe tem uma **animação própria por tipo** (corte, estocada, esmagar, flecha, golpes rápidos, garras, fogo, gelo, raio, luz, sombra, natureza, arcano, onda de Ki, cura, escudo e vento).

### Seus golpes

Os botões de golpe incluem, quando você tem acesso:
- ataque da arma equipada (ou soco) e as técnicas da arma;
- Técnica de Ki, Magia, Curar-se;
- técnicas liberadas por nível de energia, híbridas, técnicas criadas por você, magias desbloqueadas e as das casas;
- poderes dos **caminhos** que você segue;
- Defender e Fugir.

Passe o mouse sobre um botão para ver contra o que ele é **forte e fraco**.

### Tipos de inimigo e elementos

Inimigos têm um tipo: humano, fera, morto-vivo, constructo, dragão, espírito ou viscoso. Cada elemento causa +30% contra alguns tipos e -25% contra outros. O resultado mostra "(vantagem)" ou "(desvantagem)".

| Elemento | Forte contra | Fraco contra |
|---|---|---|
| Físico | humanos, viscosos | espíritos, constructos |
| Fogo | mortos-vivos, viscosos, feras | dragões, espíritos |
| Gelo | feras, dragões | mortos-vivos, viscosos |
| Raio | constructos, dragões | viscosos, feras |
| Luz | mortos-vivos, espíritos | dragões |
| Sombra | humanos, feras | espíritos, mortos-vivos |
| Natureza | constructos, mortos-vivos | dragões, viscosos |
| Arcano | espíritos, constructos | humanos |

Com a habilidade **percepção**, o título do combate mostra a fraqueza do inimigo.

### Combos

Usar dois elementos em sequência dá +25% de dano e o jogo avisa "COMBO!".

| Primeiro | Depois | Combo |
|---|---|---|
| Fogo | Natureza | Queimada |
| Gelo | Raio | Congelamento |
| Luz | Sombra | Eclipse |
| Arcano | Fogo | Explosão Arcana |
| Físico | Raio | Impacto Elétrico |
| Natureza | Gelo | Geada Viva |
| Sombra | Físico | Golpe Sombrio |
| Luz | Físico | Lâmina Sagrada |

### Domínio de técnicas

Quanto mais você usa uma técnica, mais forte ela fica: com **10 usos** ganha ★ (+10% de poder); com **25 usos** vira ★★ (mais +20% de poder e custo 2 menor). Cada marco mostra um card "Dominou".

### Monstros

Lobos, javalis, ursos, raposas, cervos, corujas arcanas, morcegos, aranhas, esqueletos, zumbis, golens, espectros, lodos e slimes, wyverns e dragões, além de bandidos, cultistas, orcs, duelistas e campeões de casas. Cada um usa um desenho de pixel art (há cerca de 10 desenhos base, com cor própria por nome).

## Armas

Ação **Escolher ou comprar arma** (categoria Treino). Comprar custa 60. Cada arma tem 2 técnicas: a primeira vem ao equipar e a segunda abre depois de **10 usos** da arma. As armas também influenciam a guerra: se a arma combina com o tipo da tropa, a tropa ganha +10%.

| Arma | Forte contra | Fraca contra | Técnicas | Observação |
|---|---|---|---|---|
| Espada | humanos | constructos | Corte Cruzado, Estocada Rápida | equilibrada |
| Lança | feras, dragões | mortos-vivos | Investida de Lança, Barreira de Lanças | boa contra cavalaria na guerra |
| Machado | constructos, mortos-vivos | espíritos | Golpe Devastador, Fúria do Machado | deixa você exposto |
| Arco | dragões, espíritos | humanos | Chuva de Flechas, Tiro Certeiro | |
| Adaga | humanos | constructos, dragões | Golpe Furtivo, Lâmina Envenenada | |
| Maça | mortos-vivos | feras | Esmagar Ossos, Golpe Atordoante | atordoa |
| Cajado | espíritos | humanos | Pancada Arcana, Canalizar | |

## Caminhos e mestres

São **15 caminhos**, 3 poderes cada. Eles liberam poderes de combate conforme o nível da energia (o poder 1 no nível 1, e assim por diante).

| Energia | Caminhos |
|---|---|
| Ki | Punho de Ferro, Estilo do Dragão, Estilo da Águia, Corpo Absoluto, Mestre de Armas |
| Mana | Mago de Fogo, Necromante, Arquimago, Mago do Gelo |
| Espiritual | Paladino (exige Ki 2), Oráculo, Clérigo |
| Vital | Domador, Druida, Berserker |

### Como encontrar e treinar com um mestre

1. Ouça um **rumor** sobre o mestre: ao explorar, viajar, conversar com NPCs aventureiros, ouvir o bardo, descobrir lugares ou quando moradores viram mestres locais.
2. Use **Buscar mestre** (Caminhos): é um minigame de pistas. Vencer **desbloqueia o mestre para sempre**.
3. Use **Estudar com um mestre**: cada mestre tem **um minigame próprio** de treino (custa 25 de dinheiro e 15 de fôlego). Precisa de 50% ou mais para a lição valer.
4. A cada 2 lições bem-sucedidas você **desbloqueia uma magia** da energia do mestre.
5. Uma lição com mestre também conta como **fonte** da energia (libera níveis 4 e 5).

### Técnicas próprias

- **Desenvolver uma técnica própria** (conhecimento 10): você cria uma técnica. Seguir um caminho melhora as técnicas criadas (mais forte e mais barata, com o nome do caminho).
- **Combinar duas energias**: conhecimento 20 e duas energias no nível 2.
- **Vender, divulgar ou guardar** uma técnica.

### Magias desbloqueáveis (13)

| Energia | Magias |
|---|---|
| Ki | Soco Trovejante, Postura do Tigre, Golpe Sísmico |
| Mana | Seta de Mana, Véu Arcano, Corrente Elétrica, Meteoro Menor |
| Espiritual | Bênção Ardente, Escudo da Fé, Palavra de Silêncio |
| Vital | Espinhos Vivos, Pele de Casca, Enxame |

Como conseguir: lições de mestre, chefes de masmorra, a bruxa da floresta e a Casa certa (técnicas próprias).

### Passivas desbloqueáveis

Elas surgem sozinhas quando você repete uma atividade muitas vezes.

| Passiva | Efeito | Como conseguir |
|---|---|---|
| Sanguinário | +20% de dano contra humanos | matar 10 humanos em combate |
| Mãos Calejadas | +10% no salário | trabalhar 30 vezes |
| Língua de Prata | o afeto das pessoas cresce sozinho | socializar ou conversar 25 vezes |
| Mente Afiada | +1 conhecimento a cada 4 semanas | estudar 25 vezes |
| Coração Generoso | +1 fama a cada 8 semanas | fazer caridade 8 vezes |
| Passos Sombrios | reduz o quanto você é procurado | contrabando ou chantagem 5 vezes |
| Pé na Estrada | expedições rendem mais rumores | viajar ou explorar 8 vezes |
| Fôlego de Ferro | +5 fôlego por semana | descansar 30 vezes |
| Diplomata Nato | relações com reinos melhoram sozinhas | diplomacia 6 vezes |
| Veterano de Guerra | +10% de dano | 15 vitórias em combate |
| Saqueador de Masmorras | +30% de saque em masmorras | concluir 3 masmorras |
| Mão de Mestre | instituições rendem +20% | ensinar 15 vezes |
| Dedos de Ouro | minigames pagam +20% | 10 desafios do ofício |

## Ofícios e minigames

**Desafio do ofício** (Trabalho) é um minigame opcional que paga mais que trabalhar normal se você for bem. Cada ofício tem o seu.

| Ofício | Minigame |
|---|---|
| Agricultor | alvos móveis (colher antes da geada) |
| Artesão | timing (moldar a peça) |
| Comerciante | cálculo rápido (dar o troco) |
| Guarda | reflexo no sinal (prender o suspeito) |
| Estudioso | ordem crescente (organizar tomos) |
| Sacerdote | pares de símbolos |
| Pescador | equilíbrio (segurar a linha) |
| Ferreiro | segurar e soltar no ponto (aquecer o metal) |
| Avaliador | digitar o nome da gema |
| Curandeiro | sequência de ingredientes |
| Mensageiro | correr (cliques rápidos) |
| Mago | digitar a palavra de poder |
| Artista Marcial | reflexo (esquiva) |

Outras ações também têm minigame:
- **Criar poção** (alquimia): juntar elementos seguindo o **livro de alquimia**, passo a passo. Depois de 3 acertos da mesma receita o livro fecha e você precisa lembrar os passos. Receitas: Poção de Cura, Poção de Energia, Antídoto, Poção de Fúria, Elixir da Visão. A poção pode ser vendida ou usada na hora.
- **Pescar**: puxar o peixe sem deixar a linha arrebentar.
- **Caçar**: reflexo no sinal.
- **Plantar e colher**: sequência das estações.
- **Desenvolver artefato, poção ou manual** (instituição): minigame por energia.
- **Mestres**: um minigame fixo de treino e outro para encontrar cada um.
- **Masmorras**: desarmar armadilhas e resolver enigmas.

Mecânicas de minigame: saco de areia (cliques), timing, runas (sequência de cores), alvos, reflexo, segurar e soltar, cálculo, ordem crescente, equilíbrio, pares, digitar, alquimia e pesca.

**Pedir demissão** (Trabalho) deixa o emprego e não gasta tempo.

## Subsistência (comer sem dinheiro)

| Ação | Tempo | Resultado |
|---|---|---|
| Pescar | 1 semana | comida e algum dinheiro |
| Caçar | 2 semanas | comida e peles |
| Plantar e colher | 3 semanas | bastante comida |
| Fazenda (edifício) | passivo | +3 comida por semana |

## Edifícios

Ação **Comprar edifícios** (Negócios). Cada obra leva 3 semanas. Só dá para ter um de cada.

| Edifício | Preço | Efeito |
|---|---|---|
| Casa | 200 | +3 fôlego e +1 saúde por semana |
| Fazenda | 250 | +3 comida por semana |
| Oficina | 300 | +8 ouro por semana |
| Armazém | 180 | +4 ouro por semana |
| Barracão de treino | 350 | +1 treino aleatório por semana |
| Posto de Guarda | 400 | +1 fama a cada 8 semanas |

## Economia: estações, colheita, guerra e custo de vida

A economia já tinha 4 mercados (comida, ferramentas, luxo e remédios) com preços por oferta e demanda. Agora há mais camadas por cima:

- **Estações:** a comida é mais barata no outono (x0,85) e mais cara no inverno (x1,2). Os remédios sobem no inverno (x1,25), e o luxo sobe no verão e cai no inverno. Ferramentas variam pouco.
- **Colheita anual:** no começo do outono sorteia-se se a colheita foi ruim (20%, comida x1,3), farta (20%, comida x0,85) ou normal, valendo até o outono seguinte.
- **Guerra:** com algum reino em guerra com você, ferramentas ficam 25% mais caras, remédios 15% e comida 10%. O luxo cai 10%.
- **Salários dos NPCs:** acompanham o preço do mercado do seu ofício. Ofícios sem mercado próprio (guarda, estudioso, mago etc.) acompanham o custo de vida geral.
- **Custo de vida dos NPCs:** toda semana cada adulto paga comida, aluguel (se tem moradia) e 1% do que possui (o padrão de vida sobe com a riqueza). Isso freia o acúmulo: a riqueza média se estabiliza em vez de crescer sem parar. Aposentados pagam 70%.
- **Tratamento e moradia:** o preço do tratamento acompanha o preço dos remédios, e o limite de dinheiro para perder ou alugar uma moradia acompanha o custo de vida.
- O painel **Economia** mostra os preços atuais já com esses efeitos, a estação, a colheita, a guerra, o custo de vida semanal e o preço do tratamento.

## Vida própria dos NPCs

Cada pessoa da vila age por conta própria, mesmo sem você:

- **Necessidades:** quem fica sem dinheiro por muitas semanas passa necessidade. Ela é ajudada por um amigo mais rico ou troca de ofício para um que paga melhor. Quem não tem amigos procura companhia e faz amizade com alguém.
- **Plano de longo prazo:** cada NPC tem um plano ligado ao objetivo de vida (riqueza, aventura, família ou estudo) que avança toda semana. Ao completar, rende um marco: expandir os negócios, voltar rico (ou arruinado) de uma expedição, ter um filho, ou escrever um tratado. Quem passa necessidade avança mais devagar.
- **Família:** quem tem o objetivo de família e está solteiro procura um cônjuge da mesma espécie.
- **Moradia e saúde:** quem fica muito tempo sem dinheiro perde a casa e só aluga outra quando junta o suficiente. Fome e falta de teto desgastam a saúde, e quem tem dinheiro paga tratamento. Doenças podem aparecer e, sem cuidado, matar.
- **Pedidos a você:** NPCs com necessidade ou perto de completar o plano pedem sua ajuda: dinheiro, sociedade em negócio, patrocínio de tratado, convite para expedição ou contribuição para um casamento. Cada pedido tem escolhas e consequências.
- **Boatos:** de vez em quando a vila comenta a situação de alguém na crônica.
- **Crises e ajuda:** quem passa fome, adoece ou está prestes a perder a casa recebe dinheiro de familiares (cônjuge, pais, filhos) ou amigos mais ricos.
- **Dívidas:** se ninguém ajuda, a pessoa pega um empréstimo (25) com alguém rico e paga aos poucos quando melhora. Quem não consegue pagar por muito tempo dá o calote e vira rival do credor. A situação aparece como "endividado".
- **Traços importam:** Lealdade alta faz o NPC ajudar com mais dinheiro e Lealdade baixa o faz recusar com frequência. Ambição alta cobra juros maiores nos empréstimos. Coragem alta escala as brigas mais rápido e Coragem baixa evita o conflito. Curiosidade alta acelera os planos de estudo e aventura.
- **Você nas disputas:** quando dois rivais estão em guerra aberta, eles pedem seu apoio: você escolhe um lado ou tenta mediar. Quando um credor cobra um devedor, você pode pagar parte da dívida, apoiar o credor ou não se meter.
- **Chegadas e partidas:** recém-chegados se estabelecem na vila quando ela tem menos de 50 moradores. Quem está sem moradia há muito tempo, sozinho e sem família, pode deixar a vila.
- **Partido nas brigas:** quando alguém perde uma briga pública, até 2 familiares ou amigos leais (Lealdade acima de 50) podem tomar seu partido e passar a rivalizar com o vencedor.
- **Troca de ofício por escolha:** de vez em quando o NPC avalia qual ofício combina mais com seus traços (Ambição pesa o salário; Coragem, Lealdade e Curiosidade favorecem ofícios como Guarda, Sacerdote ou Estudioso) e troca se a diferença valer a pena.
- **Marcos de plano com variedade:** riqueza pode render expansão, grande contrato ou prejuízo; aventura pode render expedição bem-sucedida, fracasso ou tesouro; estudo pode render um tratado ou uma escola com discípulo.
- **Intensidade do mundo:** o botão "Mundo" no topo alterna entre calmo, normal e turbulento. Calmo reduz pela metade a frequência de doenças, brigas, calotes e partidas e ajuda um pouco o dinheiro dos NPCs. Turbulento quase dobra essas frequências e drena um pouco o dinheiro. A escolha fica salva no jogo.
- **Aposentadoria e herança:** NPCs idosos (a partir de 70% da expectativa de vida da espécie) se aposentam, deixam de receber salário e passam parte dos bens e o negócio a um filho adulto, ao cônjuge ou a um discípulo. Quando um NPC morre, a herança (60% das posses e o negócio) vai para os mesmos herdeiros. Quem parte da vila aparece como "partiu da vila", e não como falecido.
- **Pessoas notáveis:** um painel mostra os 3 mais ricos, os 3 mais queridos por você e os 3 mais populares (amigos e família), com clique para abrir a ficha.
- **Convites jogáveis (duram cerca de 5 semanas):**
  - **Casamentos:** vá com presente (20), de mãos vazias ou falte.
  - **Funerais:** ajude a família (10), só compareça ou falte.
  - **Batizados:** seja padrinho (20), só compareça ou falte. Ser padrinho aumenta o afeto dos pais e da criança por você.
  - **Aniversários de idosos queridos:** leve um presente (10), visite ou falte.
  - **Julgamentos de briga:** quando a guarda multa dois rivais, você pode defender um deles (ele recupera a multa e o outro perde afeto por você) ou pedir clemência para os dois, com 50% de chance de perdoar as multas.
  - **Festa de cada estação:** contribua (15), só participe ou fique em casa. Se você for adulto e solteiro, há também a opção de se aproximar de alguém solteiro de idade parecida, o que aumenta o afeto dessa pessoa (o pedido de casamento exige afeto 50+).
- **Relatório do mundo:** um painel mostra a população, a riqueza média e mediana, a porcentagem de NPCs passando necessidade, sem moradia, endividados, doentes e aposentados, as rivalidades ativas e os acontecimentos do ano atual e do anterior (doenças, brigas, empréstimos, calotes, partidas, heranças). Quando algo foge do normal, ele sugere ajustar a intensidade do mundo.
- **Teto de população e ritmo:** os botões "População" (pequena 40, média 60, grande 90) e "Ritmo" (lento, normal, rápido) controlam quantos moradores a vila comporta e a velocidade dos nascimentos e das chegadas de forasteiros. O Relatório do mundo mostra os valores atuais e avisa quando a vila está no teto ou com menos da metade dele. As escolhas ficam salvas no jogo.
- **Rivalidades que escalam:** o rival mais rico prejudica o outro nos negócios. Depois de repetidos incidentes vira briga pública (o perdedor perde saúde e dinheiro) e, por fim, a guarda multa os dois ou eles fazem as pazes e viram amigos.
- **Histórico:** os últimos 8 acontecimentos de cada pessoa ficam na ficha, com a semana, do mais recente ao mais antigo.
- Na ficha da pessoa (quando você a conhece) aparecem **Situação** e **Plano**. Os acontecimentos aparecem na crônica quando você conhece a pessoa; os demais aparecem só às vezes.

## Status e cards de conquista

- **Área "Status"** (abaixo da ficha do personagem), com 6 abas:
  - **Habilidades:** as 4 energias (Ki, Mana, Espiritual, Vital) com nível, energia máxima, as 5 habilidades de cada uma (perícia que dá e poder de combate), e as bloqueadas com o nível que as libera.
  - **Bônus:** dano em combate, dano recebido, renda dos caminhos, sustento dos companheiros e energias máximas com o multiplicador da espécie.
  - **Passivas:** o efeito de cada uma e, nas que você ainda não tem, o progresso até desbloquear.
  - **Artefatos:** os que você tem e o que cada um faz. Os que faltam aparecem só como uma contagem.
  - **Companheiros:** bônus de dano, consumo de comida e efeitos especiais (como o Dragão).
  - **Caminhos:** bônus e poderes de cada caminho escolhido.
- **Card de conquista**, no estilo dos jogos de sobrevivência: ao ganhar uma habilidade, passiva, artefato, companheiro ou caminho, aparece um card com ícone, nome, tipo e os efeitos embaixo. Há quatro cores de raridade, e artefatos são os mais raros. Enter ou espaço passam para o próximo card, e o tempo automático pausa enquanto há card aberto.
- Os ícones são emojis sobre um fundo colorido gerado a partir do nome. Para usar imagens próprias, basta trocar a função `icon`.
- Em saves antigos, o que você já tinha não gera card: só o que for conquistado a partir de agora.

## Pessoas

- **Socializar, pedir ajuda, presentear, propor parceria, pedir em casamento, ter filhos.** Casamento aparece quando há alguém solteiro, adulto e com afeto 30 ou mais (o pedido exige afeto 50).
- **Conversar:** o diálogo depende do objetivo e das lembranças do NPC e pode revelar lugares, dicas de mercado, a opinião sobre o governo e sobre as raças.
- **Apoiar e ensinar:** patrocinar, ensinar uma técnica sua, ensinar uma energia, ou tornar a pessoa **discípulo** (afeto 40+). Discípulos prestam serviços.
- As pessoas têm visão própria sobre a sua espécie (simpatia, neutralidade, desconfiança ou hostilidade).
- Pessoas conversam entre si, brigam, fazem fofoca sobre as suas decisões e chegam e partem com o tempo.

### Órfãos e protegidos

Ação **Órfãos: adotar, apoiar e educar**.
- **Adotar um jovem órfão** (30): ele vira seu protegido (12 a 15 anos).
- **Apoiar os órfãos da vila** (40): ajuda a todos, dá fama e ânimo ao povo.
- **Fundar ou ampliar o orfanato** (150 × nível, até o nível 3): custa 5 por nível por semana e traz novos órfãos sozinho.
- **Educar o protegido selecionado** (20): mais ajuda e um foco de energia.

Quanto mais ajuda eles recebem, mais devoção sentem. Aos 18 anos aparece um evento: **convidar a servi-lo**, apoiar a carreira própria ou deixar partir. Quem tem devoção alta serve você de bom grado e rende dinheiro toda semana. Os mais fanáticos podem ter eventos de **zelo excessivo**. Protegidos não podem ser escolhidos para casamento nem filhos.

## Negócios, equipe e dinheiro

Abrir e gerir negócios, propaganda, expansão, venda, desenvolver produto, contrato com a nobreza, comprar e vender lotes de mercadorias (comida, ferramentas, luxo, remédios), contratar pessoas, dar ordens, dispensar, fundar e ampliar guilda (guilda exige fama 20).

## Grandes casas

São 6 casas, cada uma com luta, magia, técnicas, relíquias e relações próprias. Você começa conhecendo só a **Casa Valmor**. As outras são descobertas ao explorar e viajar. Novas casas podem nascer com o tempo.

| Casa | Raça | Luta | Magia | Mercado negro |
|---|---|---|---|---|
| Valmor | Humana | Esgrima Real | Selos de Ordem | não |
| Khazrim | Anã | Martelo Rúnico | Runas de Forja | não |
| Sylvaren | Élfica | Arco Lunar | Magia da Lua | não |
| Rakkar | Povo-fera | Caça em Matilha | Instinto Selvagem | sim |
| Nocthar | Mista | Lâminas Sombrias | Sombras Proibidas | sim |
| Solenn | Mista | Ordem Sagrada | Preces e Milagres | não |

Técnicas de casa: Estocada Real, Guarda Real, Martelo Rúnico, Runa de Pedra, Flecha Lunar, Névoa Lunar, Investida da Matilha, Uivo Aterrador, Lâmina Sombria, Véu de Sombras, Golpe Sagrado Maior e Bênção de Solenn. Relíquias: Espada de Valmor, Brasão Real, Martelo-Trovão, Armadura Rúnica, Arco Lunar, Manto de Prata, Presa Ancestral, Pele de Alfa, Adaga do Silêncio, Anel do Contrabando, Cálice Sagrado e Cetro da Fé.

Efeitos das relíquias que você possui (somam): mais dano, saúde por semana, fôlego por semana, ouro por semana, ou fama.

### O que fazer com uma casa (ação "Relações com as grandes casas")

| Opção | Requisito | Resultado |
|---|---|---|
| Presentear (50) | | sobe a relação |
| Duelo ritual contra o campeão | saúde 50+ | vencer dá relação e, na primeira vitória, uma relíquia |
| Pedir ensinamentos (40) | relação 35+ | aprende uma técnica da casa |
| Comprar relíquia (150) | relação 25+ | ganha uma relíquia |
| Tornar-se sócio do mercado negro | relação 20+, casa com mercado negro | renda semanal, mas aumenta o "procurado" |
| Denunciar o mercado negro | casa com mercado negro | fama e ânimo, mas a casa o odeia |
| Provocar rivalidade (60) | | piora a relação entre a casa e outra |
| **Jurar lealdade** | relação 50+ | vira **membro**: renda semanal, ganha com as vitórias da casa e perde com as derrotas; tem **missões** e **postos** |
| Contribuir com ouro (100) | ser membro | fortalece a casa |

**Missões e postos da casa:** a cada tantas semanas a casa pede um serviço (caçar uma ameaça, escoltar um comboio ou investigar uma casa rival). Cada missão sobe seu posto (Recruta, Soldado, Capitão, Braço-direito). A cada 3 missões você ganha uma técnica da casa; a cada 6, uma relíquia.

## Mundo que cresce sozinho

Mesmo sem ações suas, o mundo muda e tudo aparece no painel **Mundo e metas** (Crônica do mundo, Grandes casas, Era do mundo).

- **Grandes casas:** a cada 12 semanas acontece algo entre as casas: aliança, guerra, casamento, escândalo de mercado negro ou **golpe de estado** (uma casa forte toma o reino da casa governante, marcada com 👑). Se você for o rei, aparece um evento de golpe (lutar, negociar ou fugir).
- **Gerações:** a cada 52 semanas as casas passam de geração e podem desenvolver **técnicas e relíquias novas**. Uma casa muito poderosa pode se **dividir** e gerar uma casa nova (até 9 casas).
- **Reinos:** os reinos fazem guerra entre si e tomam vilas uns dos outros. De vez em quando uma revolta funda um **reino novo**.
- **Mestres locais:** moradores abrem escolas e viram mestres, gerando rumores.
- **Aldeburgo:** prospera (novas vagas e moradores) quando o povo está contente e encolhe quando está descontente.
- **Masmorras novas** aparecem com o tempo.
- **Eras** (a cada 104 semanas, em ciclo):

| Era | Efeito |
|---|---|
| Paz | o ânimo do povo cresce e as guerras diminuem |
| Expansão | chegam mais moradores e surgem novas masmorras |
| Guerra | reinos e casas lutam mais |
| Magia | magias e técnicas ficam 10% mais fortes |

### Política, raças e reinos

- O **ânimo do povo** reage a impostos, leis e guerras. Ânimo muito baixo causa emigração e revolta.
- **Raças:** existe uma matriz de afinidade, uma tensão racial e um respeito por raça. Isso muda o afeto dos NPCs por você, as chances em vagas e eventos. A ação **Promover convivência entre raças** (fama 8+) reduz a tensão.
- **Reinos:** cada reino conhecido tem relação com você. **Diplomacia** (30) sobe a relação e pode virar **aliança** (relação 60+), que rende comércio. Relação ruim leva a ameaça e **guerra**.
- **Viajar** (a lugares descobertos): comerciar, ouvir rumores, estudar com mestres locais ou convidar alguém a morar em Aldeburgo. Pode haver perigo na estrada.
- **Mudar-se para outro reino ou vila** (40): você vai com família e equipe, e cada cidade guarda as próprias pessoas e vagas. Títulos e cargos ficam para trás.
- **Explorar além do mapa:** expedição de 3 etapas com eventos (trilha bloqueada, acampamento, criatura, ruínas, tempestade, eremita) e uma descoberta no fim.

### Eventos aleatórios (exemplos)

Mercador ambulante, briga na taverna, festival, órfão pedindo ajuda, boato sobre você, duelista rival, bruxa da floresta, eclipse, mapa de tesouro, bardo e inspeção do senhor. Além das crises que crescem com o seu poder (invasão, epidemia, cisma entre raças, ultimato de um reino).

### Metas

O jogo sempre mantém 2 metas ativas (fama, dinheiro, lugares descobertos, aliados, população, afeto, vitórias, ânimo do povo). Cumprir uma paga recompensa e gera uma meta maior, sem fim.

## Masmorras

Descubra masmorras explorando, viajando, ouvindo o bardo ou seguindo um mapa de tesouro. A ação **Explorar uma masmorra** (25 de fôlego, 50 de saúde) leva você por 4 a 6 andares:
- monstros (combate), armadilhas (minigame para desarmar), enigmas (minigame), baús (podem ser iscas), salas de descanso;
- no último andar há um **chefe**.
- **Recuar** a qualquer andar mantém o saque.
- Vencer o chefe dá fama, saque maior e uma **magia nova**.

## Instituições (carreira de energia)

Categoria **Instituição**. Para **fundar** uma (200, conhecimento 15) você precisa da energia no **nível 3**. Cada energia tem a sua: **Dojo** (Ki), **Torre da Magia** (Mana), **Templo** (Espiritual) e **Círculo da Natureza** (Vital).

| Ação | O que faz |
|---|---|
| Ensinar alunos | renda, fama e discípulos; técnicas suas rendem mais |
| Desenvolver artefato, poção ou manual | minigame; depois **vender**, **guardar em segredo** (renda e influência) ou **divulgar** ao povo (fama e afeto) |
| Desafiar uma instituição rival | combate contra o mestre rival; vencer fecha o rival, dá fama e alunos |
| Ampliar a instituição | mais alunos, renda e influência (até o nível 4) |

A influência da instituição conta no poder político: dojo (militar), torre (acadêmica), templo (religiosa) e círculo (econômica).

## Torre dos Magos

Ação **Torre dos Magos: contratar magos** (Poder), disponível com fama 15 ou Mana nível 1.
- **Contrato da corte** (80 + 10 por semana, até 3): influência acadêmica e magos mais fortes na guerra, com um mago extra no início de cada guerra.
- **Mago pessoal** (100 + 8 por semana, até 2): luta ao seu lado em todo combate, com o elemento dele.
- Quem tem a sua própria Torre da Magia paga 30% menos. Sem dinheiro, os magos vão embora.

## Poder político e o reino

| Ação | Requisito |
|---|---|
| Pleitear título de nobreza | fama aproximada de metade do exigido |
| Disputar cargo político | fama aproximada de metade do exigido |
| Fazer lobby | cargo 1+, título 1+ ou ser o senhor |
| Propor lei | ser o senhor ou ter cargo 2+ |
| Decretar uma medida | ser o senhor ou ter cargo 3+ |
| Enviar embaixada | ser o senhor ou ter cargo 3+ |
| Dar um golpe de Estado (na vila) | cargo 2+ ou título 2+ |
| **Golpe contra o rei** | ser o senhor da vila, fama 40+, 300 de dinheiro |

Títulos: Plebeu, Cavaleiro, Barão, Conde, Duque. Cargos: Sem cargo, Conselheiro da Vila, Magistrado, Governador da Vila, Chanceler do Reino.

### Golpe contra o rei

Se o golpe **falhar, você morre** (fim de jogo). Se vencer, você governa o reino: aparece o painel **Reino** com ouro, comida, terras, impostos e 12 regiões que podem ser desenvolvidas ou fortificadas.

### Guerra em hexágonos

Ação **Declarar guerra a um reino** (custa 100 de ouro do reino). Abre um mapa de 37 hexágonos com terrenos (planície, floresta, montanha, pântano). Sua capital fica à esquerda e a inimiga à direita (★).

**Como jogar:** escolha o tipo de tropa e a raça, clique num hexágono seu vazio para recrutar, clique num exército seu e depois num hexágono vizinho para dar a ordem. As ordens rodam ao avançar a semana. Exércitos gastam ouro e comida (sem comida eles enfraquecem). Tome a capital inimiga para vencer (despojos e regiões); se a sua capital cair, você é deposto.

| Tropa | Custo | Vantagem |
|---|---|---|
| Lanceiros | 20 | vencem cavalaria |
| Espadachins | 25 | vencem lanceiros e arqueiros |
| Arqueiros | 25 | vencem lanceiros, magos e clérigos |
| Cavalaria | 40 | vence arqueiros e magos (fraca em floresta e montanha) |
| Magos | 45 | vencem espadachins, lanceiros e guerreiros Ki |
| Guerreiros Ki | 40 | vencem magos e arqueiros |
| Clérigos | 35 | vencem feras; curam |
| Feras | 30 | vencem arqueiros e clérigos |

**Raças e terrenos:** humano rende mais na planície, elfo na floresta, anão na montanha, povo-fera no pântano (+25%). Floresta e montanha dão bônus de defesa. Elfos são melhores arqueiros, anões melhores infantes, povo-fera melhores cavaleiros e feras.

**O que aumenta a força das tropas:** nível das energias (Ki para guerreiros, Mana para magos, Espiritual para clérigos, Vital para feras), arma equipada compatível, profissão (Ferreiro, Mestre de Armas, Guarda), relíquias e magos contratados da corte.

## Submundo e mercado negro

O submundo se desbloqueia quando você abre uma taverna, vira mercenário, fica procurado ou tem influência no submundo. Inclui chantagem, contrabando, contrato de servidão, libertar servos, comprar animal ou artefato raro, redes criminosas e suborno. Algumas grandes casas (Rakkar, Nocthar) fazem parte do mercado negro e você pode se tornar sócio delas.

## Limitações conhecidas

- O balanceamento (preços, danos, chances, ritmo de eventos) não foi testado em partidas longas jogadas à mão.
- A pixel art dos monstros é simples (cerca de 10 desenhos base, com cor própria por nome).
- Vários minigames compartilham a mesma mecânica com temas e parâmetros diferentes.
- Origens e predisposições só valem em partidas novas.
- O jogo é um único arquivo grande, montado em camadas. Mudanças futuras podem precisar de reorganização do código.
