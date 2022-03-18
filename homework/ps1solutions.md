ECON 2080, part 1  
Spring 2022  
Pascal Michaillat  
Brown University

# Problem Set 1: Solutions

### Problem A

**Consider a labor market in which $U$ unemployed workers send one application each to $V$ job vacancies. The size of the labor force is fixed at $L$. If a vacancy receives one or more applications it selects an applicant at random and forms a match. The other applicants are returned to the pool of unemployed workers to apply again.**

1. **Compute the matching function in this labor market.**

Index the the $U$ unemployed workers by $i \in \{1, \cdots, U\}$ and the $V$ vacancies by $j\in \{1, \cdots, V\}$. Since there are $V$ vacancies to choose from and each unemployed worker sends just one application, the probability that any given unemployed worker $i$ applies to any given vacancy $j$ is

$$\Pr(i \text{ applies to } j) = \frac{1}{V}.$$

And the probability that $i$ does not apply to $j$ is

$$\Pr(i \text{ doesn't apply to } j = 1-\Pr(i \text{ applies to } j)=1-\frac{1}{V}.$$

Therefore, assuming each unemployed worker's choice of where to apply is an independent event, the probability that a vacancy receives no applications is
    
$$\Pr(j \text{ receives no applications}) = \left(1-\frac{1}{V}\right)^{U},$$

and the probability that a vacancy receives at least one application is
    
$$\Pr(j \text{ receives more than 1 application})=1- \left(1-\frac{1}{V}\right)^{U}.$$

Because we are assuming that every vacancy that receives at least one application chooses to employ one of its applicants, the total number of matches that occur in a single round of matching is just the number of vacancies that receive at least one application:

$$M(U,V) = V\cdot \left[1 - \left(1-\frac{1}{V}\right)^{U}\right].$$

2. **What is a good approximation of the matching function when $V$ is large? Is this approximate matching function realistic?**

The first-order Taylor expansion of any function $f(x)$ around $0$ is

$$f(x) \approx f(0) + f'(0)\cdot x.$$

Hence, the first-order Taylor expansion of $e^x$ around $0$ is

$$e^x \approx 1 + x.$$

This approximation holds when $x$ is close to zero. For large $V$, $1/V$ is close to zero, so

$$e^{-\frac{1}{V}} \approx 1+\frac{1}{V}.$$

Taking both sides to the $U$ power gives
    
$$\left(1 - \frac{1}{V}\right)^U \approx e^{-\frac{U}{V}}.$$

So a good approximation of the matching function for large $V$ is
    
$$M = V\cdot \left(1-e^{-\frac{U}{V}}\right).$$

This matching function does satisfy several of the properties we assumed in class, and which we know are a good description of what we see in the data. First, the matching function exhibits constant returns to scale, because for any $\lambda$,

$$M(\lambda U, \lambda V) = \lambda V\left(1-e^{-\frac{\lambda U}{\lambda V }}\right) = \lambda V\left(1-e^{-\frac{ U}{V }}\right) = \lambda M(U,V).$$

Second, the matching function is increasing in both its arguments. Third, the matching function is the composite of concave functions and so is concave. 

However, we had to make some unrealistic assumptions to arrive at this matching function. For instance, we assumed that: (1) unemployed workers only apply to one job, (2) they randomly choose which job to apply to, (3) vacancies randomly pick among the applications they receive. In practice, we might expect unemployed workers to apply to multiple job openings, and to choose where to apply systematically. Similarly, in practice firms choose systematically between the different applications they receive.

3. **Now assume that the labor market consists of $N$ jobs that are filled and $V$ jobs that are vacant. Unemployed workers send one application each to a job, without knowing which jobs are filled and which jobs are vacant. Filled jobs reject all applicants and vacant jobs select an applicant at random. Compute the matching function in this labor market, then provide an approximation of the matching function when $V$ is large.**

Now, the probability that worker $i$ applies to job $j$ (either a filled job or a vacant job) is

$$\Pr(i \text{ applies to }j) = \frac{1}{V+N}.$$

And the probability that $i$ does not apply to job $j$ is
    
$$\Pr(i \text{ doesn't apply to }j) = 1-\frac{1}{V+N}.$$

By the same logic as in question 1, the matching function is

$$M(U,V,N) = V \cdot \left(1-\left(1-\frac{1}{N+V}\right)^{U}\right).$$

Since $N = L - U$, we can express the matching function as follows:

$$M(U,V,L) = V \cdot \left(1-\left(1-\frac{1}{L-U+V}\right)^{U}\right).$$

For large $V$, the matching function is approximately

$$M(U,V,L) = V \cdot\left(1-e^{-\frac{U}{L-U+V}}\right).$$

Notice that this matching function does not have constant returns to scale in $U$ and $V$.

4. **Finally, assume that not all $U$ unemployed workers are suitable for the $V$ vacancies available, and that workers do not know which vacancies are suitable. Let $\kappa$ be the fraction of workers who are suitable employees for a randomly selected vacancy. Compute the matching function in this labor market, then provide an approximation of the matching function when $V$ is large.**

Now the relevant probability is the probability of a vacancy receiving a suitable applicant. Since unemployed workers do not know which jobs they are suitable for, we can treat being suitable as an independent event from the choice of where to apply. The probability that unemployed worker $i$ applies to job $j$ and is suitable for that job is

$$\Pr(i \text{ applies to } j \text{ and is suitable}) = \frac{\kappa}{V}.$$

By similar logic to above, the matching function is now

$$M(U,V) = V \cdot \left(1-\left(1- \frac{\kappa}{V}\right)^{U}\right).$$

For large $V$, the matching function is approximately

$$M(U,V) = V \cdot \left(1-e^{-\frac{\kappa U}{V}}\right).$$

### Problem B

**Consider a labor market with $H$ labor-force participants. The flow of new worker-firm matches created when there are $U$ unemployed workers and $V$ vacancies is $m=\omega U^{\eta}V^{1-\eta}$, where $\omega>0$ is the matching efficiency. The job separation rate is $s>0$.**

1. **Compute the expression of the Beveridge curve $v(u)$, which relates the vacancy rate $v=V/H$ to the unemployment rate $u=U/H$ when labor market flows are balanced.**

When flows are balanced, the flows into unemployment are equal to the flows out of unemployment. This implies that

$$s(H-U) = \omega U^{\eta}V^{1-\eta}.$$

Dividing through by $H$ gives

$$s(1-u) = \omega u^{\eta} v^{1-\eta}.$$

Rearranging for $v$ gives

$$v(u) = \left[\frac{s(1-u)}{\omega u^{\eta}}\right]^{\frac{1}{1-\eta}}.\tag{1}$$
   
2. **Establish the properties of the Beveridge curve (shape, limits, etc.) Draw the Beveridge curve in a Beveridge diagram (diagram with unemployment rate on the x-axis and vacancy rate on the y-axis).**

The limit when $u\to 0$ is $\lim_{u \rightarrow 0} v(u) = \infty$. The limit when $u\to 1$ is $\lim_{u \rightarrow 1} v(u) = 0$.

Next we compute the slope of the Beveridge curve:

$$v'(u) = \frac{1}{1-\eta}\frac{u^{\eta}}{1-u}(-u-(1-u)\eta)u^{-\eta-1}\left[\frac{s(1-u)}{w u^\eta}\right]^{\frac{1}{1-\eta}}.$$

Hence the slope is

$$v'(u) = - \frac{v(u)}{u}\frac{1}{1-\eta}\left(\eta + \frac{u}{1-u}\right) <0 \text{ for } u \in (0,1].$$

The implication is that $v(u)$ is downward sloping.

Finally we study the curvature of the Beveridge curve:
   
$$ v^{\prime\prime}(u) = \frac{\eta}{(1-\eta)^2(1-u)^2 u^2} \left[\frac{s(1-u)}{w u^n}\right]^{\frac{1}{1-n}} > 0 \text{ for } u \in (0,1].$$

The implication is that $v(u)$ is convex.

The figure below represent the Beveridge curve in a Beveridge diagram with (unemployment is on the x-axis and vacancies are on the y-axis.)

<iframe src="https://www.desmos.com/calculator/i02iqv7gkj" width="100%" style="min-height:400px"></iframe>

3. **Compute the elasticity $d \ln(v)/d \ln(u)$ of the Beveridge curve. What is a plausible value for the elasticity in the United States?**

Recall that

$$\frac{d \ln v}{d \ln u} = \frac{u}{v} \frac{d v}{ d u} = \frac{u}{v} v'(u).$$

Plugging in using the expression for $v'(u)$ from question 2, we obtain

$$\frac{d \ln v}{d \ln u} = \frac{u}{v}\left[-\frac{v}{u}\frac{1}{1-\eta}\left(\eta + \frac{u}{1-u}\right)\right] = \frac{1}{1-\eta}\left(\eta + \frac{u}{1-u}\right).$$

A plausible value of the elasticity for the United States is between $0.84$ and $1.02$ [(Michaillat and Saez 2021)](https://doi.org/10.1016/j.pubecp.2021.100009).

### Problem C

**Consider a labor market with a labor force of size 1. The job-separation rate is $s>0$. The flow of new worker-firm matches created at time $t$ is $m(t) = \omega u(t)^{\eta}v(t)^{1-\eta}$, where $\omega>0$ is the matching efficiency, $u(t)$ is the unemployment rate, $v(t)$ is the vacancy rate, ad $\eta \in (0,1)$ is the matching elasticity.**

1. **Give the law of motion for the unemployment rate $u(t)$; that is, express $\dot{u}(t)$ as a function of variables and parameters of the model.**

The flow into unemployment at time $t$ is $s[1-u(t)]$. The flow out of unemployment at time $t$ is $\omega u(t)^\eta v(t)^{1-\eta}$. So the law of motion of the unemployment rate is

$$\dot{u}(t) = s[1-u(t)] - \omega u(t)^{\eta}v(t)^{1-\eta}.$$

2. **Assuming the labor market tightness $\theta = v/u$ is constant, solve the differential equation that you have just obtained.**

Assuming the labor market tightness is constant, we can rewrite the law of motion as

$$\dot{u}(t) = s[1-u(t)] - \omega \theta^{1-\eta} u(t).$$

Using $f(\theta) = \omega \theta^{1-\eta}$, we reformulate the differential equation as

$$\dot{u}(t) = s[1-u(t)] - f(\theta)u(t). \tag{2}$$

The critical point of the differential equation (the value of $u$ such that $\dot{u}=0$) satisfies balanced flows:

$$\dot{u}(t) = 0 \Rightarrow s[1-u(t)] = f(\theta) u(t) \Rightarrow u(t) = \frac{s}{s+f(\theta)} \equiv u^b.$$

The unemployment rate $u^b$ is the critical point of the differential equation.

We can rewrite the differential equation in (2) using the definition of the critical point $u^b$:

$$\dot{u}(t) +[s+f(\theta)] u(t) = \underbrace{\frac{s}{s+f(\theta)}}_{u^b}[s+f(\theta)],$$

such that

$$\dot{u}(t) +\left[s+f(\theta)\right] \left[u(t)-u^b\right] = 0. \tag{3}$$

We introduce the integrating factor $\mu(t) \equiv e^{[s+f(\theta)]t}$. Notice that $\dot{\mu}(t) = [s+f(\theta)]\mu(t)$. Multiplying both sides of (3) by $\mu(t)$ gives

$$\mu(t) \dot{u}(t) + \left[s+f(\theta)\right] \mu(t)\left[u(t) - u^b\right] = 0.$$

This is equivalent to

$$\mu(t) \dot{u}(t) + \dot{\mu}(t)\left[u(t)-\mu^b\right] = 0.$$

Using the product rule, we can write

$$\frac{d }{d t}\left[\mu(t)\left[u(t)-u^b\right]\right] = 0.$$

Integrating from $t_0 \in \mathbb{R}$ to $t$, we get

$$\mu(t)\left[u(t)-u^b\right] - \mu(t_0)\left[u(t_0)-u^b\right] = 0.$$

Finally, plugging in the definition of $\mu(t)$, we obtain

$$u(t) - u^b = [u(t_0) - u^b] \cdot e^{[s+f(\theta)](t_0 - t)}.$$

For $t_0 = 0$,
 
$$u(t) - u^b = \left[u(0) - u^b\right] e^{-\left[s+f(\theta)\right]t}.$$

This means that from any initial level of unemployment $u(0)$, unemployment decays exponentially towards the critical point $u^b$ at a rate $s+f(\theta)$. The unemployment rate $u^b$ is called Beveridgean unemployment rate because it is the unemployment rate given by the Beveridge curve for a given tightness. For any initial position, the unemployment rate reverts exponentially toward the Beveridgean unemployment rate.

3. **Denote the limit of the unemployment rate by $u^b = \lim_{t\rightarrow \infty}u(t)$. What is the half life of the unemployment rate? That is, how long does it take for $u(t)-u^b$ to decrease by $50\%$. Provide both an analytical expression of the half-life and an estimate of it for the United States.**

In the United States, $f(\theta) \approx 56\%$ per month and $s \approx 3 \%$ per month, so $s+f(\theta) \approx 59\%$ per month. 

We want to find the $t$ such that

$$\left[u(0)-u^b\right]e^{-\left[s+f(\theta)\right]t} = \frac{1}{2}\left[u(0)-u^b\right].$$

That is, we are looking for the duration $t$ such that

$$e^{-\left[s+f(\theta)\right]t} = \frac{1}{2}.$$

Taking natural logs of both sides, we find $-[s+f(\theta)t = -\ln 2$, such that the half life is

$$t = \frac{\ln 2}{s+f(\theta)} \approx 1.17 \text{ months. }$$

As discussed in class, it takes about a month for the unemployment rate to cover half of the distance to the Beveridge curve. In a quarter, the unemployment rate would have covered $1-(1/2)^3 = 7/8 = 86\%$ of the distance to the Beveridge curve. In other words, the unemployment rate is never far from the Beveridge curve.
