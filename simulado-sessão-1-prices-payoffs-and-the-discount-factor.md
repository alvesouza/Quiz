---
quiz: "Simulado — Sessão 1: Prices, Payoffs, and the Discount Factor"
tags:
  returns: "Retornos e o Registro Histórico"
  pmx: "p = E[mx] — Preços e Payoffs"
  ad: "Arrow–Debreu e Completude"
  sdf: "De State Prices ao SDF"
  consq: "Primeiras Consequências"
  rn: "Probabilidades Risco-Neutras"
---

## returns

P: Uma série de excessos de retorno mensais do mercado acionário cobre $T=1200$ meses (cem anos), com média amostral de $0{,}70\%$ ao mês e desvio-padrão amostral de $5{,}20\%$ ao mês. Trate os retornos como i.i.d. e use as convenções de anualização do curso.

Q: Anualizando a série, quais são o prêmio médio, a volatilidade e o Sharpe ratio?
- Prêmio de 8,4% a.a., volatilidade de 18,0% a.a. e Sharpe de 0,47 — a média escala com $k$ e o desvio-padrão com $\sqrt{k}$.
- Prêmio de 8,4% a.a., volatilidade de 62,4% a.a. e Sharpe de 0,13 — a média e o desvio-padrão escalam ambos com $k$.
- Prêmio de 2,42% a.a., volatilidade de 18,0% a.a. e Sharpe de 0,13 — a média escala com $\sqrt{k}$ e o desvio também.
- Prêmio de 8,4% a.a., volatilidade de 5,20% a.a. e Sharpe de 1,62 — a média anualiza e o desvio permanece mensal.
<!-- YW5zOjA= -->
> $12\times 0{,}70\%=8{,}4\%$ e $5{,}20\%\times\sqrt{12}=18{,}0\%$, logo $8{,}4/18{,}0\approx 0{,}47$. A assimetria $k$ versus $\sqrt{k}$ é o que faz o Sharpe crescer com o horizonte sob i.i.d.
> Ref: Ribeiro (2026), Cap. 1, §1.2 (p. 5); BKM 13e, Cap. 5, §5.1 (p. 126)
> Similar: Ribeiro, Exercício 1.1 (p. 33); BKM, Cap. 5, Problem Sets (p. 161)

Q: Qual o erro-padrão do prêmio anualizado, e o que aconteceria com ele ao passar para dados diários?
- Cerca de 0,15 ponto percentual ao ano; passar a dados diários no mesmo século reduziria o erro por um fator de $\sqrt{21}$.
- Cerca de 5,2 pontos percentuais ao ano; passar a dados diários no mesmo século reduziria o erro por um fator próximo de 21.
- Cerca de 1,8 ponto percentual ao ano; passar a dados diários no mesmo século não reduziria o erro, que depende do span amostral.
- Cerca de 1,8 ponto percentual ao ano; passar a dados diários no mesmo século reduziria o erro na proporção do erro da volatilidade.
<!-- YW5zOjI= -->
> $\text{SE}=5{,}20/\sqrt{1200}=0{,}150\%$ ao mês, ou $1{,}80\%$ ao ano. Amostrar mais fino melhora a estimativa de $\sigma$, nunca a da média: esta depende só de quanto tempo calendário a amostra cobre.
> Ref: Ribeiro (2026), Cap. 1, §1.2 (p. 5); BKM 13e, Cap. 5, §5.6 (p. 143)
> Similar: Ribeiro, Exercício 1.1 (p. 33); Exercício 1.6 (p. 34)

Q: Qual a média geométrica anualizada implícita, e como ela se compara à aritmética?
- Cerca de 10,0% a.a., acima da aritmética, porque a composição acumula os ganhos ao longo do horizonte de investimento.
- Cerca de 6,8% a.a., abaixo da aritmética, porque o arrasto de volatilidade subtrai aproximadamente $\sigma^2/2$ da média.
- Cerca de 8,4% a.a., igual à aritmética, porque os retornos foram supostos independentes e identicamente distribuídos.
- Cerca de 5,2% a.a., abaixo da aritmética, porque o arrasto de volatilidade subtrai a variância $\sigma^2$ inteira da média.
<!-- YW5zOjE= -->
> $\mu_g\approx\mu_a-\sigma^2/2=8{,}4\%-0{,}180^2/2=8{,}4\%-1{,}62\text{ p.p.}\approx 6{,}8\%$. A geométrica é sempre menor; dizer o contrário é a armadilha canônica do §1.2.
> Ref: Ribeiro (2026), Cap. 1, §1.2 (p. 5); BKM 13e, Cap. 5, §5.1 (p. 126)
> Similar: Ribeiro, Exercício 1.7 (p. 34); BKM, Cap. 5, Problem Sets (p. 161)

P:

Q: Por que a ordenação de classes de ativos por prêmio médio difere da ordenação por Sharpe ratio?
- O prêmio remunera a quantidade de risco e o Sharpe remunera por unidade de risco; só a segunda ordenação é invariante a alavancagem.
- O prêmio usa média aritmética e o Sharpe usa média geométrica; a diferença é o arrasto de volatilidade e some com retornos i.i.d.
- O prêmio é medido em termos nominais e o Sharpe em termos reais; a diferença reflete a inflação e some ao deflacionar as duas séries.
- O prêmio é estimado com erro-padrão e o Sharpe sem erro algum; a diferença é ruído amostral e some quando o span da amostra cresce.
<!-- YW5zOjA= -->
> Alavancar um ativo multiplica prêmio e volatilidade pelo mesmo fator: o prêmio sobe, o Sharpe não se move. É por isso que ações lideram em prêmio sem liderar em Sharpe.
> Ref: Ribeiro (2026), Cap. 1, §1.2 (p. 5); BKM 13e, Cap. 5, §5.7 (p. 147)
> Similar: Ribeiro, Exercício 1.7 (p. 34); Exercício 7.1 (Cap. 7)

Q: Segundo Dimson, Marsh e Staunton, qual o viés de estimar o prêmio de ações só com dados dos EUA, e o que isso faz com o bound de Hansen–Jagannathan?
- Os EUA tiveram inflação acima da média mundial e o prêmio nominal é inflado; deflacionar as séries remove o viés e o bound fica igual.
- Os EUA têm a série mais longa disponível e o prêmio americano é o mais preciso; o bound calculado com ele é o mais confiável possível.
- Os EUA sofreram interrupções de mercado nas duas guerras e o prêmio é subestimado; o bound resultante é menos exigente do que deveria.
- Os EUA foram um dos mercados mais bem-sucedidos do século e o prêmio é superestimado; o bound fica mais exigente do que deveria ser.
<!-- YW5zOjM= -->
> É viés de sobrevivência em nível de país: os 16 mercados de Dimson mostram prêmios menores fora dos EUA. Como o bound é $\sigma(m)/E[m]\ge$ Sharpe, um Sharpe inflado exige um $m$ mais volátil do que o necessário.
> Ref: Ribeiro (2026), Cap. 1, §1.2 (p. 5); Dimson, Marsh & Staunton, *Triumph of the Optimists*
> Similar: Ribeiro, Exercício 1.6 (p. 34)

## pmx

Q: A Sessão 1 fecha dizendo que $p=E[m\,x]$ é "quase vazia". Qual formulação capta com precisão o que a equação impõe?
- Ela impõe que os investidores maximizem utilidade esperada com preferências côncavas, pois só assim o operador de preços resulta linear.
- Ela impõe que exista algum funcional linear precificando todo o espaço de payoffs, e nada além disso; sem amarrar $m$, não há conteúdo.
- Ela impõe que o mercado seja completo, pois do contrário o espaço de payoffs não é fechado sob formação de carteira e nada se define.
- Ela impõe que $m$ seja mensurável em relação ao consumo agregado, pois é essa restrição que lhe dá conteúdo econômico testável.
<!-- YW5zOjE= -->
> Qualquer conjunto de preços sem arbitragem admite um $m$. O conteúdo empírico só aparece quando se propõe um candidato observável — consumo na Sessão 2, retorno de mercado na Sessão 4.
> Ref: Ribeiro (2026), Cap. 1, §1.3 (p. 13); Cochrane (2005), Cap. 1, §1.1
> Similar: Ribeiro, True/False 1.1–1.30 (p. 35)

Q: O espaço de payoffs é fechado sob formação de carteira e vale a lei do preço único. O que isso, sozinho, garante sobre o funcional de preços?
- Que $p(\cdot)$ seja linear e representável como $E[m\,x]$ para algum $m$, sem que se possa afirmar que esse $m$ seja positivo.
- Que $p(\cdot)$ seja linear e estritamente positivo, pois um preço negativo para um payoff não negativo violaria a lei do preço único.
- Que $p(\cdot)$ seja côncavo no espaço de payoffs, refletindo a aversão a risco do investidor representativo que sustenta o equilíbrio.
- Que $p(\cdot)$ seja linear apenas no subconjunto dos payoffs replicáveis, permanecendo indefinido nos demais elementos do espaço.
<!-- YW5zOjA= -->
> Lei do preço único $\Rightarrow$ linearidade $\Rightarrow$ representação por um produto interno, isto é, por algum $m$. Positividade é uma exigência adicional, comprada pela ausência de arbitragem.
> Ref: Ribeiro (2026), Cap. 1, §1.5 (p. 22); Cochrane (2005), Cap. 4, §4.1
> Similar: Ribeiro, Exercício 1.3 (p. 33)

Q: Seguro e bilhete de loteria têm ambos retorno esperado negativo. Na linguagem de $p=E[mx]$, o que os distingue?
- Ambos têm $\text{cov}(m,x)>0$, e a diferença é apenas de magnitude, sendo o seguro o caso extremo dessa mesma família.
- O seguro tem $\text{cov}(m,x)<0$ e a loteria tem $\text{cov}(m,x)>0$; a assimetria dos payoffs inverte o sinal das covariâncias.
- O seguro paga nos estados de $m$ alto e $\text{cov}(m,x)>0$ explica seu preço elevado; a loteria paga com $m$ baixo e escapa ao modelo.
- Nenhum dos dois é precificável por $p=E[mx]$, pois payoffs de retorno esperado negativo violam a ausência de arbitragem do capítulo.
<!-- YW5zOjI= -->
> O seguro é caro porque entrega justamente onde a escassez é maior — retorno esperado abaixo de $R_f$ é o preço da proteção. A loteria entrega onde $m$ é baixo: deveria ser barata, e não é. Isso é preferência por assimetria, fora de $p=E[mx]$.
> Ref: Ribeiro (2026), Cap. 1, §1.6 (p. 25)
> Similar: Ribeiro, Exercício 1.5 (p. 34)

Q: Um pesquisador usa $y$ como discount factor quando o verdadeiro é $m$, e $y$ precifica corretamente o ativo livre de risco. Qual é seu erro de precificação num payoff $x$, e o que o anula?
- $E[y-m]\,E[x]$; o erro se anula quando as médias coincidem, o que já foi imposto, de modo que nunca haveria erro algum.
- $\sigma(y-m)\,\sigma(x)$; o erro se anula apenas se $y=m$ estado a estado, de modo que nenhum candidato falso precifica payoff algum.
- $[\text{cov}(y,x)-\text{cov}(m,x)]/E[m]$; o erro se anula quando $y$ é transformação afim de $m$ com coeficiente unitário.
- $\text{cov}(y-m,\,x)$; o erro se anula em todo o espaço de payoffs quando $y-m$ é ortogonal a ele, isto é, quando as projeções coincidem.
<!-- YW5zOjM= -->
> $p_y(x)-p(x)=E[(y-m)x]=\text{cov}(y-m,x)+E[y-m]E[x]$, e o segundo termo some com $E[y]=E[m]$. Um $y$ errado estado a estado ainda precifica tudo se sua projeção sobre o espaço de payoffs for a mesma.
> Ref: Ribeiro (2026), Cap. 1, §1.5 (p. 22); Campbell (2018), Cap. 4
> Similar: Ribeiro, Exercício 1.3 (p. 33)

Q: Dispondo apenas de excessos de retorno, um pesquisador impõe $0=E[m\,R^e]$ para todos eles. O que essa condição identifica sobre $m$?
- Identifica $m$ por completo, desde que haja tantos excessos de retorno linearmente independentes quantos forem os estados.
- Identifica $m$ apenas até uma constante multiplicativa positiva, pois a condição é homogênea de grau um: a escala fica livre.
- Identifica $E[m]$ mas não sua dispersão entre estados, que só apareceria com um ativo cujo preço observado seja diferente de zero.
- Não identifica nada sobre $m$, pois a condição vale trivialmente para qualquer variável aleatória de média igual a zero.
<!-- YW5zOjE= -->
> Se $m$ satisfaz $0=E[mR^e]$, então $cm$ também satisfaz para todo $c>0$. Sem um ativo de preço não nulo — o livre de risco, tipicamente — não se identifica $E[m]$ nem, portanto, $R_f$. É exatamente por isso que testes com excessos de retorno estimam prêmios, não o nível do SDF.
> Ref: Ribeiro (2026), Cap. 1, §1.6 (p. 25); Cochrane (2005), Cap. 1, §1.4
> Similar: Ribeiro, Exercício 1.4 (p. 33)

## ad

P: Um mercado tem três estados — expansão, normal e recessão — com probabilidades físicas $\pi=(0{,}25;\ 0{,}50;\ 0{,}25)$. Negociam-se três ativos: um bond que paga 1 em todo estado, ao preço 0,96; uma ação de payoffs $(2{,}00;\ 1{,}00;\ 0{,}50)$, ao preço 0,945; e uma call sobre a ação com strike 1,00 e payoffs $(1{,}00;\ 0;\ 0)$, ao preço 0,15.

Q: Quais são os state prices $q$ desse mercado?
- $q=(0{,}60;\ 0{,}96;\ 1{,}32)$ — resolvendo o sistema e reponderando cada linha pela probabilidade física do estado.
- $q=(0{,}156;\ 0{,}500;\ 0{,}344)$ — resolvendo o sistema e normalizando o vetor para que os três componentes somem 1.
- $q=(0{,}15;\ 0{,}48;\ 0{,}33)$ — resolvendo o sistema linear cujas linhas são os payoffs e cujo lado direito são os preços.
- $q=(0{,}15;\ 0{,}51;\ 0{,}30)$ — resolvendo o sistema com a call avaliada no estado de recessão, e não no de expansão como devido.
<!-- YW5zOjI= -->
> A call dá $q_1=0{,}15$; o bond dá $q_1+q_2+q_3=0{,}96$; a ação dá $2q_1+q_2+0{,}5q_3=0{,}945$. Resolvendo, $q_3=0{,}33$ e $q_2=0{,}48$. Em Python: `np.linalg.solve(X, p)` com `X` quadrada e de posto cheio.
> Ref: Ribeiro (2026), Cap. 1, §1.4 (p. 16); D&D 3e, Cap. 9
> Similar: Ribeiro, Exercício 1.2 (p. 33)

Q: A partir dos state prices, quais são o SDF estado a estado e a taxa livre de risco líquida?
- $m=(0{,}60;\ 0{,}96;\ 1{,}32)$ e $R_f-1=4{,}17\%$, com $E[m]=0{,}96$ igual à soma dos três state prices.
- $m=(0{,}15;\ 0{,}48;\ 0{,}33)$ e $R_f-1=4{,}17\%$, pois o discount factor é o próprio vetor de state prices.
- $m=(0{,}60;\ 0{,}96;\ 1{,}32)$ e $R_f-1=4{,}00\%$, tomando a taxa como o complemento de $E[m]$ em relação a 1.
- $m=(0{,}0375;\ 0{,}240;\ 0{,}0825)$ e $R_f-1=4{,}17\%$, multiplicando cada state price pela probabilidade do estado.
<!-- YW5zOjA= -->
> $m(s)=q(s)/\pi(s)$ dá $(0{,}60;\,0{,}96;\,1{,}32)$: alto na recessão, baixo na expansão. $E[m]=\sum_s q(s)=0{,}96$ e $R_f=1/0{,}96=1{,}0417$. Confundir $q$ com $m$ é a armadilha do §1.5.
> Ref: Ribeiro (2026), Cap. 1, §1.5 (p. 22); Cochrane (2005), Cap. 1, §1.2
> Similar: Ribeiro, Exercício 1.4 (p. 33)

Q: Um contrato paga 1 real apenas na recessão. Qual seu preço e seu retorno bruto esperado?
- Preço de 0,33 e retorno esperado de $+4{,}17\%$, igual a $R_f$, pois os state prices já embutem todo o desconto por risco.
- Preço de 0,25 e retorno esperado de $0\%$, pois o preço de um contrato de seguro iguala seu payoff esperado sob a medida física.
- Preço de 0,22 e retorno esperado de $+13{,}6\%$, acima de $R_f$, pois o contrato é uma posição alavancada no estado de recessão.
- Preço de 0,33 e retorno esperado de $-24{,}2\%$, abaixo de $R_f$, pois $\text{cov}(m,x)>0$ encarece o payoff frente a $E[x]/R_f$.
<!-- YW5zOjM= -->
> Preço $=q_3=0{,}33$; payoff esperado $=0{,}25$; logo $E[R]=0{,}25/0{,}33=0{,}758$, isto é, $-24{,}2\%$. Seguro é caro porque paga onde $m$ é alto — retorno esperado negativo não é anomalia, é o prêmio pago pela proteção.
> Ref: Ribeiro (2026), Cap. 1, §1.6 (p. 25)
> Similar: Ribeiro, Exercício 1.5 (p. 34)

P:

Q: Com três estados e apenas bond e ação negociados o mercado é incompleto. Qual acréscimo o completa, e por quê?
- Uma call sobre a ação com strike 0,40, pois toda opção acrescenta uma dimensão nova ao espaço de payoffs negociados.
- Uma call sobre a ação com strike 1,00, pois seu payoff $(1;\,0;\,0)$ está fora do span gerado pelo bond e pela ação.
- Um segundo bond, de payoff 2 em todo estado e preço 1,92, pois eleva de dois para três o número de ativos negociados.
- Uma ação estrangeira de payoffs $(4{,}00;\,2{,}00;\,1{,}00)$, pois seus payoffs diferem entre si nos três estados da natureza.
<!-- YW5zOjE= -->
> Só a call com strike acima de 0,50 sai do span. Com strike 0,40 o payoff $(1{,}6;\,0{,}6;\,0{,}1)$ é exatamente $-0{,}4$ do bond mais 1,0 da ação — redundante; o segundo bond e a ação estrangeira são múltiplos escalares. Completude é posto 3, não contagem de ativos.
> Ref: Ribeiro (2026), Cap. 1, §1.4 (p. 16); D&D 3e, Cap. 11
> Similar: Ribeiro, Exercício 1.2 (p. 33); Exercício 1.8 (p. 35)

Q: Em mercado incompleto, um payoff não-*spanned* admite apenas limites de preço. Como se constrói cada limite?
- O superior é o preço do super-replicante mais caro e o inferior o do sub-replicante mais barato; fora desse intervalo há arbitragem.
- O superior é $E[x]/R_f$ e o inferior é zero; qualquer preço nesse intervalo é compatível com a ausência de oportunidades de arbitragem.
- O superior é o preço do super-replicante mais barato e o inferior o do sub-replicante mais caro; entre os dois não há arbitragem.
- O superior é o preço do sub-replicante mais caro e o inferior o do super-replicante mais barato; o intervalo some se o payoff for spanned.
<!-- YW5zOjI= -->
> Super-replicar é dominar o payoff em todo estado: o mais barato desses portfólios é o teto. Sub-replicar é ser dominado: o mais caro é o piso. Inverter "mais caro / mais barato" é a armadilha clássica; ambos saem de um problema de programação linear.
> Ref: Ribeiro (2026), Cap. 1, §1.4 (p. 16)
> Similar: Ribeiro, Exercício 1.8 (p. 35)

## sdf

Q: Qual associação entre hipótese e resultado do §1.5 está correta?
- Lei do preço único dá existência de algum $m$; ausência de arbitragem permite escolher $m>0$; completude dá unicidade de $m$.
- Ausência de arbitragem dá existência de algum $m$; lei do preço único dá a positividade; completude dá a unicidade de $m$.
- Lei do preço único dá existência e unicidade de $m$; ausência de arbitragem dá positividade; completude nada acrescenta ao quadro.
- Completude dá existência de algum $m$; lei do preço único dá a unicidade; ausência de arbitragem dá a positividade de $m$.
<!-- YW5zOjA= -->
> As três compras são distintas e cumulativas. Trocar as duas primeiras é o erro mais comum: a lei do preço único basta para existência, e é a ausência de arbitragem — hipótese estritamente mais forte — que compra $m>0$.
> Ref: Ribeiro (2026), Cap. 1, §1.5 (p. 22); Cochrane (2005), Cap. 4, §4.1–4.2
> Similar: Ribeiro, True/False 1.1–1.30 (p. 35)

Q: Em mercado incompleto há um continuum de discount factors válidos. O que, nesse continuum, é único?
- O discount factor de maior variância entre os estritamente positivos; os demais se obtêm dele por rotação dentro do espaço de payoffs.
- Nenhum objeto é único: a incompletude destrói inclusive o preço dos ativos negociados, que passa a admitir um intervalo de valores.
- O valor de $m$ nos estados de probabilidade física positiva; a multiplicidade se concentra apenas nos estados de probabilidade nula.
- A projeção $x^*$ de $m$ sobre o espaço de payoffs; todos os discount factors válidos a partilham e diferem por um termo ortogonal.
<!-- YW5zOjM= -->
> Todo $m$ válido se escreve $m=x^*+\varepsilon$ com $E[\varepsilon x]=0$ para todo payoff negociado. Os preços dos ativos negociados continuam perfeitamente determinados; a indeterminação atinge apenas payoffs fora do span.
> Ref: Ribeiro (2026), Cap. 1, §1.5 (p. 22); Cochrane (2005), Cap. 4, §4.1
> Similar: Ribeiro, Exercício 1.3 (p. 33); Exercício 1.8 (p. 35)

Q: Um conjunto de preços satisfaz a lei do preço único mas admite uma oportunidade de arbitragem. O que se pode afirmar sobre $m$?
- Não existe $m$ algum precificando os ativos negociados, pois a arbitragem quebra a linearidade do funcional de preços.
- Existe $m$ precificando todos os ativos negociados, mas todo $m$ com essa propriedade fica negativo em pelo menos um estado.
- Existe $m$ estritamente positivo, porém não único, e a arbitragem se manifesta apenas nessa multiplicidade de soluções.
- Existe $m$ precificando os ativos e ele é necessariamente positivo, pois $m=q/\pi$ e probabilidades são sempre positivas.
<!-- YW5zOjE= -->
> Linearidade sobrevive — a lei do preço único é tudo que ela exige — mas a representação só é possível com algum $q(s)<0$, e portanto $m(s)<0$. A última alternativa esquece que $q$ pode ser negativo justamente quando há arbitragem.
> Ref: Ribeiro (2026), Cap. 1, §1.5 (p. 22); Cochrane (2005), Cap. 4, §4.2
> Similar: Ribeiro, Exercício 1.2 (p. 33)

Q: A definição $m(s)=q(s)/\pi(s)$ é uma reponderação. O que ela implica num estado de probabilidade física muito pequena e state price não desprezível?
- $m$ é muito grande nesse estado, que passa a dominar a variabilidade do SDF; é assim que desastres raros geram prêmios altos.
- $m$ é muito pequeno nesse estado, pois a raridade desconta o valor de um real entregue ali, reduzindo sua contribuição ao preço.
- $m$ é indeterminado nesse estado, e o SDF só se define onde a probabilidade física excede estritamente o state price do estado.
- $m$ vale exatamente 1 nesse estado, pois a reponderação neutraliza a diferença entre a medida física e a medida de precificação.
<!-- YW5zOjA= -->
> $q$ mede quanto se paga; $\pi$ mede quão frequente é. Pagar caro por algo raro significa valorizar muito o real entregue lá, e $\sigma(m)$ pode ser enorme mesmo com $E[m]$ próximo de 1 — o canal que a Sessão 2 tentará, sem sucesso, obter do consumo.
> Ref: Ribeiro (2026), Cap. 1, §1.5 (p. 22)
> Similar: Ribeiro, Exercício 1.4 (p. 33); Exercício 2.4 (p. 72)

Q: Dois discount factors $m_1$ e $m_2$ precificam corretamente todos os ativos negociados. O que necessariamente vale para a diferença?
- $m_1-m_2=0$ estado a estado, pois dois discount factors que precificam o mesmo conjunto de ativos necessariamente coincidem.
- $\text{cov}(m_1-m_2,\,x)=0$ para todo payoff negociado, embora $E[(m_1-m_2)\,x]$ possa ser diferente de zero em alguns deles.
- $E[(m_1-m_2)\,x]=0$ para todo payoff negociado, sem que $m_1-m_2$ precise ser identicamente nulo fora do espaço de payoffs.
- $E[m_1-m_2]=0$ e $\sigma(m_1-m_2)=0$, de modo que a diferença entre os dois é uma constante necessariamente igual a zero.
<!-- YW5zOjI= -->
> Se ambos precificam $x$, então $E[m_1x]=E[m_2x]=p(x)$, logo a diferença é ortogonal a todo o espaço de payoffs. Fora dele ela pode ser arbitrária: é exatamente o continuum do §1.5.
> Ref: Ribeiro (2026), Cap. 1, §1.5 (p. 22); Cochrane (2005), Cap. 4, §4.1
> Similar: Ribeiro, Exercício 1.3 (p. 33)

## consq

Q: Suponha que $m$ fosse constante entre estados. O que aconteceria com os retornos esperados?
- Todo ativo teria retorno esperado nulo, pois um $m$ constante não desconta o futuro e o preço igualaria o payoff esperado.
- Os retornos esperados continuariam a variar entre ativos, pois $\beta_{i,m}$ é específico de cada ativo mesmo com $m$ constante.
- Nenhum ativo de risco poderia ser negociado, pois o bound de Hansen–Jagannathan com $\sigma(m)=0$ seria violado por qualquer um.
- Todo ativo teria retorno esperado igual a $R_f$, pois $\text{cov}(m,x)=0$ para qualquer payoff quando $m$ não varia.
<!-- YW5zOjM= -->
> Em $p=E[x]/R_f+\text{cov}(m,x)$, um $m$ constante zera o segundo termo para todo $x$. O bound com $\sigma(m)=0$ força todo Sharpe a zero, não proíbe a negociação: ativos de risco existem, apenas sem prêmio.
> Ref: Ribeiro (2026), Cap. 1, §1.6 (p. 25); Cochrane (2005), Cap. 1, §1.4
> Similar: Ribeiro, Exercício 1.4 (p. 33)

Q: Dois ativos têm o mesmo payoff esperado; A tem $\text{cov}(m,x_A)>0$ e B tem $\text{cov}(m,x_B)<0$. Qual comparação está correta?
- A é o mais caro e seu retorno esperado fica acima de $R_f$, pois preço alto e prêmio de risco alto caminham sempre juntos.
- A é o mais caro e seu retorno esperado fica abaixo de $R_f$; B é o mais barato e seu retorno esperado fica acima de $R_f$.
- A é o mais barato, pois covariância positiva com $m$ sinaliza risco, e todo risco exige um desconto no preço do ativo.
- Os dois têm o mesmo preço, pois o payoff esperado é idêntico e a covariância afeta apenas a variância do retorno realizado.
<!-- YW5zOjE= -->
> $p=E[x]/R_f+\text{cov}(m,x)$: covariância positiva soma ao preço, e preço maior com mesmo payoff esperado significa retorno esperado menor. A é o ativo tipo seguro; B é o ativo tipo ação.
> Ref: Ribeiro (2026), Cap. 1, §1.6 (p. 25); Cochrane (2005), Cap. 1, §1.4
> Similar: Ribeiro, Exercício 1.5 (p. 34)

Q: Na representação $E[R^i]=R_f+\beta_{i,m}\lambda_m$, o que é $\lambda_m$ e qual seu sinal?
- $\lambda_m=\sigma^2(m)/E[m]$, portanto positivo; ativos de beta positivo em $m$ têm retorno esperado acima de $R_f$.
- $\lambda_m=E[m]/\sigma^2(m)$, portanto positivo; é o inverso do preço de risco e cresce quando $m$ é pouco volátil.
- $\lambda_m=-\sigma^2(m)/E[m]$, portanto negativo; ativos de beta positivo em $m$ têm retorno esperado abaixo de $R_f$.
- $\lambda_m=\sigma(m)/E[m]$, portanto positivo; é exatamente o lado direito do bound de Hansen–Jagannathan.
<!-- YW5zOjI= -->
> O preço de risco associado ao próprio SDF é negativo: quem entrega mais quando $m$ é alto entrega quando você mais precisa, e paga por isso com retorno esperado menor. A última alternativa troca $\lambda_m$ pelo lado direito do bound.
> Ref: Ribeiro (2026), Cap. 1, §1.6 (p. 25); Cochrane (2005), Cap. 1, §1.4
> Similar: Ribeiro, Exercício 1.4 (p. 33)

Q: O Sharpe anual do mercado é 0,50 e $E[m]=0{,}96$. O que o bound de Hansen–Jagannathan impõe?
- $\sigma(m)\ge 0{,}48$, e nenhum ativo negociado pode exibir Sharpe acima de $\sigma(m)/E[m]$ nessa economia.
- $\sigma(m)\ge 0{,}50$, pois o bound restringe diretamente o desvio-padrão de $m$, e não seu coeficiente de variação.
- $\sigma(m)\le 0{,}48$, pois o bound é um teto sobre a volatilidade de $m$ compatível com os preços observados.
- $\sigma(m)\ge 0{,}52$, usando $E[m]=R_f=1{,}04$ como fator de escala do lado direito da desigualdade do bound.
<!-- YW5zOjA= -->
> $|E[R^e]|/\sigma(R^e)\le\sigma(m)/E[m]$ dá $\sigma(m)\ge 0{,}50\times 0{,}96=0{,}48$. É um piso, e o piso vale contra o melhor Sharpe disponível. Esse número é a metade viva do choque da Sessão 2.
> Ref: Ribeiro (2026), Cap. 1, §1.6 (p. 25); Cochrane (2005), Cap. 4, §4.3.2
> Similar: Ribeiro, Exercício 1.6 (p. 34); Exercício 2.3 (p. 71)

Q: Um colega objeta que escrever $E[R^i]=R_f+\beta_{i,m}\lambda_m$ já pressupõe o CAPM. Qual resposta é correta?
- O colega está certo: a representação beta é a security market line, e a security market line é o próprio enunciado do CAPM.
- O colega está certo em parte: a representação exige que $m$ seja estritamente positivo, e apenas o CAPM assegura essa positividade.
- A representação exige mercados completos, e é essa hipótese — e não o CAPM — que a sustenta em qualquer economia considerada.
- A representação é reescrita algébrica de $p=E[mx]$ e vale para todo $m$ válido; o CAPM só entra ao tornar $m$ linear no mercado.
<!-- YW5zOjM= -->
> A forma beta é identidade, não modelo: $\beta_{i,m}$ varia por ativo e $\lambda_m$ é comum a todos. O conteúdo do CAPM está em afirmar $m=a+bR^{mkt}$, que é a Sessão 4.
> Ref: Ribeiro (2026), Cap. 1, §1.6 (p. 25); Cochrane (2005), Cap. 6
> Similar: Ribeiro, True/False 1.1–1.30 (p. 35); Exercício 4.1 (Cap. 4)

## rn

Q: Sobre $\tilde\pi(s)=m(s)\pi(s)/E[m]$, quais propriedades a reponderação garante e sob qual hipótese?
- Soma 1 e é estritamente positiva já sob a lei do preço único; a ausência de arbitragem só é necessária para a medida ser única.
- Soma $E[m]$ e é positiva sob ausência de arbitragem; por isso é preciso descontar os preços por $R_f$ mais de uma vez ao final.
- Soma 1 por construção e é estritamente positiva sob ausência de arbitragem; só com a lei do preço único ela pode ficar negativa.
- Soma 1 apenas se o mercado for completo; sob incompletude a reponderação não chega a definir uma medida de probabilidade.
<!-- YW5zOjI= -->
> $\sum_s\tilde\pi(s)=E[m]/E[m]=1$ sempre. O que a ausência de arbitragem acrescenta é $m>0$, e portanto $\tilde\pi>0$ — sem isso teríamos pesos que somam 1 mas não são probabilidades.
> Ref: Ribeiro (2026), Cap. 1, §1.7 (p. 29)
> Similar: Ribeiro, Exercício 1.4(d) (p. 33)

Q: Por que é errado ler $\tilde\pi$ como a melhor previsão do mercado sobre a probabilidade de cada estado?
- Porque $\tilde\pi$ pondera cada estado pela variância do payoff nele realizado, e variância alta não significa probabilidade alta.
- Porque $\tilde\pi$ é $\pi$ reponderada por escassez: estados com $m$ acima da média ganham peso, e isso é compensação, não informação.
- Porque $\tilde\pi$ é calculada a partir de retornos passados, ao passo que o mercado forma expectativas voltadas para o futuro.
- Porque $\tilde\pi$ só vale até o próximo vencimento negociado, ao passo que probabilidades físicas descrevem frequências de longo prazo.
<!-- YW5zOjE= -->
> A distorção entre $\tilde\pi$ e $\pi$ é exatamente o prêmio de risco embutido no preço. Ler $\tilde\pi$ como previsão confunde "quanto o mercado teme o estado" com "quão provável o mercado o julga".
> Ref: Ribeiro (2026), Cap. 1, §1.7 (p. 29)
> Similar: Ribeiro, True/False 1.1–1.30 (p. 35)

Q: Qual afirmação sobre retornos esperados calculados sob a medida $\tilde\pi$ é correta?
- $\tilde E[R^i]=R_f$ para todo ativo, pois a reponderação absorve exatamente o prêmio de risco no peso de cada estado.
- $\tilde E[R^i]=E[R^i]$ para todo ativo, pois a mudança de medida preserva as médias de todas as variáveis aleatórias.
- $\tilde E[R^i]>R_f$ para os ativos de risco, pois a medida risco-neutra preserva a ordenação dos ativos por prêmio.
- $\tilde E[R^i]=R_f$ só para o ativo livre de risco; os demais mantêm seus prêmios de risco sob qualquer medida usada.
<!-- YW5zOjA= -->
> $p=\tilde E[x]/R_f$ é equivalente a $\tilde E[R^i]=R_f$ para todo $i$. Daí o nome: sob $\tilde\pi$ tudo se comporta como numa economia neutra ao risco, sem que ninguém precise ser neutro ao risco.
> Ref: Ribeiro (2026), Cap. 1, §1.7 (p. 29)
> Similar: Ribeiro, Exercício 1.4(d) (p. 33)

Q: Com $\pi=(0{,}25;\,0{,}50;\,0{,}25)$ e $m=(0{,}60;\,0{,}96;\,1{,}32)$, em que estados $\tilde\pi$ excede $\pi$, e por quê?
- Apenas na expansão, onde o payoff da ação é maior: $\tilde\pi_1=0{,}344$ contra $\pi_1=0{,}25$, e a recessão perde peso.
- Em todos os estados, pois dividir por $E[m]=0{,}96<1$ eleva os três pesos e a soma passa de 1 para aproximadamente 1,042.
- Em nenhum estado, pois a reponderação preserva $\pi$ sempre que $m$ é função monotônica do payoff da ação negociada.
- Apenas na recessão, onde $m>E[m]$: $\tilde\pi_3=0{,}344$ contra $\pi_3=0{,}25$; no estado normal $m=E[m]$ e o peso não muda.
<!-- YW5zOjM= -->
> $\tilde\pi(s)>\pi(s)$ se e só se $m(s)>E[m]$. Aqui $E[m]=0{,}96$, então só a recessão ganha peso, e ganha bastante: de 25% para 34,4%. A medida risco-neutra engorda os estados temidos.
> Ref: Ribeiro (2026), Cap. 1, §1.7 (p. 29)
> Similar: Ribeiro, Exercício 1.4(d) (p. 33)

Q: A precificação risco-neutra reaparece no binomial e em Black–Scholes. O que a Sessão 1 já estabelece sobre suas condições de validade?
- Tanto a existência quanto a unicidade de $\tilde\pi$ exigem completude; sem ela não existe medida risco-neutra nenhuma.
- A existência de $\tilde\pi$ exige só ausência de arbitragem; é a unicidade — e o preço único da opção — que exige completude.
- A existência de $\tilde\pi$ exige neutralidade a risco dos investidores, hipótese que o binomial adota ao descontar por $R_f$.
- A existência de $\tilde\pi$ exige payoffs log-normais, e é por isso que Black–Scholes precisa da hipótese de difusão contínua.
<!-- YW5zOjE= -->
> É o par existência/unicidade do §1.5 traduzido para a medida. No binomial a replicação dinâmica completa o mercado a cada nó, e só por isso a opção tem um preço, e não um intervalo.
> Ref: Ribeiro (2026), Cap. 1, §1.7 (p. 29); Cap. 8, §8.6
> Similar: Ribeiro, Exercícios 8.7–8.8 (p. 293)
