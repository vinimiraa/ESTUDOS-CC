# Estudos Provas 2

## Conceitos Básicos

- **Variável aleatória contínua**: 
	Uma v.a. que assume valores no intervalo dos números reais.
	
- **Função Densidade de Probabilidade**: 
	Uma função 𝑓(𝑥) é chamada função densidade de probabilidade (f.d.p.) da v.a. 𝑋, se e somente se:
	- $f(x) \geq 0, \forall x$
	- $\int_{-\infty}^{\infty} f(x) dx = 1$
	- $P(a \leq X \leq b) = \int_{a}^{b} f(x)dx$
	
- **Densidade de Probabilidade Acumulada**: 
	$F(x) = P(X \leq x) = \int_{-\infty}^{x} f(x)dx$

- **Esperança de $X: E(X)$**: 
	média de um v.a. contínua ($X$) cuja função densidade de probabilidade é dada por $f(x)$.
	
	$\mu = E(X) = \int_{-\infty}^{\infty} xf(x)dx$
	
- **Variância de $X: Var(X)$**: 
	variância de uma v.a. contínua ($X$) cuja função densidade de probabilidade é dada por $f(x)$.
	
	$\sigma^2 = Var(X) = E(X^2) - [E(X)]^2$

## Distribuição Uniforme Contínua

Uma v.a. $X$ tem distribuição uniforme no intervalo $[\alpha ,\, \beta]$, ou seja seja, $X \thicksim U(\alpha;\;\beta)$:

$$ f(x) = \begin{cases} \frac{1}{\beta - \alpha},\, \alpha \leq x \leq \beta \\ 0,\, \text{c.c} \end{cases}$$

$$k \times (b - a) = 1 \implies k = \frac{1}{(b - a)}$$

### Resumo

| Situação                                      | Fórmula                                                                 |
| --------------------------------------------- | ----------------------------------------------------------------------- |
| Função densidade de probabilidade (f.d.p.)    | $f(x) = \frac{1}{\beta - \alpha},\, \alpha \leq x \leq \beta$           |
| Probabilidade entre dois valores $x_1$ e $x_2$ | $P(x_1 \leq X \leq x_2) = \frac{x_2 - x_1}{\beta - \alpha}$             |
| Valor esperado (média)                        | $E(X) = \frac{\alpha + \beta}{2}$                                       |
| Variância                                     | $Var(X) = \frac{(\beta - \alpha)^2}{12}$                                |
| Função de distribuição acumulada (F.D.A.)     | $F(x) = \frac{x - \alpha}{\beta - \alpha}, \; \alpha \leq x \leq \beta$ |

## Distribuição Exponencial

### Fórmula da distribuição exponencial (função de probabilidade acumulada)

A fórmula para a probabilidade de que o tempo até o próximo evento seja **menor ou igual a um valor $t$** é:

$P(X \leq x) = 1 - e^{-\lambda x}$

onde:
- $X$ = tempo até o próximo evento,
- $\lambda$ = taxa média de ocorrência por unidade de tempo,
- $e$ = constante de Euler, aproximadamente 2,71828.

### Se quiser uma probabilidade entre dois tempos, $a$ e $b$

$P(a \leq X \leq b) = e^{-\lambda a} - e^{-\lambda b}$

> Isso significa a chance de que o evento **ocorra após o tempo $a$ e antes do tempo $b$**.

### Fórmula da função de densidade de probabilidade (f.d.p.)

Se queremos a f.d.p. (probabilidade de ocorrer exatamente no instante $t$), é:

$f(x) = \lambda e^{-\lambda x}$

> [!NOTE] Lembrete
> Como estamos lidando com uma variável contínua, a f.d.p. indica densidade, e não probabilidade pontual. Para calcular uma probabilidade, é sempre sobre um intervalo (por exemplo, de $a$ a $b$).

### Fórmula da probabilidade de não ocorrer evento até o tempo $x$ (ou seja, tempo maior que $x$)

$P(X > x) = e^{-\lambda x}$

### Resumo

| Situação                                                        | Fórmula                                               |
| --------------------------------------------------------------- | ----------------------------------------------------- |
| Probabilidade do evento ocorrer até $x$ (antes ou no tempo $x$) | $P(X \le x) = 1 − e^{- \lambda x}$                    |
| Probabilidade do evento não ocorrer até $x$ (após o tempo $x$)  | $P(X > x) = e^{- \lambda x}$                          |
| Probabilidade do evento ocorrer entre os tempos $a$ e $b$       | $P(a \le X \le b)= e^{- \lambda a} − e^{- \lambda b}$ |
| Probabilidade do evento ocorrer no instante $x$                 | $f(x) = \lambda e^{-\lambda x}$                       |
| Valor esperado (tempo médio até o evento)                       | $\frac{1}{\lambda}$                                   |
| Variância do tempo até o evento                                 | $\frac{1}{\lambda^2}$                                 |

> A **propriedade sem memória** (ou **falta de memória**) é uma característica fundamental da **distribuição exponencial**.
> 
> Seja $X$ uma variável aleatória com distribuição exponencial, então a propriedade sem memória afirma que:
> 
$P(T > t) = P(T > s + t \mid T > s)$
> 
> Ou seja, **o tempo adicional que você ainda vai esperar não depende do quanto você já esperou**.
## Distribuição Normal
- $f(x)$ é simétrica em relação a $\mu$;
- A área total sob a curva é igual a 1 (ou 100%);
- $\lim_{x \to \infty}f(x) = 0$
- O valor máximo de $f(x)$ ocorre em $x = \mu$;
- $\mu - \sigma$ e $\mu + \sigma$ são os pontos de inflexão da curva.

$Z$ é uma medida de quantos desvios padrão um valor $X$ está afastado de $\mu$. Quando $\mu = 0$ e $\sigma = 1$, temos uma distribuição normal padrão (ou reduzida), e o $Z$ pode ser calculado como: $Z = \frac{X - \mu}{\sigma}$.

#### Passo a passo
1. Desenhar o gráfico.
2. Calcular $Z$.
3. Encontrar o $P(Z)$ olhando na Tabela de Distribuição Normal.
4. Lembrar de normalizar o resultado (para a tabela da professora Mayara).

## Teste de Hipóteses e Intervalo de Confiança

### Passo a Passo

1. Definir as Hipóteses:
	- $H_0: \mu$
	- $H_1: \mu$
		- Se $>$: à direita;
		- Se $<$: à esquerda;
		- Se $\ne$: bilateral.
2. Calcular a Estatística de Teste:
	- Se é um problema de proporção:
		- $$Z = \frac{\hat{p} - p_0}{\sqrt{\frac{p_0 \times (1 - p_0)}{n}}}$$
		- $$IC = \hat{p} \pm z{\frac{\alpha}{2}} \sqrt{\frac{\hat{p}(1 - \hat{5})}{n}}$$
	- Se é um problema de média:
		- Se o desvio padrão populacional ($\sigma$) é **conhecido**, então:
			- $$Z = \frac{\overline{X} - \mu_0}{\frac{\sigma}{\sqrt{n}}}$$
			- $$IC = \overline{x} \pm z_{\frac{\alpha}{2}} (\frac{\sigma}{\sqrt{n}})$$
		- Se $\sigma$ é **desconhecido**:
			- Se o tamanho da amostra é menor que 30 ($n < 30$), então:
				- $$T = \frac{\overline{X} - \mu_0}{\frac{S}{\sqrt{n}}}$$
				- $$IC = \overline{x} \pm t_{(n-1;\; \frac{\alpha}{2})} (\frac{s}{\sqrt{n}})$$
			- Se $n \ge 30$, então:
				- $$Z = \frac{\overline{X} - \mu_0}{\frac{S}{\sqrt{n}}}$$
				- $$IC = \overline{x} \pm z_{\frac{\alpha}{2}} (\frac{s}{\sqrt{n}})$$
3. Calcular a Região de Rejeição:
4. Concluir:
	- De onde saiu a conclusão;
	- Rejeita ou não rejeita a hipótese (opcional);
	- Qual o nível de significância ($\alpha$);
	- Conclusão em termos de problema.

## Correlação e Regressão Linear Simples
