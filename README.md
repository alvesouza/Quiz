# Quiz

Quizzes e simulados interativos para Microeconomia e Teoria de Ativos
(MWG, Arrow-Debreu, Radner, SDF/Euler). Cada quiz é um arquivo **Markdown**;
[`quiz.html`](quiz.html) é o player que o lê e corrige na hora — sem
instalação, sem build.

**Índice online:** <https://alvesouza.github.io/Quiz/>

## Conteúdo

Cada link abre o player com o `.md` correspondente (`quiz.html#<arquivo>.md`).

| Quiz | Questões | Tema |
| --- | --- | --- |
| [MWG — Part 1A: Preference, Choice & Classical Demand (Ch 1–3)](quiz.html#mwg-part-1a-preference-choice-classical-demand-ch-13.md) | 24 | Preferências, escolha e demanda clássica |
| [MWG — Part 1B: Aggregate Demand, Production & Uncertainty (Ch 4–6)](quiz.html#mwg-part-1b-aggregate-demand-production-uncertainty-ch-46.md) | 20 | Demanda agregada, produção e incerteza |
| [Demanda Agregada — MWG Cap. 4](quiz.html#demanda-agregada-mwg-cap-4.md) | 10 | Agregação de demanda |
| [Follow-up — Demanda Agregada (Gorman, SMD, Grandmont)](quiz.html#follow-up-demanda-agregada-gorman-smd-grandmont.md) | 8 | Gorman, Sonnenschein-Mantel-Debreu, Grandmont |
| [Arrow-Debreu — Aulas 5-6](quiz.html#arrow-debreu-aulas-5-6.md) | 30 | Equilíbrio geral com mercados completos |
| [Arrow-Debreu e Radner — Aulas 5-6](quiz.html#arrow-debreu-e-radner-aulas-5-6.md) | 24 | Equilíbrio de Radner e mercados sequenciais |
| [SDF, Euler e Existência — Arrow-Debreu (avançado)](quiz.html#sdf-euler-e-exist%C3%AAncia-arrow-debreu-avan%C3%A7ado.md) | 20 | Fator estocástico de desconto e equação de Euler |
| [Simulado — Sessão 1: Prices, Payoffs, and the Discount Factor](quiz.html#simulado-sess%C3%A3o-1-prices-payoffs-and-the-discount-factor.md) | 30 | Simulado (Cochrane, Cap. 1) |
| [Follow-up — Session 1: the four confusions](quiz.html#quiz-followup-sessao-01-sdf-2026-08-16.md) | 31 | SDF, cov(m,x), medidas, registro histórico |

Os `.html` antigos (exports autocontidos, com o `.md` embutido) continuam no
repositório e funcionando, mas o índice mostra o `.md` no lugar deles.

## O índice (`index.html`)

A página inicial lista tudo e navega por pastas. Como o GitHub Pages é estático
e uma página não consegue enumerar o próprio diretório, o índice faz **uma**
chamada à API do GitHub (`git/trees/HEAD?recursive=1`), recebe a árvore inteira
do repositório e monta a navegação no cliente. Na prática:

- **arquivos novos aparecem sozinhos** — não é preciso editar o índice ao subir
  um quiz ou criar uma pasta;
- pastas são navegação de verdade: breadcrumbs, `.. voltar` e rotas por hash
  (`#/micro-2/extra`), então cada pasta tem URL própria, linkável;
- a busca cobre o repositório todo, não só a pasta atual;
- o dono/repositório é detectado pela URL, então fork ou renomeação continuam
  funcionando.

Se a API não responder — limite de 60 requisições/hora sem autenticação, ou
abertura local via `file://` — o índice cai para uma lista embutida com os
quizzes atuais, e a barra de status diz em qual modo está. Arquivos fora dessa
lista só aparecem quando a API voltar a responder.

Sem dependências externas: um único arquivo, HTML + CSS + JS. Tema claro/escuro
(segue o sistema, com alternador) e `/` para focar a busca.

O índice lê o título de cada quiz da linha `quiz:` do frontmatter (busca
preguiçosa, cacheada na sessão), então **não é preciso cadastrar nada** ao subir
um `.md` novo. O mapa `TITLES` em [`index.html`](index.html) é só reserva, para
quando a API do GitHub não responde.

## Adicionar um quiz

1. Suba o `.md` — na raiz ou em qualquer subpasta.
2. Pronto. O índice o mostra na próxima carga, com o título vindo do frontmatter
   e o link apontando para `quiz.html#<caminho>.md`.

Não há passo de export, nem HTML a gerar. Os rótulos saem do título:
`Simulado`, `Follow-up`, `Gabarito` ou `Quiz`.

### O formato

```markdown
---
quiz: "Título do quiz"
tags:
  tema: "Rótulo do Tema"
---

## tema

Q: Enunciado, com $\LaTeX$ inline.
- Alternativa A
- Alternativa B
<!-- YW5zOjA= -->            ← base64("ans:0"), 0-indexed
> Explicação.
> Ref: Livro, Cap. N (p. X)
```

Sem linha em branco entre as alternativas, o comentário da resposta e as linhas
`>`. Um `P:` antes de um bloco de `Q:` define um enunciado compartilhado, e vale
até o próximo `P:` ou `##`.

## Publicar

Settings → Pages → Deploy from branch → `main` / `/ (root)`. O site fica em
`https://<usuário>.github.io/Quiz/`.

Para rodar local é preciso um servidor — o player busca o `.md` por `fetch`, que
o navegador bloqueia em `file://`:

```bash
python -m http.server
```

Abrindo `index.html` direto do disco, o índice ainda lista (com a lista de
reserva) e o player continua aceitando um `.md` arrastado para a área de upload.
