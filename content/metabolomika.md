---
title: "Masių spektfrometrija metabolomo tyrimams"
---

## Įvadas

**Metabolomika** – tai funkcinės genomikos šaka, tirianti mažos molekulinės masės (paprastai < 1500 Da) junginius, vadinamus **metabolitais**. Masių spektrometrija (MS), sujungta su skysčių (LC-MS) arba dujų (GC-MS) chromatografija, yra pagrindinis šios srities analitinis įrankis dėl savo jautrumo, plataus dinaminio diapazono ir gebėjimo vienu metu registruoti tūkstančius cheminių junginių.


#### Metabolitų ir metabolomikos samprata

Metabolitai atspindi galutinius ląstelių biocheminių procesų, fermentinių reakcijų bei aplinkos veiksnių (mitybos, vaistų, mikrobiotos) sąveikos produktus. Skirtingai nuo genomo ar proteomo, kurie apibrėžia potencinius organizmo gebėjimus, **metabolomas suteikia momentinę esamos biologinės būsenos (fenotipo) „nuotrauką“**.

Kadangi metabolitai pasižymi išskirtine chemine įvairove – nuo stipriai polinių vandenyje tirpių aminorūgščių ir angliavandenių iki visiškai hidrofobinių lipidų, neegzistuoja vienas universalus analitinis metodas, galintis vienu metu išmatuoti visą metabolomą.


#### Pagrindinės metabolomikos šakos ir jų biologiniai tikslai

Atsižvelgiant į tiriamų molekulių klases ir sprendžiamus biologinius klausimus, metabolomika skirstoma į kelias specializuotas šakas:

##### 💡 Lipidomika
* **Tyrimo objektas**: Visapusiškas hidrofobinių molekulių – lipidų (triacilglicerolių, fosfolipidų, sfingolipidų, steroidų ir kt.) – profiliavimas.
* **Biologinis klausimas**: Kaip kinta ląstelių membranų struktūrinis vientisumas, signalų perdavimo takai bei energinis metabolizmas sergant širdies ir kraujagyslių ligomis, neurodegeneraciniais sutrikimais ar metaboliniu sindromu?

#####  🔄 Fluksomika (*Fluxomics*)
* **Tyrimo objektas**: Metabolitų srautų ir fermentinių reakcijų greičių (dinamikos) matavimas metaboliniuose takuose, naudojant stabiliųjų izotopų (pvz., $^{13}\text{C}$, $^{15}\text{N}$) žymiklius ir matematinį modeliavimą ($^{13}\text{C}$-MFA).
* **Biologinis klausimas**: Koks yra tikrasis metabolitų judėjimo greitis ir kryptis tirtame take (pvz., glikolizėje ar Krebso cikle) atsakant į genetinę mutaciją ar vaisto poveikį, nepriklausomai nuo statinės metabolitų koncentracijos?

##### 💨 Volatomika (*Volatilomics*)
* **Tyrimo objektas**: Lakiųjų organinių junginių (VOC) tyrimas, taikant mėginio viršerdvės (headspace) ekstrahavimą (HS-SPME, DHS) ir GC-MS analizę.
* **Biologinis klausimas**: Kokius specifinius lakiuosius biomarkerius išskiria biologinės terpės (iškvepiamas oras, seilės, šlapimas), leidžiančius neinvaziškai diagnozuoti plaučių ligas, gastrointestinalinius sutrikimus ar žarnyno mikrobiotos būklę?

#####  🥗 Nutrimetabolomika
* **Tyrimo objektas**: Maisto kilmės egzogeninių metabolitų (mitybos biomarkerių) ir endogeninio metabolinio atsako į mitybą vertinimas.
* **Biologinis klausimas**: Kaip tam tikri mitybos modeliai (pvz., Viduržemio jūros dieta) ar specifiniai maisto produktai veikia žmogaus metabolinį profilį, mitybos laikymąsi bei individualią ligų riziką?


#### Analitinės strategijos: Netikslinė vs. Tikslinė analizė

Masių spektrometrija metabolomikoje įgyvendinama taikant dvi pagrindines metodologines prieigas bei jų hibridinius variantus:

```mermaid
flowchart LR
    A[Metabolomikos analitinės strategijos] --> B[Pažinimo / Netikslinė analizė<br/>Untargeted / Discovery]
    A --> C[Tikslinė analizė<br/>Targeted]
    A --> D[Hibridiniai metodai<br/>SQUAD / Pseudo-targeted]

    B --> B1(Tikslas: Hipotezių kėlimas ir biomarkerų paieška)
    B --> B2(Atskyrimas: Šimtai–tūkstančiai m/z savybių)
    B --> B3(Įranga: HRMS Q-TOF, Orbitrap)
    B --> B4(Rezultatas: Santykiniai signalo intensyvumai)

    C --> C1(Tikslas: Hipotezių tikrinimas ir kiekybinis vertinimas)
    C --> C2(Atskyrimas: Apibrėžtas žinomų analičių sąrašas)
    C --> C3(Įranga: QqQ MRM arba HRMS PRM)
    C --> C4(Rezultatas: Absoliuti koncentracija ng/mL, µmol/L)

    D --> D1[/Apsijungia didelę netikslinės analizės aprėptį ir tikslinės analizės kvantifikavimą/]

    classDef strategy fill:#f3e5f5,stroke:#7b1fa2,stroke-width:2px,color:#000;
    classDef tikslas fill:#e1f5fe,stroke:#01579b,stroke-width:2px,color:#000;
    classDef atskyrimas fill:#e8f5e9,stroke:#2e7d32,stroke-width:2px,color:#000;
    classDef iranga fill:#fff3e0,stroke:#ef6c00,stroke-width:2px,color:#000;
    classDef rezultatas fill:#fce4ec,stroke:#c2185b,stroke-width:2px,color:#000;

    %% class A,B,C,D,D1 strategy;
    class B1,C1 tikslas;
    class B2,C2 atskyrimas;
    class B3,C3 iranga;
    class B4,C4,D1 rezultatas;
```

1. **Pažinimo / Netikslinė analizė (*Untargeted / Discovery*)**:
   * **Tikslas**: Išmatuoti kuo platesnį visų aptinkamų metabolitų spektrą be išankstinio šališkumo, siekiant iškelti naujas biologines hipotezes ir atrasti biomarkerius.
   * **Įranga**: Naudojami aukštos skiriamosios gebos ir masių tikslumo spektrometrai (HRMS: Q-TOF, Orbitrap) su DDA arba DIA fragmentavimo režimais.
2. **Tikslinė analizė (*Targeted*)**:
   * **Tikslas**: Tiksliai ir jautriai išmatuoti iš anksto apibrėžtą žinomų metabolitų rinkinį (pvz., konkretaus metabolinio tako junginius).
   * **Įranga**: Naudojami trigubi kvadrupeliai (QqQ) su daugialypės reakcijų stebėsenos (MRM/SRM) režimu arba HRMS su PRM režimu, taikant izotopais žymėtus vidinius standartus.
3. **Hibridiniai metodai (*SQUAD / Pseudo-targeted*)**:
   * Vieno įšvirkštimo metu sujungia netikslinės analizės plačią aprėptį su tiksliu žinomų taikinių kiekybiniu matavimu.


##### Matuojamojo dydžio (*Measurand*) sąvoka

Pagal Tarptautinį metrologijos žodyną (**VIM3**, 2.9 punktas), **matuojamasis dydis (*measurand*)** yra apibrėžiamas kaip *kiekis, kurį ketinama išmatuoti*. VIM3 aiškiai pabrėžia (Note 4), kad pati analitė (cheminės medžiagos pavadinimas) nėra matuojamasis dydis. Norint teisingai apibrėžti matuojamąjį dydį, būtina nurodyti matuojamo kiekio pobūdį, biologinę matricą (terpę) bei matavimo sąlygas:

* **Netikslinėje analizėje (*Untargeted*)**:
  * **Matuojamasis dydis** – tai *atsitiktinės chromatografinės-masių savybės (unique m/z, RT poros feature) jono signalo intensyvumas arba smailės plotas (santykinis kiekis)*, išmatuotas tam tikromis LC-HRMS sąlygomis tyrimo grupės mėginiuose, išreikštas santykiu su kontrole arba apjungtu kokybės kontrolės (Pooled QC) mėginiu. Tai yra **santykinis matavimas**, nesuteikiantis absoliučios molinės koncentracijos.
* **Tikslinėje analizėje (*Targeted*)**: 
  * **Matuojamasis dydis** – tai *konkrečios chemiškai identifikuotos medžiagos (pvz., L-triptofano) masės arba molinė koncentracija* (pvz., $\mu\text{mol/L}$ arba $\text{ng/mL}$) apibrėžtoje biologinėje matricoje (pvz., žmogaus kraujo plazmoje prie $-80^\circ\text{C}$ laikymo sąlygų), nustatyta naudojant atitinkamus grynumo kalibratorius bei izotopais žymėtus vidinius standartus.

## Netikslinė analizė

**Netikslinė metabolomika** – tai visapusiška ir neatrankinė maža molekulinė masė (< 1500 Da) pasižyminčių biologinių mėginių junginių (metabolitų ir lipidų) analizės strategija. Šio metodo tikslas – užregistruoti kuo platesnį visų biologinėje matricoje esančių cheminių savybių spektrą, palyginti jų santykines koncentracijas tarp skirtingų eksperimentinių grupių, iškelti naujas biologines hipotezes bei atrasti ligų ar būsenų biomarkerius.

Skysčių chromatografija, sujungta su aukštos skiriamosios gebos masių spektrometrija (LC-HRMS), yra pagrindinis šios srities analitinis įrankis. Masių spektrometrijos duomenų surinkimas ir tolesnis bioinformacinis duomenų apdorojimas (savybių išgavimas ir spektrinė dekonvolucija) sudaro esminį stuburą, lemiantį gautų rezultatų patikimumą, biologinę aprėptį ir spektro interpretaciją.


### DDA (Data-Dependent Acquisition) Duomenų Surinkimo Principas

**DDA (nuo duomenų priklausomas fragmentavimas)** – tai tradicinis ir plačiausiai taikomas tandeminės masių spektrometrijos (MS/MS) režimas. Šiuo režimu prietaiso valdymo sistema realiu laiku reaguoja į pirmojo lygio (MS1) spektre registruojamus signalus ir automatiškai priima sprendimus, kuriuos jonus atrinkti fragmentacijai.


DDA skenavimo ciklas sudarytas iš nuoseklių etapų, kurie cikliškai kartojami per visą chromatografinės analizės laiką:

1. **Pilnas MS1 skenas (MS1 Survey Scan):** Masių analizatorius (pavyzdžiui, „Orbitrap“ arba Q-TOF) permatuoja visą pasirinktą masės ir krūvio santykio ($m/z$) diapazoną (pavyzdžiui, 70–1000 $m/z$) ir sugeneruoja pirminį MS1 spektrą.
2. **Spektro analizė ir dinaminio atmetimo patikra:** Kiekviena spektre užregistruota smailė patikrinama ar yra dinaminio atmetimo sąraše (DEW, angl dinamic exclusion wondow). Jei smailė jau yra DEW, ji atmentama.
3. **Top-N atranka ir MS2 fragmentacija:** Iš likusių neatmestų smailių atrenkamas nustatytas skaičius $N$ intensyviausių jonų (pavyzdžiui, Top-5, Top-10 arba Top-20). Kavadrupolis (ar kitas tinkamas analizatorius) nuosekliai izoliuoja kiekvieną pasirinktą joną siaurame $m/z$ lange (paprastai 0.4–1.8 Da pločio), nukreipia jį į fragmentacijos kamerą (HCD arba CID), o sugeneruoti fragmentai užregistruojami MS2 skene.
4. **DEW sąrašo papildymas:** Sufragmentuoti Top-N jonai įtraukiami į dinaminio atmetimo sąrašą, kad kitų skenų metu prietaisas perjungtų dėmesį į mažesnio intensyvumo jonus.

```mermaid

flowchart TD
    A[MS1 skenas] --> B[MS1 spektras]
    B --> C[Kiekviena smailė / jonas]
    C --> D{Patikrinama, ar yra DEW<br/>dinaminio atmetimo sąraše?}
    D -- Taip (Sąraše) --> E[Smailė atmetama / neatsirenkama]
    D -- Ne (Nėra sąraše) --> F[Top-N intensyviausių jonų pasirinkimas]
    F --> G[Atrinktų jonų fragmentavimas MS2]
    G --> H[DEW papildymas fragmentuotais Top-N jonais]
    H --> A
    %%E --> A
```

Kadangi chromatografinė smailė trunka kelias sekundes, be papildomų apribojimų prietaisas nuolat fragmentuotų tik pačius intensyviausius jonus. Siekiant padidinti mažesnės koncentracijos metabolitų fragmentavimo tikimybę, taikomas **dinaminis atmetimas**: atlikus jono MS2 fragmentaciją, jo $m/z$ vertė tam tikram laikui (pavyzdžiui, 3–10 sekundžių, priklausomai nuo smailės pločio) įtraukiama į atmetimo sąrašą, priverčiant sistemą perjungti dėmesį į mažesnio intensyvumo jonus.

#### 1.3 DDA Privalumai ir Trūkumai

* **Privalumai:**
  * **Aukšta spektrų švara:** Siaura prekursoriaus izoliacija užtikrina, bei chromatografinis atskyrimas, kad MS2 spektre esantys fragmentai priklauso vienai konkrečiai molekulei.
  * **Tiesioginis spektrinių duomenų bazių palyginimas:** Švarūs MS2 spektrai gali būti iškart lyginami su standartinėmis spektrinėmis duomenų bazėmis (GNPS, METLIN, HMDB, NIST, mzCloud) netaikant sudėtingos dekonvolucijos.
* **Trūkumai:**
  * **Stochastinis pobūdis ir prastas atkuriamumas:** Dėl stochastinio (atsitiktinio) jonų atrankos proceso dviejose pakartotinėse to paties mėginio analizėse gali būti sufragmentuoti skirtingi mažesnio intensyvumo jonai.
  * **Ribota aprėptis:** DDA režimu sufragmentuojama mažiau nei 30–50 % visų aptiktų MS1 jonų (ypač kenčia mažos koncentracijos metabolitai).


### DIA (Data-Independent Acquisition) Duomenų Surinkimo Principas

**DIA (nuo duomenų nepriklausomas fragmentavimas)** – tai deterministinė duomenų surinkimo strategija, kurioje fragmentacija vykdoma pagal iš anksto griežtai nustatytą laiko ir $m/z$ langų tvarkaraštį, visiškai neatsižvelgiant į tai, kokie jonai tuo metu eliuuojasi iš chromatografins sistemos.

#### Veikimo mechanizmas: SWATH ir AIF

DIA pašalina prekursorių atrankos apribojimus fragmentuodama **visus** $m/z$ diapazone esančius jonus. Egzistuoja du pagrindiniai DIA įgyvendinimo būdai:

1. **AIF (All-Ion Fragmentation / $MS^E$):** Kvadrupolis (ar kitas tinkamas masių analizatorius) nefiltruoja jonų. Pakaitomis atliekamas MS1 skenas (nefragmentuoti jonai) ir MS2 skenas, kai į fragmentavimo kamerą yra pasiunčiami visi tuo metu besieliuuojantys jonai.
2. **SWATH-MS (Sequential Window Acquisition of All Theoretical Mass Spectra):** Visas $m/z$ diapazonas (pavyzdžiui, 100–900 $m/z$) padalinamas į nuoseklius izoliacijos langus (paprastai 5–25 $m/z$ pločio). Masių spektrometras cikliškai perbėga per visus langus, fragmentuodamas visus į konkretų langą patenkančius jonus. Po arba prieš kiekvieną ciklą padaromas papildomas MS1 skenas


```mermaid
flowchart TD
    A[Pasirinktas m/z diapazonas: 100–900 m/z] --> B0[MS1 skenas pasirinktam diapazone]
    A --> B[SWATH Langas 1: 100–125 m/z]
    A --> C[SWATH Langas 2: 125–150 m/z]
    A --> D[SWATH Langas N: ...–900 m/z]
    B --> B1[Fragmentuojami visi langui 1 priklausantys jonai]
    C --> C1[Fragmentuojami visi langui 2 priklausantys jonai]
    D --> D1[Fragmentuojami visi langui N priklausantys jonai]
```

Kadangi viename DIA izoliacijos lange vienu metu fragmentuojasi keli kartu eliuuojantys metabolitai, gaunami **chimeriniai (mišrūs) MS2 spektrai**. Norint susieti pradinį prekursoriaus joną su jo fragmentais, atliekama spektrinė dekonvolucija – ji remiasi chromatografinių smailių formos ir sulaikymo laiko sutapimo analize. Tipiškai gaunamų spektrų kompleksija auga, didinant izoliavimo langą.

#### DIA Privalumai ir Trūkumai

* **Privalumai:**
  * **100 % teorinė MS2 aprėptis:** Fragmentuojami absoliučiai visi jonai, patenkantys į matavimo langą.
  * **Aukštas atkuriamumas:** Ciklo tvarkaraštis yra fiksuotas, todėl tarp skirtingų mėginių ar partijų nelieka stochastinių paklaidų.
  * **Retrospektyvus duomenų gavimas:** Sugeneruojamas skaitmeninis mėginio žemėlapis, kurį galima peranalizuoti ateityje.
* **Trūkumai:**
  * **Sudėtingas duomenų apdorojimas:** Reikalingi skaičiuojamuoju požiūriu imlūs dekonvolucijos algoritmai.
  * **Triukšmas sudėtingose matricose:** Jei kartu eliuuojančių metabolitų skaičius lange yra itin didelis, dekonvolucijos kokybė krenta.


### DDA ir DIA Palyginamoji Analizė

| Parametras | DDA (Data-Dependent Acquisition) | DIA (Data-Independent Acquisition) |
| :--- | :--- | :--- |
| **MS2 fragmentacijos principas** | Izoliuojamas vienas Top-N intensyviausias jonas | Fragmentuojami visi jonai izoliacijos lange (5–25 Da) |
| **MS2 spektro švara** | Aukšta (grynasis individualaus jono spektras) | Chimerinis spektras (reikalinga dekonvolucija) |
| **MS2 fragmentacijos aprėptis** | Maža–vidutinė (riboja ciklo laikas ir intensyvumas) | 100 % teorinė aprėptis visame $m/z$ diapazone |
| **Atkuriamumas tarp mėginių** | Nuosaikus / Stochastinis (kinta atrenkami jonai) | Absoliutus / Deterministinis |
| **Duomenų apdorojimas** | Tiesioginis lygiavimas su spektrinėmis bibliotekomis | Imlus skaičiavimams (chromatografinė dekonvolucija) |
| **Kiekybinis įvertinimas** | Remiamasi MS1 pilno skenavimo smailėmis | Galima vertinti ir MS1, ir MS2 fragmentų smailėmis |



### Savybių (feature) ekstrakcija, Dekonvolucija ir Metabolitų Identifikavimas

Pirminiai masių spektrometrijos duomenys (pirminis failas) atvaizduoja tridimencinę erdvę: **masės ir krūvio santykį ($m/z$), sulaikymo laiką ($RT$) ir signalo intensyvumą**. Šio skyriaus tikslas – paaiškinti, kaip iš šios tridimencinės duomenų visumos išgaunamos savybės, kaip jos sugrupuojamos ir kaip **skirtingo lygio savybės (MS1 ir MS2)** padeda nuosekliai atpažinti bei identifikuoti biologinius metabolitus.

```mermaid
flowchart TD
    A[Pirminiai 3D duomenys: m/z, RT, intensyvumas] --> B[1. EIC išpjovimas siaurame m/z lange]
    B --> C[2. 2D smailės detekcija: Viršūnės RT ir ploto skaičiavimas]
    C --> D[3. Dekonvolucija: Chromatografinių profilių ir viršūnės RT sutapdinimas]
    D --> E[4. MS1 lygio savybės: Tiksli masė, izotopai, aduktai -> Cheminė formulė]
    E --> F[5. MS2 lygio savybės: Fragmentų spektrai -> Paieška duomenų bazėse]
    F --> G[Struktūriškai identifikuotas metabolitas]
```

#### Kas yra „Savybė“?

**Savybė (Feature)** – tai konkretaus jono (turinčio unikalų $m/z$) užregistruota chromatografinė smailė ties konkrečiu sulaikymo laiku ($RT$), apibrėžiama trimis pagrindinėmis reikšmėmis:
1. Vidutiniu $m/z$ santykiu (pavyzdžiui, $181.071 \text{ Da}$).
2. Sulaikymo laiku viršūnėje ($RT_{	\text{viršūnė}}$, pavyzdžiui, $2.45	\text{ min}$).
3. Integruotu smailės plotu, atspindinčiu santykinį kiekį mėginyje.

Svarbu pabrėžti, kad **savybė nėra pats metabolitas**. Kadangi viena molekulė jonizacijos metu sugeneruoja kelis skirtingus jonų signalus (izotopus, aduktus, šaltinio fragmentus), iš vieno metabolito susidaro kelios atskiros savybės.

Norint rasti savybę, taikomas **ekstrahuotos jonų chromatogramos (EIC)** principas: iš viso tridimencinio duomenų masyvo išpjaunamas labai siauras $m/z$ ruožas (pavyzdžiui, $\pm 5	\text{ ppm}$ arba $\pm 0.005 \text{ Da}$). Taip tridimenciniai duomenys paverčiami į paprastą dvidimencinę chromatogramą (Intensyvumas vs. Laikas).

```mermaid
flowchart TD
    subgraph EIC_Gavimo_Etapas [1. EIC išpjovimas iš tridimencinio masyvo]
        RAW[Pirminiai 3D masių duomenys] -->|Masių langas ± 5 ppm| EIC[2D chromatograma: Intensyvumas vs RT]
    end

    subgraph Detekcijos_Etapas [2. Smailės detekcija ir integravimas]
        EIC --> Apex[Viršūnės RT_viršūnė radimas]
        Apex --> Boundaries[Pradžios RT_pradžia ir pabaigos RT_pabaiga nustatymas]
        Boundaries --> Area[Smailės ploto integravimas]
    end

    Detekcijos_Etapas --> Result["Savybė: m/z 181.071, RT_viršūnė 2.45 min, Plotas 1,250,000"]
```

#### Dekonvolucijos Principas: Chromatografinio Profilio Sutapatinimas

**Problema:** Analizuojant sudėtingus biologinius mėginius (kraujo plazma, augalų ekstraktai), sutrasti chromatografines sąlygas, kai visi mėginio komponentai pilnai atsiskiria, yra neįmanoma. Dėl to kelios medžiagos patenka į masių spektrometrą vienu arba beveik vienu metu. Jei tokie junginiai patenka į tą patį fragmentavimo langą jų fragmentacijos spektrai susimaišo į vieną **chimerinį spektrą**. Kaip nustatoma, kurie fragmentai priklauso konkrečiam junginiui?

**Sprendimas (Dekonvolucijos principas):** 
Jei prekursoriaus jonas ir keli fragmentų jonai priklauso **tai pačiai fizinei molekulei**, jie iš chromatografinės kolonėlės eliuavosi kartu. Todėl jų ekstrahuotos jonų chromatogramos (EIC smailės) privalo tenkinti dvi sąlygas:
1. **Identiškas sulaikymo laikas viršūnėje ($RT_{\text{viršūnė}}$):** Prekursoriaus ir jo fragmentų smailių maksimumas būna tiksliai tą pačią sekundę.
2. **Identiška smailės forma (chromatografinio profilio koreliacija):** Didėjant ir mažėjant molekulės koncentracijai detektoriuje, prekursoriaus ir visų jo fragmentų signalai kyla ir krenta absoliučiai sinchroniškai (koreliacijos koeficientas $r > 0.90$).

Sulyginus EIC smailių formas, visi fragmentai, kurių smailės forma ar $RT_{\text{viršūnė}}$ nesutampa, atmetami kaip svetimas triukšmas. Taip iš chimerinio spektro išgryninamas **tikrasis molekulės MS2 spektras**.

```mermaid
flowchart TD
    subgraph Misinys [Chimerinis MS2 spektras ties RT = 3.20 min]
        P[Prekursorius P: m/z 300.12]
        F1[Fragmentas 1: m/z 150.06]
        F2[Fragmentas 2: m/z 180.08]
        F3[Triukšmas / Kitas junginys: m/z 210.04]
    end

    Misinys --> EIC_Patikra{EIC smailės formos ir viršūnės RT tikrinimas}

    EIC_Patikra -- "RT_viršūnė = 3.20 min ir formos koreliacija r > 0.95" --> Priklauso[Priklauso tai pačiai molekulei]
    EIC_Patikra -- "RT_viršūnė skiriasi arba formos koreliacija r < 0.50" --> Nepriklauso[Pašalinis triukšmas / Kito junginio fragmentas]

    Priklauso --> Grynas[Grynasis dekonvoliuotas MS2 spektras]
    Nepriklauso --> Atmetama[Pašalinama iš spektro]
```


### Metabolitų Atpažinimas pagal MS1 ir MS2 Lygio Savybes

Savybių išgavimo ir apdorojimo eigoje sugeneruota informacija yra padalinama į **dviejų lygmenų savybes (MS1 ir MS2)**. Šių skirtingų lygmenų duomenys atlieka skiriamąjį vaidmenį atpažįstant ir identifikuojant metabolitus.

```mermaid
flowchart TD
    subgraph MS1_Lygis [MS1 Lygio Savybės]
        M1[Tiksli masė m/z ± 5 ppm]
        M2[Izotopinis raštas M+1, M+2, santykiai]
        M3[Aduktų grupavimas M+H, M+Na, M+K]
        M1 --> MS1_Out[Apskaičiuojama neutrali masė ir Cheminė Formulė e.g. C6H12O6<br/>MSI 3 Lygis]
        M2 --> MS1_Out
        M3 --> MS1_Out
    end

    subgraph MS2_Lygis [MS2 Lygio Savybės]
        F1[Unikalus fragmentacijos spektras]
        F2[Būdingi produkto jonai ir neutralūs netekimai]
        F1 --> MS2_DB[Paieška spektrinėse duomenų bazėse<br/>GNPS, METLIN, HMDB, NIST]
        F2 --> MS2_DB
        F2 --> MS2_InSilico[In Silico fragmentacija<br/>SIRIUS, MetFrag]
        MS2_DB --> MS2_Out[Struktūrinis Metabolito Identifikavimas<br/>MSI 2 Lygis]
        MS2_InSilico --> MS2_Out
    end

    MS1_Out --> MS2_Lygis
```

#### MS1 Lygio Savybės: Neutralios Masės ir Cheminės Formulės Nustatymas

MS1 lygio savybės suteikia pradinę informaciją apie molekulės fizines ir chemines savybes tiriamoje biologinėje matricoje:

1. **Tiksli masė ($m/z$):** Aukštos skiriamosios gebos masių spektrometrija (HRMS) užtikrina masių tikslumą iki $\le 3–5	ext{ ppm}$. Tai leidžia siaurame masės lange ieškoti galimų cheminių junginių.
2. **Izotopinis raštas ($M+1$, $M+2$):** Natūralus $13\text{C}$, $15\text{N}$, $34\text{S}$ ar $37\text{Cl}$ izotopų paplitimas sugeneruoja unikalų izotopinių smailių aukščių santykį. Šio santykio palyginimas su teoriniu pasiskirstymu (pavyzdžiui, taikant Septynias Auksines Taisyklės – *Seven Golden Rules*) atmeta 90–95 % netinkamų elementų kombinacijų.
3. **Aduktų grupavimas:** Savybių sujungimas pagal atstumus ($\Delta m/z = +21.9820	\text{ Da}$ for $[M+Na]^+$, $+37.9558 \text{ Da}$ for $[M+K]^+$) leidžia tiksliai nustatyti **neutralios molekulės masę ($M$)**.

**Rezultatas (MSI 3 lygis):** MS1 lygio savybės leidžia patikimai nustatyti **bruto cheminę formulę** (pavyzdžiui, $\text{C}_6 \text{H}_{12} \text{O}_6$), tačiau negali vienareikšmiškai atskirti struktūrinių izomerų (pavyzdžiui, gliuokozės nuo fruktozės ar galaktozės). Tai atitinka Metabolomikos standartų iniciatyvos (**MSI – Metabolomics Standards Initiative**) **3 lygį (Level 3 – Putative compound class / Molecular formula)**.


#### MS2 Lygio Savybės: Spektrinė Paieška ir Struktūrinis Identifikavimas

Norint atskirti izomerus ir nustatyti tikslią cheminę struktūrą, būtina panaudoti MS2 lygio savybes:

1. **Paieška spektrinėse duomenų bazėse (Spectral Library Search):** Deconvolution būdu išvalytas arba DDA režimu užregistruotas grynasis MS2 spektras palyginamas su atvirųjų bei komercinių spektrinių duomenų bazių (**GNPS**, **METLIN**, **HMDB**, **MassBank**, **NIST**, **mzCloud**) įrašais. Palyginimui skaičiuojamas spektrinio panašumo įvertis (pavyzdžiui, kosinuso (cosine similarity) arba skaliarinės sandaugos (dot product) balai (tipiškai nuo 0 iki 1)).
2. **Būdingi fragmentai ir neutralūs netekimai:** Specifiniai produkto jonai (pavyzdžiui, $m/z\ 184.0733$ cholino fragmentui fosfolipiduose) arba neutralūs netekimai (pavyzdžiui, $-176.0321 \text{ Da}$ glukouronido konjugatams) patvirtina konkrečią metabolitų klasę.
3. ***In Silico* Fragmentacija:** Jei eksperimentinis MS2 spektras neturi tiesioginio atitikmens duomenų bazėse, naudojami bioinformaciniai įrankiai (**SIRIUS / CSI:FingerID**, **MetFrag**, **CFM-ID**). Šie algoritmai paima MS1 lygio sugeneruotą cheminę formulę, ištraukia visas galimas chemines struktūras iš cheminių duomenų bazių („PubChem“, „ChemSpider“) ir *in silico* būdu modeliuoja jų fragmentaciją, sulygindami su eksperimentiniu MS2 spektru.

**Rezultatas (MSI 2 lygis):** Kai eksperimentinis MS2 spektras sutampa su spektrinės duomenų bazės įrašu (kosinuso balas $> 0.80$), metabolitui suteikiamas **MSI 2 lygis (Level 2 – Putatively annotated compound)**.

*(Pastaba: Norint pasiekti aukščiausią **MSI 1 lygį – Confirmed compound**, būtina eksperimentiškai išmatuoti gryną autentišką standartą toje pačioje laboratorijoje, patvirtinant atitiktį pagal du nepriklausomus parametrus: $RT$ ir MS2 spektrą).*

## Tikslinė (Targeted metabolomika)

**Tikslinė metabolomika (Targeted Metabolomics)** – tai bioanalitinės chemijos šaka, skirta apibrėžto, biologinėje sistemoje žinomo metabolitų rinkinio atsekamam kiekybiniam įvertinimui. Metodologija grindžiama fiziniu-cheminiu analičių atskyrimu ir masių spektrometriniu registravimu, siekiant maksimalaus jautrumo, selektyvumo, tiesiškumo ir metrologinio atsekamumo.


### Instrumentinė Dalis ir Duomenų Surinkimo Fizika

####  Duomenų deterministiškumas kaip kiekybinės analizės sąlyga

Kiekybinės masių spektrometrijos analitinis signalas – analitės adukto (MS1 lygmenyje) arba būdingo fragmento jono (MS2 lygmenyje) **ekstrahuotos jonų chromatogramos (EIC / XIC)** plotas $A$, gautas integruojant signalo intensyvumą $I(t)$ chromatografinės zonos plotyje $[t_1, t_2]$:

$$A = \int_{t_1}^{t_2} I(t) \, dt \approx \sum_{k=1}^{M} I(t_k) \cdot \Delta t_k$$

Kad skaitmeninio integralo suma $\hat{A}$ atitiktų tikrąjį integralą $A$ be sisteminių ir atsitiktinių paklaidų, pirminiai masių spektrometrijos duomenys privalo tenkinti griežtą **duomenų surinkimo deterministiškumo** sąlygą:

1. **Pastovus matavimo laiko žingsnis (Deterministic Time Sampling):** Imčių ėmimo intervalas $\Delta t_k = t_k - t_{k-1}$ privalo būti fiksuotas arba tolygiai kintantis žinomoje laiko funkcijoje. Stochastiniai duomenų surinkimo režimai (pavyzdžiui, DDA), kuriuose MS1 ar MS2 nuskaitymai aktyvuojami atsitiktinai priklausomai nuo matricos intensyvumo, pažeidžia $\Delta t$ pastovumą, sukelia neapibrėžtą integravimo paklaidą ir yra netinkami kiekybinei analizei.
2. **Nekintanti m/z koordinatė ir izoliacijos langas:** Kiekvienas duomenų taškas $I(t_k)$ privalo būti užregistruotas tiksliai tame pačiame prekursoriaus bei produkto jono masės ir krūvio santykio ($m/z$) filtre.

Pagal Nyquist-Shannon atrankos teoremą ir chromatografinių smailių integravimo praktiką, patikimam smailės ploto ir viršūnės ($RT_{\text{viršūnė}}$) apskaičiavimui būtina užtikrinti **ne mažiau kaip 10–12 duomenų taškų ($M \ge 10\text{–}12$)** per chromatografinę smailę (matuojant smailės plotyje $W_{\text{peak}}$ ties $3.5\%$ smailės aukščio, t. y. $6\sigma$). Jei $M < 8$, smailės ploto integracijos variacijos koeficientas ($RSD$) negrįžtamai išauga.

#### Deterministiniai skenavimo režimai

Nurodytus kiekybinius reikalavimus užtikrina tik tie masių spektrometro darbo režimai, kuriuose perėjimų ir skenų seka vykdoma pagal deterministinį tvarkaraštį.

```mermaid
flowchart LR
    A[Deterministiniai Skenavimo Režimai Kiekybinei Analizei] --> B[Žemos Skyros Analizatoriai QqQ / QTRAP]
    A --> C[Aukštos Skyros Analizatoriai HRAM Q-TOF / Q-Orbitrap]

    B --> B1[SRM / MRM Režimas: Q1 prekursoriaus filtras -> Q2 CID -> Q3 fragmento filtras]
    B --> B2[Scheduled / Dynamic MRM: Perėjimų skenavimas tik aktyviame ΔtR lange]

    C --> C1[PRM Režimas: Prekursoriaus izoliacija -> CID/HCD -> HRAM visų fragmentų spektras]
    C --> C2[Targeted SIM / Full-Scan: Pilnas MS1 skenas su siauru ±5 ppm EIC langu]
    C --> C3[DIA / SWATH-MS: Deterministinis visų m/z langų skenavimas]
```

##### A. Žemos skiriamosios gebos analizatoriai (Trigubi Kvadrupeliai – QqQ, QTRAP)
* **Atsirinktų / Daugialypių Reakcijų Stebėsena (SRM):**
  * **Q1 (pirmasis kvadrupolis):** Veikia kaip siauras masių filtras (paprastai $\Delta m/z \approx 0.7\text{ Da}$, vienetinė skyra), praleidžiantis tik analitės prekursoriaus joną ($m/z_{\text{prec}}$).
  * **Q2 (susidūrimų kamera):** Pagreitinti prekursoriaus jonai sudraskomi susidūrimuose su inertinių dujų molekulėmis (CID – *Collision-Induced Dissociation*).
  * **Q3 (trečiasis kvadrupolis):** Filtruoja ir praleidžia tik vieną būdingą produkto (fragmento) joną ($m/z_{\text{prod}}$).
  * *Rezultatas:* Dviguba masių atranka ($m/z_{\text{prec}} \to m/z_{\text{prod}}$) eliminuoja cheminį foną ir užtikrina platų tiesinį dinaminį diapazoną ($10^4\text{–}10^5$).
* **Dinaminis / Tvarkaraštinis MRM (Dynamic SRM / Scheduled SRM – dSRM / sSRM):**
  * Kiekviena SRM reakcija skenuojama ne visą analizės laiką, o tik apibrėžtame laiko lange ($\Delta t_R$, pavyzdžiui, $1.0\text{ min}$) aplink žinomą metabolito sulaikymo trukmę. Tai užtikrina aukštą buvimo laiką (*dwell time*) net analizuojant šimtus analičių vienu matavimu.

##### B. Aukštos skiriamosios gebos analizatoriai (HRAM – Q-TOF, Q-Orbitrap)
* **Lygiagrečioji Reakcijų Stebėsena (PRM – Parallel Reaction Monitoring):**
  * Kvadrupolis (ar kitas tinkamas masių analizatorius) izoliuoja prekursorių, HCD/CID kameroje sugeneruojami fragmentai, o aukštos skyros masių analizatorius užregistruoja **visą produkto jonų spektrą** vienu metu su didele skiriamąja geba ($R \ge 17\,500\text{–}70\,000$) ir tikslios masės paklaida ($< 5\text{ ppm}$).
* **Targeted HRAM SIM / Full-Scan:**
  * Užregistruojami pilni MS1 spektrai. Kiekybinė EIC chromatograma iškerpama taikant itin siaurą masės tolerancijos langą (pavyzdžiui, $\pm 5\text{ ppm}$). Aukšta masių skyra atskiria analitės signalą nuo izobarinių matricos trukdžių be MS2 fragmentacijos.


#### Ciklo laikas (Duty Cycle / Cycle Time) ir Poisson triukšmo matematika

Kiekybinio matavimo ciklo laikas ($T_{\text{cycle}}$) – tai laiko tarpas, per kurį spektrometras atlieka vieną pilną aktyvių perėjimų seką:

$$T_{\text{cycle}} = \sum_{i=1}^{N} \left( t_{\text{dwell}, i} + t_{\text{interscan}} \right)$$

kur $N$ – tuo pačiu laiko momentu stebimų reakcijų skaičius, $t_{\text{dwell}}$ – jono signalo integravimo laikas detektoriuje (*dwell time*), o $t_{\text{interscan}}$ – vidinis masių analizatorių įtampos ir elektronikos persijungimo laikas ($1\text{–}5\text{ ms}$).

#### Optimalaus buvimo laiko ($t_{\text{dwell}}$) fizikinė kompromiso lygtis
Jono detekcija masių spektrometre paklūsta **Poisson skirsiniui**. Užregistruoto signalo $I$ (užregistruotų jonų skaičiaus, *counts*) santykinis standartinis nuokrypis (triukšmo lygis) yra atvirkščiai proporcingas užregistruotų jonų skaičiaus kvadratinei šakniai:

$$\frac{\sigma_I}{I} = \frac{1}{\sqrt{I_{\text{jonų}}}} = \frac{1}{\sqrt{J_{\text{jonų}} \cdot t_{\text{dwell}}}}$$

kur $J_{\text{jonų}}$ – jonų srauto intensyvumas ($\text{jonai/s}$).

1. **Jei $t_{\text{dwell}}$ per trumpas ($< 2\text{–}5\text{ ms}$):** Registruojamas jonų skaičius $I_{\text{jonų}}$ yra mažas, todėl Poisson triukšmas $\frac{\sigma_I}{I}$ drastiškai padidėja, o signalo ir triukšmo santykis krenta ($\frac{S}{N} \propto \sqrt{t_{\text{dwell}}}$).
2. **Jei $t_{\text{dwell}}$ per ilgas:** Ciklo laikas $T_{\text{cycle}}$ viršija leistiną ribą, todėl taškų skaičius per smailę $M = \frac{W_{\text{peak}}}{T_{\text{cycle}}}$ nukrenta žemiau 10 taškų, deformuodamas smailės integravimo kontūrą.

*Išvada:* Ciklo laikas kontroliuojamas taikant dinaminį langų skirstymą (dMRM) ir adaptyvųjį buvimo laiką (*adaptive dwell time*), išlaikant $M \ge 12$ bei $t_{\text{dwell}} \ge 10\text{ ms}$.


### Diagnostinių Jonų Chemija ir Spektrinis Identifikavimas

#### Diagnostinio jono sąvoka ir informacinė vertė

**Diagnostinis jonas** – tai specifinis MS1 (prekursorius, aduktas, izotopologas) arba MS2 (produkto fragmentas, neutralus netekimas) jonas, pasižymintis aukštu masių spektriniu selektyvumu ir tiesiogine struktūrine priklausomybe nuo analitės cheminės formulės bei fragmentacijos mechanizmo.

Diagnostinio jono atranka remiasi dviem kriterijais:
1. **Struktūrinis specifiškumas:** Fragmentas atspindi būdingą cheminį karkasą (pavyzdžiui, aminorūgštims būdingą karboksi grupės netekimą ar fosfolipidų cholino fragmentą $m/z \ 184.074$).
2. **Spektrinis selektyvumas ($S/N$):** Jonas neturi sutapti su matricos fono fragmentais.


#### Diagnostiniai jonai daugiamatėje erdvėje ir Kosinuso Panašumo Rodiklis

Kai atliekama analizė PRM arba Full-Scan HRMS režimais, analitės spektrinė tapatybė vertinama lyginant eksperimentinį fragmentacijos spektrą su etaloninės duomenų bazės spektru, arba laboratorijoje gautu etaloninės medžiagos spektru.

Eksperimentinis ir etaloninis spektrai išreiškiami kaip $N$-mačiai intensyvumų vektoriai diagnostinių jonų $m/z$ erdvėje:

$$\mathbf{I}_{\text{exp}} = \begin{pmatrix} i_{1, \text{exp}} \\ i_{2, \text{exp}} \\ \vdots \\ i_{N, \text{exp}} \end{pmatrix}, \quad \mathbf{I}_{\text{ref}} = \begin{pmatrix} i_{1, \text{ref}} \\ i_{2, \text{ref}} \\ \vdots \\ i_{N, \text{ref}} \end{pmatrix}$$

**Kosinuso panašumo rodiklis ($S_{\text{cosine}}$)** apskaičiuojamas kaip kampo $\theta$ kosinusas tarp šių dviejų vektorių:

$$S_{\text{cosine}} = \cos(\theta) = \frac{\mathbf{I}_{\text{exp}} \cdot \mathbf{I}_{\text{ref}}}{\|\mathbf{I}_{\text{exp}}\| \|\mathbf{I}_{\text{ref}}\|} = \frac{\sum_{k=1}^{N} i_{k, \text{exp}} \cdot i_{k, \text{ref}}}{\sqrt{\sum_{k=1}^{N} i_{k, \text{exp}}^2} \cdot \sqrt{\sum_{k=1}^{N} i_{k, \text{ref}}^2}}$$

```mermaid
flowchart TD
    A[Diagnostiniai Jonai: m/z_1, m/z_2, ..., m/z_N] --> B[Vektorių Sudarymas: I_exp ir I_ref]
    B --> C[Kampo θ Kosinuso Skaičiavimas: S_cosine]
    C --> D{S_cosine >= 0.85 ir RT nuokrypis <= ±1.5%?}
    D -- Taip --> E[Aukštas Spektrinis Identifikavimo Patikimumas]
    D -- Ne --> G[Atmetimas / Matricos Trukdžiai]
```


1. **$N = 1$ jonas (1D erdvė):**
   * Vektoriai yra vienamatėje erdvėje. Kampas $\theta$ neegzistuoja ($S_{\text{cosine}} \equiv 1$). Spektrinis kosinuso panašumas **negali būti taikomas**. Vieno jono matavimas nesuteikia jokio spektrinio patvirtinimo, nes bet koks izobarinis matricos triukšmas tuo pačiu $m/z$ duos $100\%$ atitiktį.
2. **$N = 2$ jonai (2D erdvė: Kiekybinis *Quantifier* + 1 Kokybinis *Qualifier*):**
   * Vektoriai apibrėžiami plokštumoje. Kosinuso panašumo balas tapatus dviejų jonų intensyvumų santykiui $R = \frac{i_2}{i_1}$:
     $$S_{\text{cosine}} = \frac{1 + R_{\text{exp}} \cdot R_{\text{ref}}}{\sqrt{1 + R_{\text{exp}}^2} \cdot \sqrt{1 + R_{\text{ref}}^2}}$$
   * Šis matavimas atitinka klasikinį **jonų santykio (Ion Ratio)** tikrinimą.
3. **$N \ge 3$ jonai ($N$-matė erdvė: *Quantifier* + 2+ *Qualifiers*):**
   * Vektoriai egzistuoja daugiamatėje erdvėje. Kosinuso rodiklis atspindi unikalų spektrinį „piršto atspaudą“. Net jei vienas izobarinis fragmentas matricoje padidėja dėl fono, kiti fragmentai išlaiko savo proporcijas, todėl $S_{\text{cosine}}$ matematiniu būdu įvertina bendrą spektrinį nuokrypį.


#### Diagnostinių jonų transformacija į Identifikavimo Taškus (IP)

Metrologiniam ir teisiniam bioanalitinių matavimų patikimumui užtikrinti (remiantis ES reglamentu **(EU) 2021/808** ir SANTE/11312/2021 gairėmis), diagnostinių jonų skaičius transformuojamas į **Identifikavimo Taškus (IP – Identification Points)**. Toks sprendimas priimtas siekiant išvengti sudėtingos matematikos ir padaryti gaires pasiekiamas visose laboratorijose.

#### Identifikavimo taškų skaičiavimo taisyklės:
* **Žemos skiriamosios gebos MS (QqQ / QTRAP):**
  * Prekursoriaus jonas (MS1): **1.0 IP** (tiesiogiai nestebimas)
  * Kiekvienas produkto jonas (MS2 fragmentas): **1.5 IP**
* **Aukštos skiriamosios gebos HRMS (Q-TOF / Orbitrap, $\Delta m/z < 5\text{ ppm}$):**
  * Tikslios masės prekursoriaus jonas (HR-MS1): **2.0 IP** (reikalingas atskiras skenas)
  * Kiekvienas tikslios masės produkto jonas (HR-MS2 fragmentas): **2.5 IP**

#### Identifikavimo patikimumo augimo hierarchija:

| Diagnostinių Jonų Konfigūracija | Instrumentinis Režimas | IP Suma | Tautologinis Patikimumas ir Dydžio Vertinimas |
| :--- | :--- | :---: | :--- |
| **1 Jonas** ($m/z_{\text{prec}}$) | MS1 SIM / Full-Scan | **1.0 IP** | **Nepakankamas.** Didelė klaidingai teigiamų rezultatų rizika dėl matricoje esančių izobarinių junginių. |
| **2 Jonai** ($m/z_{\text{prec}} \to m/z_{\text{prod1}}$) | QqQ SRM (1 perėjimas) | **2.5 IP** | **Nepakankamas.** Nepasiekiamas teisinis $\ge 4.0\text{ IP}$ slenkstis. |
| **3 Jonai** ($1 \ m/z_{\text{prec}} \to 2 \ m/z_{\text{prod}}$) | QqQ SRM (2 perėjimai: *Quant + Qual*) | **4.0 IP** | **Minimalus Pilnas Identifikavimas (MSI 1 Lygis).** Būtina patikrinti $\text{Ion Ratio} \le \pm 20\%$. |
| **3 Jonai (HRMS)** ($1 \ m/z_{\text{prec}} \to 2 \ m/z_{\text{prod}}$) | HRMS PRM su tikslia mase | **6.0-7.0 IP** | **Aukštas Patikimumas.** Viršija IP slenkstį + skaičiuojamas $S_{\text{cosine}} \ge 0.85$. |

### Analitės koncentracijos vertinimas

#### Jonizacijos slopinimas ir jo įtaka kiekio nustatymui

Elektropurškiamoje jonizacijoje (ESI) analitės jonizacijos efektyvumas priklauso nuo skysčio lašelio paviršinio krūvio ir išgaravimo greičio (Kebarle ir Tang lašelio modelis).

Kai kartu su analite eliuuojasi didelės koncentracijos matricos komponentai (pavyzdžiui, šlapimo rūgštis, druskos arba kraujo plazmos fosfolipidai, pvz., glicerofosfocholinai) galimi sekantys efektai:
1. **Paviršiaus konkurencija:** Matricos junginiai užima vietą ESI lašelio paviršiuje, nustumdami analitę į lašelio vidų ir apribodami jos desorbciją į dujų fazę.
2. **Protonų konkurencija:** Jei matricos komponentai turi didesnį giminingumą protonui (*proton affinity*), jie prisijungia $H^+$, palikdami analitę neutralioje formoje.

Matricos efektas yra pamatuojamas dydis ir gali būti išreiškiamas ($ME, \%$) išreiškiamas:

$$ME (\%) = \frac{A_{\text{matrica}}}{A_{\text{tirpiklis}}} \times 100\%$$

kai $ME < 80\%$, stebimas **jonų slopinimas (ion suppression)**.


Eksperimentiškai įrodyta, kad vienintelis metodas, galintis $100\%$ kompensuoti tiek mėginio paruošimo nuostolius, tiek kintantį matricos slopinimo koeficientą $f_{ME}(t)$, yra **stabiliais izotopais žymėti vidiniai standartai (SIL-IS, stable izotope labeled internal standards)** ($^{13}\text{C}$, $^{15}\text{N}$). Tai sintetinės medžiagos, kurios negali būti natūraliai sutinkamos mėginyje. Analizės eigoje, žinomas (pastovus) šių medžiagų kiekis pridedamas į mėginį pasirinktoje fazėje (mėginio paruošimo pradžia, ekstraktas, ar injekcijos tirpalas) ir toliau analiz4 vykdoma stebint natyvias bei izotopais žymėtas medžiagas.

![13C ir 15N žymėtas lizino hidrochloridas](/content/img/lecture5/labeled-lysine.jpg)

Analitės signalo koreciją SIL-IS matematiškai galime aprašyti ir įrodyti:

Tegul analitės $A$ ir vidinio standarto $IS$ matuojami EIC smailės plotai yra $Y_A$ ir $Y_{IS}$. Bendra bioanalitinė lygtis aprašoma taip:

$$Y_A = \eta_A \cdot f_{ME}(t) \cdot R_{\text{rec}} \cdot C_A$$

$$Y_{IS} = \eta_{IS} \cdot f_{ME}(t) \cdot R_{\text{rec}} \cdot C_{IS}$$

kur:
* $\eta_A, \eta_{IS}$ – prietaiso detekcijos ir jonizacijos atsako faktoriai tirpiklyje,
* $f_{ME}(t)$ – laike kintanti matricos jonizacijos slopinimo funkcija ($0 < f_{ME}(t) \le 1$),
* $R_{\text{rec}}$ – mėginio ekstrahavimo išeiga ($0 < R_{\text{rec}} \le 1$),
* $C_A, C_{IS}$ – analitės ir SIL-IS molekulinės koncentracijos mėginyje.

Apskaičiavus matuojamą Atsako Santykį (*Response Ratio – RR*):

$$RR = \frac{Y_A}{Y_{IS}} = \frac{\eta_A \cdot f_{ME}(t) \cdot R_{\text{rec}} \cdot C_A}{\eta_{IS} \cdot f_{ME}(t) \cdot R_{\text{rec}} \cdot C_{IS}} = \left( \frac{\eta_A}{\eta_{IS} \cdot C_{IS}} \right) \cdot C_A = K \cdot C_A$$

Kadangi SIL-IS pasižymi **identiška chemine struktūra ir identišku sulaikymo laiku ($RT_A \equiv RT_{IS}$)**, funkcijos $f_{ME}(t)$ ir $R_{\text{rec}}$ skaitiklyje ir vardiklyje yra **absoliučiai vienodos ir sutrumpėja**. Gautas atsako santykis $RR$ yra griežtai tiesiogiai proporcingas koncentracijai $C_A$ ir visiškai nepriklauso nuo matricos slopinimo ar mėginio paruošimo nuostolių.

Deuteruoti standartai ($^{2}\text{H} / \text{D}$) pasižymi mažesniu lipofiiliškumu nei natūralūs junginiai. Dėl to deuteruotas standartas iš chromatografinės kolonėlės (RP sąlygomis) išsieliuoja šiek tiek ankščiau ($\Delta RT = 0.02\text{–}0.05\text{ min}$). Jei matricos slopinimo funkcija $f_{ME}(t)$ chromatofrafinėje zonoje kinta, $f_{ME}(t_A) \neq f_{ME}(t_{IS})$, todėl kompensavimas tampa nevisiškas. Todėl $^{13}\text{C}$ ir $^{15}\text{N}$ žymėti standartai yra metrologiškai pranašesni.


### Metrologiniai Kalibravimo Modeliai

Metrologiniam koncentracijos matavimo siečiai užtikrinti taikomi trys pagrindiniai kalibravimo modeliai:

```mermaid
flowchart TD
    A[Kalibravimo Modelio Pasirinkimas] --> B{Ar yra tuščia matrica?}
    B -- Taip --> C[Išorinis Kalibravimas Matricoje: Y_A/Y_IS = b1*C + b0]
    B -- Ne --> D{Ar tyrimo matrica unikali/brangi?}
    D -- Ne --> E[Standartinio Priedo Metodas SAM: C_x = b0/b1]
    D -- Taip --> F[Vidinis Kalibravimas Mėginyje In-Sample Calibration]
    F --> F1[Vieno Taško Kalibravimas su SIL-IS: C_x = Y_A/Y_IS * C_IS/RF]
    F --> F2[Izotopinio Rašto Dekonvolucija IPD: S_obs = M_teor * C]
    F --> F3[Daugialypis Izotopologų Stebėjimas MIRM]
```

#### Išorinis kalibravimas matricoje (Matrix-Matched External Calibration)
* **Taikymas:** Kai prieinama biologinė matrica be analitės (pavyzdžiui, kraujo plazma, išvalyta aktyvuota anglimi).
* **Matematinis modelis:** Sudaroma tiesinės regresijos lygtis pagal matricos standartus:
  $$\frac{Y_A}{Y_{IS}} = b_1 \cdot C_A + b_0$$
  Nežinoma koncentracija $C_x$ apskaičiuojama:
  $$C_x = \frac{\left( \frac{Y_{A, x}}{Y_{IS, x}} \right) - b_0}{b_1}$$


#### Standartinio priedo metodas (Standard Addition Method – SAM)
* **Taikymas:** Kai neįmanoma gauti tuščios matricos, o matricos efektai stipriai kinta tarp skirtingų mėginių.
* **Matematinis modelis:** Mėginio alikvotas papildomos žinomais standartų kiekiais ($0, C_1, C_2, C_3$). Apskaičiuojama tiesės susikirtimo su X ašimi vertė ties $Y = 0$:
  $$C_x = \frac{b_0}{b_1}$$


#### Vidinis kalibravimas mėginyje (In-Sample Calibration – IsC)

##### Vieno taško vidinis kalibravimas
Į mėginį pridedama tiksli žinoma SIL-IS koncentracija $C_{IS}$. Iš anksto nustačius prietaiso atsako veiksnį $RF = \frac{\eta_A}{\eta_{IS}}$, analitės koncentracija $C_x$ randama tiesiogiai iš vieno įšvirkštimo:

$$C_x = \frac{Y_A}{Y_{IS}} \cdot \frac{C_{IS}}{RF}$$

##### Izotopinio rašto dekonvolucija (Isotopic Pattern Deconvolution – IPD)
Kai analitė ir SIL-IS turi dalinį izotopinį persidengimą, matuojama izotopinių smailių ($M+0, M+1, M+2$) (pvz. estradiolis, ir estradiolis-D2)  pasiskirstymo sumaišymo matrica $\mathbf{S}_{\text{obs}}$.
Taikant tiesinę matricų algebrą:

$$\mathbf{S}_{\text{obs}} = \mathbf{M}_{\text{teor}} \cdot \mathbf{C}$$

išsprendžiama tiesinių lygčių sistema ir išskiriamos natūralios analitės bei SIL-IS molinės dalys, užtikrinant absoliutų matavimo tikslumą. Raeikalinga specifinė programinė įranga.

#####  Daugialypis izotopologų reakcijų stebėjimas (MIRM)
Į mėginį įterpiama viena SIL-IS koncentracija, tačiau stebimos kelios SIL-IS izotopologų reakcijos ($^{13}\text{C}_1, ^{13}\text{C}_2, ^{13}\text{C}_3$), kurių teoriniai gausumai žinomi. Taip iš vieno įšvirkštimo gaunama 5–8 taškų kalibravimo kreivė pačiame biologiniame mėginyje.
