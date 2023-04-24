# Hardware presentatie 2: Opslag (HDD/SSD)

## Feedback 24/04/23
* mogelijks switchen presentatie (iemand ander pres geven)
* presentatie + sidenotes moet voldoende inhoud bevatten (niet uit het hoofd lullen)

## Aanpak:

* Opslagmogelijkheden grotendeels (HDD en SSD)
* waarvan we komen (historisch) en waar we heen gaan 

## Soorten opslag

Cache -> Primary storage -> secondary storage -> tertiary storage

Cache: 
1. zo snel mogelijk
2. snelheid gelimiteerd door afstand tot CPU
3. door afstand, gelimiteerd in grootte

Primary storage: Main memory
1. Memory (RAM) | ROM
2. geheugen voor meerdere processen aanwezig te houden
3. soort van cache tussen secondary storage en CPU cache
4. direct accessible by CPU (via memory bus)
5. cache soort van primary storage

Secondary storage:
1. connection via input/output channels
2. data from secondary to primary before using
3. non-volatile (niet verliezend bij stroomverlies)
4. SSD en HDD access time per byte order ms
5. USB-sticks, ...

Tertiary storage:
1. backup van weinig gebruikte data
2. niet zoveel gebruikt
   
## Onderwerp: Eigenschappen

1. Niet volatile:
   1. houd data bij bij spanningsverlies
   2. geschikt voor lange-termijn opslag
2. Aanpasbaar:
   1. zowel lees als schrijfbaar
3. Leesbaarheid:
   1. Random access: gegeven een random address (op het device), krijg de data dat aan het address hangt.


## HDD

### Connectoren:
* PATA
* SATA
* SCSI

### Disk:
Materie:
* Aluminium Magnesium alloy
* Magnetische functionele laag:
   * 120nm dik
   * Cobalt Chromium Tantalum Alloy
   * verschillende regios die individueel magnetiseerbaar zijn
* brushless DC-motor draait disk rond op 7200rpm (soms ook 5400rpm)

Werking:
* opgedeeld in concentrische cirkels (meer dan 500000 tracks)
* elke track opgedeeld in sectors (vakjes)
* preamble in sector (voor snelheid en grootte bit data)
* adress (voor te weten welke sector gefocust is)
* data (4KB per sector)
* ECC (verificatie van data)
* kleine gap tussen sectoren

### Arm:
Materie:
* 2 armen
* slider
   * zorgt voor afstand of geen afstand tussen disk en head
   * 15nm is afstand
* read/write head
* motor op einde van arm zorgt voor snelle bewegingen (20/sec)

Werking:
* read/write head geeft magnetische zin aan en over aan stukje van sector (1 bit) (ongeveer 90nm x 100nm x 120nm)
* magnetisch veld gecreerd en gechaneld naar write head
* read head leest magnetische zin van bit
* 0 = geen verandering van cel tot volgende
* 1 = verandering van cel tot volgende


### Nieuwe veranderingen
* Orientatie cellen horizontaal naar verticaal (rond 2010) (meer cellen per oppervlakte)
* Shingled Magnetic Recording: (rond 2020) geen vrije ruimte, cellen overlappen licht (kleine read head waardoor deze goed gelezen kan worden ondanks overlap)
* CMR: 90nm breed met vrije ruimte tussen
* Heat Assisted Magnetic Recording: warm cel op met kleine laser om switch makkelijker te maken

## SSD

* Charge Trap Flash Memory Cell: 
   * Charge trap word opgevuld met meer of minder electronen (zorgt voor verschillende waarden) (tot 16 waardes 4 bit)
   * lezen: meet electron-level van de charge-trap
   * clearen: alle electronen eruit forceren door negatieve spanning
   * VNAND: vertical NAND (heeft 10 cellen) (1 String)
   * 1 cell per keer geactiveerd (lezen of schrijven)
   * lezen en schrijven gaan van en naar Bitline om informatie door te geven
   * 1 Row = 32 Stings
   * Control gates voor alle equivalente cellen in verschillende Strings zijn gelijk
   * 1 Block = 6 Rows
   * 1 Column = 2 Blocks
   * bitlines shared over equivalente Strings
   * bitline selectors = selecteren welke bitline actief is
   * page buffer om telkens page bij page op te slaan (bufferen)

* Tegenwoordig: 
   * 1 String = 96-136 lagen hoog
   * 1 Row = 30.000 - 60.000 Strings
   * 1 Block = 4-8 Rows
   * 4000 - 6000 blocks * 2
   * 8 keren deze chip kopieren stacken


## Logboek:

| Datum | Linkje voor de dag/vorige dag |
| ----- | ----------------------------- |
| 09/04/23 | [Wikipedia Computer data storage](https://en.wikipedia.org/wiki/Computer_data_storage#Hierarchy_of_storage) |
|          | [Wikipedia Hard disk drive](https://en.wikipedia.org/wiki/Hard_disk_drive) |
| 23/04/23 | [Video interne werking HDD](https://www.youtube.com/watch?v=wtdnatmVdIg) |
|          | [extra informatie HDD](https://turbofuture.com/computers/Types-of-Computer-Hard-Disk-Drives) |

