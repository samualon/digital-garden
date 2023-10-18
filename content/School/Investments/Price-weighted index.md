A price-weighted index corresponds to a portfolio in which every asset is weighted according to its price.

The weight of an asset $n$ in an index with $N$ assets is calculated as follows:
$$ w_n = \frac{P_n}{P_1 + P_2 \: + \:...\: + \:P_3} $$
The value of the index can be calculated as follows:
$$ V = \frac{1}{N} \sum^N_{n=1} P_n $$
## In practice
A price-weighted index is influenced by [[stock splits]], dividends, mergers, index adjustments, etc. This is why in practice a divider $d$ is used to calculate the value of the index without it being affected by before mentioned events.
$$ V = \frac{1}{d} \sum^n_{n=1} P_n $$
