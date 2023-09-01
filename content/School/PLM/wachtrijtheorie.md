## Definities

| $t_a$                                          | gemiddelde aankomsttijd                         |
| ---------------------------------------------- | ----------------------------------------------- |
| $\lambda = \frac{1}{t_a}$                      | gemiddelde aankomstritme                        |
| $\sigma_a$                                     | standaardvariatie van de tussenaankomsttijden   |
| $C_a = \frac{\sigma_a}{t_a}$                   | variatiecoëfficiënt van de tussenaankomsttijden |
| $t_e$                                          | gemiddelde (effectieve) productietijd           |
| $\mu = \frac{1}{t_e}$                          | gemiddelde (effectieve) productieritme          |
| $\sigma_e$                                     | standaarddeviatie van de productietijd          |
| $C_e = \frac{\sigma_e}{t_e}$                   | variatiecoëfficient van de productietijd        |
| $\rho = \frac{t_e}{t_a} = \frac{\lambda}{\mu}$ | bezettingsgraad van een resource                |
| $\tau$                                         | omsteltijd per lot                              |
| $Q$                                            | lotgrootte                                      |
| $E(W_n)$                                       | verwachte doorlooptijd (van machine n)          | 

## Verschillende soorten wachtrijen
De verschillende soorten wachtrijen worden voorgesteld aan de hand van de Kendall-notatie A / S / m met:
- A: de verdeling van de aankomsttijden
- S: de verdeling van de productietijden
- m: het aantal parallelle machines

Voor verdelingen van A en S maken we gebruik van de volgende code:
- M: exponentiële verdeling
- G: algemene (general) verdeling
- D: deterministische verdeling

## Drie te kennen wachtrijen
1. M/M/1-wachtrij = zie formularium
2. M/G/1-wachtrij = zie formularium
3. G/G/1-wachtrij = VUT-vergelijking, zie formularium

De formule voor de G/G/1-wachtrij kan ook gebruikt worden voor M/M/1 en M/G/1, met:
- M/M/1: $C_a^2 = C_e^2 = 1$
- M/G/1: $C_a^2 = 1$

## Meerdere machines
$t_e$ , $C_e$  en $\tau$ zijn variabelen specifiek aan de machines, de andere variabelen blijven constant doorheen het traject tenzij anders aangegeven.

Wanneer we de $E(W_1)$ willen berekenen kan dat simpelweg via de formule op het formularium met $C_e^2(1)$ en $\rho(1)$.

Voor de tweede machine moeten we een $C_a$(2) berekenen aan de hand van de verbindingsvergelijking:
$$ C_a^2(2) = C_d^2(1) = \rho^2(1) C_e^2(1) + (1 - \rho^2(1)) C_a^2 $$

## Belangrijke observaties
### Wet van Little
$$ E(L) = E(W) * \lambda $$
Met:
$E(L) =$ gemiddelde voorraad
$E(W) =$ gemiddelde doorlooptijd
$\lambda =$ gemiddelde aankomstritme

### Doorlooptijd (lead time) berekenen adhv een bepaald serviceniveau
Methode:
1. $F_X(x)$-functie van de verdeling gelijkstellen aan [[serviceniveau]].
2. $E(W)$ invullen in de plaats van $E(X)$ in de formule
3. Oplossen naar $x$

### Ordergrootte bepaling
Als $\rho < 1$:
$$ Q* = \frac{t_e \tau + \sqrt{t_a t_e \tau^2}}{t_e t_a - t_e^2} $$
Indien $\rho$ groter zou zijn dan 1, dan is de bestelgrootte waarvoor de bezetting toch onder 1 zou zijn, de kritieke ordergrootte:
$$ Q_{kritiek} = \frac{\tau}{t_a - t_e} $$
