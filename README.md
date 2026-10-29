# Fotografia do Cerrado

Site de uma empresa fictícia de fotografia de fauna do cerrado. Comecei como a mini interface da atividade de paletas
de cores e WCAG da disciplina de Desenvolvimento de Interfaces (CEUB, 2026/2) e depois transformei num site completo.

**No ar:** https://cerrado.linupedia.com.br

## Páginas

| Página | O que tem |
|---|---|
| [`index.html`](index.html) | Abertura com foto, as últimas fotos e por que o cerrado importa |
| [`galeria.html`](galeria.html) | Cinco espécies com filtro (mamíferos/aves) e foto ampliada |
| [`expedicoes.html`](expedicoes.html) | Três saídas fotográficas e as regras de campo |
| [`sobre.html`](sobre.html) | Missão, público e a paleta com os contrastes medidos |
| [`contato.html`](contato.html) | Formulário (de demonstração: nada é enviado) |
| [`creditos.html`](creditos.html) | Autor e licença de cada foto |

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
alternativos em todas as fotos.

## Fotos

Todas são do [Wikimedia Commons](https://commons.wikimedia.org/), com licença livre (CC BY, CC BY-SA ou CC0), e
foram apenas redimensionadas. O autor e a licença de cada uma estão na página de créditos e em `img/creditos.json`.

## Como abrir

É só abrir o `index.html` no navegador; não tem build nem dependência.

## Segurança

Segue a política de segurança dos sites do Linu Sites: tudo vem do próprio endereço, sem CDN e sem estilo ou script
dentro do HTML (por isso não há nenhum `style="…"`: tudo está em classes no `css/estilo.css`).
