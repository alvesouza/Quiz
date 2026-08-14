# Quiz

Quizzes e simulados interativos em HTML para Microeconomia e Teoria de Ativos
(MWG, Arrow-Debreu, Radner, SDF/Euler). Cada arquivo é uma página autocontida:
abre no navegador, responde, corrige na hora — sem instalação, sem servidor.

**Índice online:** <https://alvesouza.github.io/Quiz/>

## Conteúdo

| Quiz | Tema |
| --- | --- |
| [MWG — Part 1A: Preference, Choice & Classical Demand (Ch 1–3)](mwg-part-1a-preference-choice-classical-demand-ch-13.html) | Preferências, escolha e demanda clássica |
| [MWG — Part 1B: Aggregate Demand, Production & Uncertainty (Ch 4–6)](mwg-part-1b-aggregate-demand-production-uncertainty-ch-46.html) | Demanda agregada, produção e incerteza |
| [Demanda Agregada — MWG Cap. 4](demanda-agregada-mwg-cap-4.html) | Agregação de demanda |
| [Follow-up — Demanda Agregada (Gorman, SMD, Grandmont)](follow-up-demanda-agregada-gorman-smd-grandmont.html) | Gorman, Sonnenschein-Mantel-Debreu, Grandmont |
| [Arrow-Debreu — Aulas 5-6](arrow-debreu-aulas-5-6.html) | Equilíbrio geral com mercados completos |
| [Arrow-Debreu e Radner — Aulas 5-6](arrow-debreu-e-radner-aulas-5-6.html) | Equilíbrio de Radner e mercados sequenciais |
| [SDF, Euler e Existência — Arrow-Debreu (avançado)](sdf-euler-e-exist%C3%AAncia-arrow-debreu-avan%C3%A7ado.html) | Fator estocástico de desconto e equação de Euler |
| [Simulado — Sessão 1: Prices, Payoffs, and the Discount Factor](simulado-sess%C3%A3o-1-prices-payoffs-and-the-discount-factor.html) | Simulado (Cochrane, Cap. 1) |

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

## Adicionar um quiz

1. Suba o `.html` — na raiz ou em qualquer subpasta.
2. Pronto: o índice o mostra na próxima carga, com o título derivado do nome do
   arquivo.
3. Opcional: para um título mais bonito, acrescente o caminho ao mapa `TITLES`
   em [`index.html`](index.html) (é onde ficam os títulos que vêm do `<h1>` de
   cada quiz, e também o que alimenta a lista de reserva quando a API falha).

Os rótulos saem do título: `Simulado`, `Follow-up`, `Gabarito` ou `Quiz`.

## Publicar

Settings → Pages → Deploy from branch → `main` / `/ (root)`. O site fica em
`https://<usuário>.github.io/Quiz/`.

Para rodar local, basta abrir `index.html` no navegador; os quizzes funcionam
normalmente, e o índice usa a lista embutida se a API estiver bloqueada.
