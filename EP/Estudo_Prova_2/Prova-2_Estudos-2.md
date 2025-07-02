# Estudos — Prova 2

## Conceitos Básicos

- **Variável Aleatória Contínua:**  
    Uma variável que assume qualquer valor dentro de um intervalo dos números reais.
    
- **Função Densidade de Probabilidade (f.d.p.):**  
    Uma função $f(x)$ é uma f.d.p. se:
    
    - $f(x) \geq 0, \; \forall x$
        
    - $\int_{-\infty}^{\infty} f(x) dx = 1$
        
    - $P(a \leq X \leq b) = \int_{a}^{b} f(x)dx$
        
- **Função de Distribuição Acumulada (F.D.A.):**  
    
    $$F(x) = P(X \leq x) = \int_{-\infty}^{x} f(x)dx$$
    
- **Esperança (Média) de $X$:**  

    $$E(X) = \mu = \int_{-\infty}^{\infty} x f(x) dx$$
    
- **Variância de $X$:**  
	
	$$Var(X) = \sigma^2 = E(X^2) - [E(X)]^2$$
    

## Distribuição Uniforme Contínua

- $X \sim U(\alpha, \beta)$
    
- A variável $X$ tem a mesma probabilidade em qualquer ponto do intervalo $[\alpha, \beta]$.

### Função Densidade de Probabilidade:

$$f(x) = \begin{cases} \frac{1}{\beta - \alpha}, & \alpha \leq x \leq \beta \\ 0, & \text{caso contrário} \end{cases}$$

> Observação: $k \times (\beta - \alpha) = 1 \implies k = \frac{1}{\beta - \alpha}$

### Resumo

|Situação|Fórmula|
|---|---|
|f.d.p.|$f(x) = \frac{1}{\beta - \alpha}$, se $\alpha \leq x \leq \beta$|
|Probabilidade entre dois valores $[x_1, x_2]$|$P(x_1 \leq X \leq x_2) = \frac{x_2 - x_1}{\beta - \alpha}$|
|Valor Esperado (Média)|$E(X) = \frac{\alpha + \beta}{2}$|
|Variância|$Var(X) = \frac{(\beta - \alpha)^2}{12}$|
|F.D.A.|$F(x) = \frac{x - \alpha}{\beta - \alpha}$, se $\alpha \leq x \leq \beta$|

## Distribuição Exponencial

- Modelo clássico para descrever **tempo até a ocorrência de um evento**.
    
- $X \sim Exp(\lambda)$

### Função de Densidade de Probabilidade

$$f(x) = \lambda e^{-\lambda x},\; x \geq 0$$

### Função de Distribuição Acumulada (F.D.A.)

$$F(x) = P(X \leq x) = 1 - e^{-\lambda x}$$
### Probabilidade do Tempo Ser Maior que $x$

$$P(X > x) = e^{-\lambda x}$$

### Probabilidade Entre Dois Tempos $[a, b]$

$$P(a \leq X \leq b) = e^{-\lambda a} - e^{-\lambda b}$$

### Resumo

| Situação                             | Fórmula                           |
| ------------------------------------ | --------------------------------- |
| $P(X \le x)$ — até o tempo $x$       | $1 - e^{-\lambda x}$              |
| $P(X > x)$ — após o tempo $x$        | $e^{-\lambda x}$                  |
| $P(a \le X \le b)$ — entre $a$ e $b$ | $e^{-\lambda a} - e^{-\lambda b}$ |
| f.d.p. — densidade no instante $x$   | $\lambda e^{-\lambda x}$          |
| Valor Esperado (tempo médio)         | $\frac{1}{\lambda}$               |
| Variância                            | $\frac{1}{\lambda^2}$             |

### Propriedade Sem Memória:

Seja $X \sim Exp(\lambda)$, então:  

$$P(X > s + t \mid X > s) = P(X > t)$$

> Ou seja, **o tempo adicional de espera é independente do tempo já decorrido**.

## Distribuição Normal

- A mais importante da estatística.
    
- Notação: $X \sim N(\mu, \sigma^2)$

### Características

- Curva **simétrica** em relação à média $\mu$.
    
- Área total sob a curva = 1.
    
- Pontos de inflexão em $\mu - \sigma$ e $\mu + \sigma$.
    
- O pico ocorre em $x = \mu$.

### Padronização (Distribuição Normal Padrão)

Quando $\mu = 0$ e $\sigma = 1$, temos $Z \sim N(0, 1)$.

$$Z = \frac{X - \mu}{\sigma}$$

### Passo a Passo:

1. Desenhar a curva normal e identificar a área de interesse.
    
2. Calcular $Z$.
    
3. Consultar a tabela de valores de $Z$ (Tabela Normal).
    
4. Interpretar o resultado (lembrar do ajuste conforme a tabela utilizada).

## Teste de Hipóteses & Intervalo de Confiança (IC)

### Conceitos

#### Hipóteses 

- Hipótese nula ($H_0$): é a hipótese aceita como verdadeira até que existam evidências estatísticas que comprovem o contrário. 
	
- Hipótese alternativa ($H_1$): é a hipótese de interesse, a hipótese que rejeita a hipótese nula.
#### Nível de Significância ($\alpha$)

É a probabilidade de ocorrência do erro Tipo I, ou seja: 

$$\alpha = P(\text{rejeitar } H_0 \mid H_0 \text{ é verdadeiro})$$

#### Estatística de Teste

|                       | Testes para uma média                                      | Teste para uma proporção                                  |
| --------------------- | ---------------------------------------------------------- | --------------------------------------------------------- |
| $\sigma$ conhecido    | $Z = \frac{\overline{X} - \mu_0}{\frac{\sigma}{\sqrt{n}}}$ |                                                           |
| $\sigma$ desconhecido | $T = \frac{\overline{X} - \mu_0}{\frac{S}{\sqrt{n}}}$      |                                                           |
| $n \ge 30$            | $Z = \frac{\overline{X} - \mu_0}{\frac{S}{\sqrt{n}}}$      | $Z = \frac{\hat{p} - p_0}{\sqrt{\frac{p_0(1 - p_0)}{n}}}$ |

#### Região de Rejeição

É um valor, obtido através das tabelas das distribuições, que será comparado com o valor da estatística de teste para que se decida sobre a rejeição ou não de $H_0$.

> A região de rejeição depende da hipótese alternativa (bilateral ou unilateral).

- Bilateral: rejeita-se $H_0$ se:
	- $Z < -z_{\frac{\alpha}{2}}$
	- $Z > z_{\frac{\alpha}{2}}$
	- $T > t_{(n-1;\;\frac{\alpha}{2})}$
	- $T < -t_{(n-1;\;\frac{\alpha}{2})}$

### Passo a Passo

1. **Definir as Hipóteses:**
    
    - $H_0$: hipótese nula (ex.: $\mu = \mu_0$)
        
    - $H_1$: hipótese alternativa (ex.: $\mu > \mu_0$, $\mu < \mu_0$ ou $\mu \ne \mu_0$)
        
2. **Calcular a Estatística de Teste:**
    
    - **Para proporções:**
        
        - $Z = \frac{\hat{p} - p_0}{\sqrt{\frac{p_0(1 - p_0)}{n}}}$
            
        - $IC = \hat{p} \pm z_{\frac{\alpha}{2}} \sqrt{\frac{\hat{p}(1 - \hat{p})}{n}}$
        
    - **Para médias:**
        
        - **Se $\sigma$ é conhecido:**
            
            - $Z = \frac{\overline{X} - \mu_0}{\frac{\sigma}{\sqrt{n}}}$
                
            - $IC = \overline{X} \pm z_{\frac{\alpha}{2}} (\frac{\sigma}{\sqrt{n}})$
                
        - **Se $\sigma$ é desconhecido:**
            
            - Se $n < 30$:
                
                - $T = \frac{\overline{X} - \mu_0}{\frac{S}{\sqrt{n}}}$
                    
                - $IC = \overline{X} \pm t_{(n-1;\frac{\alpha}{2})} (\frac{S}{\sqrt{n}})$
                    
            - Se $n \ge 30$:
                
                - $Z = \frac{\overline{X} - \mu_0}{\frac{S}{\sqrt{n}}}$
                    
                - $IC = \overline{X} \pm z_{\frac{\alpha}{2}} (\frac{S}{\sqrt{n}})$
                    
3. **Determinar a Região Crítica (Região de Rejeição).**
    
4. **Conclusão:**
    
    - De onde saiu a conclusão;
		
	- Rejeita ou não rejeita a hipótese (opcional);
		
	- Qual o nível de significância ($\alpha$);
		
	- Conclusão em termos de problema.

## Correlação e Regressão Linear Simples

### Passo a Passo na Calculadora

1. Pressionar Tecla "Mode" (2) e selecionar a opção "Reg" (3).
2. Selecionar a opção "Lin" (1).
3. Limpar a calculadora, pressionando "Shift" + "Mode".
4. Selecionar "Scl" (1).
5. Pressionar "=".
6. Enquando houver valores:
	1. Entrar com o dado X, pressionar o "$,$" e entrar com o dado Y.
	2. Pressionar "M+"
7. Pressionar "Shift" + "S-Var".
8. Com o botão do meio da calculadora, ir para a direita.
	1. "A" = $b_0$
	2. "B" = $b_1$
	3. "r" = $r_{x,y}$

> A equação de correlação linear é: $\hat{y} = b_0 + b_1 \times x$.
