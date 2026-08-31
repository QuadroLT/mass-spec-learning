---
title: "Masių spektras"
definitions:
  - term: "Masių spektrometrija"
    description: "Analizinės chemijos metodas, skirtas medžiagos cheminei sudėčiai ir struktūrai tirti pagal jos jonų masės ir krūvio santykį (m/z)."
  - term: "Masių spektras"
    description: "Dviejų dimensijų grafikas, kuriame pavaizduotas santykinis jonų intensyvumas priklausomai nuo jų masės ir krūvio santykio (m/z)."
---

## Įvadas

Masių spektrometrija yra vienas iš svarbiausių šiuolaikinių analizinių metodų, leidžiantis nustatyti junginių molekulinę masę, struktūrą bei kiekybinę sudėtį su itin aukštu jautrumu. Šiame kurse susipažinsite su pagrindiniais masių spektro principais, jonizacijos būdais, analizatoriais bei duomenų apdorojimo metodais.

## Matavimo principas

![Masių spekro gavimas](/content/img/lecture1/gen_mass_spectrum.png)

Masių spektro matavimas yra procesas, kurio metu tiriamos medžiagos neutralios molekulės paverčiamos dujinės fazės jonais, atskiriamos pagal jų masės ir krūvio santykį (m/z) ir užregistruojamos detektoriumi. 

Šį matavimo kelią sudaro penki nuoseklūs etapai:


#### 1. Mėginio įvedimas
Pirmasis žingsnis – analitės įvedimas į prietaisą. Mėginys gali būti dujinės, skystos arba kietos agregatinės būsenos. Priklausomai nuo mėginio sudėtingumo ir fizinių savybių, taikomi šie įvedimo būdai:
- Tiesioginis įvedimas
- Dujų chromatografija (DCh-MS)
- Skysčių chromatografija (ESCh-MS)


#### 2. Jonizacija
Masių spektrometras elektriniais ir magnetiniais laukais geba valdyti ir registruoti tik elektringąsias daleles, todėl neutralias molekules būtina paversti jonais. Pagrindiniai jonizacijos metodai skirstomi į dvi kategorijas:
##### Kietoji jonizacija
- **Elektronų jonizacija (EI – *Electron ionization*):** Garų fazės molekulės bombarduojamos didelės energijos elektronais (standartiškai 70 eV). Iš molekulės išmušamas elektronas, suformuojant nesuporuoto elektrono radikalą-katijoną – **molekulinį joną ($M^{\bullet+}$)**. Perteklinė energija sukelia kovalentinių ryšių trūkimą, sukurdama būdingus fragmentinius jonus („cheminį pirštų atspaudą“).

##### Švelnioji jonizacija
- **Cheminė jonizacija (CI – *Chemical Ionization*):** Naudojamos jonizuotos reagentinės dujos (metanas, izobutanas ar amonis). Vykstant dujų fazės jonų ir molekulių reakcijoms, protono pernaša sukuria pseudomolekulinį joną $[M+H]^+$.
- **Elektropurškimas (ESI – *Electrospray Ionization*):** Skystas bandinys purškiamas per kapiliarą esant aukštai įtampai (2–5 kV) atmosferos slėgyje. Susidaro smulkūs krūvį turintys lašeliai; tirpikliui garuojant, susidaro pseudomolekuliniai aduktai ($[M+H]^+$, $[M+Na]^+$, deprotonizuoti $[M-H]^-$ arba daugakrūviai jonai $[M+zH]^{z+}$). Tai pagrindinis metodas biomolekulėms ir baltymams tirti
- **Matricos lazerinė desorbcija/jonizacija (MALDI):** Mėginys sumaišomas su kietąja matrica ir apšvitinamas lazerio impulsu, išmetant jonizuotas stambias molekules su maža fragmentacija.


#### 3. Jonų atskyrimas vakuume (*Mass Analyzer*)
Visi jonų atskyrimo procesai vyksta esant **aukštam vakuumui** ($10^{-5} - 10^{-8}$ Torr), kad jonai laisvai judėtų nesusidurdami su liekamosiomis oro molekulėmis. Pagrindinės analizatorių architektūros:

| Analizatoriaus tipas | Fizikinis atskyrimo principas | Pagrindinės savybės |
| :--- | :--- | :--- |
| **Kvadrupolis (Quadrupole, Q)** | Keturi lygiagretūs strypai su kintamosios (RF) ir nuolatinės (DC) srovės įtampomis. Rezonansinė trajektorija leidžia praeiti tik konkretaus $m/z$ jonams. | Greitas, kompaktiškas, puikiai tinka kiekybinei analizei (SIM režimas). |
| **Lėkio laiko (TOF – *Time-of-Flight*)** | Jonams suteikiama vienoda kinetinė energija ($qV = \frac{1}{2}mv^2$). Skriejimo laikas vakuuminiame vamzdyje proporcingas $\sqrt{m/z}$. | Neribotas teorinis masių rėžis, didelis skenavimo greitis, didelė skiriamoji geba. |
| **Jonų gaudyklė (Ion Trap, IT)** | Jonai sugaunami ir kaupiami trimatėje arba tiesinėje (LIT) erdvėje, po to selektyviai išstumiami link detektoriaus. | Leidžia atlikti daugiapakopę $MS^n$ analizę toje pačioje erdvėje laiko atžvilgiu (*tandem-in-time*). |
| **Orbitrap / FT-ICR** | Jonai sugaunami elektrostatiniais ar magnetiniais laukais, kur jie periodiškai osciliuoja. Virpesių dažnis paverčiamas spektru Furjė transformacija. | Ypatingai didelė skiriamoji geba (HRAM) ir tikslumas (< 1–5 ppm). |
| **Tandeminės sistemos (MS/MS, pvz., QqQ, Q-TOF)** | Pirmuoju analizatoriumi išskiriamas prekursoriaus jonas, susidūrimo celėje (*collision cell*) fragmentuojamas inertinėmis dujomis (CID), o fragmentai atskiriami antruoju analizatoriumi. | Struktūros patvirtinimas, izomerų atskyrimas, didelis atrankumas. |


#### 4. Detekcija (*Ion Detection*)
Pasiekę detektorių, atskirti jonai registruojami:
- **Elektronų daugintuvai (*Electron Multipliers*) ir mikrokanalų plokštelės (MCP):** Į detektoriaus paviršių pataikęs jonas išmuša antrinius elektronus, kurie sukelia grandininę stiprinimo kaskadą.
- **Indukcinės srovės detekcija (FT-ICR, Orbitrap):** Jonai fiziškai nesunaikinami – registruojama jų sukeliama atvaizdo srovė detektoriaus elektroduose.
Išmatuotas elektrinis signalas (srovė arba įtampa) yra tiesiogiai proporcingas užregistruotų jonų skaičiui.

---


## Masių spektras

### Profilio ir Centruotas spektro formatai

![Masių spektras: A - profilio formate, B - centruotame formate](/content/img/lecture1/profile_to_centroid.png)

Teoriškai kiekvienas unikalios cheminės sudėties ir krūvio jonas turėtų pasižymėti viena diskrečia $m/z$ verte. Tačiau realioje eksperimentinėje aplinkoje to paties $m/z$ jonai detektorių pasiekia ne vienu be galo siauru tašku ar akimirka, o su tam tikru erdviniu ir laiko pasiskirstymu:

1. **Pradinės kinetinės energijos sklaida:** Jonizacijos šaltinyje (pvz., EI, ESI, MALDI) susidarę jonai įgyja nedidelį kinetinių energijų pasiskirstymą, todėl greitintuve ir analizatoriuje jų greičiai nežymiai skiriasi.
2. **Erdvinė trajektorijų dispersija:** Skriedami per analizatorių (pvz., kvadrupolio strypus ar TOF lėkio vamzdį), jonai patiria minimalių trajektorijos nuokrypių dėl netolygių laukų kraštų bei mikroskopinių liekamųjų dujų susidūrimų.
3. **Detektoriaus atsako laikas:** Detektoriui (elektronų daugintuvui ar mikrokanalų plokštelei) registruojant jonų smūgius, antrinių elektronų kaskados sukelia baigtinio laiko trukmės elektros impulsą.

Dėl šių veiksnių kiekviena analitės jonų grupė suformuoja ne nulinio pločio liniją, o varpo formos (dažniausiai Gauso arba Lorentzo) fizinį smailės kontūrą.


#### 1. Analoginio signalo skaitmenizavimas ir diskretizavimo dažnis

Detektoriaus registruojama jonų srovė yra tolydus analoginis signalas. Tam, kad šis signalas būtų perkeltas į kompiuterinę sistemą, naudojamas analoginis-skaitmeninis keitiklis (ADC):

* **Tankus diskretizavimas (Sampling intervals):** Kiekvienas nominalus masės vienetas padalijamas į dešimtis ar šimtus matavimo intervalų.
* **Momentinio intensyvumo registravimas:** Kiekviename intervale išmatuojamas momentinis elektros srovės stipris.
* **Tolydžios kreivės atkūrimas:** Sujungus šiuos tankius matavimo taškus išilgai $m/z$ ašies, suformuojamas ištisinis profilio signalas (*continuous waveform*).


#### 2. Profilio ir Centruoto duomenų formatų palyginimas

Masių spektrometrijos duomenys gali būti saugomi ir interpretuojami dviem pagrindiniais režimais:

| Parametras | Profilio formatas (*Profile Data*) | Centruotas formatas (*Centroid Data*) |
| :--- | :--- | :--- |
| **Fizinė struktūra** | Ištisinė banguota kreivė (*waveform*) su daugybe matavimo taškų | Atskiri vertikalūs stulpeliai (nulinio pločio linijos) |
| **$m/z$ reikšmės** | Tolydus taškų rinkinys per visą smailės plotį | Viena diskreti reikšmė smailės masės centre |
| **Intensyvumo reikšmė** | Momentinis signalo stiprumas kiekviename taške | Integruotas smailės plotas arba viršūnės (*apex*) aukštis |
| **Smailės forma ir plotis** | Išsaugoma visa informacija apie FWHM ir asimetriją | Informacija apie smailės formą prarandama |
| **Duomenų apimtis** | Labai didelė (užima daug disko vietos ir atminties) | ~10 kartų mažesnė nei profilio |
| **Pirminė paskirtis** | Prietaiso diagnostika, skiriamosios gebos vertinimas, sudėtingų biomolekulių dekonvoliucija | Greita duomenų bazių paieška, metabolomikos funkcijų išskyrimas |


#### 3. Kodėl spektrometrai išlaiko profilio režimą

Nors profilio duomenų failai yra dideli, profilio formatas yra būtinas dėl kelių esminių priežasčių:

##### A. Skiriamosios gebos (Resolving Power) modeliavimas
Tikrame profilio spektre galima tiksliai išmatuoti smailės plotį pusėje jos aukščio (**FWHM** – *Full Width at Half Maximum*) bei 10 % nusileidimo slėnį ($R_{10\%}$). Tai leidžia tiesiogiai įvertinti spektrometro atskyrimo kokybę $R = \frac{m/z}{\Delta(m/z)}$.

##### B. Persiklojančių smailių atpažinimas (Peak Overlap)
Jei du izobariniai jonai ar aduktai turi labai artimas $m/z$ vertes, kurios nėra visiškai atskirtos, profilio spektre matomas charakteringas smailės asimetriškumas, dviguba viršūnė ar „petys“. Centravimo algoritmas tokį signalą gali klaidingai sujungti į vieną bendrą stulpelį, prarandant informaciją apie antrąjį komponentą.

##### C. Didelių biomolekulių analizė
Analizuojant intaktinius baltymus ar oligonukleotidus su didelėmis krūvio būsenomis (pvz., $[M+20H]^{20+}$), atstumai tarp izotopologų $m/z$ ašyje tampa itin maži ($\Delta(m/z) \approx 0.05$). Profilio režimas leidžia tiksliai sumodeliuoti izotopinį pasiskirstymą ir atlikti patikimą dekonvoliuciją.


#### 4. Centravimo procesas (Centroiding)

Kadangi didelės raiškos spektrometrijos (HRMS) duomenų srautai ilgų chromatografinių analizių (LC-MS) metu tampa sunkiai valdomi, duomenų apdorojimo sistema profilio kreivę paverčia centruotu spektru:
1. **Triukšmo filtravimas:** atmetami signalai, nesiekiantys nustatyto fono slenksčio.
2. **Smailės ribų nustatymas:** nustatomi pradžios ir pabaigos taškai išilgai $m/z$ ašies.
3. **Masės centro radimas:** apskaičiuojamas intensyvumu pasvertas centras (*center of mass*), kuris tampa fiksuota $m/z$ koordinate.
4. **Intensyvumo priskyrimas:** stulpeliui priskiriamas integruotas smailės plotas arba viršūnės intensyvumas.

### MS ir MSⁿ spektrai

Masių spektrometrijoje analitės identifikavimas ir struktūrinis charakterizavimas remiasi jonų elgsenos tyrimu vakuume. Pagal matavimo etapų skaičių ir atliekamas manipuliacijas su jonais masių spektrai skirstomi į **vienos pakopos (MS arba MS¹)** ir **daugiapakopius (MSⁿ, kur n ≥ 2)** spektrus.


| Parametras | MS (MS¹) spektras | MSⁿ (MS², MS³, …) spektras |
| :--- | :--- | :--- |
| **Apibrėžimas** | Vienkartinio matavimo rezultatas, gautas naudojant vieną masių analizatorių. | Kelių nuoseklių atrankos, fragmentacijos ir detekcijos etapų rezultatas. |
| **Registruojami jonai** | Intaktiniai prekursoriai, pseudomolekuliniai jonai (aduktai: $[M+H]^+$, $[M-H]^-$) arba pirminiai jonizacijos metu susidarę jonai. | Produktų (fragmentų) jonai, susidarę kontroliuojamai suardžius atrinktą pirmtaką. |
| **Informacijos pobūdis** | Molekulinė masė, izotopinis pasiskirstymas, bendras mėginio profilis. | Kovalentinių jungčių junglumas, funkcinės grupės, sekvenavimo informacija, izomerų atskyrimas. |
| **Aparatinis reikalavimas** | Vienas masių analizatorius (pvz., paprastas kvadrupolis, TOF). | Keli analizatoriai iš eilės (*Tandem-in-Space*) arba jonų gaudyklė (*Tandem-in-Time*). |


#### MS (MS¹) spektras: Vieno etapo analizė

Vienos pakopos eksperimente (**MS¹**) mėginio molekulės jonizuojamos jonų šaltinyje (pvz., ESI, EI, MALDI), nukreipiamos į masių analizatorių, išskiriamos pagal masės ir krūvio santykį ($m/z$) ir tiesiogiai registruojamos detektoriuje.

* **Paskirtis:** Nustatyti nepažeistų molekulių masę, įvertinti elementinę formulę pagal tiksliąją masę bei analizuoti izotopinį profilį.
* **Apribojimai:** MS¹ spektras negali atskirti struktūrinių izomerų (junginių, turinčių identišką formulę ir masę, bet skirtingą atomų išsidėstymą) bei neleidžia vienareikšmiškai nustatyti kovalentinių ryšių sekos sudėtingose biomolekulėse.


#### 3. MS² (MS/MS) ir MSⁿ: Daugiapakopė tandeminė analizė

Tandeminė masių spektrometrija įveda papildomus atrankos ir cheminio sužadinimo etapus.

#### Nuoseklus MSⁿ ciklas:
1. **Atranka (Selection, MS¹):** Analizatorius izoliuoja tik vieną dominantį joną (**prekursorių / pirmtaką**, *precursor ion*), turintį specifinį $m/z$, o visi kiti jonai pašalinami.
2. **Fragmentacija (Fragmentation):** Atrinktas jonas nukreipiamas į susidūrimų gardelę arba sužadinamas gaudyklėje, kur dėl susidūrimų su inertinėmis dujomis (CID – *Collision-Induced Dissociation*, HCD) kovalentinės jungtys suyra ir susidaro **produktų (fragmentų) jonai**.
3. **Analizė (Detection, MS²):** Antrasis analizatorius išskiria susidariusius fragmentus pagal $m/z$, suformuodamas **MS² spektrą**.
4. **Rekursyvus tęsinys (MS³ → MSⁿ):** Jei atliekamas MSⁿ tyrimas, vienas iš MS² spektre stebimų fragmentų vėl izoliuojamas ir pakartotinai fragmentuojamas. Šis ciklas gali būti kartojamas keletą kartų ($n = 3, 4, \dots$).

---

## Chemininės formulės nustatymas

Masių spektrometrijoje **MS1 (pirmosios pakopos masių spektras)** yra pradinis ir pamatinis matavimas. Šiame spektre registruojami visi jonų šaltinyje suformuoti dujinės fazės jonai, išskirti pagal jų masės ir krūvio santykį ($m/z$), neatliekant atrankinės jų fragmentacijos susidūrimų gardelėje.

Šioje ataskaitoje pateikiama susisteminta informacija, kurią galima išgauti iš MS1 spektro, išskiriant žemos ir aukštos skiriamosios gebos bei masių tikslumo matavimus ir daugiakrūvių jonų matematinį apdorojimą.


### Žemos skiriamosios gebos bei masių tikslumo spektrometrija

Žemos skiriamosios gebos prietaisai (pvz., vienetinio atskyrimo kvadrupoliai, paprastos jonų gaudyklės), kurių skiriamoji geba siekia vienetinį masės vienetą ($\Delta m \approx 1\text{ Da}$), o matavimo paklaida yra dešimtosiose daltono dalyse, teikia esminę informaciją apie junginį, remiantis nominaliosiomis masėmis ir klasikinėmis empirinėmis taisyklėmis.

#### Nominali jono masė ir adukto nustatymas, kai žinoma cheminio junginio formulė
* **Nominalioji masė ($M$):** Tai neutralios molekulės masė, apskaičiuojama sudedant labiausiai gamtoje paplitusių stabilių izotopų sveikuosius masės skaičius ($^{1}\text{H} = 1$, $^{12}\text{C} = 12$, $^{14}\text{N} = 14$, $^{16}\text{O} = 16$, $^{31}\text{P} = 31$, $^{32}\text{S} = 32$).
* **Molekulinis jonas ($M^{\bullet+}$):** 
  * Taikant kietąją jonizaciją (elektronų smūgį, EI), neutrali molekulė netenka vieno elektrono: $M + e^- \rightarrow M^{\bullet+} + 2e^-$.
  * Kadangi elektrono masė yra nykstamai maža, vienakrūvio molekulinio jono registruojamas $m/z$ tiesiogiai atitinka junginio nominaliąją masę ($m/z = M$).
* **Pseudomolekuliniai aduktai (švelnioji jonizacija, pvz., ESI):**
  Molekulės jonizuojamos prisijungiant arba prarandant krūvio nešiklius:
  * **Teigiamų jonų režimas (*Positive mode*):**
    * Protonizuota molekulė: $[M+H]^+ \implies m/z = M + 1$
    * Natrio aduktas: $[M+Na]^+ \implies m/z = M + 23$
    * Kalio aduktas: $[M+K]^+ \implies m/z = M + 39$
    * Amonio aduktas: $[M+NH_4]^+ \implies m/z = M + 18$
  * **Neigiamų jonų režimas (*Negative mode*):**
    * Deprotonizuota molekulė: $[M-H]^- \implies m/z = M - 1$
    * Formiato aduktas: $[M+HCOO]^- \implies m/z = M + 45$
    * Acetato aduktas: $[M+CH_3COO]^- \implies m/z = M + 59$
    * Chloro aduktas: $[M+Cl]^- \implies m/z = M + 35$ / $M + 37$
* **Aduktų atpažinimas:** Žinant būdingus masės poslinkius (pvz., $\Delta(m/z) = 22$ tarp $[M+H]^+$ ir $[M+Na]^+$, arba $\Delta(m/z) = 16$ tarp $[M+Na]^+$ ir $[M+K]^+$), galima vienareikšmiškai patvirtinti, kuris signalas priklauso konkrečiam aduktui, ir apskaičiuoti pradinės neutralios molekulės nominaliąją masę.

### Izotomomerai ir izotopologai

-------

#### Izotoplogai

**Izotopologai** (angl. *isotopic homologues*) – tai molekulės arba jonai, kurie viena nuo kitos skiriasi **tik savo izotopine sudėtimi** (t. y. tam tikrų izotopų skaičiumi molekulėje).

* **Pavyzdžiai:**
  * Metano izotopologai: $\text{CH}_4$, $\text{CH}_3\text{D}$, $\text{CH}_2\text{D}_2$, $\text{CHD}_3$, $\text{CD}_4$ arba $^{12}\text{CH}_4$ ir $^{13}\text{CH}_4$.
  * Vandens izotopologai: $\text{H}_2^{16}\text{O}$, $\text{H}_2^{18}\text{O}$, $\text{HD}^{16}\text{O}$, $\text{D}_2^{16}\text{O}$.
* **Fizikinės ir cheminės savybės:**
  * Izotopologai turi **skirtingą molekulinę masę** (tiek nominaliąją, tiek tiksliąją).
  * Masės skirtumas atsiranda dėl papildomų arba trūkstamų neutronų branduolyje.


#### Izotopomerai

**Izotopomerai** (angl. *isotopic isomers*) – tai molekulės, kurios turi **lygiai tą patį kiekvieno izotopo atomų skaičių**, tačiau skiriasi **šių izotopų padėtimi (lokalizacija) molekulės struktūroje**.

Izotopomerai skirstomi į dvi pagrindines grupes:
1. **Konstituciniai (padėties) izotopomerai:** Izotopas yra prisijungęs prie skirtingų anglies atomų ar funkcinių grupių:
   * 1-deuteropropanas ($\text{CH}_3\text{--CH}_2\text{--CH}_2\text{D}$) ir 2-deuteropropanas ($\text{CH}_3\text{--CHD--CH}_3$).
   * Deiteruotas etanolis: $\text{CH}_2\text{D--CH}_2\text{OH}$ ir $\text{CH}_3\text{--CH}_2\text{OD}$.
2. **Izotopiniai stereoizomerai (enantiomerai / diastereomerai):** Izotopinis pakeitimas sukuria chiralumo centrą:
   * $(R)\text{-CH}_3\text{CHDOH}$ ir $(S)\text{-CH}_3\text{CHDOH}$.
   * $(Z)\text{-CH}_3\text{CH=CHD}$ ir $(E)\text{-CH}_3\text{CH=CHD}$.

* **Fizikinės ir cheminės savybės:**
  * Izotopomerai turi **visiškai identišką suminę elementinę ir izotopinę formulę**.
  * Jų **molekulinė masė yra absoliučiai vienoda** (tiek nominalioji, tiek tikslioji, suderinta iki begalybės po kablelio).

------

| Kriterijus | Izotopologai (*Isotopologues*) | Izotopomerai (*Isotopomers*) |
| :--- | :--- | :--- |
| **Kas skiriasi molekulėje?** | Izotopų skaičius ir sudėtis formulėje | Izotopų padėtis (topologija) molekulėje |
| **Molekulinė formulė** | Skiriasi (pvz., $\text{C}_3\text{H}_8$ vs $\text{C}_3\text{H}_7\text{D}$) | Identiška (abi molekulės yra $\text{C}_3\text{H}_7\text{D}$) |
| **Tikslioji masė ($m/z$)** | **Skirtinga** ($\Delta m \approx 1,003\text{ Da}$) | **Identiška** ($\Delta m = 0,00000\text{ Da}$) |
| **Atskyrimas MS1 spektre** | **Taip**, matomos atskiros smailės ($M, M+1, M+2\dots$) | **Ne**, sutampa toje pačioje smailėje |
| **Reikalingas HRAM prietaisas?** | Dažnai pakanka net žemos skiriamosios gebos | Neišsprendžiama net su FT-ICR (21 Tesla) |
| **Atskyrimo metodas** | Tiesioginė MS1 registracija | Tandeminė MS/MS (CID) arba BMR spektroskopija |

Vienos pakopos masių spektrometrijoje (MS1) jonai atskiriami griežtai pagal jų masės ir krūvio santykį ($m/z$):
* **Izotopologai** turi skirtingą neutronų skaičių, todėl jų $m/z$ vertės skiriasi. Pavyzdžiui, tiriant benzeną, $^{12}\text{C}_6\text{H}_6$ ($m/z = 78,0469$) ir $^{13}\text{C}_1^{12}\text{C}_5\text{H}_6$ ($m/z = 79,0503$) yra aiškiai atskiriamos smailės.
* **Izotopomerai**, turėdami tą patį protonų, neutronų ir elektronų skaičių, turi identišką branduolių ryšio energiją ir masės defektą. Todėl 1-deuteropropano ir 2-deuteropropano jonai analizatoriaus elektriniuose ar magnetiniuose laukuose elgiasi visiškai vienodai. 

Norint nustatyti, kurioje molekulės vietoje yra sunkusis izotopas, **būtina kovalentiškai suardyti molekulę** ir nustatyti susidariusių fragmentų mases. Būtent tai atlieka tandeminė masių spektrometrija (MS/MS).




#### X+1 bei X+2 izotopai bei su jais susijusios smailės
Gamtoje elementai egzistuoja kaip stabilių izotopų mišiniai, todėl kiekvienas jonas MS1 spektre suformuoja izotopinį klasterį:
* **Monoizotopinė smailė ($M$):** Sudaryta tik iš pačių lengviausių ir labiausiai paplitusių izotopų ($^{12}\text{C}$, $^{1}\text{H}$, $^{14}\text{N}$, $^{16}\text{O}$, $^{32}\text{S}$).
* **X+1 elementai ir $M+1$ smailė:**
  * Elementai, turintys pastebimą vienu neutronu sunkesnio izotopo dalį: $^{13}\text{C}$ (1,1 %), $^{15}\text{N}$ (0,37 %).
  * $M+1$ smailės intensyvumas (procentais, kai $M = 100\text{ \%}$) nusakomas formule:
    $$\%[M+1] \approx (1,1 \times n_C) + (0,37 \times n_N) + (0,04 \times n_O) + (5,1 \times n_{Si}) + (0,78 \times n_S)$$
* **X+2 elementai ir $M+2$ smailė:**
  * Elementai, turintys ryškią dviem neutronais sunkesnio izotopo dalį: $^{18}\text{O}$ (0,20 %), $^{29}\text{Si} \rightarrow ^{30}\text{Si}$ (3,3 %), $^{34}\text{S}$ (4,4 %), $^{37}\text{Cl}$ (32,5 %), $^{81}\text{Br}$ (98,0 %).
  * Būdingi $M$ ir $M+2$ santykiai leidžia iš karto atpažinti heteroatomus:
    * **Chloras (Cl):** $M : M+2 \approx 3 : 1$ (apie 33 % $M+2$ aukščio).
    * **Bromas (Br):** $M : M+2 \approx 1 : 1$ (lygaus intensyvumo smailės).
    * **Siera (S):** pastebima apie 4,4 % $M+2$ smailė.
  * $M+2$ intensyvumo teorinė išraiška:
    $$\%[M+2] \approx \frac{(1,1 \times n_C)^2}{200} + (0,2 \times n_O) + (4,4 \times n_S) + (32,5 \times n_{Cl}) + (98,0 \times n_{Br})$$

#### Anglies kiekio nustatymas jone
Kadangi organiniuose junginiuose anglis sudaro molekulės karkasą, o $^{13}\text{C}$ gamtinis paplitimas yra pastovus (apie 1,1 %), $M+1$ smailės santykinis intensyvumas yra tiesioginis anglies skaitiklis:
* **Anglies atomų skaičiaus ($n_C$) formulė:**
  $$n_C \approx \frac{\%[M+1]}{1,1\text{ \%} \times \%[M]}$$
  *(Jei bazinė monoizotopinė smailė $M$ normalizuota į 100 %, formulė suprastėja iki $n_C \approx \frac{\%[M+1]}{1,1}$)*.
* **Pavyzdys:** Jei $M$ intensyvumas yra 100 %, o $M+1$ intensyvumas yra 8,8 %, junginyje yra apytiksliai $8,8 / 1,1 = 8$ anglies atomai.

### Azoto taisyklė (*Nitrogen Rule*) EI ir ESI atvejams
Azoto taisyklė remiasi faktu, kad azoto atomas pasižymi unikaliu deriniu: lyginis nominalus masės skaičius (14 Da) ir nelyginis kovalentinis valentingumas (3 jungtys).
* **EI atvejis (nesuporuoto elektrono jonai-radikalai, $M^{\bullet+}$):**
  Kadangi jonizacijos metu kovalentinės jungtys nesusidaro ir nenutrūksta:
  * **Nelyginis $m/z$** $\implies$ junginyje yra **nelyginis azoto atomų skaičius** (1, 3, 5...).
  * **Lyginis $m/z$** $\implies$ junginyje azoto **nėra arba yra lyginis azoto atomų skaičius** (0, 2, 4...).
* **ESI atvejis (suporuoto elektrono aduktai, pvz., $[M+H]^+$, $[M-H]^-$):**
  Kadangi formuojant arba nutraukiant vieną kovalentinę jungtį prisijungia arba pasišalina protonas ($+1$ arba $-1\text{ Da}$), **taisyklė apverčiama**:
  * **Lyginis $[M+H]^+$ ar $[M-H]^-$** $\implies$ neutralioje molekulėje yra **nelyginis azoto atomų skaičius**.
  * **Nelyginis $[M+H]^+$ ar $[M-H]^-$** $\implies$ neutralioje molekulėje azoto **nėra arba yra lyginis skaičius**.
  * *Pastaba:* Jei jungiasi azoto turintis aduktas (pvz., $[M+NH_4]^+$), bendras azoto skaičius komplekse pasipildo vienu vienetu, kas atitinkamai pakoreguoja galutinę pariteto taisyklę.

---

### Aukštos skiriamosios gebos bei masių matavimo tikslumo spektrai (HRAM)

Didelės skiriamosios gebos prietaisai (TOF, Orbitrap, FT-ICR) leidžia pereiti nuo nominaliųjų masių prie fizikinių atomų masių matavimo tūkstantųjų ar dešimttūkstantųjų daltono dalių tikslumu.

#### Tikslios eksperimentinės masės (*Accurate Mass*) ir tikslios teorinės masės (*Exact Mass*) sąvokos
* **Tiksli teorinė masė (*Exact Mass*):** Tai matematiškai apskaičiuota jono masė, gaunama sudedant konkrečių izotopų tikslias mases (kartu su masės defektu) ir atsižvelgiant į prarasto ar prisijungusio elektrono masę ($m_e \approx 0,0005486\text{ Da}$).
* **Tiksli eksperimentinė masė (*Accurate Mass*):** Tai eksperimentiniu būdu didelės skiriamosios gebos masių spektrometru išmatuota jono masės vertė.

#### Masių matavimo paklaidos vertinimas
Matavimo tikslumas nusakomas eksperimentinės ir teorinės masės skirtumu. Dažniausiai naudojami du rodikliai:
* **Santykinė paklaida milijoninėmis dalimis (ppm):**
  $$\Delta m\text{ (ppm)} = \frac{m_{\text{eksperimentinė}} - m_{\text{teorinė}}}{m_{\text{teorinė}}} \times 10^6$$
* **Absoliuti paklaida milidaltonais (mDa):**
  $$\Delta m\text{ (mDa)} = (m_{\text{eksperimentinė}} - m_{\text{teorinė}}) \times 1000$$
* **HRAM reikalavimai:** Kad spektrometrą būtų galima laikyti didelio tikslumo prietaisu, masės paklaida metabolitų identifikavimui paprastai turi būti **$< 5\text{ ppm}$** (arba $< 1-2\text{ mDa}$ mažos masės jonams).

#### Masės defektas (*Mass Defect*)
* **Apibrėžimas:** Tai skirtumas tarp tiksliosios izotopo/molekulės masės ir artimiausio sveikojo skaičiaus (nominaliosios masės):
  $$\text{Masės defektas} = \text{Tiksli masė} - \text{Nominali masė}$$
* **Fizikinė kilmė:** Remiantis Einšteino formule $E = mc^2$, protonams ir neutronams susijungiant į atomo branduolį, dalis masės virsta branduolio ryšio energija. Dėl to atomų masės nėra griežtai sveikieji skaičiai:
  * $^{1}\text{H} = 1,007825\text{ Da}$ (teigiamas masės defektas $+0,0078$)
  * $^{12}\text{C} = 12,000000\text{ Da}$ (atskaitos taškas, defektas $0,0000$)
  * $^{16}\text{O} = 15,994915\text{ Da}$ (neigiamas masės defektas $-0,0051$)
* **Analitinė reikšmė:** Masės defektas leidžia atskirti izobarus (pvz., $\text{CO}$, $\text{N}_2$ ir $\text{C}_2\text{H}_4$, kurių nominali masė 28 Da, bet tikslios masės atitinkamai 27,9949 Da, 28,0062 Da ir 28,0312 Da).

#### Cheminės formulės nustatymas ir priklausomybė nuo masės matavimo paklaidos (tikslumo)
Kombinatorikos požiūriu, didėjant molekulinei masei, galimų atomų kombinacijų skaičius auga eksponentiškai. Matavimo tikslumas tiesiogiai riboja šią paieškos erdvę:
* **Matavimo tikslumo įtaka:**
  * Jei masei $m/z \approx 272$ matavimo paklaida yra **1000 ppm**, algoritmai randa **> 7000 galimų formulių**.
  * Sumažinus paklaidą iki **5 ppm**, galimų formulių skaičius susitraukia iki keliolikos.
  * Pasiekus **1 ppm**, dažnai lieka tik viena arba kelios chemiškai pagrįstos formulės.
* **Filtravimo taisyklės:** Kartu su tikslia mase taikomos papildomos taisyklės (azoto taisyklė, nesočiųjų jungčių skaičius DBE, atomų santykiai H/C, izotopų klasterio profilio sutapimas), leidžiančios vienareikšmiškai nustatyti teisingą elementinę formulę.

---

### Daugiakrūviai jonai bei neutralios molekulės masės skaičiavimas

Biomolekulės (baltymai, peptidai, oligonukleotidai) elektropurkštuko (ESI) šaltinyje prijungia arba atiduoda daug protonų, todėl spektre registruojami daugiakrūviai jonai $[M+zH]^{z+}$ arba $[M-zH]^{z-}$.

#### Kai gaunamas izotopinis atskyrimas (*Isotopically Resolved*)
Jei prietaiso skiriamoji geba yra pakankamai didelė, kiekviena jono smailė išsiskleidžia į atskirus izotopologus:
* **Jono krūvio ($z$) nustatymas:**
  Kadangi gretimi izotopologai skiriasi vienu neutronu ($\Delta m \approx 1,00335\text{ Da}$), atstumas tarp gretimų izotopinių smailių spektro $m/z$ ašyje yra:
  $$\Delta(m/z) = \frac{1,00335}{z} \implies z = \text{round}\left(\frac{1,00335}{\Delta(m/z)}\right)$$
  * Pavyzdžiai:
    * Jei $\Delta(m/z) \approx 1,00 \implies z = 1$
    * Jei $\Delta(m/z) \approx 0,50 \implies z = 2$
    * Jei $\Delta(m/z) \approx 0,33 \implies z = 3$
    * Jei $\Delta(m/z) \approx 0,20 \implies z = 5$
    
* **Neutralios molekulės tikslios masės ($M$) apskaičiavimas:**
  Nustačius krūvį $z$ ir išmatavus monoizotopinės smailės $(m/z)_{\text{mono}}$ vertę:
  $$M = z \times (m/z)_{\text{mono}} - z \times m_{\text{protono}}$$
  *(kur $m_{\text{protono}} \approx 1,007276\text{ Da}$)*.
* **Monoizotopinės smailės iššūkis ir „Averžino“ (*Averagine*) modelis:**
  Didelėse biomolekulėse ($> 10\text{ kDa}$) monoizotopinė smailė dėl statistinio $^{13}\text{C}$ pasiskirstymo būna per silpna arba pasislepia triukšme. Todėl naudojamas **Averžino modelis** – hipotetinė vidutinė aminorūgštis ($C_{4,938}H_{7,758}N_{1,358}O_{1,477}S_{0,042}$, masė $\approx 111,1\text{ Da}$). Pagal išmatuotą masę sugeneruojamas teorinis izotopų vokas, kuris matematiškai priderinamas prie eksperimentinio signalo, taip nustatant teorinės monoizotopinės smailės vietą.

#### Kai izotopinis atskyrimas negaunamas (*Unresolved Envelope*)
Esant žemesnei skiriamajai gebai arba tiriant labai didelius baltymus, stebimi lygūs gaubtiniai daugiakrūviai signalai, atspindintys **vidutinę molekulinę masę (*Average Mass*)**.
* **Lygčių sistema gretimoms smailėms:**
  Pasirenkamos dvi gretimos to paties baltymo smailės:
  * Didesnės $m/z$ vertės smailė $x$, turinti mažesnį krūvį $z$.
  * Mažesnės $m/z$ vertės smailė $y$, turinti didesnį krūvį $z+1$.
  
  Jų ryšys su mase (teigiamų jonų ESI):
  $$x = \frac{M + z \cdot m_H}{z}, \quad y = \frac{M + (z + 1) \cdot m_H}{z + 1}$$
* **Krūvio ($z$) apskaičiavimas:**
  $$z = \frac{y - m_H}{x - y} \approx \frac{y - 1}{x - y}$$
  *(Gauta $z$ vertė suapvalinama iki artimiausio sveikojo skaičiaus)*.
* **Neutralios molekulės masės ($M$) apskaičiavimas:**
  $$M = z \times (x - m_H) = (z + 1) \times (y - m_H)$$
* **Rezultatų tobulinimas:** Praktikoje apskaičiuojamos $M$ vertės visoms spektre matomoms poroms ir išvedamas svertinis vidurkis arba atliekama kompiuterinė matematinė dekonvoliucija (*deconvolution*), pateikianti vieną aiškią neutralaus baltymo masės smailę.

---

### Apibendrinamoji parametrų palyginimo lentelė

| Analizės aspektas | Žema skiriamoji geba (Nominali) | Didelė skiriamoji geba (HRAM) |
| :--- | :--- | :--- |
| **Pirminis masės matas** | Sveikieji skaičiai ($m/z \pm 0,5\text{ Da}$) | Tikslus skaičius ($m/z$ iki 4–5 ženklų po kablelio) |
| **Tikslumo išraiška** | Dešimtosios daltono dalys | $\le 5\text{ ppm}$ arba $< 1\text{ mDa}$ |
| **Izotopinė informacija** | Bendras $M+1, M+2$ santykis | Smulkioji izotopų struktūra ($^{13}\text{C}$ vs $^{15}\text{N}$) |
| **Formulės nustatymas** | Spėjama pagal azoto ir 13-os taisykles | Vienareikšmiškai apribojama pagal tikslią masę |
| **Izobarų skyra** | Neįmanoma (viena bendra smailė) | Pilnas atskyrimas pagal masės defektą |
| **Biomolekulių krūvis ($z$)** | Nustatomas tik iš gretimų smailių poros | Nustatomas tiesiogiai iš izotopinių smailių žingsnio |


## Pratimai ir užduotys

Šioje skiltyje pateikiamos teorinės užduotys, kurias turite išspręsti, kad pasitikrintumėte žinias.


::::exercise

### 1 Užduotis: Adukto nustatymas ir $m/z$ prognozavimas
Nesteroidinio vaisto nuo uždegimo **ibuprofeno** formulė yra $\text{C}_{13}\text{H}_{18}\text{O}_2$ (nominalioji molekulinė masė $M = 206{,}1307\text{ Da}$, tiksli monoizotopinė masė $M = 206{,}1307\text{ Da}$).
1. ESI(+) spektre stebima intensyvi smailė ties nominalia verte $m/z = 229$. Koks tai aduktas?
2. Kokios tiksliosios $m/z$ vertės reikėtų tikėtis ESI(−) spektre, jei susidaro deprotonizuotas jonas $[M-\text{H}]^-$? *(protono masė $m(\text{H}) = 1{,}0073\text{ Da}$)*.


:::solution
#### Sprendimas:
1. **Adukto nustatymas ESI(+):**
   * Masės poslinkis: $\Delta m = (m/z)_{\text{stebimas}} - M_{\text{nominali}} = 229 - 206 = 23\text{ Da}$.
   * Poslinkis $+23\text{ Da}$ teigiamų jonų režime būdingas natrio katijono prisijungimui ($^{23}\text{Na}^+$).
   * **Atsakymas:** Stebimas jonas yra natrio aduktas **$[M+\text{Na}]^+$**.

2. **ESI(−) deprotonizuoto jono $m/z$ skaičiavimas:**
   * Molekulė netenka vieno protono: $[M-\text{H}]^-$.
   * $(m/z)_{\text{teor}} = M_{\text{tiksli}} - m(\text{H}) = 206{,}1307 - 1{,}0073 = 205{,}1234$.
   * **Atsakymas:** Tikėtina smailė ESI(−) spektre bus ties **$m/z = 205{,}1234$**.
:::
::::


::::exercise

### 2 Užduotis: Adukto formulavimas ESI(+) režime nežinomam metabolitui
Tiriant kraujo plazmos mėginį ESI(+) režimu, esant tai pačiai sulaikymo trukmei chromatogramoje užregistruotos dvi susijusios smailės: $m/z = 181{,}0859$ ir $m/z = 203{,}0678$. 
Nustatykite:
1. Koks masės skirtumas skiria šias smailes ir kokius aduktus jos atitinka?
2. Kokia yra neutralios molekulės tikslioji masė?

:::solution
#### Sprendimas:
1. **Smailių skirtumas:**
   * $\Delta(m/z) = 203{,}0678 - 181{,}0859 = 21{,}9819\text{ Da}$.
   * Žinome, kad skirtumas tarp protonizuoto $[M+\text{H}]^+$ ir natrio adukto $[M+\text{Na}]^+$ yra:
     $$m(\text{Na}) - m(\text{H}) = 22{,}9898 - 1{,}0073 = 21{,}9825\text{ Da}$$
   * Vadinasi, $m/z = 181{,}0859$ atitinka **$[M+\text{H}]^+$**, o $m/z = 203{,}0678$ atitinka **$[M+\text{Na}]^+$**.
2. **Neutralios molekulės masė:**
   * $M = (m/z)_{[M+\text{H}]^+} - m(H^+) = 181{,}0859 - 1{,}0073 = 180{,}0786\text{ Da}$ (atitinka heksozę / gliukozę $\text{C}_6\text{H}_{12}\text{O}_6$).
   * **Atsakymas:** Neutralios molekulės tikslioji masė yra **$180{,}0786\text{ Da}$**.
:::
::::

::::exercise
### 3 Užduotis: Halogenų (Cl, Br) ir sieros atpažinimas pagal $M+2$ smailę
EI-MS spektre stebimas molekulinis jonas $M^{\bullet+}$ su būdingu izotopiniu klasteriu:
* $m/z = 112$ ($I = 100\,\%$)
* $m/z = 113$ ($I = 6{,}8\,\%$)
* $m/z = 114$ ($I = 32{,}5\,\%$)

1. Koks heteroatomas lemia smailės $m/z = 114$ intensyvumą?
2. Koks būtų santykinis $M+2$ smailės intensyvumas, jei junginyje vietoj šio elemento būtų:
   * a) Vienas bromo atomas?
   * b) Vienas sieros atomas?
:::solution
#### Sprendimas:
1. **Elemento nustatymas:**
   * Smailė $m/z = 114$ yra $M+2$ smailė. Jos intensyvumas yra $32{,}5\,\%$ bazinės smailės $M$ (100 %) atžvilgiu.
   * Šis santykis ($\approx 3:1$) yra unikalus **chlorui** ($^{35}\text{Cl} \approx 75{,}8\,\%$, $^{37}\text{Cl} \approx 24{,}2\,\%$, todėl $^{37}\text{Cl}/^{35}\text{Cl} \approx 32{,}5\,\%$).
   * **Atsakymas:** Junginyje yra **vienas chloras (Cl)** (tiriamas junginys – chlorbenzenas, $\text{C}_6\text{H}_5\text{Cl}$).

2. **Palyginimas su kitais elementais:**
   * **a) Bromas ($\text{Br}$):** $^{79}\text{Br}$ ir $^{81}\text{Br}$ paplitimas gamtoje beveik vienodas ($1:1$). Jei junginyje būtų 1 Br atomas, $M+2$ smailės intensyvumas būtų **$\approx 97 - 98\,\%$** bazinės smailės aukščio.
   * **b) Siera ($\text{S}$):** $^{34}\text{S}$ natūralus paplitimas yra apie $4{,}4\,\%$. Jei junginyje būtų tik 1 S atomas (be kitų X+2 elementų), $M+2$ smailės intensyvumas siektų vos **$\approx 4{,}4\,\%$**.

:::
::::

::::exercise
### 4 Užduotis: Polihalogenintų junginių klasterio prognozavimas
Pesticido fungicido dichlorano formulėje yra du chloro atomai ($\text{Cl}_2$). 
Apskaičiuokite teorinį izotopinį smailių $M$, $M+2$ ir $M+4$ intensyvumo santykį, atsižvelgiant į tai, kad chloro izotopų santykis $^{35}\text{Cl} : ^{37}\text{Cl} \approx 3 : 1$.
:::solution
#### Sprendimas:
* Taikome binominį skaidinį $(a + b)^n$, kur $n = 2$ (chloro atomų skaičius), $a = 3$ ($^{35}\text{Cl}$), $b = 1$ ($^{37}\text{Cl}$):
  $$(3 + 1)^2 = 3^2 + 2 \cdot (3 \cdot 1) + 1^2 = 9 : 6 : 1$$
* Čia:
  * $M$ (abu $^{35}\text{Cl}$): dalis lygi $9$.
  * $M+2$ (vienas $^{35}\text{Cl}$ ir vienas $^{37}\text{Cl}$): dalis lygi $6$.
  * $M+4$ (abu $^{37}\text{Cl}$): dalis lygi $1$.
* Normalizuojant $M = 100\,\%$:
  * $M = 100\,\%$
  * $M+2 = \frac{6}{9} \times 100\,\% = 66{,}7\,\%$
  * $M+4 = \frac{1}{9} \times 100\,\% = 11{,}1\,\%$
* **Atsakymas:** Santykis yra **$9 : 6 : 1$** (arba $100\,\% : 66{,}7\,\% : 11{,}1\,\%$).
:::
::::

::::exercise
### 5 Uždavinys: Anglies atomų skaičiaus ($n_C$) nustatymas ir pagrindinė izotopinė smailė
1. Nežinomo organinio junginio MS spektre matoma molekulinė smailė $M$ ties $m/z = 180$ ($I = 100\,\%$) ir $M+1$ smailė ties $m/z = 181$ ($I = 12{,}3\,\%$). Nustatykite anglies atomų skaičių molekulėje $\pm 1$ atomo tikslumu.
2. Tiriamas sintetinis polimerinis oligopeptidas, kurio formulėje yra **$n_C = 110$** anglies atomų. 
   * Apskaičiuokite teorinį $M+1$ smailės intensyvumą lyginant su monoizotopine smaile $M$ ($I_M = 100\,\%$).
   * Kuri smailė ($M$ ar $M+1$) spektre bus intensyvesnė?

:::solution
#### Sprendimas:
1. **Anglies kiekio nustatymas:**
   * Žinoma formulė: $n_C \approx \frac{\%[M+1]}{1{,}1\,\% \cdot \%[M]} \times 100\,\%$.
   * $n_C \approx \frac{12{,}3}{1{,}1} \approx 11{,}18 \approx 11$.
   * **Atsakymas:** Molekulėje yra **11 anglies atomų** ($\pm 1$).

2. **Didelės biomolekulės ($n_C = 110$) analizė:**
   * Tikėtinas $M+1$ intensyvumas:
     $$I_{M+1} \approx n_C \times 1{,}1\,\% \times I_M = 110 \times 1{,}1\,\% \times 100\,\% = 121\,\%$$
   * **Atsakymas:** $M+1$ smailės intensyvumas sieks **$121\,\%$** monoizotopinės smailės aukščio. Tai reiškia, kad **$M+1$ smailė bus intensyvesnė už monoizotopinę smailę $M$**, todėl bazinė smailė šiame izotopiniame voke pasislenka į dešinę.

:::
::::

::::exercise
### 6 Užduotis: Masės paklaidos (ppm) skaičiavimas
Atliekama dopingo kontrolė. Šlapimo mėginyje įtariamas stimuliatorius **amfetaminas** ($\text{C}_9\text{H}_{13}\text{N}$).
* Teorinė protonizuoto jono $[M+\text{H}]^+$ tikslioji masė: **$136{,}1121\text{ Da}$**.
* HRAM spektrometre užregistruota eksperimentinė smailė ties **$m/z = 136{,}1127$**.
1. Apskaičiuokite masės matavimo paklaidą milijoninėmis dalimis (ppm).
2. Įvertinkite, ar prietaiso matavimas tenkina griežtą didelio tikslumo (HRAM) kriterijų ($\le 5\text{ ppm}$).
:::solution
#### Sprendimas:
1. **PPM skaičiavimas:**
   $$\text{Paklaida (ppm)} = \frac{|m_{\text{eksp}} - m_{\text{teor}}|}{m_{\text{teor}}} \times 10^6$$
   $$\text{Paklaida (ppm)} = \frac{|136{,}1127 - 136{,}1121|}{136{,}1121} \times 10^6 = \frac{0{,}0006}{136{,}1121} \times 10^6 \approx 4{,}41\text{ ppm}$$

2. **Vertinimas:**
   * Gauta paklaida yra **$4{,}41\text{ ppm}$**.
   * Kadangi $4{,}41\text{ ppm} < 5{,}0\text{ ppm}$, matavimas tenkina standartinį HRAM identifikavimo kriterijų.
   * **Atsakymas:** Paklaida yra **$4{,}41\text{ ppm}$**; smailė patikimai gali būti siejama su amfetamino formule.
:::
::::


::::exercise
### 7 Užduotis: Azoto taisyklė EI ir ESI spektrometrijoje
1. Nežinomo analito EI-MS spektre molekulinis jonas $M^{\bullet+}$ registruojamas ties $m/z = 195$. Ką azoto taisyklė sako apie azoto atomų skaičių?
2. Kitas analitas tiriamas ESI(+) režimu. Jo protonizuotas jonas $[M+\text{H}]^+$ registruojamas ties nominalia verte $m/z = 285$. Kiek azoto atomų (lyginį ar nelyginį skaičių) turi neutrali molekulė?

:::solution
#### Sprendimas:
1. **EI-MS atvejis ($M^{\bullet+}$):**
   * EI sukuria radikalą-katijoną be atomų pridėties ar netekties. Jo nominalioji masė tiesiogiai lygi neutralios molekulės masei: $M = 195\text{ Da}$.
   * Kadangi masė yra **nelyginis skaičius (195)**, pagal azoto taisyklę molekulėje privalo būti **nelyginis azoto atomų skaičius (1, 3, 5...)**.
2. **ESI(+) atvejis ($[M+\text{H}]^+$):**
   * ESI suformuoja suporuoto elektrono joną pridedant protoną ($\text{H}^+$, masė 1).
   * Neutralios molekulės nominali masė: $M = [M+\text{H}]^+ - 1 = 285 - 1 = 284\text{ Da}$.
   * Kadangi neutralios molekulės nominalioji masė yra **lyginis skaičius (284)**, molekulėje yra **0 arba lyginis azoto atomų skaičius (0, 2, 4...)**.

:::
::::

::::exercise
### 8 Uždavinys: Izobarinių vaistinių junginių identifikavimas (Nominali masė 151)
Teismo ekspertizės laboratorija tiria nežinomus miltelius. ESI(+) HRAM spektrometrija parodė intensyvų signalą:
* **Eksperimentinė tikslioji masė:** $m/z = 152{,}0706$
* **Izotopinis pasiskirstymas:**
  * $m/z = 152{,}07$ ($I = 100\,\%$)
  * $m/z = 153{,}07$ ($I = 9{,}0\,\%$)
  * $m/z = 154{,}07$ ($I = 0{,}6\,\%$)

Duotos trys izobarinės kandidatinės formulės (visų neutralių molekulių nominali masė $M = 151\text{ Da}$, protonuoto jono nominali masė $m/z = 152$):
* **Kandidatas A (Paracetamolis):** $\text{C}_8\text{H}_9\text{NO}_2$ (teorinė $[M+\text{H}]^+ = 152{,}0706\text{ Da}$)
* **Kandidatas B (Izobarinis aminas):** $\text{C}_9\text{H}_{13}\text{NO}$ (teorinė $[M+\text{H}]^+ = 152{,}1070\text{ Da}$)
* **Kandidatas C (Dinitro junginys):** $\text{C}_7\text{H}_5\text{N}_2\text{O}_2$ (arba kitas lyginiu N skaičiumi pasižymintis junginys)

**Užduotis:**
1. Pritaikykite azoto taisyklę neutraliai molekulei ir nurodykite, ar ji atmeta kurį nors kandidatą.
2. Įvertinkite heteroatomų buvimą pagal $M+2$ smailę.
3. Pagal $M+1$ smailės intensyvumą apskaičiuokite anglies atomų skaičių.
4. Apskaičiuokite masės matavimo paklaidą (ppm) kandidatams A ir B. Kuris junginys yra mėginyje?

:::solution

#### Sprendimas:
1. **Azoto taisyklė:**
   * $[M+\text{H}]^+ = 152$ (lyginis) $\implies$ neutralios molekulės nominali masė $M = 151$ (nelyginis).
   * Vadinasi, molekulėje privalo būti **nelyginis azoto atomų skaičius (1, 3...)**. Kandidatai A ir B (abu po 1 N) atitinka šią sąlygą, o dinitro junginys su 2 N atmetamas.
2. **$M+2$ smailės analizė:**
   * $M+2$ intensyvumas yra vos $0{,}6\,\%$.
   * Tai vienareikšmiškai atmeta halogenų ($\text{Cl} \sim 32\,\%$, $\text{Br} \sim 100\,\%$) bei sieros ($\text{S} \sim 4{,}4\,\%$) buvimą.
3. **Anglies kiekio nustatymas iš $M+1$:**
   * $n_C \approx \frac{\%[M+1]}{1{,}1\,\%} = \frac{9{,}0\,\%}{1{,}1\,\%} \approx 8{,}18 \approx 8\text{ atomai}$.
   * Paracetamolis turi **8 anglis** ($\text{C}_8$), o kandidatas B turi **9 anglis** ($\text{C}_9$, kuriam $M+1$ turėtų siekti $\approx 9{,}9 - 10\,\%$). Izotopų santykis rodo kandidatą A.
4. **Tiksliosios masės ir ppm paklaidos skaičiavimas:**
   * **Kandidatui A ($\text{C}_8\text{H}_{10}\text{NO}_2^+$):**
     $$\text{ppm} = \frac{|152{,}0706 - 152{,}0706|}{152{,}0706} \times 10^6 = \mathbf{0{,}0\text{ ppm}}$$
   * **Kandidatui B ($\text{C}_9\text{H}_{14}\text{NO}^+$):**
     $$\text{ppm} = \frac{|152{,}0706 - 152{,}1070|}{152{,}1070} \times 10^6 = \frac{0{,}0364}{152{,}1070} \times 10^6 \approx \mathbf{239\text{ ppm}}$$
* **Išvada:** Kandidato B paklaida yra nepriimtinai didelė ($239\text{ ppm} \gg 5\text{ ppm}$). Mėginyje vienareikšmiškai identifikuotas **Paracetamolis (Kandidatas A)**.

:::
::::


::::exercise

### 9 Užduotis: Žemės ūkio pesticidų (izobarinių junginių) atranka (Nominali masė 215)
**Sąlyga:**
Tiriant vandens telkinio taršą pesticidais, ESI(+) HRAM spektre gauti šie duomenys:
* **Eksperimentinė smailė:** $m/z = 216{,}1011$
* **Izotopinis profilis:**
  * $m/z = 216{,}10$ ($I = 100\,\%$)
  * $m/z = 217{,}10$ ($I = 9{,}5\,\%$)
  * $m/z = 218{,}10$ ($I = 32{,}8\,\%$)

Žinoma, kad regione naudojami pesticidai, kurių protonizuotų jonų nominali masė yra $m/z = 216$:
1. **Atrazinas:** $\text{C}_8\text{H}_{14}\text{ClN}_5$ (teorinė $[M+\text{H}]^+ = 216{,}1010\text{ Da}$)
2. **Junginys X :** $\text{C}_{10}\text{H}_{22}\text{N}_3\text{O}_2$ (teorinė $[M+\text{H}]^+ = 216{,}1707\text{ Da}$)
3. **Junginys Y :** $\text{C}_5\text{H}_{14}\text{NO}_4\text{PS}$ (teorinė $[M+\text{H}]^+ = 216{,}0454\text{ Da}$)

**Užduotis:**
1. Pagal $M+2$ smailės intensyvumą nustatykite, ar junginyje yra chloras, siera, ar halogenų nėra.
2. Apskaičiuokite azoto taisyklės reikalavimą neutraliai molekulei.
3. Apskaičiuokite stebimo jono ppm paklaidą Atrazinui ir kitiems kandidatams.
4. Padarykite galutinę išvadą.

:::solution
#### Sprendimas:
1. **$M+2$ smailės interpretavimas:**
   * $M+2$ smailės ($m/z = 218{,}10$) santykinis intensyvumas yra **$32{,}8\,\%$**.
   * Tai klasikinis vieno **chloro atomo ($^{37}\text{Cl}$)** požymis ($M : M+2 \approx 3:1$).
   * Tai iš karto atmeta Junginį X (be halogeno, $M+2 < 1\,\%$) ir Izobarą Y (turintį tik sierą, kurio $M+2 \approx 4{,}4\,\%$).
2. **Azoto taisyklė:**
   * $[M+\text{H}]^+ = 216$ (lyginis) $\implies$ neutrali molekulė $M = 215$ (nelyginis).
   * Reikalingas **nelyginis azoto atomų skaičius**. Atrazinas turi 5 azoto atomus ($N=5$, nelyginis) – taisyklė tenkinama.
3. **Anglies kiekio patikra ($M+1$):**
   * $n_C \approx \frac{9{,}5\,\%}{1{,}1\,\%} \approx 8{,}6 \approx 8 - 9$ atomai. Atrazinas turi 8 anglies atomus ($\text{C}_8$).
4. **Masės tikslumo (ppm) skaičiavimas:**
   * **Atrazinui ($\text{C}_8\text{H}_{15}\text{ClN}_5^+$):**
     $$\text{ppm} = \frac{|216{,}1011 - 216{,}1010|}{216{,}1010} \times 10^6 = \frac{0{,}0001}{216{,}1010} \times 10^6 \approx \mathbf{0{,}46\text{ ppm}}$$
   * **Junginiui  X:** paklaida siektų $\frac{|216{,}1011 - 216{,}1707|}{216{,}1707} \times 10^6 \approx 322\text{ ppm}$.
   * **Junginiui Y:** paklaida siektų $\frac{|216{,}1011 - 216{,}0454|}{216{,}0454} \times 10^6 \approx 258\text{ ppm}$.
* **Atsakymas:** Vandens mėginyje vienareikšmiškai patvirtintas herbicidas **Atrazinas** (paklaida vos $0{,}46\text{ ppm}$, idealus chloro izotopinis profilis).
:::
::::

::::exercise 
### 10 Užduotis: Vaistinių preparatų izobarų atranka (Nominali masė 284)
Klinikinės toksikologijos laboratorijoje tiriant apsinuodijusio paciento kraują, ESI(+) HRAM režimu gautas spektras su šiais parametrais:
* **Eksperimentinė smailė:** $m/z = 285{,}0789$
* **Izotopų santykiai:**
  * $m/z = 285{,}08$ ($I = 100\,\%$)
  * $m/z = 286{,}08$ ($I = 18{,}2\,\%$)
  * $m/z = 287{,}08$ ($I = 33{,}1\,\%$)
  * $m/z = 288{,}08$ ($I = 5{,}8\,\%$)

Duotos trys galimos junginių formulės (visų neutralių molekulių nominali masė $M = 284\text{ Da}$, o $[M+\text{H}]^+$ nominali masė $m/z = 285$):
* **Kandidatas 1 (Trankviliantas Diazepamas):** $\text{C}_{16}\text{H}_{13}\text{ClN}_2\text{O}$ (teorinė $[M+\text{H}]^+ = 285{,}0789\text{ Da}$)
* **Kandidatas 2 (Izobarinis steroidas / lipidinis darinys):** $\text{C}_{19}\text{H}_{24}\text{O}_2$ (teorinė $[M+\text{H}]^+ = 285{,}1849\text{ Da}$)
* **Kandidatas 3 (Vaistas su dviem sieros atomais):** $\text{C}_{12}\text{H}_{16}\text{N}_2\text{OS}_2$ (teorinė $[M+\text{H}]^+ = 285{,}0726\text{ Da}$)

**Užduotis:**
1. Įvertinkite azoto taisyklę: kiek azoto atomų turi turėti neutrali molekulė?
2. Nustatykite heteroatomo tipą pagal $M+2$ ($m/z = 287{,}08$) smailės intensyvumą.
3. Pagal $M+1$ smailės intensyvumą patvirtinkite anglies atomų skaičių.
4. Apskaičiuokite eksperimentinės masės paklaidą (ppm) visiems trims kandidatams ir nurodykite, kokia medžiaga sukėlė intoksikaciją.

:::solution
#### Sprendimas:
1. **Azoto taisyklė:**
   * $[M+\text{H}]^+ = 285$ (nelyginis skaičius).
   * Neutralios molekulės nominali masė $M = 284$ (lyginis skaičius).
   * Vadinasi, molekulė turi **0 arba lyginį azoto atomų skaičių (0, 2, 4...)**.
   * Diazepamas turi 2 N, Kandidatas 2 turi 0 N, Kandidatas 3 turi 2 N – visi trys kandidatai atitinka azoto taisyklę.
2. **$M+2$ smailės diagnostika:**
   * $M+2$ smailės intensyvumas siekia **$33{,}1\,\%$**.
   * Šis intensyvumas (apie $1/3$ nuo $M$) rodo **vieną chloro atomą ($\text{Cl}$)**.
   * Kandidatas 2 (be halogenų) turėtų $M+2 < 2\,\%$.
   * Kandidatas 3 turi du sieros atomus ($\text{S}_2$), todėl jo $M+2$ būtų apytiksliai $2 \times 4{,}4\,\% \approx 8{,}8\,\%$, o tai visiškai neatitinka stebimų $33{,}1\,\%$.
   * Heteroatomo profilis vienareikšmiškai rodo chloruotą junginį (Diazepamą).
3. **Anglies kiekio patvirtinimas iš $M+1$:**
   * $n_C \approx \frac{\%[M+1]}{1{,}1\,\%} = \frac{18{,}2\,\%}{1{,}1\,\%} \approx 16{,}5 \approx 16\text{ atomų}$.
   * Diazepamas turi lygiai **16 anglies atomų** ($\text{C}_{16}$).
4. **Tiksliosios masės ir ppm paklaidos:**
   * **Diazepamui ($\text{C}_{16}\text{H}_{14}\text{ClN}_2\text{O}^+$):**
     $$\text{ppm} = \frac{|285{,}0789 - 285{,}0789|}{285{,}0789} \times 10^6 = \mathbf{0{,}0\text{ ppm}}$$
   * **Kandidatui 2:**
     $$\text{ppm} = \frac{|285{,}0789 - 285{,}1849|}{285{,}1849} \times 10^6 = \frac{0{,}1060}{285{,}1849} \times 10^6 \approx \mathbf{371{,}7\text{ ppm}}$$
   * **Kandidatui 3:**
     $$\text{ppm} = \frac{|285{,}0789 - 285{,}0726|}{285{,}0726} \times 10^6 = \frac{0{,}0063}{285{,}0726} \times 10^6 \approx \mathbf{22{,}1\text{ ppm}}$$
* **Galutinis atsakymas:** Paciento kraujyje identifikuotas vaistas **Diazepamas** (paklaida $0{,}0\text{ ppm}$, atitinka $\text{C}_{16}$ anglies kiekis bei būdingas chloro izotopų profilis).
:::
::::
