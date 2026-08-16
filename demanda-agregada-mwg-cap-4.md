---
quiz: "Demanda Agregada — MWG Cap. 4"
tags:
  gorman: "Forma de Gorman e consumidor representativo"
  falha: "Falha da agregação e SMD"
  regular: "Regularização e propriedades agregadas"
---

## gorman

Q: Das propriedades da demanda individual — (i) homogeneidade de grau zero, (ii) lei de Walras, (iii) simetria da matriz de Slutsky — quais se preservam na demanda agregada $x(p, w_1, \ldots, w_I) = \sum_i x_i(p, w_i)$ sem restrições adicionais sobre preferências?
- Apenas (i)
- Apenas (i) e (ii)
- (i), (ii) e (iii)
- Nenhuma — todas exigem condições adicionais
<!-- YW5zOjE= -->
> Homogeneidade de grau zero e lei de Walras se preservam por simples soma: se cada $x_i(p, w_i)$ é homogênea de grau zero, $\sum_i x_i(\alpha p, \alpha w_i) = \sum_i x_i(p, w_i)$; e a lei de Walras vale pois $p \cdot \sum_i x_i = \sum_i w_i$. A simetria da Slutsky NÃO sobrevive — a matriz de Slutsky agregada é soma de matrizes simétricas NSD *individuais* com termos de efeito-riqueza que dependem da distribuição, destruindo a simetria em geral.
> Ref: MWG §4.B (pp. 105–107); N&S Cap. 5 §5.8
> Similar: MWG Ex. 4.B.1

Q: Na forma de Gorman, $v_i(p, w_i) = a_i(p) + b(p) w_i$. Aplicando a identidade de Roy, a demanda individual do bem $l$ pelo consumidor $i$ é $x_{il}(p, w_i) = \alpha_{il}(p) + \beta_l(p) w_i$. A demanda agregada é $X_l = \sum_i \alpha_{il}(p) + \beta_l(p) \bar{w}$, que depende só de $\bar{w} = \sum_i w_i$. Qual termo é responsável por eliminar a dependência da distribuição de riqueza?
- O termo $\alpha_{il}(p)$, que é idêntico entre consumidores
- O termo $\beta_l(p)$, que é comum a todos os consumidores
- A restrição de que $\sum_i a_i(p) = 0$
- A condição de que todas as preferências sejam homotéticas
<!-- YW5zOjE= -->
> A propensão marginal a consumir o bem $l$ é $\beta_l(p) = \partial x_{il}/\partial w_i$, idêntica para todos os consumidores porque $b(p)$ é comum. Ao somar, $\sum_i \beta_l(p) w_i = \beta_l(p) \sum_i w_i = \beta_l(p) \bar{w}$. Se $\beta_l$ variasse entre consumidores, transferir \$1 do agente 1 para o agente 2 mudaria a demanda agregada — a distribuição importaria. Os $\alpha_{il}(p)$ podem diferir (somam-se numa constante agregada) sem afetar o resultado.
> Ref: MWG §4.B, Proposição 4.B.1 (pp. 107–109)
> Similar: MWG Ex. 4.B.2

Q: Preferências quasilineares $u_i(x_0, x_1, \ldots, x_L) = x_0 + \phi_i(x_1, \ldots, x_L)$ satisfazem a forma de Gorman. A utilidade indireta correspondente tem:
- $a_i(p) = \phi_i^*(p_{-0})$ e $b(p) = 1/p_0$, com $b$ comum porque o bem $0$ entra linearmente para todos
- $a_i(p) = 0$ e $b_i(p) = \phi_i(p)$, com $b_i$ distinto por consumidor
- $a_i(p) = w_i$ e $b(p) = 0$ — a riqueza não afeta a demanda dos outros bens
- $a_i(p) = \phi_i(p)$ e $b(p) = p_0$ — o bem numerário fixa o coeficiente
<!-- YW5zOjA= -->
> Com quasilinear, o consumidor gasta $x_0 = w_i/p_0 - g_i(p_{-0}/p_0)$ no numerário e o resto é determinado pelos preços relativos via $\phi_i$, independente de $w_i$ (para soluções interiores). A utilidade indireta é $v_i = \phi_i^*(p_{-0}) + w_i/p_0$, onde $b(p) = 1/p_0$ é comum a todos. A parcela $a_i$ captura as diferenças de preferência sobre os bens não-numerários, mas como $b$ é comum, a demanda agregada depende apenas de $\bar{w}$.
> Ref: MWG §4.B (pp. 108–110); N&S Cap. 4 (quasilinear)
> Similar: MWG Ex. 4.B.3

Q: A distinção entre **consumidor representativo positivo** e **normativo** (MWG §4.D) é:
- O positivo exige preferências idênticas; o normativo permite preferências distintas
- O positivo requer que a demanda agregada possa ser racionalizada por preferências; o normativo requer que mudanças no bem-estar do representativo reflitam mudanças no bem-estar social
- O positivo requer Gorman; o normativo requer apenas WARP agregado
- Não há distinção — ambos exigem que a demanda agregada satisfaça WARP
<!-- YW5zOjE= -->
> O consumidor representativo positivo é puramente descritivo: a demanda agregada é como se gerada por um agente racional (racionalizada por $\succeq$). Já o normativo exige que o bem-estar desse agente fictício tenha significado para a sociedade — que aumentos na utilidade indireta do representativo correspondam a melhorias no sentido de alguma função de bem-estar social. O normativo é mais exigente: requer que exista uma função de bem-estar social $W(u_1, \ldots, u_I)$ cujo ótimo gere as mesmas demandas.
> Ref: MWG §4.D, Def. 4.D.1–4.D.2 (pp. 115–118)
> Similar: MWG Ex. 4.D.1

## falha

Q: Sem a forma de Gorman, duas economias com os mesmos preços $p$ e mesma riqueza total $\bar{w}$ podem ter demandas agregadas diferentes. Isso ocorre porque:
- A lei de Walras falha sem Gorman
- A demanda agregada não é contínua em $p$
- A demanda de cada consumidor depende de $w_i$, e a distribuição $(w_1, \ldots, w_I)$ afeta a soma mesmo com $\bar{w}$ fixo
- A homogeneidade de grau zero da demanda individual é perdida na agregação
<!-- YW5zOjI= -->
> Se $\beta_l$ varia entre consumidores (propensões marginais distintas), $\sum_i \beta_{il}(p) w_i \neq f(p, \bar{w})$ — a mesma riqueza total distribuída diferentemente gera demandas diferentes. Um exemplo simples: consumidor A com preferências Cobb-Douglas $(\alpha = 0.3)$ e B com $(\alpha = 0.7)$: dar toda a riqueza a A vs. a B muda radicalmente a composição da demanda agregada. Homogeneidade e Walras se preservam; o que falha é a dependência exclusiva em $\bar{w}$.
> Ref: MWG §4.B (pp. 106–107)
> Similar: MWG Ex. 4.C.1

Q: O WARP (Axioma Fraco da Preferência Revelada) pode falhar na demanda agregada mesmo quando cada consumidor satisfaz WARP individualmente. A razão fundamental é:
- Funções de demanda contínuas podem ter soma descontínua
- Mudanças de preço alteram a distribuição de riqueza real entre consumidores, e WARP individual não controla o efeito-riqueza cruzado entre agentes
- A lei de Walras impõe restrições incompatíveis com WARP no nível agregado
- A soma de matrizes de Slutsky NSD pode ser positiva definida
<!-- YW5zOjE= -->
> Quando $p$ muda, cada consumidor $i$ enfrenta um novo orçamento e faz escolhas consistentes (WARP). Mas as mudanças de preço redistribuem riqueza real (via efeitos sobre dotações, ou transferências dependentes de preço). O WARP individual controla o efeito-substituição de cada agente, mas não o efeito-riqueza agregado que emerge da redistribuição. A soma de escolhas individuais pode ser "como se" irracional no agregado.
> Ref: MWG §4.C, Proposição 4.C.1 (pp. 110–114)
> Similar: MWG Ex. 4.C.2

Q: O resultado de **Sonnenschein-Mantel-Debreu** (SMD), previamente discutido no MWG Cap. 4 e formalizado no Cap. 17, afirma que qualquer função $z: \mathbb{R}^L_{++} \to \mathbb{R}^L$ que satisfaça (i) continuidade, (ii) homogeneidade de grau zero, e (iii) lei de Walras pode ser a função de excesso de demanda agregada de alguma economia com consumidores racionais. A implicação mais devastadora desse resultado para a teoria é:
- O equilíbrio geral não existe em geral
- A racionalidade individual praticamente não restringe o comportamento agregado — é impossível testar a teoria do consumidor com dados agregados
- A demanda agregada nunca pode ser racional
- A lei de Walras é mais restritiva do que se pensava
<!-- YW5zOjE= -->
> SMD mostra que as únicas restrições testáveis da racionalidade individual sobre a demanda agregada são continuidade, homogeneidade e Walras — propriedades triviais que qualquer modelo "razoável" satisfaz. Em particular, simetria e NSD da Slutsky não são testáveis no agregado. Isso significa que dados agregados não podem refutar (nem confirmar) a teoria do consumidor. É por isso que a teoria de equilíbrio geral recorre a teoremas de existência (Brouwer/Kakutani) em vez de caracterizar diretamente a demanda agregada.
> Ref: MWG §4.C (pp. 113–114), §17.E (pp. 598–606)
> Similar: MWG Ex. 17.E.1

Q: Uma consequência direta do SMD é que a **unicidade** do equilíbrio Walrasiano:
- É garantida quando todos os consumidores satisfazem WARP
- Não pode ser deduzida apenas da racionalidade individual — são necessárias condições adicionais (como substituibilidade bruta ou Gorman)
- É sempre garantida pela lei de Walras e pela continuidade do excesso de demanda
- Exige que a demanda agregada satisfaça a condição de Lipschitz
<!-- YW5zOjE= -->
> Se o excesso de demanda agregado pode ser "qualquer coisa" (respeitando apenas continuidade, homogeneidade e Walras), ele pode ter múltiplos zeros — múltiplos equilíbrios. A unicidade requer condições estruturais adicionais: substituibilidade bruta ($\partial z_l/\partial p_k > 0$ para $k \neq l$), forma de Gorman com preferências homotéticas (que garante que $z$ aponta para dentro do simplex de forma "bem comportada"), ou dominância diagonal da Slutsky agregada.
> Ref: MWG §17.F (pp. 606–616); N&S Cap. 13 §13.6
> Similar: MWG Ex. 17.F.1, 17.F.3

## regular

Q: O efeito de **regularização por agregação** (Grandmont) mostra que a demanda agregada pode ser suave mesmo quando demandas individuais não o são. A condição-chave para esse resultado é:
- Que os consumidores tenham preferências idênticas mas riquezas diferentes
- Que exista um número suficientemente grande de consumidores ($I \to \infty$)
- Que a distribuição de parâmetros de preferência na população seja suficientemente dispersa e suave
- Que todas as funções de demanda individuais sejam Lipschitz-contínuas
<!-- YW5zOjI= -->
> Grandmont (1992) mostra que se a população tem parâmetros de preferência distribuídos segundo uma densidade suave e com suporte amplo, as irregularidades individuais (descontinuidades, violações de WARP) são "alisadas" na integração. A demanda agregada herda a suavidade da distribuição populacional, não das demandas individuais — análogo econômico da lei dos grandes números. O resultado não exige $I \to \infty$; depende da dispersão do espaço de tipos, não do número de agentes.
> Ref: MWG §4.C (pp. 113–114); Grandmont (1992)
> Similar: MWG Ex. 4.C.4

Q: As curvas de Engel individuais (demanda como função da riqueza, para preços fixos) são lineares e passam pela origem quando as preferências são homotéticas. Para a demanda agregada depender apenas de $\bar{w}$ com preferências homotéticas (não necessariamente idênticas), é necessário que:
- As curvas de Engel tenham a mesma inclinação para todos os consumidores
- As curvas de Engel passem pela origem para todos os consumidores (que é automático com preferências homotéticas)
- As preferências sejam homotéticas e idênticas
- As curvas de Engel sejam lineares mas com intercepto não-nulo (quasilinear)
<!-- YW5zOjE= -->
> Com preferências homotéticas, $x_{il}(p, w_i) = \beta_{il}(p) w_i$ (Engel linear passando pela origem, $a_i = 0$). A demanda agregada é $\sum_i \beta_{il}(p) w_i$. Se $\beta_{il}$ difere entre consumidores, a soma depende da distribuição de $w_i$, não apenas de $\bar{w}$. Mas como $a_i = 0$, a forma de Gorman se satisfaz (cada $v_i = \phi_i(p) w_i$, e $b_i(p) = \phi_i(p)$ não precisa ser comum quando $a_i = 0$). Na verdade, o ponto sutil é que curvas de Engel passando pela origem garantem que transferências entre agentes não mudam a demanda agregada quando todos têm mesma propensão marginal — o que exige mesma inclinação. Portanto, preferências homotéticas mas não idênticas NÃO garantem Gorman em geral.
> Ref: MWG §4.B (pp. 108–110)
> Similar: MWG Ex. 4.B.3, 4.B.4
