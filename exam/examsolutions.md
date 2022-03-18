ECON 2080, part 1  
Spring 2022  
Pascal Michaillat  
Brown University

# Midterm Exam: Solutions

### Multiple-Choice Questions

* Question A: 3
* Question B: 3
* Question C: 3
* Question D: 5
* Question E: 5
* Question F: 1
* Question G: 3
* Question H: 4 and 6
* Question I: 2, 4, and 6
* Question J: 1, 4, and 6

### Problem A

**Consider a matching model with a labor force of size $H$. The matching function is  Cobb-Douglas:  $m(U,V) = \omega \cdot U^{\eta} \cdot V^{1-\eta}$, where $U$ is the number of unemployed workers, $V$ is the number of vacant jobs, and $\eta\in (0,1)$ is the matching elasticity. All workers are paid at a minimum wage $w>0$. Firms have a production function $y(N) = a \cdot N^{\alpha}$, where $a$ governs labor productivity, $N$ denotes the number of producers in the firm, and $\alpha \in (0,1)$ indicates diminishing marginal returns to labor. Firms incur a recruiting cost of $r > 0$ recruiters per vacancy and face a job-destruction rate $s > 0$. The labor market tightness is $\theta = V/U$.**

1. **Compute the job-finding rate $f(\theta)$ and vacancy-filling rate $q(\theta)$. Assuming that labor-market flows are balanced, compute the recruiter-producer ratio $\tau(\theta)$. Compute the elasticities of $f$, $q$, and $1+\tau$ with respect to $\theta$.**

The job finding rate is

$$f(\theta) = m(1,\theta) = \omega \theta^{1-\eta}.$$

The vacancy filling rate is

$$q(\theta) = m(\theta^{-1},1) = \omega \theta^{-\eta}.$$

Assuming balanced flows, $sL = q(\theta)V$, implies

$$rs(N+R) = q(\theta) R.$$

Then dividing both sides by $R$, we obtain

$$rs(1+\tau(\theta)^{-1}) = q(\theta),$$

which then gives

$$\tau(\theta) = \frac{rs}{q(\theta)-rs}.$$

This means that

$$1+\tau(\theta) = \frac{q(\theta)}{q(\theta)-rs}.$$

The elasticities of the job-finding rate and vacancy-filling rate are

$$\epsilon^f_{\theta} = \frac{d \ln f}{d\ln\theta} = (1-\eta), \quad \epsilon^q_{\theta} = \frac{d \ln q}{d \ln \theta} = -\eta.$$

The elasticity of $(1+\tau)$ with respect to $\theta$ is

$$\epsilon^{1+\tau}_{\theta} = \epsilon^{q}_{\theta} - \epsilon^{q-rs}_{\theta} = -\eta - \underbrace{\frac{q(\theta)}{q(\theta)-rs}}_{1+\tau}(-\eta),$$

which finally gives

$$\epsilon^{1+\tau}_{\theta}= \eta\tau(\theta).$$

2. **Assuming that labor-market flows are balanced, compute labor supply $L^s(\theta,H)$. Compute the elasticities of $L^s$ with respect to $\theta$ and $H$.**

Assuming balanced flows, $sL^s = f(\theta)U$ or equivalently $sL^s = f(\theta)(H-L^s)$,  we get

$$L^s(\theta,H) = \frac{f(\theta)}{s+f(\theta)}H.$$

The elasticity of $L^s$ with respect to $\theta$ is

$$\epsilon^{L^s}_{\theta} = \epsilon^{f}_{\theta} - \epsilon^{s+f}_{\theta} = \epsilon^{f}_{\theta} - \frac{f}{s+f}\epsilon^{f}_{\theta},$$

which means,

$$\epsilon^{L^s}_{\theta} = (1-\eta) - \underbrace{\frac{f(\theta)}{s+f(\theta)}}_{\frac{L^s}{H}}(1-\eta) =\left(1-\frac{L^s}{H}\right)(1-\eta) = u (1-\eta).$$

The elasticity of $L^s$ with respect to $H$ is

$$\epsilon^{L^s}_H = 1.$$

3. **Firms choose employment to maximize flow profits: $y(N) - [1+\tau(\theta)] \cdot w \cdot N$. Compute the labor demand $L^d(\theta)$ by solving this maximization problem. Compute the elasticity of $L^d$ with respect to $\theta$.**

The firm solves

$$\max_N a N^{\alpha} - [1+\tau(\theta)]w N.$$

The first-order condition implies that

$$a \alpha N^{\alpha-1} =[1+\tau(\theta)]w.$$

Using $[1+\tau(\theta)]N = L^d$, we can write

$$a \alpha [1+\tau(\theta)]^{1-\alpha}{L^d}^{\alpha-1} = [1+\tau(\theta)]w,$$

which then yields

$$L^d(\theta) = \left(\frac{a\alpha}{w[1+\tau(\theta)]^{\alpha}}\right)^{\frac{1}{1-\alpha}}.$$

The elasticity of $L^d$ with respect to $\theta$ is

$$\epsilon^{L^d}_{\theta} = -\frac{\alpha}{1-\alpha}\epsilon^{1+\tau}_{\theta} = -\frac{\alpha}{1-\alpha}\eta\tau(\theta).$$

4. **Characterize tightness $\theta(H)$ and unemployment rate $u(H)$ in the model. Illustrate with a diagram how $\theta(H)$ and $u(H)$ are determined.**

The model requires that firms maximize profits and labor-market flows are balanced, which imposes that labor demand equals labor supply:

$$L^d(\theta) = L^s(\theta,H).$$

This condition implies

$$\left(\frac{a\alpha}{w[1+\tau(\theta)]^{\alpha}}\right)^{\frac{1}{1-\alpha}} = \frac{f(\theta)}{s+f(\theta)}H.$$

For any given $H$, this equation pins down a unique $\theta$. Therefore, the supply-equals-demand condition implicitly defines $\theta(H)$. Once we have $\theta(H)$, plugging into either labor supply or labor demand defines the employment level as a function of $H$, $L(H)$. The unemployment rate is then $u(H)=[1-L(H)]/H$. For instance, using the labor supply equation,

$$u(H) = \left[H-\frac{f(\theta(H))}{s+f(\theta(H))}H\right]\frac{1}{H}= \frac{s}{s+f(\theta(H))}.$$

5. **Denote the elasticities of $\theta(H)$ and $u(H)$ with respect to $H$ as $\epsilon^{\theta}_H$ and $\epsilon^{u}_H$. Compute $\epsilon^{\theta}_H$ and $\epsilon^{u}_H$. Interpret the signs of these elasticities.**

Using the definition of an elasticity,

$$d \ln L^s = \epsilon^{L^s}_{\theta} d\ln \theta + \epsilon^{L^s}_H d\ln H, \,\, d \ln L^{d} = \epsilon^{L^d}_{\theta}d\ln \theta.$$

Since the supply-equals-demand condition must hold both before and after a small change in $H$, $d\ln L^s = d\ln L^d$. This means that

$$\epsilon^{L^s}_{\theta} d\ln \theta + \epsilon^{L^s}_H d\ln H = \epsilon^{L^d}_{\theta}d\ln \theta.$$

In other words, 

$$\epsilon^{\theta}_H  = \frac{d \ln \theta}{d \ln H} = \frac{\epsilon^{L^s}_H}{\epsilon^{L^d}_{\theta}-\epsilon^{L^s}_{\theta}} = \frac{-1}{1-[\epsilon^{L^d}_{\theta}/\epsilon^{L^s}_{\theta}]}.$$

Plugging in for the elasticities worked out above,

$$\epsilon^{\theta}_H  = \frac{-1}{1+ \frac{\alpha}{1-\alpha}\cdot\frac{\eta}{1-\eta}\cdot\frac{\tau(\theta)}{u(\theta)}} < 0.$$

The elasticity of tightness with respect to the size of the labor force is negative. An increase in the labor force increases the number of available workers, but not the number of jobs, so it raises supply and not demand. This leads to a decrease in tightness.

The unemployment rate, $u(H)$ is

$$u(H) = \frac{s}{s+f(\theta(H))}.$$

By the chain rule,

$$\epsilon^u_{H} = -\frac{f}{s+f} \epsilon^f_{\theta}\epsilon^{\theta}_{H} = -[1-u(\theta)] (1-\eta) \epsilon^{\theta}_{H}.$$

Plugging in the elasticities above, we get

$$\epsilon^u_{H} = \frac{[1-u(\theta)] (1-\eta)}{1+ \frac{\alpha}{1-\alpha}\cdot\frac{\eta}{1-\eta}\cdot\frac{\tau(\theta)}{u(\theta)}} > 0.$$

Increasing the size of the labor force increases the unemployment rate. Labor-market tightness falls when the size of the labor force rises, so it becomes harder to find a job, and the unemployment rate increases. The underlying reason is that after an influx of new workers into the labor force, there is the same number of jobs but more jobseekers, so a larger fraction of workers remain unemployed.

6. **What is the sign of the derivative $d|\epsilon^{\theta}_H|/da$? There are times when people are strongly opposed to immigration, and other times when immigration is a nonissue. Based on the sign of the derivatives, when is it likely that opposition to immigration is particularly strong? As far as you know, is this prediction supported by historical evidence?**

Since the wage is fixed, we know that an increase in productivity $a$ leads to higher tightness $\theta$. We also know that the recruiter-producer ratio $\tau(\theta)$ is increasing in $\theta$ and the unemployment rate $u(\theta)$ is decreasing in $\theta$. This means that an increase in productivity $a$ leads to a higher ratio $\tau(\theta)/u(\theta)$. Therefore, the elasticity $|\epsilon^{\theta}_H|$ is smaller in good times, when $a$ is large, and higher in bad times, when $a$ is small. That is,

$$\frac{d|\epsilon^{\theta}_H|}{da}<0.$$

An increase in the size of the labor force reduces tightness. It therefore makes it harder for unemployed workers to find jobs. In fact the elasticity of the job-finding rate is just $(1-\eta)\times \epsilon^{\theta}_H$. In bad times, the elasticity will have high amplitude, which means that immigration will reduce the job-finding rate more drastically. The locals are therefore more likely to be opposed to immigration in bad times, because it will hurt their labor-market prospects more. Opposition to immigration is likely to be particularly large in a recession. This seems to fit with the general pattern that immigration tends to crop up more in political conversations in bad times. (Immigrant are often used as scapegoats for bad labor-market conditions and a lack of available jobs.)

### Problem B

**Consider a one-period matching model with a labor force of size 1, a mass 1 of firms, and a government. All workers are initially unemployed. Private firms and the government post vacancies and match with workers. Then production occurs. The matching function is $m(V) = \sqrt{V}$, where $V$ is the total number of vacancies posted by firms and the government. Given that all workers are initially unemployed, the labor market tightness equals the aggregate number of vacancies: $\theta = V$.**

**Firms incur a recruiting cost of $r > 0$ recruiters per vacancy. Firms have a production function $y(N) = 2 \times a \times \sqrt{N}$, where $a$ governs labor productivity and $N$ denotes the number of producers in the firm. We denote by $F$ the total number of workers in the firm. The firm pays a rigid wage $w = \sqrt{a}$ to all their $F$ workers. Each firm choose employment $F$ to maximize profits.**

**The government employs $G>0$ workers. Aggregate employment is the sum of public and private employment: $L = G + F$. The share of public employment in the labor market is denoted by $\sigma = G/L$.**

1. **The labor supply $L^s(\theta)$ gives the number of worker who find a job (either in the public or private sector) through the matching process when tightness is $\theta$. Given the expression of $L^s(\theta)$. What is the elasticity of $L^s(\theta)$ with respect to $\theta$.**

Given that $\theta=V$ and $U=1$, the labor supply is simply 

$$L^s(\theta) = \sqrt{\theta}.$$ 

The elasticity of the labor supply with respect to the tightness is

$$\epsilon^{L^s}_{\theta} = \frac{1}{2}.$$

2. **The aggregate labor demand $L^d(\theta,G)$ is the sum of the private labor demand $F^d(\theta)$ and the public labor demand $G$. Compute $L^d(\theta,G)$. What are the elasticities of $L^d(\theta,G)$ with respect to $\theta$ and with respect to $G$?**

Dividing the matching function by $V$ and using $V=\theta$ gives the vacancy-filling rate $q(\theta) = \frac{m(V)}{V} = 1/\sqrt{\theta}$. A firm that wants to hire $F$ workers therefore needs to post enough vacancies to satisfy

$$F = q(\theta)V.$$

Plugging in using $F=N+R$ and $rV=R$ gives

$$r(N+R) = q(\theta)R.$$

Dividing through by $R$ and defining $\tau = R/N$ gives 

$$r (\tau^{-1}+1) = q(\theta),$$

which implies

$$\tau(\theta) = \frac{r}{q(\theta)-r} = \frac{r\sqrt{\theta}}{1-r\sqrt{\theta}}.$$

The firm solves

$$\max_{N} 2 a \sqrt{N} - w F = \max_{N}2a\sqrt{N} - \sqrt{a}[1+\tau(\theta)]N.$$

The first-order condition of this maximization problem implies

$$aN^{-\frac{1}{2}} = \sqrt{a}[1+\tau(\theta)].$$

Using $F[1+\tau(\theta)]^{-1} = N$ and rearranging terms gives

$$\sqrt{F} = \frac{\sqrt{a}}{\sqrt{1+\tau(\theta)}}$$

and then

$$F^d(\theta) = \frac{a}{1+\tau(\theta)}=a\left[1-r\sqrt{\theta}\right].$$

The aggregate labor demand is given by adding $G$, the number of workers the government employs.

$$L^d(\theta,G) = a\left[1-r\sqrt{\theta}\right] + G.$$

The elasticity of the labor demand with respect to tightness is

$$\epsilon^{L^d}_{\theta} = -(1-\sigma)\cdot \frac{r\sqrt{\theta}}{1-r\sqrt{\theta}}\cdot\frac{1}{2} = -\frac{(1-\sigma)\tau}{2}.$$

The elasticity of labor demand with respect to $G$ is

$$\epsilon^{L^d}_{G} = G/L = \sigma.$$

3. **Compute an expression for the government multiplier $\lambda = dL/dG$. Is the multiplier $\lambda$ positive or negative? Is $|\lambda|$ more or less than 1? Interpret these findings.**

We want to know what happens to employment $L$ in response as small change in $G$, $dG$. First, the model imposes that labor demand equals labor supply $L^s(\theta) = L^d(\theta,G)$. This equation pins down $\theta(G)$ implicitly, and therefore also $L(\theta(G))$. Feeding in a small change in $G$, we get

$$\lambda =\frac{dL}{dG} = \frac{dL^s}{d\theta}\cdot \frac{d\theta}{dG}.$$

What is $d\theta/dG?$ We can exploit the supply-equals-demand condition again. The condition must hold both before and after a small change in $G$, $dG$. This implies that $dL^s = dL^d$, or

$$\frac{d L^s}{d \theta} d\theta = \frac{d L^d}{d \theta} d \theta + d G.$$

Rearranging the terms gives

$$\frac{d\theta}{dG} = \frac{1}{(d L^s/d\theta)-(d L^d/d\theta)}.$$

Elasticity and derivative are related by $\epsilon^f_x = \frac{x}{f}\frac{df}{dx} \Rightarrow \frac{df}{dx} = \frac{f}{x}\epsilon^f_x$. Using the elasticities calculated in previous parts, we obtain

$$\frac{d\theta}{dG} = \frac{1}{\frac{L}{\theta}\cdot\frac{1}{2}+\frac{L}{\theta}\cdot\frac{(1-\sigma)\tau}{2}}=\frac{2\theta}{L \cdot [1+(1-\sigma)\tau]}.$$

Finally, combining the expression above for $\lambda$, the elasticity of labor supply with respect to $\theta$, and the expression for $d\theta/dG$, we obtain

$$\lambda = \frac{L}{\theta}\cdot\frac{1}{2} \cdot \frac{2\theta}{L [1+(1-\sigma)\tau]} = \frac{1}{1+(1-\sigma)\tau} = \frac{1-r\sqrt{\theta}}{1-\sigma r\sqrt{\theta}}.$$

Tightness $\theta$ is always such that $r\sqrt{\theta}<1$, to keep the ratio $\tau$ positive and finite. Since $\sigma<1$, then $\sigma r \sqrt{\theta}<1$. Hence the multiplier $\lambda$ is positive. 

Moreover, since $\sigma<1$, $r\sqrt{\theta}>\sigma r\sqrt{\theta}$, which implies that the multiplier $\lambda$ is less than one. 

This implies that increasing government employment increases aggregate employment, but by less than the original increase in government employment. Since increased government employment increases tightness, this reduces private labor demand, slightly crowding out private employment. As a result, some, but not all, of the increase in public employment is offset by the response of the private sector.

4. **What is the sign of the derivative $d\lambda/da$? What does this result imply for the effectiveness of fiscal policy over the business cycle? As far as you know, does the result seem realistic?**

For any $\sigma<1$ and for $x\in[0,1]$, the function $x\mapsto (1-x)/(1-\sigma x)$ is positive and decreasing in $x$. This means that the multiplier $\lambda$ is decreasing in tightness $\theta$.

At the same time, since the wage is rigid, we know that an increase in productivity $a$ leads to higher tightness $\theta$.

Therefore, an increase in productivity $a$ leads to a lower multiplier $\lambda$. That is,

$$\frac{d\lambda}{da}<0.$$

This means that fiscal policy is more effective at boosting employment in bad times, when productivity is low, and is less effective in good times, when productivity is high. This is because matching frictions don't matter very much in bad times, and so the increase in competition from public jobs does not affect private jobs much. As far as I know, this does seem realistic. The empirical literature does suggest that fiscal policy is more potent in slumps, when unemployment is high. For US evidence see [Auerbach & Gorodnichenko [2012]](https://doi.org/10.1257/pol.4.2.1), [Candelon & Lieb [2013]](https://doi.org/10.1016/j.jedc.2013.09.001), or[ Fazzari, Morley, & Panovska [2015]](https://doi.org/10.1515/snde-2014-0022).
