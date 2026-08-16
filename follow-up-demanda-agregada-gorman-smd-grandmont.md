---
quiz: "Follow-up — Demanda Agregada (Gorman, SMD, Grandmont)"
tags:
  regular: "Regularização por agregação — Grandmont (dispersão de tipos ≠ nº de agentes)"
  gorman: "Forma de Gorman e propriedades que sobrevivem à agregação"
  falha: "SMD e a ponte com a perda de simetria"
---

## regular

Q: O resultado de regularização de Grandmont valeria numa população com número **fixo e finito** de consumidores, desde que:
- O número de consumidores seja pelo menos igual ao número de bens ($I \geq L$)
- Os parâmetros de preferência sejam extraídos de uma densidade suficientemente **dispersa e suave** sobre o espaço de tipos
- Cada função de demanda individual seja diferenciável
- Consumidores sejam adicionados até $I \to \infty$
<!-- YW5zOjE= -->
> A regularização não depende da **contagem** de agentes, mas da **dispersão** dos tipos. Com uma população finita e fixa, basta que os parâmetros de preferência estejam suficientemente espalhados (densidade suave, suporte amplo) para que as irregularidades individuais se "alisem" na integração. Exigir $I \to \infty$ é a falácia da lei dos grandes números; exigir diferenciabilidade individual contradiz o próprio ponto (a demanda individual pode ser irregular).
> Ref: MWG Cap. 4, Appendix A (pp. 122–123); Grandmont (1992)
> Similar: MWG Ex. 4.C.4 (p. 122)

Q: A regularização de Grandmont é frequentemente confundida com a lei dos grandes números. A diferença essencial é:
- A lei dos grandes números elimina ruído amostral **aumentando o número de observações**; Grandmont alisa via a **dispersão dos tipos** no espaço de parâmetros, sem exigir crescimento populacional
- São o mesmo mecanismo com nomes diferentes
- A lei dos grandes números exige tipos independentes; Grandmont exige correlação perfeita entre tipos
- Grandmont exige $I \to \infty$ enquanto a lei dos grandes números vale para $I$ finito
<!-- YW5zOjA= -->
> A lei dos grandes números é sobre **quantidade** de sorteios; Grandmont é sobre **heterogeneidade** (o quão espalhados estão os tipos). A última opção inverte exatamente os papéis — é o erro típico. Grandmont vale para população finita; o que precisa "crescer" é a dispersão, não o número de agentes.
> Ref: MWG Cap. 4, Appendix A (pp. 122–123); Grandmont (1992)
> Similar: MWG Ex. 4.C.4 (p. 122)

Q: No resultado de Grandmont, a suavidade da demanda agregada é herdada de:
- Da convexidade dos conjuntos orçamentários individuais
- Da **densidade suave** que descreve como os parâmetros de preferência se distribuem na população
- Da continuidade de cada função de demanda individual
- Do teorema do máximo aplicado à demanda individual
<!-- YW5zOjE= -->
> A demanda agregada herda a suavidade **da distribuição populacional de tipos**, não das demandas individuais — que podem ser descontínuas ou violar WARP. É o análogo econômico de "integrar uma função feia contra uma densidade suave gera algo suave".
> Ref: MWG Cap. 4, Appendix A (pp. 122–123)
> Similar: MWG Ex. 4.C.4 (p. 122)

## gorman

Q: Ao somar demandas individuais para formar a demanda agregada $x(p, w_1, \ldots, w_I) = \sum_i x_i(p, w_i)$, **sem** hipóteses adicionais sobre preferências, a propriedade que **NÃO** sobrevive é:
- Homogeneidade de grau zero
- Lei de Walras
- **Simetria da matriz de Slutsky**
- Continuidade (quando cada $x_i$ é contínua)
<!-- YW5zOjI= -->
> Homogeneidade de grau zero e lei de Walras passam pela soma automaticamente; a continuidade também (soma de contínuas). A **simetria da Slutsky** é a única que se perde: a matriz de Slutsky da demanda agregada inclui termos de efeito-riqueza que dependem da distribuição $(w_1,\ldots,w_I)$, destruindo a simetria em geral. NSD e simetria da racionalidade individual **não** são propriedades agregadas.
> Ref: MWG §4.B–§4.C (pp. 106–116); §2.F (pp. 28–36)
> Similar: MWG Ex. 4.C.6 (p. 122); 2.F.5 (p. 35)

Q: A matriz de Slutsky da demanda agregada é simplesmente a soma das matrizes de Slutsky individuais, herdando simetria e NSD? A resposta correta é:
- Sim, e por isso ela herda simetria e NSD
- **Não exatamente:** cada $S_i$ individual é simétrica e NSD, mas a matriz de Slutsky da demanda **agregada** (definida sobre a riqueza agregada) inclui termos de efeito-riqueza que dependem da distribuição $(w_1,\ldots,w_I)$ e quebram a simetria
- Não, porque a lei de Walras agregada falha
- Sim, mas ela perde a NSD e mantém a simetria
<!-- YW5zOjE= -->
> O erro comum é tratar "Slutsky agregada" como soma limpa de $S_i$'s simétricas. A definição correta da Slutsky agregada compensa pela **riqueza agregada**, e a redistribuição de riqueza entre agentes injeta termos cruzados de efeito-riqueza que não são simétricos. Por isso a simetria (que vem da maximização de utilidade individual, via Shephard + Young) não é uma propriedade do agregado.
> Ref: MWG §4.C (pp. 109–116); §3.G (pp. 67–75)
> Similar: MWG Ex. 4.C.6 (p. 122)

Q: Para que a demanda agregada se comporte "como se" viesse de um único consumidor racional (representativo positivo), recuperando estrutura como a lei da demanda, a hipótese suficiente clássica é:
- **Forma de Gorman**: $v_i(p, w_i) = a_i(p) + b(p) w_i$ com $b(p)$ comum a todos
- Que todos os consumidores satisfaçam WARP individualmente
- Que a matriz de Slutsky individual seja diagonal
- Que $I \to \infty$
<!-- YW5zOjA= -->
> A forma de Gorman (utilidade indireta linear em $w_i$ com coeficiente marginal $b(p)$ **comum**) faz a demanda agregada depender só de $\bar w = \sum_i w_i$, o que permite tratá-la como a de um consumidor representativo. WARP individual não basta (pode falhar no agregado); Slutsky diagonal e $I\to\infty$ são distratores.
> Ref: MWG §4.B, Prop. 4.B.1 (pp. 106–109); §4.D (pp. 116–122)
> Similar: MWG Ex. 4.B.1, 4.B.2 (p. 122)

## falha

Q: O teorema de Sonnenschein-Mantel-Debreu diz que a função de excesso de demanda agregada só precisa satisfazer continuidade, homogeneidade de grau zero e lei de Walras. Qual afirmação sobre a **matriz de Slutsky agregada** é **consistente** com o SMD?
- A Slutsky agregada é sempre simétrica e NSD, como a individual
- **SMD implica que simetria e NSD da Slutsky NÃO são restrições impostas pela racionalidade individual no nível agregado**
- SMD garante simetria mas não NSD
- SMD só se aplica quando as preferências são idênticas
<!-- YW5zOjE= -->
> Esta é a **ponte** com a questão da simetria: se o excesso de demanda agregado pode ser essencialmente qualquer função (respeitando só continuidade + homogeneidade + Walras), então simetria e NSD da Slutsky **não** podem ser restrições agregadas — senão elas apareceriam na lista do SMD. Afirmar que a Slutsky agregada é sempre simétrica contradiz frontalmente o SMD.
> Ref: MWG §4.C (pp. 113–114); §17.E (pp. 598–606)
> Similar: MWG Ex. 4.C.8 (p. 122)

Q: Como a demanda agregada "pode ser quase qualquer coisa" (SMD), a **unicidade** do equilíbrio Walrasiano exige condições estruturais adicionais. Uma condição suficiente clássica é:
- **Substituibilidade bruta (gross substitutes)** no excesso de demanda agregado
- Que cada consumidor satisfaça WARP
- Homogeneidade de grau zero da demanda agregada
- Continuidade do excesso de demanda
<!-- YW5zOjA= -->
> Substituibilidade bruta ($\partial z_l/\partial p_k > 0$ para $k \neq l$) garante um único zero do excesso de demanda. Homogeneidade e continuidade **sempre** valem (pelo próprio SMD) e por isso não podem, sozinhas, entregar unicidade. WARP individual não se estende ao agregado.
> Ref: MWG §17.F (pp. 606–616); N&S Cap. 13 §13.6
> Similar: MWG Ex. 17.F.1 (p. 616)
