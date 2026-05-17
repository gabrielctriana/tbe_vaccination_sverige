# TBE-vaccination i Sverige
## Regional subventionspolicy och hälsoekonomisk effekt

**Gabriel Cederholm Triana · Maj 2026**  
Portföljprojekt inom hälsodataanalys och HEOR

---

Sverige har 21 regioner och 21 olika svar på samma fråga: ska 
TBE-vaccin subventioneras för barn? Prisskillnaden spänner från 
1 620 kr till över 6 000 kr för en familjs grundvaccination.

I det här projektet kombinerar jag medicinsk domänkunskap med statistisk 
analys och hälsoekonomisk modellering för att undersöka om 
skillnaden spelar roll – epidemiologiskt och ekonomiskt.

![TBE-incidens Sverige 2003–2025](figures/tbe_karta.gif)  
*Interaktiv version med år-reglage finns i notebooken.*

---

## Tre huvudfynd

**Subventionen ökar vaccinationsaktiviteten – men når inte hela målgruppen**  
Receptdata visar paradoxalt nog en minskning i subventionsregioner. 
Det är ett kanalbyte, inte ett fall: vaccination förflyttas från 
apotek till vårdcentral utan recept. Statistiskt bekräftat via 
t-test (p = 0,001). Primärdata från regionerna visar kraftiga 
ökningar i faktiska doser – men Sörmlands volymer når ännu inte 
de ~11 000 doser per år som krävs för fullständigt skydd av 
barnpopulationen.


![Sörmland vaccinationsvolymer](figures/sormland_vacc.png)

*TBE-doser i Sörmland per åldersgrupp. Barnvolymerna mer än 
fördubblas vid subventionens införande 2018 – men når ännu 
inte de ~11 000 doser per år som krävs för fullständigt 
populationsskydd.*


**Ingen kortsiktig incidenseffekt – och det är förväntat**  
DiD-analys (Sörmland vs. aggregerad kontroll) visar p = 0,956. 
TBE är en zoonos utan flockimmunitet. Skyddseffekten på 
befolkningsnivå realiseras om 20–40 år – inte nästa säsong.

**Hälsoekonomisk brytpunkt: 6,4 fall per 100 000**  
Periodiseringsanalys av Västmanlands program ger 538 000 kr per förhindrat fall – under total samhällskostnad (745 000 kr, Slunge et al. 2022). Brytpunkten härleds via NNV (Number Needed to Vaccinate): vid en incidens över 6,4 per 100 000 är varje subventionerad dos en samhällsekonomisk vinstaffär. Den gränsen är redan överskriden i Mälardalen – och choropleth-animationen visar att fler regioner passerar den varje år. 

*För regioner över brytpunkten är frågan inte om man har råd 
att subventionera – utan om man har råd att låta bli.*

---

## Metod

**Datainsamling och tvätt**  
Manuell insamling från regionala smittskyddsenheter och årsrapporter, 
kombinerat med automatiserad hämtning från Folkhälsomyndigheten och 
Socialstyrelsen (ATC J07BA01). Datatvätt med pandas inkluderar 
hantering av inkonsekventa regionnamn, dolda mellanslag och 
lång/bred transformation av tidsserierna.

**Statistisk analys**  
Korrelationsanalys med confounding-diskussion · t-test för 
displacement-hypotesen · Difference-in-Differences (Sörmland vs. 
aggregerad kontroll Uppsala + Västmanland)

**Hälsoekonomisk modellering**  
NNV · Periodiseringsanalys baserad på kliniskt vaccinationsschema 
(19 doser, ålder 3–83) · Break-even-incidens · Jämförelse mot 
Shedrawy et al. (2018) ICER 27 761 SEK/QALY

---

## Om mig

Jag är en analytiker med bakgrund i matematik, biologi och medicin – 
legitimerad gymnasielärare med 4,5 års medicinstudier (247,5 hp) 
inom epidemiologi, biostatistik och farmakologi. Det här projektet 
är en del av min omställning mot hälsodataanalys och HEOR, där jag 
kombinerar kvantitativ träning med medicinsk domänkunskap.

**Gabriel Cederholm Triana** · [LinkedIn](https://www.linkedin.com/in/gabriel-triana-040256167/?locale=en) · [E-post](mailto:gabrieltriana@gmail.com)

