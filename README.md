# sta355h1s-assignment-2-solved
**TO GET THIS SOLUTION VISIT:** [STA355H1S Assignment #2 Solved](https://www.ankitcodinghub.com/product/assignment-2-sta355h1s-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;116651&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;STA355H1S Assignment #2 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
1. The Hidalgo stamp data is a (semi-)famous dataset containing thicknesses of 482 postage stamps from the 1872 Mexican “Hidalgo” issue. It is believed that these stamps were printed on different types of papers so that the data can be modeled as a “mixture” of several distributions with the density having between 5 and 7 modes. These data (which have been “jittered” by adding noise) are available on Quercus in a file stamp.txt.

(a) Use the density function in R to estimate the density. Choose a variety of bandwidths (the parameter bw) and describe how the estimates change as the bandwidth changes. How small does the bandwidth need to be for the density estimate to have 5 modes? 7 modes?

(b) One automated approach to selecting the bandwidth parameter h is leave-one-out cross-validation. This is a fairly general procedure that is useful for selecting tuning parameters in a variety of statistical problems.

If f and g are density functions, then we can define the Kullback-Leibler divergence

For a given density f, DKL(fkg) is minimized over densities g when g = f (and DKL(fkf) = 0). In the context of bandwith selection, define ) to be a density estimator with bandwidth h and f(x) to be the true (but unknown) density that produces the data. Ideally, we would like to minimize DKL(fkfh) with respect to h but since f is unknown, the best we can do is to minimize an estimate of DKL(fkfh). Noting that

= −Ef[ln(fh(X))] + constant,

this suggests that we should try to maximize an estimate of Ef[ln(fh(X))], which can be estimated for a given h by the following (leave-one-out) substitution principle estimator:

CV(

where

is the density estimate with bandwidth h using all the observations except Xi.

Now suppose we replaced ) in the formula for CV(h) and maximized

.

Maximizing L(h) or CV(h) over h &gt; 0 has the flavour of maximum likelihood estimation. However, selecting the bandwidth by maximizing L(h) does not work while maximizing CV(h) typically (but not always!) produces a good result.

For (i) and (ii) below, assume that w(0) &gt; 0 and for x 6= 0, h−1w(x/h) → 0 as h ↓ 0 (which is true for most commonly used kernels).

(i) Show that L(h) ↑ ∞ as h ↓ 0.

(ii) In the case where X1,···,Xn are distinct (that is, no tied observations), show that

CV(h) → −∞ as h ↓ 0 and h ↑ ∞.

(c) On Quercus, there is a function kde.cv (in a file kde.cv.txt) that computes CV(h) for various bandwidth parameters h for the Gaussian kernel. This function has two arguments, the data x and a vector of bandwidth parameters h; the default for h is a vector of 101 bandwidths ranging from h∗/10 to 4h∗ where h∗ is the default bandwidth in the R function density. The function kde.cv can be used as follows:

&gt; r &lt;- kde.cv(x)

&gt; plot(r$bw,r$cv) # plot of bandwidth versus CV

&gt; r$bw[r$cv==max(r$cv)] # bandwidth maximizing CV

Use this function to estimate the density of the Hidalgo stamp data. How many modes does this density have?

2. Suppose that F is a distribution concentrated on the positive real line (i.e. F(x) = 0 for x &lt; 0). If µ(F) = EF(X) then the mean population share of the distribution F is defined as MPS(F) = F(µ(F)−) = PF(X &lt; µ(F)). (When F is a continuous distribution, F(µ(F)−) = F(µ(F)).) For most income distributions, MPS(F) &gt; 1/2 with MPS(F) = 0 if (and only if) all incomes are equal and MPS(F) → 1 as Gini(F) → 1. Associated with MPS(F) is the mean income share MIS(F) = LF(MPS(F)) where LF(t) is the Lorenz curve

with

(a) Suppose that F is a continuous distribution function with Lorenz curve LF(t). Show that MPS(F) satisfies the condition

(MPS(F)) = 1

where L0F(t) is the derivative (with respect to t) of the Lorenz curve.

(b) Suppose that LF(t) = tα+1 for some α ≥ 0. Find MPS(F) and MIS(F).

(c) Given observations X1,···,Xn from a distribution F, a substitution principle estimate of MPS(F) is

n

MPS(d

=1

A sample of 200 incomes is given on Quercus in a file incomes.txt. Using these data compute an estimate of MPS(F) and use the jackknife to give an estimate of its standard error.

(d) Derive a substitution principle estimator for MIS(F). Using the data in part (c), compute an estimate of MIS(F) and use the jackknife to estimate its standard error. (Hint: Use the following estimator of the Lorenz curve:

where dxe is the smallest integer greater than or equal to x.)

Supplemental problems (not to be handed in):

3. Suppose that X1,···,Xn are independent random variables with common density f(x−θ) where f is symmetric around 0 (i.e. f(x) = f(−x)) and θ is an unknown location parameter. If Var(Xi) is finite then the sample mean X¯ will be a reasonable estimator of µ; however, if f has heavy tails then X¯ will be less efficient than other estimators of θ, for example, the sample median.

An useful alternative to the sample mean is the α-trimmed mean, which trims the smallest α and largest α fractions of the data and averages the middle order statistics. Specifically, if we define r = bnαc (where bxc is the integer part of x) then the α-trimmed mean, θb(α), is defined by

.

(a) Suppose (for simplicity) that bnαc = b(n−1)αc and define ) to be α-trimmed mean with X(i) deleted from the sample. Find expressions for ); in particular, note that

) and

(b) Using the setup in part (a), show that the pseudo-values {Φi} are given by

for i = 1,···,r + 1

for i = r + 2,···,n − r − 1

for i = n − r,···,n

and give a formula for the jackknife estimator of variance of θb(α). (Think about how you might use this variance estimator to choose an “optimal” value of r.)

4. Suppose that θb1 and θb2 are unbiased estimators of a parameter θ and consider estimators of the form

.

(a) Show that θe is unbiased for any a.

(b) Find the value of a that minimizes Var(θe) in terms of Var( ), and Cov( Under what conditions would a = 1? Can a be greater than 1 or less than 0?

5. A histogram is a very simple example of a density estimator. For a sample X1,···,Xn from a continuous distribution with density f(x), we define breakpoints a0,···,ak satisfying a0 &lt; min(X1,···,Xn) &lt; a1 &lt; a2 &lt; ··· &lt; ak−1 &lt; max(X1,···,Xn) &lt; ak

and define for x ∈ [aj−1,aj):

with and x ≥ ak.

(a) Show that fb is a density function.

(b) For a given value of x, evaluate the mean and variance of

(c) What conditions on a0,···,ak are needed for the bias and variance of ) to go to 0 as n → ∞?

6. Another measure of inequality based on the Lorenz curve is the Pietra index defined by P(F) = max {t − LF(t)}

0≤t≤1

where LF(t) is the Lorenz curve.

(a) Show that g(t) = t − LF(t) is maximized at t satisfying F −1(t) = µ(F).

(b) Using the result of part (a), show that

.

(c) Give a substitution principle estimator for the Pietra index P(F) based on the empirical distribution function of X1,···,Xn. Using the data in Problem 2, compute an estimate of P(F) and use the jackknife to compute an estimate of its standard error.

(d) Suppose that you can assume that the incomes follow a log-normal distribution, that is,ln(X1),···,ln(Xn) are independent N(µ,σ2) random variables. Show that the Pietra index for the log-normal distribution is given by

P(F) = 2Φ(σ2/2) − 1

where Φ(x) is the cdf of a N(0,1) distribution.
