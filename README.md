# Fotografia do Cerrado

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
| [`galeria.html`](galeria.html) | Cinco espécies com filtro (mamíferos/aves) e foto ampliada, com o nome, o nome científico e o texto; passa para a anterior e a próxima pelos botões, pelas setas do teclado ou deslizando o dedo |
| [`expedicoes.html`](expedicoes.html) | “Quando ir?” (escolher o mês e ver a estação e as saídas na melhor época), três saídas fotográficas, as regras de campo e as perguntas frequentes (abrem sem JavaScript) |
| [`sobre.html`](sobre.html) | Missão, público e a paleta com os contrastes medidos |
| [`contato.html`](contato.html) | Formulário (de demonstração: nada é enviado) |
| [`creditos.html`](creditos.html) | Autor e licença de cada foto |

### Scripts

| Arquivo | O que faz |
|---|---|
| `js/tema-inicio.js` | No `<head>`, sem `defer`: aplica o tema escolhido antes de desenhar a página |
| `js/tema.js` | O botão de tema: troca e guarda a escolha; sem escolha, segue o sistema |
| `js/menu.js` | O menu do celular, com o `aria-expanded` em dia |
| `js/galeria.js` | O filtro (mamíferos/aves) e a foto ampliada num `<dialog>`, com anterior e próxima (botões, setas do teclado e deslizar) |
| `js/quando.js` | O “Quando ir?”: os 12 meses no idioma da página (pelo `Intl`), a estação e o selo “Melhor época” em cada expedição |
| `js/contato.js` | O formulário: valida e confirma o que foi preenchido (o site é estático, nada é enviado) |

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
