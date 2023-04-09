# Hardware Presentatie 1: Apple Silicon

## Waarom eigenlijk?

Van waar komt Apple Silicon?
Vraag: Waarom altijd geld uitgeven aan Intel voor onze processoren als we die goedkoper "zelf" kunnen maken?
Antwoord: Sure, why not right? The more money, the better.

## Hoe?

DE arm (Advanced RISC Machines) structuur. 
Zij maken de architectuur en licensies voor andere bedrijven, 
die zelf hun de architectuur implementeren in hun product.
Zo zijn ook SoC (system on a chip) en SoM (system on module) mogelijk waarbij verschillende componenten 
ingebakken zijn (zoals geheugen, interfaces etc.).

## Waarom ARM?

Voordelen:

1. Goedkoper dan een volle CPU
2. Lage energiegebruik (efficient)

Nadelen:

1. incompatibel met x86
2. gelimiteerde instruction set kan beperkingen geven

## Wanneer ARM?

Begonnen met A4 voor mobiele apparaten zoals iPad, iPod etc.
MAAR op 10/11/2020 veranderde dat allemaal:
de M1 werd gepresenteerd, gebaseerd op de ARMv8.5-A architectuur en staat VOORAL voor performance per watt.
Daar presteerde hij zeker en vast in, fans waren soms overbodig, alles ging zowel sneller als 
koeler. Een nieuwe versie van hun macOS moest gemaakt worden (wegens incompitabiliteit met x86).

## Apple doet het vaker:

Eerste Macinoshes gebruikte Motorola 68000, 1990 switch naar PowerPC.
Daarna switch naar intel in 2005 en in 2020 naar apple silicon (ARM).

## Wat is M1?

Geoptimaliseerde chip gemaakt voor Mac, System On a Chip gebruik makende van 5-nm processen 
met 16 miljard transistoren. De beste CPU performance per watt, snelste geintegreerde gpu in 
personal computer (ook een Neural Engine voor betere machine learning performance). 

Verder gebouwd op 10+ jaar aan ervaring met iPhone en iPad ARM-cpu's.

PC's gebruiken traditioneel meerdere chips voor CPU, I/O security etc. 
Met de M1, deze technologieen worden gecombineerd in een enkele SoC,
hierdoor heeft met betere performance en efficientie.
Door unified memory architecture (RAM en ROM tesamen) heeft men hogere bandwidth
en lagere latency. 

Standaard 8-core CPU met 4 high-performance cores en 4 high-efficientie cores.
Dit geeft goede single-thread performance wegens de high-performance cores 
met goede efficientie maar ook goede multi-thread performance omdat men alle 8 
tegelijk kan gebruiken. Batterijleven is ook een pak gebeterd omdat men de efficientiecores
kan gebruiken voor achtergrond-programmas.

Support voor USB4 met snelheid tot 40Gbps.

## Vergelijking met andere moderne CPU's

Meest logische vergelijking intel en AMD door concurrentie in markt.
Tijd van uitkomst M1 was intel 11th gen en AMD 4000 serie uit.
Betere vergelijking M2, intel 12th gen en AMD 6000 series.

Kleine introductie 3 chips:

1. apple M2:
   * 2 miljard transistoren meer
   * grote upgrade aan GPU + 1-3 cores
   * tot 24GB LPDDR5 RAM
   * 100GB/s mem bandwidth
   * core is 21% groter maar slechts 
2. intel 12th gen:
   * DDR5 en DDR4 memory
   * P-cores en E-cores
3. AMD 6000:
   * 6nm process
   * ENKEL DDR5 support
   * improvement van Zen3 -> Zen3+

Devices voor vergelijking:
1. Apple macbook air M2
2. Dell XPS 13 i7
3. Asus zenbook 13 OLED Ryzen 7 6000 

### Vergelijking:

| Vergelijking | Apple | Intel | AMD | 
| ------------ | ----- | ----- | --- |
| specs        | M2    | i7-1280P | R7 6800U | 
| cores        | 8-core (4+4) | 14-core (6+8) | 8-core  |
| threads      | ?     | 20    | 16  |
| power        | 21W   | 44W   | 28W |
| efficientie  | 409 ppw | 244 ppw | 374 ppw |
| performance cR23 | 1585p | 1793p | 1488p |
| multicore    | 8154p | 10383p | 9413p |


## Logboek:

| Datum | Linkje voor de dag/vorige dag |
| ----- | ----------------------------- |
| 20/02/23: | [Wikipedia Apple silicon](https://en.wikipedia.org/wiki/Apple_silicon) |
|           | [Wikipedia ARM](https://en.wikipedia.org/wiki/ARM_architecture_family) | 
|           | [artikel ARMv9](https://www.anandtech.com/show/16584/arm-announces-armv9-architecture) |
| 04/03/23: | [m1 vs m2](https://web.archive.org/web/20220610100728/https://semianalysis.com/apple-m2-die-shot-and-architecture-analysis-big-cost-increase-and-a15-based-ip/) |
|           | [apple m1](https://www.apple.com/newsroom/2020/11/apple-unleashes-m1/) |
|           | [apple m2 vs 12th gen vs ryzen 6000](https://www.youtube.com/watch?v=Jw21otdS9Nk)|
|           | [intel 12th gen](https://www.intel.com/content/www/us/en/products/docs/processors/core/12th-gen-core-mobile-processors-brief.html)|
|           | [AMD 6000 series](https://www.amd.com/en/partner/ryzen-6000-series-mobile-processors) |
|           | [apple M2](https://www.apple.com/benl/newsroom/2022/06/apple-unveils-m2-with-breakthrough-performance-and-capabilities/)|
|           | [notebookcheck M2 i7-1280P](https://www.notebookcheck.net/Apple-M2-SoC-Analysis-Worse-CPU-efficiency-compared-to-the-M1.637834.0.html)|


