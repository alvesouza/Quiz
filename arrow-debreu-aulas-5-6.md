---
quiz: "Arrow-Debreu — Aulas 5-6"
tags:
  contingentes: "Bens contingentes e R^{LS}"
  completo: "Mercados completos e equilíbrio AD"
  sdf: "SDF e equação fundamental"
  seguro: "Seguro completo e utilidade esperada"
  tbe: "TBE estendidos"
  existencia: "Existência (Brouwer/Kakutani)"
  radner: "Radner e comércio sequencial"
  incompletos: "Mercados incompletos e Hart"
  precificacao: "Precificação por não-arbitragem"
---

## contingentes

Q: No modelo Arrow-Debreu, um "bem contingente" é definido como:
- Um bem físico indexado pelo estado da natureza em que é entregue
- Um ativo financeiro que paga dividendos em todos os estados
- Um bem cujo preço varia com a probabilidade do estado
- Uma promessa de entrega que independe do estado realizado
<!-- YW5zOjA= -->
> Arrow e Debreu reindexam bens: "café na chuva" e "café na seca" são bens distintos. Cada bem é indexado por (mercadoria, estado), e toda a teoria de equilíbrio geral se transporta para esse espaço ampliado.
> Ref: Aula 5 Bloco 1 "Bem contingente"; N&S Cap 7 §7.2; MWG §19.B

Q: Com $L$ mercadorias físicas e $S$ estados da natureza, o espaço de bens do modelo AD é:
- $\mathbb{R}^{L+S}$ (mercadorias mais estados)
- $\mathbb{R}^{L}$ (a incerteza não amplia o espaço)
- $\mathbb{R}^{S}$ (só importam os estados)
- $\mathbb{R}^{LS}$ (uma coordenada por par mercadoria-estado)
<!-- YW5zOjM= -->
> Cada uma das $L$ mercadorias passa a existir em cada um dos $S$ estados, gerando $L\times S$ bens contingentes. É a ampliação que permite reusar todos os resultados de EG.
> Ref: Aula 5 Bloco 1 "Estados, bens contingentes, R^{LS}"

Q: A frase "tempo é um caso particular de estado" significa que:
- O modelo AD ignora a dimensão temporal
- Preços de equilíbrio não podem depender do tempo
- Só existe um único período de negociação
- Datas futuras podem ser indexadas como estados, tratando bens por data como bens por estado
<!-- YW5zOjM= -->
> Indexar bens por data é formalmente idêntico a indexá-los por estado; por isso o aparato AD cobre tanto incerteza quanto intertemporalidade com a mesma álgebra.
> Ref: Aula 5 Bloco 1 "Tempo é caso particular de estado"

## completo

Q: Dizer que o mercado é "completo" no sentido de Arrow-Debreu significa que:
- Existe um título contingente negociável para cada estado (posto da matriz de payoffs igual a $S$)
- Todos os agentes têm a mesma informação sobre os estados
- Os preços dos títulos refletem as probabilidades verdadeiras
- Não há custos de transação na negociação dos ativos
<!-- YW5zOjA= -->
> Completude é uma propriedade do span dos ativos: com $S$ títulos linearmente independentes, qualquer transferência de recursos entre estados é alcançável. Informação simétrica e custo zero são hipóteses auxiliares, não a definição.
> Ref: Aula 5 Bloco 2 "Mercado completo"; MWG §19.E

Q: Um título de Arrow associado ao estado $s$ paga:
- 1 unidade em todos os estados
- 1 unidade no estado $s$ e 0 nos demais
- $\pi_s$ unidades no estado $s$
- o valor esperado do payoff agregado
<!-- YW5zOjE= -->
> O título de Arrow é o "tijolo elementar": paga 1 só no seu estado. Combinações desses títulos replicam qualquer payoff contingente, o que torna o mercado completo quando há um para cada estado.
> Ref: Aula 5 Bloco 2; N&S Cap 7

Q: A Lei de Walras estendida ao ambiente Arrow-Debreu afirma que:
- $q\cdot z(q)\equiv 0$, somando o excesso de demanda sobre todos os $L\times S$ bens contingentes
- a soma se faz apenas sobre os $L$ bens físicos
- a soma se faz apenas sobre os $S$ estados
- ela deixa de valer quando há incerteza
<!-- YW5zOjA= -->
> Exatamente como na economia sem incerteza, a exaustão do orçamento (NSL) somada sobre os agentes dá $q\cdot z(q)\equiv 0$ — agora com $q$ e $z$ vivendo em $\mathbb{R}^{LS}$.
> Ref: Aula 5 Bloco 2 "Lei de Walras estendida"

Q: Com mercados completos e preferências convexas, os Teoremas do Bem-Estar:
- Falham necessariamente sob qualquer incerteza
- Valem como na economia sem incerteza (1º e 2º TBE estendidos)
- Só valem se todos os agentes forem neutros ao risco
- Exigem que as probabilidades sejam idênticas entre agentes
<!-- YW5zOjE= -->
> Como bens contingentes são "bens comuns" em $\mathbb{R}^{LS}$, a prova do 1º TBE se reaproveita (precisa de NSL) e a do 2º também (precisa de convexidade). A incerteza não muda a estrutura.
> Ref: Aula 5 Bloco 3; J-R §5.5

## sdf

Q: Na UMP com utilidade esperada $\sum_s\pi_s v(c_s)$ e preços de Arrow $q_s$, a condição de primeira ordem interior é:
- $v'(c_s)=\lambda$ para todo $s$
- $\pi_s=\lambda\,q_s$ para todo $s$
- $v'(c_s)=q_s$ para todo $s$
- $\pi_s\,v'(c_s)=\lambda\,q_s$ para todo $s$
<!-- YW5zOjM= -->
> Derivando o Lagrangiano $\sum_s\pi_s v(c_s)-\lambda(\sum_s q_s c_s-W)$ em $c_s$: a utilidade marginal ponderada pela probabilidade iguala o preço de estado vezes o multiplicador.
> Ref: Aula 5 Bloco 2 "Equação fundamental do SDF"

Q: O fator de desconto estocástico (SDF) que precifica os ativos é:
- $m_s=\dfrac{\pi_s}{q_s}$
- $m_s=q_s\,\pi_s$
- $m_s=v'(c_s)$
- $m_s=\dfrac{q_s}{\pi_s}$
<!-- YW5zOjM= -->
> O SDF é a razão preço de estado / probabilidade. Pela CPO, $m_s=q_s/\pi_s=v'(c_s)/\lambda$: ele carrega a utilidade marginal relativa entre estados.
> Ref: Aula 5/6 "Equação fundamental do SDF"

Q: A precificação por SDF de um ativo $j$ com payoffs $X_{js}$ é:
- $q_j=\sum_s \pi_s\,m_s\,X_{js}$
- $q_j=\sum_s X_{js}$
- $q_j=\sum_s \pi_s\,X_{js}$
- $q_j=m_s\,X_{js}$
<!-- YW5zOjA= -->
> Preço = valor esperado do payoff ponderado pelo SDF. Equivalentemente $q_j=\sum_s q_s X_{js}$, já que $q_s=\pi_s m_s$. É a fórmula de não-arbitragem.
> Ref: Aula 6 Bloco 4 "SDF + Euler"

Q: Quando o SDF é constante entre estados ($m_s=\bar m$ para todo $s$), os preços de Arrow são:
- Iguais a 1 em todos os estados
- Nulos no estado mais provável
- Atuarialmente justos ($q_s\propto\pi_s$)
- Proporcionais ao payoff agregado
<!-- YW5zOjI= -->
> $m_s=q_s/\pi_s$ constante implica $q_s=\bar m\,\pi_s$: os preços de estado são proporcionais às probabilidades — a definição de preços atuarialmente justos.
> Ref: Aula 5 Bloco 2; Aula 6 Bloco 4

## seguro

Q: Com Bernoulli estritamente côncava e preços atuarialmente justos ($q_s=\pi_s$), o consumo contingente ótimo é:
- Maior no estado de maior probabilidade
- Igual em todos os estados ($c_s$ constante) — seguro completo
- Proporcional à probabilidade $\pi_s$ de cada estado
- Nulo no estado desfavorável
<!-- YW5zOjE= -->
> Da CPO $\pi_s v'(c_s)=\lambda q_s$ com $q_s=\pi_s$ vem $v'(c_s)=\lambda$ constante; como $v'$ é estritamente decrescente (injetora), $c_s$ é constante. O agente avesso suaviza o consumo entre estados.
> Ref: Aula 5 Bloco 4 "Resultado canônico"; MWG §19.C

Q: Por que preços justos levam a $c_s$ constante (Bernoulli côncava estrita)?
- Porque a probabilidade some da restrição orçamentária
- A CPO força $v'(c_s)$ constante, e $v'$ injetora implica $c_s$ constante
- Porque o agente é, na verdade, neutro ao risco
- Porque a dotação já é igual em todos os estados
<!-- YW5zOjE= -->
> O mecanismo é puramente a injetividade de $v'$: utilidade marginal igual entre estados só é possível com consumo igual entre estados. Independe da dotação ser igual.
> Ref: Aula 5 Bloco 4

Q: Geradora com $v(c)=\ln c$, probabilidades $\pi=(\tfrac34,\tfrac14)$, preços de Arrow justos $q=(\tfrac34,\tfrac14)$ e dotação contingente $\omega=(100,20)$. O consumo ótimo $c^*$ é:
- $(100,20)$ — mantém a dotação, sem seguro
- $(60,60)$ — constante, porém abaixo da dotação esperada
- $(80,80)$ — constante, igual ao valor da dotação a preços $q$
- $(75,25)$ — proporcional às probabilidades
<!-- YW5zOjI= -->
> Log é côncava, preços justos ⟹ $c^*$ constante. O nível sai do orçamento: $q\cdot c=q\cdot\omega=\tfrac34(100)+\tfrac14(20)=80$, e com $c$ constante e $q_1+q_2=1$, $c^*=(80,80)$.
> Ref: Simulado 1 Q4a; Aula 5 Bloco 4

Q: Mantidas as probabilidades, suponha agora que o título da "seca" fique caro ($q_2>\pi_2$). O agente:
- Aumenta a cobertura contra a seca acima do pleno
- Deixa de se segurar plenamente, tolerando consumir menos na seca
- Mantém $c_s$ constante, ignorando o preço
- Passa a consumir zero no estado bom
<!-- YW5zOjE= -->
> Com $q_2/\pi_2>1$, segurar o estado ruim ficou caro; a CPO dá $v'(c_2)/v'(c_1)=q_2/\pi_2\cdot(\pi_1/q_1)>1$, logo $c_2<c_1$. O seguro deixa de ser completo.
> Ref: Simulado 1 Q4b; Aula 5

## tbe

Q: O 1º TBE estendido (mercados completos) é demonstrado:
- Apenas sob neutralidade ao risco dos agentes
- Via teorema de ponto fixo de Brouwer
- Reaproveitando a prova sem incerteza, tratando os bens contingentes como bens comuns
- Somente no caso de exatamente dois estados
<!-- YW5zOjI= -->
> Em $\mathbb{R}^{LS}$ o equilíbrio AD é um equilíbrio walrasiano usual; a contradição do 1º TBE (com NSL) vale linha a linha. Nada de novo é exigido além de completude.
> Ref: Aula 5 Bloco 3 "1º TBE — prova reaproveitada"

Q: Além de mercados completos, o 2º TBE estendido requer crucialmente:
- Neutralidade ao risco de todos os agentes
- Convexidade das preferências (sobre planos contingentes em $\mathbb{R}^{LS}$)
- Probabilidades idênticas entre os agentes
- Exatamente dois bens físicos
<!-- YW5zOjE= -->
> Como sempre, descentralizar uma alocação eficiente por preços lineares exige convexidade (hiperplano separador). A novidade é apenas que a convexidade é avaliada em $\mathbb{R}^{LS}$.
> Ref: Aula 5 Bloco 3 "2º TBE estendido"

Q: A eficiência de Pareto no equilíbrio Arrow-Debreu é avaliada:
- Ex-ante, sobre os planos de consumo contingente (antes de o estado se realizar)
- Ex-post, estado a estado, após a realização
- Apenas no estado efetivamente realizado
- Ignorando as probabilidades dos estados
<!-- YW5zOjA= -->
> AD é uma economia de planos contingentes negociados em $t=0$; a eficiência é ex-ante, em utilidade esperada. Ex-post, um estado azarado pode parecer "ineficiente", mas o plano era eficiente ex-ante.
> Ref: Aula 5 Bloco 3

## existencia

Q: O Teorema de Brouwer garante que:
- O equilíbrio walrasiano é único
- Todo equilíbrio é Pareto-eficiente
- O núcleo de uma economia de trocas é não-vazio
- Toda função contínua de um simplex (compacto convexo) nele mesmo tem ponto fixo
<!-- YW5zOjM= -->
> Brouwer é a ferramenta topológica da existência: continuidade + domínio compacto convexo garantem $f(x^*)=x^*$. Unicidade e eficiência são questões distintas.
> Ref: Aula 6 Bloco 1 "Brouwer (1911)"

Q: Na prova de existência de equilíbrio walrasiano, o ponto fixo da aplicação no simplex de preços corresponde a:
- Uma alocação Pareto-eficiente qualquer
- A dotação inicial dos agentes
- Um vetor de preços que zera o excesso de demanda agregada
- O centro do núcleo da economia
<!-- YW5zOjI= -->
> Constrói-se $f:\Delta\to\Delta$ que empurra o preço na direção do excesso positivo; no ponto fixo o preço não se move, logo $z(p^*)=0$ (usando Walras e homogeneidade).
> Ref: Aula 6 Bloco 1 "Sketch — existência em economia AD"

Q: Passa-se de Brouwer para Kakutani quando:
- Há apenas um bem na economia
- A demanda é uma correspondência (multivalorada), e.g., preferências não estritamente convexas
- As preferências são sempre lineares
- Não há incerteza no modelo
<!-- YW5zOjE= -->
> Sem convexidade estrita a demanda pode ser um conjunto, não um ponto; Kakutani estende o ponto fixo a correspondências de valor convexo e gráfico fechado.
> Ref: Aula 6 Bloco 1 "Quando Brouwer falha — Kakutani"

## radner

Q: O equilíbrio de Radner descreve uma economia em que:
- Negocia-se sequencialmente — ativos financeiros primeiro, bens à vista em cada estado depois
- Tudo é negociado num único leilão à vista
- Os mercados são incompletos por definição
- Não há ativos financeiros, só bens contingentes
<!-- YW5zOjA= -->
> Radner é a versão "realista": em vez de um mercado AD que abre todos os contratos em $t=0$, há um número pequeno de ativos negociados e depois mercados spot. A pergunta é quando isso replica AD.
> Ref: Aula 6 Bloco 2 "Setup formal de Radner"

Q: A equivalência entre equilíbrio Arrow-Debreu e equilíbrio de Radner vale quando:
- A matriz de payoffs dos ativos tem posto completo (gera $\mathbb{R}^S$)
- Existe um único ativo negociável
- Todos os agentes são neutros ao risco
- Há no máximo dois estados da natureza
<!-- YW5zOjA= -->
> Se os ativos geram todo o $\mathbb{R}^S$, qualquer transferência contingente é replicável por carteira; aí a sequência de restrições de Radner equivale à única restrição AD.
> Ref: Aula 6 Bloco 2 "Equivalência AD↔Radner"

Q: Sob a equivalência (posto completo), a sequência de restrições orçamentárias de Radner:
- É sempre mais restritiva que a de AD
- Permite estritamente mais consumo que AD
- Independe dos preços dos ativos
- Colapsa na única restrição orçamentária de Arrow-Debreu, dando a mesma alocação
<!-- YW5zOjM= -->
> Com span completo, a carteira que financia qualquer plano contingente existe e seu custo é exatamente o preço AD daquele plano; as restrições se fundem e o conjunto factível coincide.
> Ref: Aula 6 Bloco 2 "Equivalência — sketch"

## incompletos

Q: Um mercado é incompleto quando:
- Não existe nenhum ativo financeiro
- Há custos de transação positivos
- O posto da matriz de ativos é menor que $S$ — nem todo risco é segurável
- Os preços de equilíbrio não existem
<!-- YW5zOjI= -->
> Incompletude é deficiência de span: faltam ativos para alcançar alguns padrões de transferência entre estados. Resta risco residual não-diversificável.
> Ref: Aula 6 Bloco 3 "Mercado incompleto"

Q: Hart (1975) mostrou que, em mercados incompletos, abrir um novo mercado de ativos:
- Sempre melhora a eficiência
- Pode piorar todos os agentes (Pareto), pois altera os preços relativos dos ativos existentes
- Nunca tem efeito algum sobre o equilíbrio
- Viola a Lei de Walras
<!-- YW5zOjE= -->
> A intuição "mais mercados, melhor" falha: como o equilíbrio incompleto não é eficiente, mudanças no conjunto de ativos têm efeitos de preço de segunda ordem que podem prejudicar a todos (reforçado por Geanakoplos-Polemarchakis, 1986).
> Ref: Aula 6 Bloco 3 "Hart (1975)"

Q: O equilíbrio com mercados incompletos é, no melhor caso:
- Sempre Pareto-eficiente, como em AD
- Inexistente em geral
- Pareto-restrito (constrained efficient), não Pareto-eficiente pleno
- Eficiente apenas com exatamente dois estados
<!-- YW5zOjI= -->
> Dado o conjunto limitado de ativos, o equilíbrio é o melhor possível "restrito" a esse span, mas em geral há ineficiência relativa ao ótimo de mercados completos.
> Ref: Aula 6 Bloco 3 "constrained PE"

## precificacao

Q: Mercado completo, dois estados. Título $X$ paga $(3,1)$ e custa $1{,}90$; título $Y$ paga $(1,2)$ e custa $1{,}30$. Um contrato $Z$ paga $(10,30)$. Por não-arbitragem, o preço de $Z$ é:
- $18$
- $19$
- $17$
- $16$
<!-- YW5zOjI= -->
> Extraia os preços de estado de $3q_1+q_2=1{,}90$ e $q_1+2q_2=1{,}30$: $q_1=0{,}50,\ q_2=0{,}40$. Logo $P_Z=10(0{,}50)+30(0{,}40)=17$. (18 usa a média $q_1=q_2=0{,}45$; 19 troca os payoffs de estado.)
> Ref: Simulado 3 Q3b; Aula 6 Bloco 4

Q: Os preços de estado (Arrow) implícitos num conjunto de ativos são únicos se, e somente se:
- Os agentes são avessos ao risco
- As probabilidades verdadeiras são conhecidas
- Existem ao menos dois ativos quaisquer
- O mercado é completo (a matriz de payoffs tem posto $S$)
<!-- YW5zOjM= -->
> Com posto $S$, o sistema $X q = \text{preços}$ tem solução única $q$; faltando posto, há um subespaço de preços de estado compatíveis (preço não-único de payoffs fora do span).
> Ref: Aula 6 Bloco 4; precificação por não-arbitragem

Q: A equação de Euler intertemporal escreve o SDF como:
- $m_{t+1}=\beta\,\dfrac{u'(c_{t+1})}{u'(c_t)}$, com $1=\mathbb{E}_t[m_{t+1}R_{t+1}]$
- $m_{t+1}=\dfrac{u'(c_t)}{u'(c_{t+1})}$, sem desconto
- $m_{t+1}=\beta$ (constante, independente do consumo)
- $m_{t+1}=R_{t+1}$ (o próprio retorno bruto)
<!-- YW5zOjA= -->
> O SDF intertemporal é a taxa marginal de substituição descontada $\beta u'(c_{t+1})/u'(c_t)$; a condição de não-arbitragem $1=\mathbb{E}_t[m_{t+1}R_{t+1}]$ precifica qualquer retorno.
> Ref: Aula 6 Bloco 4 "Equação de Euler intertemporal"
