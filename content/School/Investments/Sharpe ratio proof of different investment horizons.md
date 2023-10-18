## Given
$$SR_t >< SR_T$$
$$r_t \sim IIDN(\mu, \sigma^2)$$
$$r_t \sim ln(1 + R_T)$$
## Proof
$$SR_t = \frac{E(r_t) - r_f}{\sigma} = \frac{\mu - r_f}{\sigma}$$
$$r_T = \sum{r_t}$$
$$E(r_T) = var(\sum{r_t})$$
$$ = var(r_1) + var(r_2) \: + \: ... \: + \: 2\:  cov_{1,2} \: + \: ... \: + \:\sigma^2$$
$$= T * \sigma^2$$
$$\sigma_{rt} = \sqrt{T}*\sigma$$
$$SR_T = \frac{T\mu - T r_f}{\sqrt{T}\sigma} * \frac{T}{\sqrt{T}} * SR_T$$
