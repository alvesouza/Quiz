---
quiz: "Arrow-Debreu e Radner — Aulas 5-6"
tags:
  risco: "Utilidade esperada, risco e seguro"
  contingentes: "Bens contingentes e R^{LS}"
  equilibrio: "Equilíbrio AD, SDF e seguro completo"
  existencia: "Existência e TBE estendidos"
  radner: "Radner e comércio sequencial"
  ativos: "Mercados de ativos e não-arbitragem"
  incompletos: "Mercados incompletos e Hart"
---

## risco

Q: Sob o axioma de von Neumann-Morgenstern, a utilidade de uma loteria é avaliada como:
- A esperança das utilidades de Bernoulli, $\sum_s \pi_s v(c_s)$ (linear nas probabilidades)
- A utilidade de Bernoulli do prêmio médio, $v(\sum_s \pi_s c_s)$ (linear dentro dos prêmios)
- A soma simples das utilidades, $\sum_s v(c_s)$ (sem ponderar pelas probabilidades)
- O maior prêmio medido em utilidade, $\max_s v(c_s)$ (critério maximin, ignora $\pi_s$)
<!-- YW5zOjA= -->
> A utilidade esperada é linear nas probabilidades: pondera $v(c_s)$ pelos $\pi_s$. Avaliar $v$ no prêmio esperado seria o caso de neutralidade ao risco (Jensen), não a definição geral.
> Ref: N&S Cap 7; J-R §2.1; MWG §6.B

Q: Um agente é avesso ao risco quando sua função de Bernoulli $v$ é:
- Convexa, e então prefere a loteria justa ao valor esperado (prêmio de risco negativo)
- Linear, e então fica indiferente entre loteria e valor esperado (prêmio de risco nulo)
- Crescente, e então valoriza mais riqueza em qualquer cenário (sem relação com risco)
- Côncava, e então prefere o valor esperado à loteria justa (prêmio de risco positivo)
<!-- YW5zOjM= -->
> Concavidade de $v$ equivale a aversão ao risco: por Jensen, $\E[v(c)]<v(\E[c])$, logo o agente paga um prêmio para trocar a loteria pelo certo. Monotonicidade (crescente) é independente da atitude ao risco.
> Ref: N&S Cap 7; MWG §6.C

Q: Diante de uma perda possível e de seguro atuarialmente justo, um agente avesso ao risco compra:
- Cobertura parcial, retendo de propósito parte do risco residual
- Nenhuma cobertura, pois o prêmio justo não alteraria seu bem-estar
- Cobertura acima da perda, usando a apólice como aposta no sinistro
- Cobertura integral, igualando a riqueza líquida nos dois estados
<!-- YW5zOjM= -->
> Com prêmio justo, a reta orçamentária tem inclinação igual à razão de probabilidades; a tangência com a indiferença avessa ocorre na diagonal de consumo igual — cobertura integral (o resultado de seguro completo).
> Ref: N&S Cap 7 (Insurance), Ex. 7.4; MWG §6.C

Q: Na abordagem state-preference, a "renda contingente" $(c_1,c_2)$ representa:
- O consumo médio dos estados, ponderado pelas probabilidades
- O prêmio de risco que se paga para evitar a loteria
- O consumo de cada estado da natureza, tratado como bens distintos
- A dotação certa, comum e idêntica em todos os estados
<!-- YW5zOjI= -->
> State-preference indexa o consumo por estado: $c_1$ e $c_2$ são bens contingentes distintos. É exatamente a porta de entrada para o espaço $\mathbb{R}^{LS}$ de Arrow-Debreu.
> Ref: N&S Cap 7 (State-Preference, p. 232), Ex. 7.7

## contingentes

Q: Um "bem contingente" em Arrow-Debreu é definido como:
- Um ativo que paga o mesmo valor em todos os estados
- Um bem físico indexado pelo estado em que será entregue
- Um bem cujo preço acompanha a probabilidade do estado
- Uma promessa de entrega válida sob qualquer estado futuro
<!-- YW5zOjE= -->
> A mesma mercadoria em estados diferentes vira bens distintos; é a reindexação que transporta toda a teoria de equilíbrio geral para o ambiente com incerteza.
> Ref: Aula 5 Bloco 1; N&S Cap 7; MWG §19.B

Q: Com $L$ mercadorias e $S$ estados, o espaço de bens do modelo é:
- $\mathbb{R}^{L+S}$, justapondo as mercadorias e os estados
- $\mathbb{R}^{L}$, pois a incerteza não cria mercadorias novas
- $\mathbb{R}^{LS}$, com uma coordenada por par mercadoria-estado
- $\mathbb{R}^{S}$, pois apenas os estados importam ao consumo
<!-- YW5zOjI= -->
> Cada mercadoria passa a existir em cada estado: $L\times S$ bens contingentes. Essa multiplicação (não soma) é o que permite reaproveitar os teoremas de EG.
> Ref: Aula 5 Bloco 1 "Estados, bens contingentes, R^{LS}"

Q: Tratar o tempo como um caso particular de estado permite:
- Eliminar de vez a necessidade de probabilidades no modelo
- Restringir a economia a um único período de negociação
- Tornar todos os preços independentes da data de entrega
- Unificar incerteza e troca intertemporal no mesmo aparato
<!-- YW5zOjM= -->
> Indexar bens por data é formalmente o mesmo que indexá-los por estado; por isso Arrow-Debreu cobre risco e intertemporalidade com a mesma álgebra.
> Ref: Aula 5 Bloco 1 "Tempo é caso particular de estado"

## equilibrio

Q: Um mercado é completo, no sentido de Arrow-Debreu, quando:
- Todos os agentes compartilham a mesma informação completa sobre os estados
- Os preços de cada ativo coincidem exatamente com as probabilidades dos estados
- Não incidem quaisquer custos de transação sobre a negociação dos ativos
- Há tantos ativos independentes quantos estados, gerando toda transferência
<!-- YW5zOjM= -->
> Completude é uma propriedade do span: $S$ ativos independentes (posto $=S$) tornam alcançável qualquer padrão de consumo contingente. Informação e custos são hipóteses auxiliares.
> Ref: Aula 5 Bloco 2; MWG §19.E

Q: A condição de primeira ordem da UMP com utilidade esperada e preços de Arrow $q_s$ é:
- $v'(c_s)=\lambda$ para todo estado $s$ (utilidade marginal igual entre estados)
- $\pi_s\, v'(c_s)=\lambda\, q_s$ para todo estado $s$ (utilidade marginal ponderada)
- $\pi_s=\lambda\, q_s$ para todo estado $s$ (probabilidade proporcional ao preço)
- $v'(c_s)=q_s$ para todo estado $s$ (utilidade marginal igual ao preço de estado)
<!-- YW5zOjE= -->
> Derivando $\sum_s \pi_s v(c_s)-\lambda(\sum_s q_s c_s-W)$ em $c_s$, a utilidade marginal ponderada pela probabilidade iguala o preço de estado vezes $\lambda$.
> Ref: Aula 5 Bloco 2 "Equação fundamental do SDF"

Q: O fator de desconto estocástico (SDF) que precifica os ativos é:
- $m_s=\pi_s/q_s$, a probabilidade sobre o preço de estado (inverso do núcleo)
- $m_s=q_s\,\pi_s$, o produto do preço pela probabilidade (peso conjunto)
- $m_s=v'(c_s)$, a utilidade marginal do estado (não normalizada por $\lambda$)
- $m_s=q_s/\pi_s$, o preço de estado sobre a probabilidade (núcleo de precificação)
<!-- YW5zOjM= -->
> O SDF é preço de estado por unidade de probabilidade; pela CPO, $m_s=q_s/\pi_s=v'(c_s)/\lambda$. Ele precifica qualquer ativo via $q_j=\sum_s \pi_s m_s X_{js}$.
> Ref: Aula 5 Bloco 2; Aula 6 Bloco 4

Q: Com Bernoulli côncava e preços justos ($q_s=\pi_s$), o consumo ótimo fica:
- Crescente na probabilidade, com $c_s\propto\pi_s$ (proporcional ao risco)
- Concentrado no estado provável, com $c_s$ máximo nele (aposta no provável)
- Constante entre estados, com $c_s$ igual em todo $s$ (seguro completo)
- Igual à dotação de cada estado, com $c_s=\omega_s$ (ausência de troca)
<!-- YW5zOjI= -->
> Preços justos na CPO dão $v'(c_s)=\lambda$ constante; por $v'$ injetora, $c_s$ é constante. O agente avesso suaviza o consumo entre estados.
> Ref: Aula 5 Bloco 4 "Resultado canônico"; MWG §19.C

Q: $v(c)=\ln c$, $\pi=(\tfrac34,\tfrac14)$, preços justos $q=(\tfrac34,\tfrac14)$ e dotação $\omega=(100,20)$. O ótimo $c^*$ é:
- $(100,20)$
- $(75,25)$
- $(80,80)$
- $(60,60)$
<!-- YW5zOjI= -->
> Log côncava + preços justos ⟹ $c^*$ constante. O nível vem do orçamento $q\cdot c=q\cdot\omega=\tfrac34(100)+\tfrac14(20)=80$, e como $q_1+q_2=1$, $c^*=(80,80)$.
> Ref: Simulado 1 Q4a; Aula 5 Bloco 4

## existencia

Q: O Teorema de Brouwer assegura, para uma função contínua do simplex nele mesmo:
- A unicidade do equilíbrio competitivo de preços relativos (regularidade global)
- A existência de ao menos um ponto fixo de preços (que zera o excesso de demanda)
- A eficiência de Pareto da alocação resultante de equilíbrio (1º Teorema)
- A não-vacuidade do núcleo da economia de trocas (estabilidade de coalizões)
<!-- YW5zOjE= -->
> Continuidade sobre um compacto convexo garante $f(p^*)=p^*$; usando Walras e homogeneidade, o ponto fixo zera o excesso de demanda. Unicidade e eficiência são questões à parte.
> Ref: Aula 6 Bloco 1 "Brouwer (1911)"

Q: Passa-se de Brouwer para Kakutani precisamente quando:
- A demanda agregada é uma correspondência, e não uma função
- A economia analisada tem um único bem físico negociável
- As preferências são sempre lineares nos preços de mercado
- A incerteza desaparece por completo do ambiente do modelo
<!-- YW5zOjA= -->
> Sem convexidade estrita, a demanda pode ser um conjunto; Kakutani estende o ponto fixo a correspondências de valor convexo e gráfico fechado.
> Ref: Aula 6 Bloco 1 "Quando Brouwer falha — Kakutani"

Q: Em mercados completos, a validade do 1º Teorema do Bem-Estar:
- Exige adicionalmente neutralidade ao risco (funções de Bernoulli lineares)
- Reaproveita a prova sem incerteza (bens contingentes como comuns)
- Restringe-se ao caso de exatamente dois estados (cardinalidade mínima)
- Depende de probabilidades idênticas entre agentes (crenças homogêneas)
<!-- YW5zOjE= -->
> Bens contingentes são bens comuns em $\mathbb{R}^{LS}$; a prova do 1º TBE (com NSL) vale linha a linha. A eficiência é avaliada ex-ante.
> Ref: Aula 5 Bloco 3 "1º TBE — prova reaproveitada"

## radner

Q: O equilíbrio de Radner descreve uma economia na qual:
- Todos os contratos contingentes abrem num único leilão inicial
- Ativos são negociados antes e bens à vista em cada estado depois
- Não há ativos financeiros; negociam-se diretamente os bens contingentes
- Os mercados são, por construção, mercados sem completude
<!-- YW5zOjE= -->
> Radner é a versão sequencial: poucas negociações de ativos seguidas de mercados spot por estado. A pergunta central é quando isso reproduz o equilíbrio AD.
> Ref: Aula 6 Bloco 2 "Setup formal de Radner"; MWG §19.D

Q: A equivalência entre Radner e Arrow-Debreu exige, essencialmente, que:
- A matriz de payoffs dos ativos tenha posto completo (gere $\mathbb{R}^S$)
- Exista um único ativo livre de risco a ser negociado (apenas o bond)
- Todos os agentes sejam neutros ao risco no modelo (utilidade linear)
- Haja no máximo dois estados possíveis da natureza (cardinalidade baixa)
<!-- YW5zOjA= -->
> Posto completo significa que carteiras geram todo $\mathbb{R}^S$, replicando qualquer transferência contingente; aí as restrições sequenciais equivalem à de AD.
> Ref: Aula 6 Bloco 2 "Equivalência AD↔Radner"

Q: Sob posto completo, as restrições orçamentárias sequenciais de Radner:
- Tornam-se estritamente mais apertadas que a de AD (factível menor)
- Permitem um consumo estritamente maior que em AD (orçamento folgado)
- Colapsam na única restrição de Arrow-Debreu (mesma alocação)
- Deixam de depender por completo dos preços dos ativos (preços neutros)
<!-- YW5zOjI= -->
> A carteira que financia qualquer plano contingente existe e custa exatamente o preço AD daquele plano; as restrições se fundem e o conjunto factível coincide.
> Ref: Aula 6 Bloco 2 "Equivalência — sketch"

Q: Com dois estados e ativos que geram $\mathbb{R}^2$, qualquer plano contingente é:
- Replicável por uma carteira dos ativos negociados (combinação que o reproduz)
- Atingível apenas com um título de Arrow por estado (Arrow puro exigido)
- Impossível de financiar sem um mercado AD completo (sequencial insuficiente)
- Indiferente aos preços dos ativos efetivamente negociados (custo nulo)
<!-- YW5zOjA= -->
> Span completo ($\mathbb{R}^2$) garante uma combinação de ativos que reproduz qualquer payoff $(z_1,z_2)$ — o passo de replicação da equivalência de Radner.
> Ref: Aula 6 Bloco 2 "Réplica numérica — bond + ação"

## ativos

Q: Dados preços e payoffs de ativos que geram $\mathbb{R}^S$, os preços de Arrow:
- Ficam unicamente determinados pela ausência de arbitragem (solução única)
- Dependem das probabilidades subjetivas de cada agente (preços heterogêneos)
- Exigem conhecer a aversão ao risco do investidor (preço preferência-dependente)
- Só existem se houver um ativo livre de risco no mercado (numerário exigido)
<!-- YW5zOjA= -->
> Com posto $S$, o sistema "preço $=$ payoff $\times$ preços de estado" tem solução única; a não-arbitragem fixa os $q_s$ sem precisar de probabilidades ou preferências.
> Ref: Aula 6 Bloco 4; precificação por não-arbitragem

Q: Estados 1 e 2. Ativo X paga $(3,1)$ e custa $1{,}90$; Y paga $(1,2)$ e custa $1{,}30$. Um claim $Z=(10,30)$ vale:
- $18$
- $19$
- $16$
- $17$
<!-- YW5zOjM= -->
> De $3q_1+q_2=1{,}90$ e $q_1+2q_2=1{,}30$: $q_1=0{,}50,\ q_2=0{,}40$. Então $P_Z=10(0{,}50)+30(0{,}40)=17$. (18 usa a média $0{,}45$; 19 troca os estados.)
> Ref: Simulado 3 Q3b; Aula 6 Bloco 4

Q: Uma opção (ativo derivativo) é precificada, em mercado completo, por:
- Sua probabilidade de exercício vezes o prêmio cobrado (regra atuarial)
- A preferência de risco do comprador marginal (preço subjetivo do agente)
- Replicação por carteira dos ativos-base e não-arbitragem (custo da réplica)
- A taxa livre de risco aplicada ao seu valor de face (desconto determinístico)
<!-- YW5zOjI= -->
> Em mercado completo o payoff da opção é replicável; por não-arbitragem, seu preço é o custo da carteira replicante, independentemente de probabilidades ou de quem compra.
> Ref: Aula 6 Bloco 4; MWG §19.E (opções)

## incompletos

Q: Um mercado é dito incompleto precisamente quando:
- O posto da matriz de ativos é menor que $S$ (risco residual não-segurável)
- Não existe nenhum ativo financeiro negociável (ausência total de ativos)
- Há custos de transação positivos na negociação (mercado com fricção)
- Os preços de equilíbrio simplesmente deixam de existir (não-existência)
<!-- YW5zOjA= -->
> Incompletude é deficiência de span (posto $<S$): faltam ativos para alcançar certos padrões de transferência, deixando risco residual não-segurável.
> Ref: Aula 6 Bloco 3 "Mercado incompleto"

Q: Hart (1975) mostrou que, em mercados incompletos, abrir um novo mercado de ativos:
- Sempre melhora a eficiência da alocação de equilíbrio (ganho garantido)
- Pode piorar todos os agentes, mudando preços relativos (Pareto-deterioração)
- Nunca altera o equilíbrio nem a alocação preexistentes (neutralidade total)
- Viola necessariamente a Lei de Walras agregada da economia (inconsistência)
<!-- YW5zOjE= -->
> Como o equilíbrio incompleto não é eficiente, efeitos de preço de segunda ordem ao adicionar um ativo podem prejudicar a todos (reforçado por Geanakoplos-Polemarchakis, 1986).
> Ref: Aula 6 Bloco 3 "Hart (1975)"
