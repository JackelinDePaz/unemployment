[ECON 2080, part 1](https://canvas.brown.edu/courses/1087669)
Spring 2022  
Pascal Michaillat  
Brown University

# Problem Set 3: Solutions

### Problem A (7 points)

**Consider a matching model with a labor force of size $1$. The matching function is  Cobb-Douglas:  $m(U,V) = \sqrt{U \cdot V}$, where $U$ is the number of unemployed workers and $V$ is the number of vacant jobs. Firms have a production function $y(N) = 2\cdot a \cdot \sqrt{N}$, where $a \leq 1$ governs labor productivity and $N$ denotes the number of producers in the firm. All workers are paid at a $w = \sqrt{a}$. Firms incur a recruiting cost of $r > 0$ recruiters per vacancy and face a job-destruction rate $s > 0$. The labor market tightness is $\theta = V/U$ and the employment level is $L=1 - U$.**

1. **Compute the job-finding rate $f(\theta)$ and vacancy-filling rate $q(\theta)$. Assuming that labor-market flows are balanced, compute the recruiter-producer ratio $\tau(\theta)$. Compute the elasticities of $f$, $q$, and $\tau$ with respect to $\theta$. Interpret the signs of the elasticities.**

The job-finding rate $f(\theta)$ is

$$f(\theta) = \frac{m(U,V)}{U} = m(1,\theta) = \sqrt{\theta}.$$

The vacancy-filling rate is

$$q(\theta) = \frac{m(U,V)}{V} = m(\theta^{-1},1) = 1/\sqrt{\theta}.$$

Balanced flows means that the number of workers flowing into unemployment $sL=s(N+R)$ is equal to the number of workers flowing out of unemployment, $m(U,V) = q(\theta) V=R/(r\sqrt{\theta})$, where the last equality uses $rV = R$. This means

$$s(N+R) = \frac{R}{r \sqrt{\theta}}.$$

Reshuffling terms around, we obtain

$$sN = \frac{1-sr\sqrt{\theta}}{r\sqrt{\theta}} R,$$

so that the recruiter-producer ratio is

$$\tau(\theta)=\frac{R}{N} = \frac{sr \sqrt{\theta}}{1-sr \sqrt{\theta}}.$$

The elasticity of $f$ with respect to $\theta$ is

$$\epsilon^f_{\theta} = \frac{d \ln f}{d \ln \theta} = \frac{1}{2}.$$

This means that a $1\%$ increase in tightness increases the job-finding rate by $\tfrac{1}{2}\%$. A tighter labor market means more vacancies per unemployed worker, which makes it easier and quicker to find a job. 

Similarly, the elasticity of $q$ with respect to $\theta$ is

$$\epsilon^q_{\theta} = \frac{d \ln q}{d \ln \theta} = -\frac{1}{2}.$$

A $1\%$ increase in tightness decreases the vacancy-filling rate by $\tfrac{1}{2}\%$. A tighter labor market means more vacancies per unemployed worker, which makes it harder and slower to fill a vacancy. 

The elasticity of $\tau$ with respect to $\theta$ is

$$\epsilon^{\tau}_{\theta} = -\epsilon^{q-rs}_{\theta} = -\frac{q(\theta)}{q(\theta)-rs}\epsilon^{q}_{\theta} = \frac{1}{2} \frac{q(\theta)}{q(\theta)-rs} = \frac{1+\tau}{2},$$

which is greater than $1/2$. An increase in tightness raises the recruiter-producer ratio. Maintaining balanced flows at a higher tightness requires more vacancies since the vacancy-filling rate is smaller. And maintaining more vacancies requires more producers.

2. **Assuming that labor-market flows are balanced, compute labor supply $L^s(\theta)$. Compute the elasticity of $L^s$ with respect to $\theta$. Interpret the sign of the elasticity.**

Assuming flows are balanced, we have

$$s L = f(\theta) U = f(\theta) (1-L).$$

Rearranging the terms yields

$$L^{s}(\theta) = \frac{f(\theta)}{s+f(\theta)} = \frac{\sqrt{\theta}}{\sqrt{\theta}+s}.$$

The elasticity of $L^s$ with respect to $\theta$ is

$$\epsilon^{L^s}_{\theta} = \epsilon^f_{\theta} - \epsilon^{s+f}_{\theta} = \epsilon^f_{\theta} - \frac{f}{s+f}\epsilon^f_{\theta} = \frac{s}{s+f}\epsilon^f_{\theta} = \frac{u}{2} > 0,$$

where $u = s/(s+f)$ is the unemployment rate.

The labor supply is increasing in tightness, which is why the elasticity is positive. Higher tightness means more vacancies per unemployed workers. This makes it easier and faster to find a job, and therefore increases the labor supply. Notice that the elasticity of the labor supply is proportional to the unemployment rate: the labor supply is almost inelastic at low unemployment rate, and it is very elastic at high unemployment rates. 

3. **Firms choose employment to maximize flow profits: $y(N) - [1+\tau(\theta)] \cdot w \cdot N$. Compute the labor demand $L^d(\theta,a)$ by solving this maximization problem. Compute the elasticities of $L^d$ with respect to $\theta$ and with respect to $a$. Interpret the signs of these elasticities.**

A representative firm chooses $N$ to maximize

$$2 a N^{\frac{1}{2}} - w \left[1+\tau(\theta)\right]N.$$

The first-order condition is

$$aN^{-\frac{1}{2}} = w \left[1+\tau(\theta)\right]$$

Using $L=\left[1+\tau(\theta)\right]N$, we obtain

$$a \left[1+\tau(\theta)\right]^{\frac{1}{2}}L^{-\frac{1}{2}}  = w \left[1+\tau(\theta)\right]$$

Rearranging gives

$$L^d(\theta,a) = \left[\frac{a}{w}\left[1+\tau(\theta)\right]^{-\frac{1}{2}}\right]^2 = \left[\frac{a}{\sqrt{a}}\left[1+\tau(\theta)\right]^{-\frac{1}{2}}\right]^2 = \frac{a}{1+\tau(\theta)},$$

which can be re-expressed as

$$L^d(\theta,a) = a \cdot \left[1-sr\sqrt{\theta}\right].$$

The elasticity of $L^d$ with respect to $\theta$ is

$$\epsilon^{L^d}_{\theta} = -\frac{\tau}{1+\tau}\epsilon^{\tau}_{\theta} = -\frac{\tau(\theta)}{2} <0.$$

Labor demand is decreasing in tightness, which is why the elasticity is negative. A higher tightness makes it harder to fill vacancies, and therefore more expensive to maintain a certain workforce size, reducing the labor demand. The elasticity of $L^d$ with respect to $a$ is

$$\epsilon^{L^d}_{a} = 1 > 0.$$

Labor demand is increasing in productivity. If production workers become more productive, this increases their relative value to firms since wages do not fully adjust. As a result, firms want to higher more workers.

4. **Characterize tightness $\theta(a)$ and employment $L(a)$ in the model. Compute the elasticities of $\theta(a)$ and $L(a)$ with respect to $a$. Interpret the signs of these elasticities.**

Tightness is such that labor supply equals labor demand:

$$L^s(\theta) = L^d(\theta).$$

For a given $a$, this relationship uniquely determines a $\theta$. Therefore, this equation implicitly defines $\theta(a)$. Once we have $\theta(a)$, plugging into either the labor demand or labor supply equation (they will be equal by construction) gives $L(a)$.

To compute the elasticity of $\theta(a)$ with respect to $a$, we consider the effect of a small change in $d\ln a$ on supply and demand. First, the effect on supply is 

$$d\ln L^s = \epsilon^{L^s}_{\theta} \cdot d \ln \theta = \frac{u}{2} \cdot d \ln \theta.$$ 

Second, the effect on demand is 

$$d\ln L^d = \epsilon^{L^d}_{\theta} \cdot d\ln \theta + \epsilon^{L^d}_{a} \cdot d \ln a =  -\frac{\tau(\theta)}{2}\cdot d\ln \theta + d \ln a .$$

Since supply and demand are equal both before and after the shock, we have $d \ln L^s = d \ln L^d.$ This condition imposes

$$\frac{u}{2} \cdot d \ln \theta =  -\frac{\tau(\theta)}{2}\cdot d\ln \theta + d \ln a.$$

Rearranging the terms, we obtain the elasticity:

$$\epsilon^{\theta}_a = \frac{d \ln \theta}{d \ln a} = \frac{2}{u+\tau} > 0.$$

Tightness is increasing in productivity. As workers become more productive it becomes more worthwhile for firms to hire additional workers despite the increase in recruiting costs from posting additional vacancies. This raises the vacancies to unemployment ratio. This is why the elasticity is positive.

Consider the composition $f(x) = g(h(x))$, then 

$$\epsilon^f_x=\epsilon^g_h  \cdot \epsilon^h_x$$ 

by the chain rule, since 

$$\frac{x}{f} \frac{df}{dx}=\frac{h}{g} \frac{d g}{d h} \cdot \frac{x}{h}\frac{dh}{dx}.$$

Therefore, the elasticity of $L(a) = L^s(\theta(a))$ with respect to $a$ is

$$\epsilon^{L}_{a} = \epsilon^{L^s}_{\theta} \cdot \epsilon^{\theta}_{a} = \frac{u}{2} \cdot\frac{2}{u+\tau} = \frac{u}{u+\tau}>0.$$

We could use the labor demand as well, but then we would need to account for the fact that labor demand is a function of both $\theta$ and $a$, so using labor supply is easier. $L(a)$ is increasing in productivity. This is because when productivity is higher, workers become more valuable to firms (and wages do not fully adjust to offset this), so that firms hire more workers.

5. **Would shocks to labor productivity $a$ create realistic business cycles?**

Yes, a shock to labor productivity would create a qualitatively realistic business cycle. A positive productivity shock raises both tightness and employment, and reduces unemployment. A negative shock to productivity reduces both tightness and employment, and raises unemployment. This positive correlation between labor-market tightness and employment is [exactly what is observed in the data](https://doi.org/10.1093/qje/qjv006).

6. **Compute the amount of rationing unemployment $U^r(a)$ and frictional unemployment $U^f(a)$ in the model.**

Rationing unemployment is the amount of unemployment that would prevail if the recruiting cost $r$ was zero. Total unemployment can be obtained by reading employment off of the labor demand:

$$U(a) = 1 - L(a) = 1 - L^d(\theta(a),a) = 1 - a + a\cdot s\cdot r\cdot \sqrt{\theta(a)}.$$ 

Setting $r=0$ in the expression above, we see that rationing unemployment takes a particularly simple form here:

$$U^r(a) = 1-a.$$

Frictional unemployment is the difference between total unemployment and rationing unemployment. Hence frictional unemployment is 

$$U^f(a) = U(a) - U^r(a) = a\cdot s \cdot r \sqrt{\theta(a)}.$$

7. **Prove that $dU^f/da > 0$. Interpret the result and provide some policy implications.**

The elasticity of frictional unemployment with respect of productivity is

$$\epsilon^{U^f}_a = 1 + \frac{1}{2}\cdot \epsilon^{\theta}_a = 1 + \frac{1}{u+\tau} >0 .$$ 

Clearly, since $\epsilon^{U^f}_a>0$, we have $d U^f/d a>0$: frictional unemployment is increasing in labor productivity. This means that in good times, when labor productivity is high, frictional unemployment is high; by contrast, in bad times, when labor productivity is low, frictional unemployment is low. This result is maybe counterintuitive because total unemployment is decreasing in productivity.

The logic is in bad times, jobs are lacking, so the labor market is slack and recruiting is easy and inexpensive. Accordingly, matching and recruiting frictions do not matter much. In contrast, in good times, jobs are plentiful, so the labor market is tight and recruiting is difficult and expensive. Accordingly, matching and recruiting frictions generate a significant amount of unemployment.

The main policy implication is that the policies that effectively reduce unemployment are different in good and bad times. In good times, unemployment is caused by matching frictions, so policies reducing these frictions are effective: for instance, placement agencies. In bad times, unemployment is caused by a lack of jobs, so policies creating jobs directly are effective: for instance, public employment or wage subsidies.

### Problem B (3 points)

**Consider an economy with a mass 1 of participants in the labor force. The Beveridge curve takes a very simple form: $v(u) = \omega/u$, where $\omega>0$ governs the location of the Beveridge curve. Each vacancy requires the attention of a full-time worker. Finally, all production takes place in firms and there is no home production at all. As a result, social welfare is determined by the number of producers in firms.**

1. **Compute the socially efficient labor market tightness $\theta^{\star}$. How does $\theta^{\star}$ depend on the parameter $\omega$?**

There are two approaches here. 

The first approach directly use the sufficient-statistic formula developed by [Michaillat & Saez (2021)](https://doi.org/10.1016/j.pubecp.2021.100009) and discussed in lecture. 
The recruiting cost, the number of recruiters allocated to each vacancy, is $\kappa=1$. The social value of nonwork is equal to $\zeta = 0$ here, because there is no home production at all. The elasticity of the Beveridge curve is just $\epsilon = 1$ here. Therefore, the efficient labor-market tightness satisfies

$$\theta^{\star} = \frac{1-\zeta}{\epsilon\kappa} = 1.$$

The efficient tightness does not depend on $\omega$.

The second approach rederives the efficient tightness in the specific Beveridgean model described here. Since there is no home production at all, social welfare is determined by the number of producers in the economy. The social planner therefore maximizes the number of producers, which is just the number of workers in the labor force (1) minus the number of unemployed workers ($u$) minus the number of recruiters ($v$). The social planner chooses $u$ and $v$ to maximize

$$1-u-v$$

subject to the Beveridge curve:

$$v \cdot u = \omega.$$

The maximization problem is entirely symmetric in $u$ and $v$ so the optimal  $u$ and $v$ must be the same: $u^{\star} = v^{\star}$. Accordingly the optimal tightness is one:

$$\theta^{\star} = v^{\star}/u^{\star} = 1.$$


2. **Compute the socially efficient unemployment rate $u^{\star}$ as a function of the actual unemployment and vacancy rates, $u$ and $v$.**

Since $u^{\star} = v^{\star}$, the Beveridge curve imposes 

$$u^{\star} = \sqrt{\omega}.$$

In practice, $\omega$ is unobserved. However, we can observe $u$ and $v$. Moreover, $u$, $v$, and $\omega$ are linked through the Beveridge curve: $v \cdot u = \omega$. Replacing $\omega$ with $v \cdot u$ in the equation above gives

$$u^{\star} = \sqrt{v \cdot u}.$$

3. **Using the formulas derived in Questions 1 and 2, compute the efficient tightness, efficient unemployment rate, and unemployment gap in the United States in December 2021. What are the policy implications of your results?**

In December 2021 in the United States the [unemployment rate](https://fred.stlouisfed.org/series/UNRATE) was 3.9% while the [vacancy rate](https://fred.stlouisfed.org/series/JTSJOR) was 6.8%. Accordingly, the implied efficient unemployment rate, tightness, and unemployment gap are:

| | $u^{\star}$| $\theta^{\star}$| $u^{gap} = u - u^{\star}$|
|--|:--:|:--:|:--:|
|December, 2021 | 5.2 | 1 | -1.2 |

The unemployment gap was negative in December 2021, which means that the unemployment rate was below the efficient level according to our model. 

In terms of policy, this means that it might be a good time for the Fed to raise interest rates so has to lower labor-market tightness and raise the unemployment rate. The goal for the Fed is to keep the unemployment gap as close to zero as possible (see section 5.2 in ["An Economical Business-Cycle Model"](https://www.pascalmichaillat.org/7.html)). 

Section 5.3 of ["An Economical Business-Cycle Model"](https://www.pascalmichaillat.org/7.html) also argues that in the US the monetary multiplier is close to 0.5. This means that an increase in interest rate by 1 percentage point raises the unemployment rate by 0.5 percentage point. Given that the unemployment gap is -1.2 in December 2021, the Federal Reserve should increase its interest rate by $1.2/0.5 = 2.4$ percentage points so as to eliminate the unemployment gap.