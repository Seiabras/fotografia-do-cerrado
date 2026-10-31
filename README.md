# Guia do Cerrado

> Antes, Fotografia do Cerrado. Em 31/10/2026 virou um guia do bioma; o nome novo vale em português, e as outras línguas
> continuam com o nome antigo até a tradução.

> **In English:** a fictional wildlife photography studio from the Brazilian Cerrado. It began as a small interface for
> a colour palette and WCAG assignment (CEUB, 2026/2) and grew into a full site, in 13 languages, with light and dark
> modes. Live: https://cerrado.linupedia.com.br

Site de uma empresa fictícia de fotografia de fauna do cerrado. Comecei como a mini interface da atividade de paletas
de cores e WCAG da disciplina de Desenvolvimento de Interfaces (CEUB, 2026/2) e depois transformei num site completo.

**No ar:** https://cerrado.linupedia.com.br

## Páginas

| Página | O que tem |
|---|---|
| [`index.html`](index.html) | Abertura com foto, as últimas fotos e por que o cerrado importa |
| [`galeria.html`](galeria.html) | Cinco espécies com filtro (mamíferos/aves) e foto ampliada, com o nome, o nome científico e o texto; passa para a anterior e a próxima pelos botões, pelas setas do teclado ou deslizando o dedo. Em português, cada foto leva à ficha da espécie, e o “Do tamanho de quê?” compara os cinco com a altura de uma pessoa |
| `especie-*.html` | Uma ficha por espécie: as 5 com foto (lobo-guará, tamanduá-bandeira, arara-canindé, seriema, tucano-toco) e, desde 31/10, as outras 65 espécies do catálogo do guia; em 1/11, mais 44 espécies novas, já com ficha (todas as 114 têm ficha), com “Foto em breve” até a foto chegar em `img/especies/`. Nas fichas: medidas, o que come, quando aparece, como reconhecer, como fotografar, onde a gente vê e o bicho em escala ao lado de uma pessoa de 1,70 m. Desde 1/11, 36 fichas têm “Não confunda com”: 21 pares de espécies parecidas lado a lado, com a diferença numa frase. Só em português |
| [`diario.html`](diario.html) | Diário de campo: três relatos de expedição, com links para a ficha e para o contato já preenchido. Só em português |
| [`como-fotografamos.html`](como-fotografamos.html) | A regra de distância, a luz, o equipamento, a edição e de onde vêm as fotos do site. Só em português |
| [`404.html`](404.html) | A página de erro, com endereços absolutos (aparece em qualquer caminho que não existe) |
| [`expedicoes.html`](expedicoes.html) | “Quando ir?” (escolher o mês e ver a estação e as saídas na melhor época), três saídas fotográficas, o mapa dos três parques (em português), as regras de campo e as perguntas frequentes (abrem sem JavaScript) |
| [`sobre.html`](sobre.html) | Missão, público, a paleta com os contrastes medidos e, em português, o “Teste as cores”: escolher texto e fundo da paleta e ver a razão de contraste e se passa no AA e no AAA |
| [`contato.html`](contato.html) | Formulário (de demonstração: nada é enviado), que chega preenchido com a expedição e o mês (`?expedicao=emas&mes=7`); em português, com o mês da viagem e o quadro “Sua saída” |
| [`creditos.html`](creditos.html) | Autor e licença de cada foto |

### Scripts

| Arquivo | O que faz |
|---|---|
| `js/tema-inicio.js` | No `<head>`, sem `defer`: aplica o tema escolhido antes de desenhar a página |
| `js/tema.js` | O botão de tema: troca e guarda a escolha; sem escolha, segue o sistema |
| `js/menu.js` | O menu do celular, com o `aria-expanded` em dia |
| `js/galeria.js` | O filtro (mamíferos/aves) e a foto ampliada num `<dialog>`, com anterior e próxima (botões, setas do teclado e deslizar) |
| `js/quando.js` | O “Quando ir?”: os 12 meses no idioma da página (pelo `Intl`), a estação e o selo “Melhor época” em cada expedição |
| `js/contato.js` | O formulário: preenche pelo endereço, mostra o erro embaixo do campo assim que a pessoa sai dele (a frase é a do navegador, no idioma de quem visita), monta o quadro “Sua saída” e confirma o que foi preenchido (o site é estático, nada é enviado) |
| `js/contraste.js` | O “Teste as cores” da página Sobre, com a fórmula de contraste da WCAG 2.2 |

## Guia do cerrado (31/10/2026)

Pedido de 31/10: “o site mais completo sobre o cerrado do mundo”, em português primeiro. O site passa a ser um guia do
bioma, com a parte de expedições em segundo plano. Cada número tem fonte (a página `fontes.html`, numerada).

| Página | O que tem |
|---|---|
| [`index.html`](index.html) | Em português, a inicial do guia: três números, as portas para cada parte e algumas espécies |
| [`bioma.html`](bioma.html) | Onde fica (mapa dos biomas do IBGE 2019, com botões para destacar cada um), quanto de cada estado é Cerrado (calculado aqui), clima, solo, fogo e biodiversidade, com índice que acompanha a leitura |
| [`paisagens.html`](paisagens.html) | As 11 fitofisionomias de Ribeiro e Walter (Embrapa) num corte desenhado: tocar num trecho mostra a ficha dele |
| `paisagem-*.html` | Uma página por paisagem (11): o desenho dela entre as vizinhas do corte (ou a foto, quando houver), como reconhecer, por que importa, onde ver (os parques de Onde ver) e as espécies dela, tiradas do catálogo |
| [`especies.html`](especies.html) | O catálogo: 70 espécies (bichos e plantas), com busca (sem acento), filtro por grupo e por paisagem, só as ameaçadas (lista nacional) e o calendário das frutas nativas. Cada paisagem leva às espécies dela (`?paisagem=vereda`) |
| [`agua.html`](agua.html) | O berço das águas: quanto de cada grande rio nasce no Cerrado (Embrapa), a esponja, os aquíferos e Águas Emendadas |
| [`povos.html`](povos.html) | Os povos do Cerrado: indígenas, Kalunga, geraizeiros, quebradeiras de coco babaçu e outros |
| [`ameacas.html`](ameacas.html) | Quanto já se perdeu (MapBiomas), o desmatamento ano a ano (PRODES/INPE), onde ele acontece, quanto está protegido e o que dá para fazer |
| [`onde-ver.html`](onde-ver.html) | Onde ver o Cerrado: 13 parques numerados sobre o mapa dos biomas, com o que se vê em cada um (posições aproximadas) |
| [`busca.html`](busca.html) | Buscar no guia (1/11): espécies (nome comum ou científico), paisagens, parques, povos, glossário, Mês a mês e páginas, sem acento e sem servidor; o índice (cerca de 200 itens) vai dentro da página; a lupa fica no menu (`js/busca.js`) |
| [`roteiro.html`](roteiro.html) | Monte sua visita (1/11): escolha o parque e o mês e veja a estação, as paisagens, as espécies para procurar (os destaques do parque primeiro) e o que acontece no mês (`js/roteiro.js`) |
| [`mes-a-mes.html`](mes-a-mes.html) | O Cerrado mês a mês (1/11): escolha o mês e veja o que floresce, que fruta está madura, que bicho aparece e o que acontece na paisagem; 23 acontecimentos, cada um com a fonte da ficha (`js/mes-a-mes.js`) |
| [`como-ajudar.html`](como-ajudar.html) | Como ajudar o Cerrado (1/11): registrar, denunciar (Ibama, 193, 190), socorrer um bicho, comprar, plantar e evitar o fogo, com “Vou fazer isto” guardado no navegador (`js/como-ajudar.js`) |
| [`aprender.html`](aprender.html) | Quiz de 16 perguntas por tema (com explicação e link para o guia), “Qual é esta espécie?” (desde 1/11: dez espécies por partida, adivinhadas pelas pistas das fichas, com “Mais uma pista”), “Qual paisagem é esta?” (o desenho do corte, sem o nome, e três opções) e um glossário com busca (`js/aprender.js`) |
| [`fontes.html`](fontes.html) | As fontes numeradas de cada número do guia |

O script é o `js/guia.js`. As quatro partes pedidas estão prontas (o bioma e as paisagens; fauna e flora; água, povos e ameaças; aprender brincando). Em português, o menu tem as partes do guia; Expedições e Sobre ficam no rodapé. São 32 fontes numeradas. Fotos novas entram sozinhas: `img/especies/<id>.webp` e `<id>-640.webp`, com o crédito em
`img/especies/creditos.json` (e o mesmo em `img/paisagens/`).

## Só em português por enquanto (31/10/2026)

O pedido de 31/10 foi melhorar primeiro em português e traduzir depois. Por isso:

- **Páginas só em português:** as cinco fichas (`especie-*.html`), o `diario.html`, o `como-fotografamos.html` e o
  `404.html`. Estão listadas no `ferramentas/estudo/fotografia-do-cerrado/so-pt.json` do `linu-sites`, com o texto direto
  no modelo.
- **Trechos só em português nas outras páginas** (entre `{{?pt-BR}}` e `{{/pt-BR}}` no modelo): o “Diário” no menu e
  “Como fotografamos” no rodapé; “Ver a ficha” na galeria e na inicial; o “Do tamanho de quê?” da galeria; o mapa das
  Expedições; o “Teste as cores” do Sobre; o mês da viagem e o quadro “Sua saída” do Contato; o “Mapa e fontes” dos
  créditos.
- **Para traduzir:** trocar o texto por chaves nos 13 `textos/<código>.json`, tirar os `{{?pt-BR}}` e esvaziar o
  `so-pt.json`. Até lá, as páginas nas outras 12 línguas ficam como estavam em 31/10, com o “Quando ir?”, a foto ampliada
  nova e o contato preenchido, que já funcionam em todas.

## Caderno de campo (31/10/2026)

A identidade é a de um caderno de campo, sem mexer na paleta da atividade:

- **Títulos e nomes científicos na Newsreader** (licença OFL, `fontes/OFL.txt`), servida pelo próprio site, só com o
  alfabeto latino (48 KB nos dois arquivos). O texto continua na fonte do aparelho; em japonês, coreano e chinês os
  títulos também.
- **Fotos sem caixa em volta**, como numa revista. Na inicial, no computador, a primeira foto ocupa a altura das outras
  duas; no tablet, vai de lado a lado.
- **Os números do cerrado** em tipografia grande separada por fios, no lugar dos três cartões iguais.
- **Expedições:** no computador, o “Quando ir?” fica parado numa coluna ao lado da lista; no celular, os meses rolam de
  lado, e cada mês tem embaixo a cor da estação (oliva nas chuvas, areia no começo da seca, marrom no auge).
- **Fotos em WebP**, cada uma com uma versão de 640 px para o celular (`srcset`): as páginas abrem com 33 a 86 KB no
  celular.
- **Troca de página suave** (View Transitions), com o cabeçalho parado; nada se mexe com “menos movimento” ligado.

## Paleta e acessibilidade

As cores vêm do próprio bioma, e cada uma foi testada pela fórmula de contraste da WCAG 2.2:

| Cor | Uso | Contraste |
|---|---|---|
| `#814F12` | primária (cabeçalho, botões) | 6,86:1 com branco |
| `#7E7450` | oliva | 4,67:1 com branco |
| `#C8985A` | areia (selos) | 8,09:1 com preto |
| `#CFA58C` | terra (faixas) | 9,41:1 com preto |
| `#6E6465` | texto secundário | 5,72:1 com branco |

Regra que segui: as cores escuras levam texto branco e as claras, texto preto. Todo texto da página fica acima de
4,5:1 (nível AA). Também tem link para pular ao conteúdo, foco visível, menu que funciona pelo teclado e textos
alternativos em todas as fotos. No modo escuro, as amostras de areia e terra da página Sobre continuam com texto preto,
e os links do rodapé têm pelo menos 24 px de altura. Conferido com o axe 4.10 em 31/10/2026, nos dois modos: nenhuma
falha em nenhuma página.

## Idiomas

O site está em 13 idiomas: português do Brasil na raiz e `/pt-pt/`, `/es/`, `/ca/`, `/nl/`, `/en/`, `/fr/`, `/de/`,
`/it/`, `/intl/` (inglês internacional), `/ja/`, `/ko/` e `/zh-hant/`, com os outros idiomas no rodapé (o formulário de contato responde no idioma da página) e as
alternativas de cada página para os buscadores. As páginas de cada idioma são geradas no repositório do
[Linu Sites](https://github.com/Seiabras/linu-sites) (o modelo e os textos ficam em `ferramentas/estudo/fotografia-do-cerrado/`); aqui ficam as
páginas prontas. As frases que o script escreve vão num `<script type="application/json">` em cada página.

## Modo claro e escuro

Segue o tema do sistema e tem um botão no topo para trocar, que guarda a escolha. O `js/tema-inicio.js` aplica o tema
antes de pintar (sem piscar a página clara) e o `js/tema.js` cuida do botão. As cores do modo escuro também foram
medidas pela fórmula de contraste da WCAG, com a mesma regra do modo claro.

## Fotos

Todas são do [Wikimedia Commons](https://commons.wikimedia.org/), com licença livre (CC BY, CC BY-SA ou CC0), e
foram apenas redimensionadas e convertidas para WebP. O autor e a licença de cada uma estão na página de créditos e em
`img/creditos.json`.

## Como abrir

É só abrir o `index.html` no navegador; não tem build nem dependência.

## Segurança

Segue a política de segurança dos sites do Linu Sites: tudo vem do próprio endereço, sem CDN e sem estilo ou script
dentro do HTML (por isso não há nenhum `style="…"`: tudo está em classes no `css/estilo.css`).
