FSA houdt in dat de producent de eindproducten 'eerlijk' zal verdelen zodat elk magazijn aan hetzelfde aantal periodes vraag kan voldoen. Dit heet de system time suply of STS.

## Berekening
Huidige beginvoorraad = $BV$
Te alloceren eenheden = "ontvangen"

### Berekenen STS van alle depots en het centrum
$\overline{DDLT}$ heeft twee mogelijke waarden:
- Geen veiligheidsvoorraad:
  $\overline{DDLT} = E(D) * L$
- Wel veiligheidsvoorraad:
  Nieuwe $L_2 = L_1 + \frac{vv}{E(D)}$
  $\overline{DDLT} = E(D) * L_2$

$STS_n = \frac{BV - \overline{DDLT}}{E(D)}$

### Berekenen STS
$$ STS_{systeem} = \frac{(BV_1 + BV_2 + ... + BV_n) + ontvangen - (OP_1 + OP_2 + ... + OP_n)}{E(D_1) + E(D_2) + ... + E(D_n)} $$

### Berekening toewijzing
$$ Allocatie = (STS_{systeem} - STS_n) * E(D_n) $$
