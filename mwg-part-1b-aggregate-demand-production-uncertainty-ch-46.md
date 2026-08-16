---
quiz: "MWG — Part 1B: Aggregate Demand, Production & Uncertainty (Ch 4–6)"
tags:
  agreg: "Demanda Agregada (Ch 4)"
  prod: "Produção (Ch 5)"
  vnm: "Utilidade Esperada e VNM (Ch 6A–6B)"
  risco: "Aversão ao Risco e Arrow-Pratt (Ch 6C–6F)"
---

## agreg

Q: A forma de Gorman requer que a função de utilidade indireta de cada consumidor $i$ tenha a estrutura $v_i(p, w_i) = a_i(p) + b(p) w_i$. A condição essencial para que a demanda agregada dependa apenas de preços e riqueza total $\bar{w} = \sum_i w_i$ é:
- Cada $a_i(p)$ deve ser idêntico entre consumidores
- As preferências devem ser homotéticas e idênticas
- O termo $b(p)$ deve ser o mesmo para todos os consumidores
- Cada consumidor deve satisfazer WARP individualmente
<!-- YW5zOjI= -->
> Na forma de Gorman, as demandas individuais (via identidade de Roy) são $x_i(p,w_i) = \alpha_i(p) + \beta(p) w_i$. A demanda agregada é $\sum_i \alpha_i(p) + \beta(p) \bar{w}$, que depende só de $\bar{w}$ porque o coeficiente marginal $\beta(p) = -\nabla_p b(p)/b(p)$ é comum. Os termos $a_i(p)$ podem diferir entre consumidores sem afetar o resultado.
> Ref: MWG §4.B, Proposição 4.B.1 (pp. 107–109); N&S Cap. 5
> Similar: MWG Ex. 4.B.1, 4.B.2

Q: Preferências homotéticas satisfazem a forma de Gorman porque suas funções de utilidade indireta podem ser escritas como:
- $v_i(p, w_i) = a(p) + b(p) w_i$ com $a(p) = 0$
- $v_i(p, w_i) = a_i(p) + b_i(p) w_i$ com $b_i$ distinto por consumidor
- $v_i(p, w_i) = \phi_i(p) \cdot w_i$ onde $\phi_i$ pode diferir entre consumidores
- $v_i(p, w_i) = \phi(p) \cdot w_i$ com $\phi$ idêntico entre consumidores
<!-- YW5zOjI= -->
> Com preferências homotéticas, $v_i(p, w_i) = \phi_i(p) \cdot w_i$, ou seja, $a_i(p) = 0$ e $b_i(p) = \phi_i(p)$. O coeficiente $\phi_i(p)$ pode diferir entre consumidores (cada um tem sua própria função de utilidade homotética). O ponto crucial é que a utilidade indireta é linear em $w_i$, com $a_i = 0$. Porém, para a forma de Gorman, o $b(p)$ deve ser comum — logo, preferências homotéticas satisfazem Gorman apenas quando $\phi_i(p) = \phi(p)$ para todo $i$, o que ocorre, por exemplo, com preferências homotéticas idênticas. De forma geral, preferências homotéticas com $\phi_i$ distintos geram curvas de Engel lineares passando pela origem, e a demanda agregada depende apenas de $\bar{w}$ — pois o termo $a_i = 0$ elimina a dependência da distribuição.
> Ref: MWG §4.B (pp. 108–110); N&S Cap. 5 §5.4
> Similar: MWG Ex. 4.B.3

Q: O WARP (Weak Axiom of Revealed Preference) para a demanda agregada $x(p, \bar{w})$ pode falhar mesmo quando cada consumidor individual satisfaz WARP. Isso ocorre porque:
- A soma de funções de demanda contínuas pode ser descontínua
- A demanda agregada não é homogênea de grau zero
- A lei de Walras não se estende ao nível agregado
- Mudanças de preço redistribuem riqueza entre consumidores, e WARP individual não controla o efeito riqueza agregado
<!-- YW5zOjM= -->
> A falha ocorre porque, quando preços mudam, a distribuição de riqueza entre consumidores muda (via dotações, transferências ou efeitos de riqueza). Cada consumidor satisfaz WARP para seu $w_i$ fixo, mas a demanda agregada enfrenta redistribuição endógena. Homogeneidade de grau zero e lei de Walras se preservam na agregação; o que falha é a consistência revelada.
> Ref: MWG §4.C, Proposição 4.C.1 (pp. 110–114); ZaE Cap. 4
> Similar: MWG Ex. 4.C.1, 4.C.2

Q: O conceito de **consumidor representativo positivo** (MWG Def. 4.D.1) exige que a demanda agregada possa ser gerada por um problema de maximização com preferências racionais. Qual condição é suficiente para sua existência?
- Que todos os consumidores tenham preferências idênticas e homotéticas
- Que a demanda agregada satisfaça WARP, com a compensação feita via variação na riqueza agregada
- Que exista uma função de bem-estar social com pesos iguais
- Que a matriz de Slutsky agregada seja simétrica
<!-- YW5zOjE= -->
> MWG distingue o consumidor representativo positivo (a demanda agregada "parece" racional — satisfaz WARP com compensação via riqueza agregada) do normativo (o bem-estar do representativo reflete o bem-estar social). A satisfação de WARP agregado com compensação por riqueza agregada é a condição-chave para existência do representativo positivo. Simetria da Slutsky agregada é mais forte e não necessária.
> Ref: MWG §4.D, Def. 4.D.1 (pp. 115–117)
> Similar: MWG Ex. 4.D.1

Q: O resultado de Grandmont sobre a **regularização por agregação** mostra que, mesmo com preferências individuais não-suaves, a demanda agregada pode ser suave. A intuição é:
- A lei dos grandes números elimina a estocasticidade das escolhas individuais
- A convexidade do conjunto orçamentário força a demanda agregada a ser côncava
- O teorema do ponto fixo de Kakutani garante continuidade da correspondência agregada
- Se a distribuição de parâmetros de preferência na população é suficientemente dispersa (suave), efeitos individuais irregulares são "alisados" na agregação
<!-- YW5zOjM= -->
> Grandmont (1992) mostra que a heterogeneidade de preferências na população (capturada por uma distribuição suave sobre parâmetros de preferência) pode produzir demanda agregada bem-comportada, mesmo que demandas individuais tenham descontinuidades ou não satisfaçam WARP. A dispersão "alisa" as irregularidades — a demanda agregada herda a suavidade da distribuição populacional, não das demandas individuais.
> Ref: MWG §4.C (pp. 113–114); Grandmont (1992)
> Similar: MWG Ex. 4.C.4

## prod

Q: O conjunto de produção $Y \subseteq \mathbb{R}^L$ de uma firma satisfaz **livre descarte** (free disposal) se:
- $y \in Y$ e $y' \geq y$ implica $y' \in Y$
- $y \in Y$ implica $-y \in Y$
- $y \in Y$ e $y' \leq y$ implica $y' \in Y$
- $y \in Y$ implica $\alpha y \in Y$ para todo $\alpha \in [0,1]$
<!-- YW5zOjI= -->
> Livre descarte significa que é possível usar mais insumos sem reduzir o produto, ou equivalentemente, descartar produto sem custo. Se $y \in Y$ e $y' \leq y$ (cada componente menor ou igual), então $y' \in Y$. Na convenção MWG, insumos entram negativos e produtos positivos, então $y' \leq y$ significa mais insumos ou menos produto — ambos factíveis se o descarte é livre. A opção com $y' \geq y$ seria "livre aquisição" (não é propriedade padrão).
> Ref: MWG §5.B, p. 133 (Def. 5.B.1); N&S Cap. 9
> Similar: MWG Ex. 5.B.1

Q: A função de lucro $\pi(p) = \max_{y \in Y} p \cdot y$ satisfaz diversas propriedades. Qual das seguintes NÃO é propriedade de $\pi(p)$?
- Homogeneidade de grau 1 em $p$
- Convexidade em $p$
- Continuidade em $p$ (quando $Y$ é compacto)
- Concavidade em $p$
<!-- YW5zOjM= -->
> A função de lucro é: (i) homogênea de grau 1, (ii) convexa em $p$ (como máximo de funções lineares), (iii) contínua (pelo Teorema do Máximo, quando $Y$ é fechado e a maximização bem definida). A função de lucro é CONVEXA, não côncava — resultado importante que contrasta com a concavidade da função dispêndio. A convexidade reflete que a firma ajusta $y$ ao mudar de $p$, podendo explorar as novas direções lucrativas.
> Ref: MWG §5.C, Proposição 5.C.1 (pp. 137–139); N&S Cap. 11
> Similar: MWG Ex. 5.C.1, 5.C.2

Q: O **Lema de Hotelling** afirma que a oferta líquida da firma $y_l(p)$ satisfaz:
- $y_l(p) = \partial \pi(p)/\partial p_l$
- $y_l(p) = -\partial \pi(p)/\partial p_l$
- $y_l(p) = \partial c(w, q)/\partial w_l$
- $y_l(p) = -\partial c(w, q)/\partial q$
<!-- YW5zOjA= -->
> O Lema de Hotelling é a aplicação do teorema da envoltória ao problema de maximização de lucro: $\partial \pi(p)/\partial p_l = y_l(p)$. O sinal é positivo (diferente do Lema de Shephard na EMP do consumidor). A opção com $\partial c/\partial w_l$ é o Lema de Shephard para firmas (demandas condicionais de fatores), e $-\partial c/\partial q$ não é identidade padrão.
> Ref: MWG §5.C, Proposição 5.C.1(iv) (p. 138); N&S Cap. 11 §11.4
> Similar: MWG Ex. 5.C.3

Q: A função custo $c(w, q) = \min_{z \geq 0} w \cdot z$ s.t. $f(z) \geq q$ é côncava em $w$ (preços dos insumos). Isso implica que a matriz de derivadas segundas $\nabla^2_w c(w, q)$ é:
- Positiva semi-definida
- Indefinida em geral
- Positiva definida se a tecnologia é estritamente convexa
- Negativa semi-definida
<!-- YW5zOjM= -->
> Concavidade de $c$ em $w$ significa que a Hessiana $\nabla^2_w c(w,q)$ é negativa semi-definida. Pelo Lema de Shephard, $\partial c/\partial w_l = z_l(w,q)$, então $\partial^2 c/\partial w_l \partial w_k = \partial z_l/\partial w_k$ — os efeitos-preço próprios das demandas condicionais são não-positivos ($\partial z_l/\partial w_l \leq 0$). Isso é o análogo para firmas da concavidade da função dispêndio do consumidor.
> Ref: MWG §5.C, Proposição 5.C.2 (pp. 139–142); N&S Cap. 11 §11.6; ZaE Cap. 4
> Similar: MWG Ex. 5.C.7, 5.C.9

Q: Considere uma firma com tecnologia de retornos constantes de escala. Qual das seguintes afirmações é verdadeira?
- O lucro máximo é zero quando finito, e a oferta líquida é indeterminada em escala
- A função custo $c(w, q)$ é estritamente convexa em $q$
- A oferta líquida $y(p)$ é sempre única
- O lucro máximo é sempre estritamente positivo
<!-- YW5zOjA= -->
> Com retornos constantes, $f(\alpha z) = \alpha f(z)$. Se lucro positivo fosse atingível para algum $y$, dobrando a escala dobraria o lucro — sem limite superior. Logo, o lucro máximo finito é zero. A escala de operação é indeterminada: qualquer múltiplo de um plano ótimo também é ótimo. A função custo é linear em $q$: $c(w, q) = q \cdot c(w, 1)$, não estritamente convexa.
> Ref: MWG §5.B (pp. 133–135), §5.C (pp. 140–141); N&S Cap. 11
> Similar: MWG Ex. 5.B.3, 5.C.11

## vnm

Q: O axioma da **independência** (MWG Axioma 6.B.2) afirma que para loterias $L$, $L'$ e $L''$ e $\alpha \in (0,1)$: $L \succeq L'$ se e somente se:
- $\alpha L + (1-\alpha) L'' \succeq \alpha L + (1-\alpha) L'$
- $\alpha L + (1-\alpha) L'' \succeq \alpha L' + (1-\alpha) L''$
- $\alpha L + (1-\alpha) L' \succeq \alpha L'' + (1-\alpha) L'$
- $\alpha L + (1-\alpha) L' \succeq \alpha L' + (1-\alpha) L$
<!-- YW5zOjE= -->
> O axioma da independência diz que misturar uma terceira loteria $L''$ com $L$ e $L'$ nas mesmas proporções não altera a ordenação: $L \succeq L' \iff \alpha L + (1-\alpha) L'' \succeq \alpha L' + (1-\alpha) L''$. A "mistura" é feita com o mesmo componente $L''$ em ambos os lados. Este é o axioma central da teoria VNM e o que o Paradoxo de Allais viola.
> Ref: MWG §6.B, Axioma 6.B.2 (pp. 171–172); J-R §1
> Similar: MWG Ex. 6.B.1, 6.B.2

Q: O Teorema de VNM (Proposição 6.B.3) estabelece que se $\succeq$ sobre loterias satisfaz os axiomas de preferência, continuidade e independência, então existe $u: \mathcal{C} \to \mathbb{R}$ tal que:
- $L \succeq L'$ se e somente se $\sum_s p_s u(x_s) \geq \sum_s p'_s u(x_s)$, e $u$ é única
- $L \succeq L'$ se e somente se $\min_s u(x_s) \geq \min_s u(x'_s)$ (critério maximin)
- $L \succeq L'$ se e somente se $U(L) = \sum_s p_s u(x_s) \geq \sum_s p'_s u(x_s) = U(L')$, e $u$ é única a menos de transformação afim positiva
- $L \succeq L'$ se e somente se $U(L) \geq U(L')$, e $u$ é única a menos de transformação monótona crescente
<!-- YW5zOjI= -->
> O teorema VNM garante representação pela utilidade esperada $U(L) = \sum_s p_s u(x_s)$, com $u$ (a função de utilidade de Bernoulli) única a menos de transformação afim positiva: se $u$ representa, então $\hat{u} = a + bu$ com $b > 0$ também representa, mas $g(u)$ com $g$ não-linear não. Isso torna $u$ "cardinal" (até transformação afim), diferentemente da utilidade ordinal sob certeza.
> Ref: MWG §6.B, Proposição 6.B.3 (pp. 173–176); N&S Cap. 7; ZaE §3.4
> Similar: MWG Ex. 6.B.3, 6.B.5

Q: O **axioma da redução de loterias compostas** (MWG §6.B) afirma que o agente é indiferente entre uma loteria composta e a loteria simples obtida pela regra de:
- Maximização da utilidade esperada em cada estágio
- Minimização do risco em cada estágio
- Cálculo das probabilidades por multiplicação e soma (lei da probabilidade total)
- Aplicação de pesos de decisão não-lineares (como em Prospect Theory)
<!-- YW5zOjI= -->
> O axioma da redução diz que o agente avalia loterias compostas pela loteria simples "reduzida" — cujas probabilidades são calculadas pela lei da probabilidade total ($p_s^{\text{reduzida}} = \sum_k \alpha_k p_s^k$). Em outras palavras, o agente não se importa com a "árvore" de resolução, apenas com a distribuição final. Isso é crucial para a representação VNM e é violado em modelos como preferências recursivas (Kreps-Porteus).
> Ref: MWG §6.B (pp. 169–171); J-R §1
> Similar: MWG Ex. 6.B.1

Q: No **Paradoxo de Allais**, um agente prefere \$1 milhão com certeza a uma loteria com 89% de chance de \$1M, 10% de \$5M e 1% de \$0, mas também prefere 10% de \$5M a 11% de \$1M. Essa combinação de escolhas viola:
- Transitividade
- Continuidade (axioma Arquimediano)
- O axioma da independência
- Completude
<!-- YW5zOjI= -->
> O Paradoxo de Allais viola o axioma da independência. Nas duas escolhas, a diferença entre as opções é a mesma "substituição" de uma probabilidade de \$1M por uma loteria envolvendo \$5M e \$0. Pelo axioma da independência, a preferência deveria ser consistente. A reversão mostra que o agente pondera excessivamente a "certeza" — o chamado "efeito certeza" — violando linearidade nas probabilidades.
> Ref: MWG §6.B (pp. 176–178); N&S Cap. 7
> Similar: MWG Ex. 6.B.6, 6.B.7

Q: Um agente com utilidade VNM $u$ avalia loterias sobre $\mathbb{R}_+$. A afirmação "a utilidade de Bernoulli $u$ é única a menos de transformação afim positiva" significa que se $\hat{u}$ também representa as mesmas preferências sobre loterias, então:
- $\hat{u}(x) = a + b \cdot u(x)$ para constantes $a$ e $b > 0$
- $\hat{u}(x) = g(u(x))$ para qualquer $g$ estritamente crescente
- $\hat{u}(x) = b \cdot u(x)$ com $b > 0$ (sem constante aditiva)
- $\hat{u}(x) = u(x)^b$ para $b > 0$
<!-- YW5zOjA= -->
> A cardinalidade da utilidade VNM é o resultado central: $u$ e $\hat{u}$ representam as mesmas preferências sobre loterias se e somente se $\hat{u} = a + bu$ com $b > 0$. Isso é mais restritivo que a ordinalidade (qualquer $g$ crescente), pois a linearidade da utilidade esperada nas probabilidades impõe que a transformação seja afim. A constante $a$ é permitida (diferente de representações puramente homogêneas).
> Ref: MWG §6.B, Proposição 6.B.2 (p. 173); N&S Cap. 7 §7.3
> Similar: MWG Ex. 6.B.4

## risco

Q: O coeficiente de aversão absoluta ao risco de Arrow-Pratt é definido como $r_A(x) = -u''(x)/u'(x)$. Para a função CARA $u(x) = -e^{-ax}$ com $a > 0$, temos:
- $r_A(x) = a/x$, crescente em $x$
- $r_A(x) = a$, constante
- $r_A(x) = 1 - a$, constante
- $r_A(x) = a^2 x$, crescente em $x$
<!-- YW5zOjE= -->
> Para $u(x) = -e^{-ax}$: $u'(x) = ae^{-ax}$, $u''(x) = -a^2 e^{-ax}$. Logo $r_A(x) = -(-a^2 e^{-ax})/(ae^{-ax}) = a$. A aversão absoluta é constante e igual ao parâmetro $a$ — daí o nome CARA (Constant Absolute Risk Aversion). O prêmio de risco por riscos pequenos $\pi \approx \frac{1}{2} a \sigma^2$ não depende da riqueza.
> Ref: MWG §6.C (pp. 190–191); N&S Cap. 7 §7.6; ZaE §3.4
> Similar: MWG Ex. 6.C.3

Q: Considere dois agentes com funções de utilidade VNM $u_A$ e $u_B$, ambas crescentes e côncavas. O agente $A$ é **mais avesso ao risco** que $B$ se e somente se:
- $r_A^A(x) > r_A^B(x)$ para todo $x$, e equivalentemente $u_A = g(u_B)$ com $g$ côncava
- $u_A = g(u_B)$ com $g$ convexa e crescente
- O equivalente certo de $A$ excede o de $B$ para toda loteria
- $r_A^A(x) < r_A^B(x)$ para todo $x$
<!-- YW5zOjA= -->
> A Proposição 6.C.2 de MWG estabelece equivalência entre: (i) $r_A^A(x) \geq r_A^B(x)$ para todo $x$, (ii) $u_A = g(u_B)$ com $g$ côncava crescente, (iii) $CE_A(L) \leq CE_B(L)$ para toda loteria $L$, (iv) $\pi_A(L) \geq \pi_B(L)$ para toda loteria. O agente mais avesso aceita menos risco, tem menor equivalente certo e maior prêmio de risco. A concavidade de $g$ "curva mais" $u_A$ em relação a $u_B$.
> Ref: MWG §6.C, Proposição 6.C.2 (pp. 190–194); N&S Cap. 7
> Similar: MWG Ex. 6.C.4, 6.C.5

P: Considere as funções de utilidade CRRA: $u(x) = \frac{x^{1-\gamma}}{1-\gamma}$ para $\gamma > 0, \gamma \neq 1$, e $u(x) = \ln x$ para $\gamma = 1$.

Q: O coeficiente de aversão relativa ao risco $r_R(x) = x \cdot r_A(x)$ para a família CRRA é:
- $r_R(x) = 1 - \gamma$, podendo ser negativo
- $r_R(x) = \gamma / x$, decrescente na riqueza
- $r_R(x) = \gamma x$, crescente na riqueza
- $r_R(x) = \gamma$, constante e positivo
<!-- YW5zOjM= -->
> Para $u(x) = x^{1-\gamma}/(1-\gamma)$: $u'(x) = x^{-\gamma}$, $u''(x) = -\gamma x^{-\gamma-1}$. Logo $r_A(x) = \gamma/x$ e $r_R(x) = x \cdot \gamma/x = \gamma$. Para $\gamma = 1$ (log): $r_A = 1/x$, $r_R = 1 = \gamma$. A aversão relativa é constante e igual a $\gamma$ — daí CRRA (Constant Relative Risk Aversion). Note que $r_A = \gamma/x$ é decrescente (DARA), propriedade empiricamente desejável.
> Ref: MWG §6.C (pp. 193–194); N&S Cap. 7 §7.6; ZaE §3.4
> Similar: MWG Ex. 6.C.6

Q: Uma loteria $F$ domina $G$ por **dominância estocástica de primeira ordem** (FOSD) se e somente se:
- $F(\cdot) \leq G(\cdot)$ para todo nível de riqueza, e $E_F[u] \geq E_G[u]$ para toda $u$ crescente
- $\int [G(x) - F(x)] dx \geq 0$ para todo nível, e $E_F[u] \geq E_G[u]$ para toda $u$ crescente e côncava
- $F(\cdot) \geq G(\cdot)$ para todo nível de riqueza
- $E_F[x] > E_G[x]$ (média de $F$ maior que de $G$)
<!-- YW5zOjA= -->
> FOSD: $F$ domina $G$ $\iff$ $F(x) \leq G(x)$ para todo $x$ $\iff$ $E_F[u] \geq E_G[u]$ para toda $u$ não-decrescente. Intuitivamente, $F$ coloca mais peso em valores altos (sua CDF está "abaixo" da de $G$). A condição com integral é SOSD. Ter média maior é necessário mas não suficiente para FOSD.
> Ref: MWG §6.D, Proposição 6.D.1 (pp. 194–199); N&S Cap. 7
> Similar: MWG Ex. 6.D.1, 6.D.2

Q: No framework de **Savage** (probabilidade subjetiva), as preferências são definidas sobre **atos** (funções de estados para consequências). O teorema de Savage mostra que, sob axiomas incluindo o sure-thing principle, existem:
- Probabilidades objetivas e utilidade ordinal sobre consequências
- Uma medida de probabilidade subjetiva $\mu$ sobre estados e uma utilidade VNM $u$ sobre consequências, tal que atos são avaliados por $\int u(f(s)) d\mu(s)$
- Uma utilidade definida diretamente sobre atos, sem separação entre probabilidades e payoffs
- Probabilidades subjetivas mas sem representação de utilidade esperada (apenas ordenação de atos)
<!-- YW5zOjE= -->
> O teorema de Savage (1954) é um dos resultados fundamentais da teoria da decisão. Sob seus axiomas (incluindo o sure-thing principle, que é o análogo do axioma da independência para atos), as preferências sobre atos admitem representação por utilidade esperada subjetiva: o agente age como se possuísse crenças probabilísticas subjetivas $\mu$ e avaliasse atos por $\int u(f(s)) d\mu(s)$. A separação entre crenças ($\mu$) e gostos ($u$) é resultado central.
> Ref: MWG §6.F (pp. 205–208); Savage (1954)
> Similar: MWG Ex. 6.F.1
