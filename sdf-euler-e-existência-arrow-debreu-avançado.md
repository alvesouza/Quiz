---
quiz: "SDF, Euler e Existência — Arrow-Debreu (avançado)"
tags:
  sdf: "SDF e precificação"
  euler: "Equação de Euler intertemporal"
  existencia: "Existência: Brouwer e Kakutani"
  falha: "Onde a existência falha"
  incompletos: "Eficiência restrita (GP, Hart)"
  macro: "Aplicações macro-finanças"
---

## sdf

Q: O fator de desconto estocástico $m_s$ tende a ser alto exatamente:
- Nos estados bons, em que o consumo já se encontra bem abundante
- Nos estados de maior probabilidade objetiva atribuída pelo agente
- Nos estados com o maior payoff agregado de toda a economia
- Nos estados ruins, em que a utilidade marginal do consumo é alta
<!-- YW5zOjM= -->
> O SDF carrega a utilidade marginal relativa: vale mais um real entregue no estado ruim (onde $v'$ é alta). Por isso claims que pagam no mau estado são caros — embutem um prêmio de seguro.
> Ref: Aula 6 Bloco 4 "SDF"; MWG §19.E

Q: Pela equação fundamental, o preço de um ativo $j$ com payoffs $X_{js}$ é:
- $q_j=\sum_s \pi_s m_s X_{js}$ (payoff esperado ponderado pelo SDF)
- $q_j=\sum_s \pi_s X_{js}$ (payoff esperado sob probabilidades objetivas)
- $q_j=\sum_s m_s X_{js}$ (payoff somado sem ponderar por probabilidade)
- $q_j=\max_s m_s X_{js}$ (maior payoff descontado entre os estados)
<!-- YW5zOjA= -->
> Preço $=$ valor esperado do payoff ponderado pelo SDF. Como $q_s=\pi_s m_s$, isso equivale a $q_j=\sum_s q_s X_{js}$ — a fórmula de não-arbitragem.
> Ref: Aula 6 Bloco 4 "SDF + Euler"

Q: As probabilidades neutras ao risco $\tilde\pi_s$ são definidas como:
- $\tilde\pi_s=\pi_s\, m_s$ (probabilidade vezes o fator de desconto)
- $\tilde\pi_s=\pi_s/\sum_k \pi_k$ (probabilidades objetivas renormalizadas)
- $\tilde\pi_s=q_s/\sum_k q_k$ (preços de estado normalizados a somar 1)
- $\tilde\pi_s=m_s/\sum_k m_k$ (fatores de desconto simplesmente normalizados)
<!-- YW5zOjI= -->
> A medida neutra ao risco reescala os preços de estado para somarem 1; precifica como se o agente fosse neutro, descontando à taxa livre de risco. Equivale a $\pi_s m_s/\sum_k \pi_k m_k$.
> Ref: Aula 6 Bloco 4; precificação por não-arbitragem

Q: A taxa bruta livre de risco $R_f$ implícita nos preços de estado é:
- $R_f=\sum_s q_s$ (a própria soma dos preços de estado da economia)
- $R_f=\sum_s \pi_s$ (a soma das probabilidades objetivas dos estados)
- $R_f=\sum_s \pi_s\, m_s^2$ (segundo momento do SDF sob a medida física)
- $R_f=1/\sum_s q_s$ (inverso do preço do título que paga 1 em todo estado)
<!-- YW5zOjM= -->
> O título sem risco paga 1 em todo estado, logo custa $\sum_s q_s$; seu retorno bruto é o inverso, $R_f=1/\sum_s q_s$. Sob preços justos, $\sum_s q_s=\sum_s \pi_s=1$ e $R_f=1$.
> Ref: Aula 6 Bloco 4

Q: Preços atuarialmente justos ($q_s=\pi_s$) correspondem a um SDF que é:
- Crescente nos estados ruins, refletindo uma forte aversão ao risco
- Constante entre estados, refletindo neutralidade ao risco na precificação
- Decrescente na probabilidade do estado, refletindo puro otimismo
- Nulo no estado livre de risco, refletindo ausência de desconto
<!-- YW5zOjE= -->
> $q_s=\pi_s$ significa $m_s=q_s/\pi_s=1$ constante: nenhum estado é descontado de forma diferenciada, exatamente a precificação neutra ao risco.
> Ref: Aula 5 Bloco 2; Aula 6 Bloco 4

## euler

Q: Na equação de Euler intertemporal, o SDF entre $t$ e $t+1$ é:
- $m_{t+1}=u'(c_t)/u'(c_{t+1})$ (razão invertida das utilidades, sem desconto)
- $m_{t+1}=\beta\, u'(c_t)$ (utilidade marginal corrente descontada por $\beta$)
- $m_{t+1}=\beta\, R_{t+1}$ (retorno bruto descontado pelo fator $\beta$)
- $m_{t+1}=\beta\, u'(c_{t+1})/u'(c_t)$ (TMS intertemporal descontada por $\beta$)
<!-- YW5zOjM= -->
> O SDF intertemporal é a taxa marginal de substituição entre consumo de hoje e de amanhã, descontada pela impaciência $\beta$. É a versão dinâmica de $m_s=v'(c_s)/\lambda$.
> Ref: Aula 6 Bloco 4 "Equação de Euler intertemporal"

Q: A condição que precifica qualquer retorno bruto $R_{t+1}$ é:
- $1=\E_t[m_{t+1}\, R_{t+1}]$ (custo de poupar igual ao benefício esperado)
- $1=\E_t[m_{t+1}]\cdot\E_t[R_{t+1}]$ (produto das esperanças, ignora covariância)
- $R_f=\E_t[m_{t+1}\, R_{t+1}]$ (taxa livre de risco igual ao valor esperado)
- $0=\E_t[m_{t+1}+R_{t+1}]$ (soma esperada do SDF com o retorno é nula)
<!-- YW5zOjA= -->
> A condição de Euler $1=\E_t[m_{t+1}R_{t+1}]$ vale para todo ativo: o custo marginal de poupar uma unidade iguala o benefício esperado descontado pelo SDF.
> Ref: Aula 6 Bloco 4

Q: Na lógica do SDF, o prêmio de risco de um ativo decorre de:
- Sua variância total, independentemente da correlação com o consumo
- Sua probabilidade de retorno positivo no período seguinte
- Sua covariância negativa com o fator de desconto estocástico
- Seu retorno médio descontado pela inflação esperada do período
<!-- YW5zOjI= -->
> De $1=\E[mR]$ vem $\E[R]-R_f=-R_f\,\mathrm{Cov}(m,R)$: ativos com covariância negativa com o SDF (pagam pouco no estado ruim, caro) exigem retorno esperado maior.
> Ref: Aula 6 Bloco 4

## existencia

Q: O Teorema de Brouwer basta para a existência de equilíbrio quando:
- O excesso de demanda agregada é uma correspondência de valores convexos
- O excesso de demanda agregada é uma função contínua dos preços
- As preferências são lineares e a demanda resulta multivalorada
- A economia tem um agente representativo com utilidade quaselinear
<!-- YW5zOjE= -->
> Brouwer é um ponto fixo para funções contínuas do simplex nele mesmo; serve quando a demanda é função. Se a demanda é correspondência, precisa-se de Kakutani.
> Ref: Aula 6 Bloco 1 "Brouwer (1911)"

Q: A demanda agregada vira uma correspondência (e não função) quando:
- As preferências não são estritamente convexas (indiferenças planas ou com bico)
- As preferências são estritamente convexas e diferenciáveis (demanda única)
- A economia tem um único bem físico negociado (escolha trivial)
- As dotações são interiores e estritamente positivas (orçamento regular)
<!-- YW5zOjA= -->
> Sem convexidade estrita, a cesta ótima pode ser um conjunto (segmentos de indiferença), tornando a demanda multivalorada — daí a necessidade de Kakutani.
> Ref: Aula 6 Bloco 1 "Quando Brouwer falha — Kakutani"

Q: Para aplicar Kakutani à correspondência de excesso de demanda, ela deve ter:
- Valores sempre unitários e variação linear nos preços de mercado
- Valores não-vazios, convexos e compactos, com gráfico fechado
- Continuidade de Lipschitz e derivada limitada em toda parte
- Monotonicidade estrita em cada uma das coordenadas de preço
<!-- YW5zOjE= -->
> Kakutani estende Brouwer a correspondências de valor não-vazio, convexo e compacto, com gráfico fechado (semicontinuidade superior) — condições satisfeitas pelo excesso de demanda.
> Ref: Aula 6 Bloco 1 "Kakutani"

Q: A condição de fronteira (desejabilidade) na prova de existência serve para:
- Garantir que a demanda seja diferenciável no interior do simplex
- Manter os preços de equilíbrio estritamente positivos
- Assegurar que o núcleo da economia de trocas seja não-vazio
- Tornar o excesso de demanda homogêneo de grau um nos preços
<!-- YW5zOjE= -->
> Quando algum preço tende a zero a demanda explode (bem desejável), empurrando o ponto fixo para o interior — assim o equilíbrio tem todos os preços estritamente positivos.
> Ref: Aula 6 Bloco 1 "Sketch — existência em economia AD"

## falha

Q: A existência de equilíbrio walrasiano pode falhar quando:
- As preferências são contínuas, convexas e localmente não saciadas
- Existe um título de Arrow negociável para cada estado da natureza
- O excesso de demanda satisfaz a Lei de Walras e a homogeneidade
- Há não-convexidades relevantes nas preferências ou na produção
<!-- YW5zOjM= -->
> Não-convexidades quebram a hipótese de valores convexos de Kakutani; sem ela, o ponto fixo pode não existir e o equilíbrio pode falhar.
> Ref: Aula 6 Bloco 1 "Onde existência pode falhar"

Q: A hipótese de sobrevivência (ponto mais barato) é necessária porque:
- Sem ela, o núcleo da economia de trocas se torna automaticamente vazio
- Ela garante que todos os agentes da economia sejam avessos ao risco
- Ela impõe que os preços de estado somem exatamente um no simplex
- Sem dotação interior, a demanda pode ser descontínua no orçamento
<!-- YW5zOjM= -->
> Se o agente não consegue ficar abaixo de sua restrição (sem ponto mais barato), a demanda pode saltar na fronteira, quebrando a continuidade exigida na prova.
> Ref: Aula 6 Bloco 1

## incompletos

Q: Em mercados incompletos, o equilíbrio é, no melhor caso:
- Pareto-eficiente pleno, exatamente como em mercados completos
- Estritamente ineficiente, sem nenhuma noção possível de otimalidade
- Constrained Pareto-eficiente, eficiente só dado o span de ativos
- Eficiente em sentido forte, via transferências lump-sum adequadas
<!-- YW5zOjI= -->
> Dado o conjunto limitado de ativos, o melhor alcançável é a eficiência "restrita" a esse span; em geral há perda relativa ao ótimo de mercados completos.
> Ref: Aula 6 Bloco 3 "constrained PE"

Q: Geanakoplos-Polemarchakis (1986) mostraram que, em mercados incompletos:
- O equilíbrio é genericamente nem mesmo constrained-eficiente
- O equilíbrio é Pareto-eficiente pleno, como em AD completo
- A adição de ativos jamais altera o bem-estar dos agentes
- A Lei de Walras deixa de valer no comércio sequencial
<!-- YW5zOjA= -->
> Mesmo um planejador restrito ao mesmo span de ativos costuma conseguir melhorar o bem-estar: o equilíbrio incompleto é, genericamente, constrained-ineficiente.
> Ref: Aula 6 Bloco 3 "Geanakoplos-Polemarchakis (1986)"

Q: O resultado de Hart (1975) sobre abrir um novo mercado de ativos é que ele:
- Eleva o bem-estar de todos, por ampliar o conjunto de seguros
- Não tem efeito algum, pois o equilíbrio já era Pareto-eficiente
- Pode reduzir o bem-estar de todos, mudando preços relativos dos ativos
- Restaura a completude e os dois Teoremas do Bem-Estar Social
<!-- YW5zOjI= -->
> Como o equilíbrio incompleto não é eficiente, efeitos de preço de segunda ordem ao adicionar um ativo podem prejudicar a todos — a intuição "mais mercados, melhor" falha.
> Ref: Aula 6 Bloco 3 "Hart (1975)"

## macro

Q: Interpretar a SELIC como um "SDF macro" é vê-la como:
- A taxa que desconta fluxos futuros na precificação de ativos
- O preço de um seguro específico contra o estado de recessão
- A probabilidade objetiva do estado de alta inflação futura
- O prêmio de risco exigido pelo investidor marginal do mercado
<!-- YW5zOjA= -->
> A taxa básica funciona como o desconto agregado que precifica fluxos futuros — o análogo macro do fator de desconto que precifica ativos contingentes.
> Ref: Aula 6 Bloco 4 "Box Brasil — SELIC como SDF macro"

Q: Ver o VIX como "preço de Arrow do estado de stress" significa que ele mede:
- A probabilidade física de ocorrer uma crise no próximo período
- Quanto custa um claim que paga justamente nos estados ruins de mercado
- O retorno médio esperado da carteira de mercado no período
- A taxa livre de risco ajustada pela inflação corrente da economia
<!-- YW5zOjE= -->
> Um VIX alto reflete preço alto para proteção contra estados ruins — exatamente o preço de Arrow elevado desses estados, onde a utilidade marginal é alta.
> Ref: Aula 6 Bloco 4 "Box Mundo — VIX"

Q: O Tesouro IPCA+ aproxima um ativo contingente porque seu payoff real:
- É fixo e idêntico em todos os possíveis estados da natureza
- Independe por completo de qualquer estado futuro da economia
- É indexado ao estado da natureza dado pela inflação realizada
- Paga no estado específico de deflação observada no período
<!-- YW5zOjI= -->
> Ao corrigir pelo IPCA, o título entrega um payoff real que depende do estado inflacionário realizado — um passo concreto rumo a bens contingentes ao estado.
> Ref: Aula 6 Bloco 3 "Box Brasil — Tesouro IPCA+"
