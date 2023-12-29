Naudojimasis kodu:

1. Visų pirma reikia įvesti asmens vardą, tada pavardę, tada vesti norimą kiekį pažymių, norint nutraukti pažymių vedimą, reikia įvesti -1, tada reikia įvesti egzamino pažymį. Šis procesas parodo klasės Zmogus įvesties ir išvesties operatorių perdengimą.

2. Tada programa paklausia, ar norime, kad duomenys būtų saugomi list tipo konteineryje ar vector tipo. Kad pasitinkti tipą, reikia įvesti raidę l, jei norite, kad būtų naudojamas list ir v, jei vector. Tada yra klausiama, ar sugeneruoti failus, atsakius taip bus sugeneruoti 5 tekstiniai failai: 1000, 10 000, 100 000, 1 000 000 ir 10 000 000 srudentų. Tada yra klausiama, ar norime studentus rūšiuoti pagal jų galutinį pažymį (vidurkį) ar pagal pavardes, norint pagal vidurkį, veskite v, pagal pavardes p.  Tuomet yra skaitomi duomenys iš pasirinkto failo. Norint pakeisti failą, iš kurio bus skaitoma, reikia atlikti pakeitimus funkcijoje StudentuSkirstymas. Kai duomenys yra nuskaityti, studentai yra surūšiuojami pagal pradžioje pasirinktą būdą, paskaičiuojamas studentų galutinis pažymys pagal vidurkį ir studentai yra suskirtomi į du failus: Moksliukai, kurių vidurkis yra >=5 ir Vargšiukai, kurių vidurkis <5. Eigoje yra skaičiuojami visų šių operacijų įvykdymo laikai.

   
3. tada paklausiama ar norite nuskaityti duomenis iš failo. Galimi atsakymai yra tik taip arba ne.
   
     3.1. Įvedus taip, duomenys yra nuskaitomi iš failo kursiokai.txt. Jei vedant pažymius į tekstinį failą buvo padarytos klaidos,   studento nebus galutiniame sąraše ir bus parašyta kelintas studentas turi klaidų savo pažymių tarpe.
   
     3.2. Įvedus ne, reikia pasirinkti kiek norėsite vesti studentų. Galima vesti tik skaičius.
   
     3.2.1. Tuomet reikia įvesti studento vardą bei pavardę.
   
     3.2.2. Klausiama ar norite įvesti studento pažymius bei egzamino rezutatą ranka, ar kad kompiuteris juos sugeneruotų automatiškai. Galimi įvedimo rezultatai taip arba ne.
   
     3.2.2.1. Įvedus taip galite vesti kiek norite studento pažymių, norėdami nutraukti įvedimą parašykite -1; Tuomet reikia įvesti egzamino rezultatą. Rezultatai būtinai turi būtų (0,10] ribose.
   
     3.2.2.2. Įvedus ne reikia pasirinkti kiek buvo atliktų namų darbų ir tada studento namų darbų ir egzamino rezultatai bus generuojami automatiškai.
Galutiniame rezultate matysime studentų pavades ir vardus surūšiuotus abeceliškai ir jų galutinį dalyko rezutatą, paskaičiuotą tiek pagal medianą, tiek pagal vidurkį.

# 2.0

Kodui pridėta dokumentacija Doxygen aplankale html.

# 1.5

Sukurta abstrakti klasė Zmogus su virtualiu destruktoriumi ir virtualiais parametrais, skirtais gauti žmogaus vardą ir pavardę. Klasė Duomenys yra išvestinė klasė (derived) nuo klasės Zmogus. Tai reiškia, kad visi Duomenys klasės objektai taip pat yra Zmogus objektai. Zmogus klasė suteikia bendrą sąsają visiems žmonėms, bet nepateikia jokio konkretaus įgyvendinimo. Ši abstrakcija leidžia sukurti bendrą funkcionalumą ir apibrėžti bendrus metodus visiems žmogaus tipams. Kadangi Zmogus klasė yra virtuali, negalima tiesiogiai kurti jos objektų.

Išvesties rezultatai nepakito, taigi juos galima rasti prie v1.1 užduoties aprašymo.

# 1.2
Šiame darbe buvo atliktas "rule-of-three". Štai pagrindiniai pakitimai, užtikrinantys taisyklės realizavimą:
Yra destruktorius.

Kopijavimo Konstruktorius: 
    Atlieka gilų Container objekto kopijavimą, priskiria naują atmintį nukopijuotam objektui. 

Kopijavimo Priskyrimo Operatorius: 
    Atlaisvina esamus išteklius ir atlieka gilų Container objekto kopijavimą. 


Taip pat pridėti:
    Įvesties operatorius:
        Nuskaito įvedamus kintamuosius vardas, pavarde, pažymys. Pažymys yra vedamas tol, kol neįvedama -1, visi nuskaityti pažymiai yra kaupiamu nd konteineryje pasitelkus          addScore, tada yra nuskaitomas egzamino pažymys.
        
    Išvesties operatorius: 
        Išveda duomenis, surašytus pasitelkus įvesties operatorių. 


Pademonstruotas įvedimo metodas:

<img width="580" alt="image" src="https://github.com/ElenaSutkute/V1.1/assets/145843117/43fcade5-3de3-42c8-9b4c-73f6ae1429ae">


Išvedimo į ekraną rezultatas:

<img width="247" alt="image" src="https://github.com/ElenaSutkute/V1.1/assets/145843117/9b049850-586c-46c3-8959-b402d51d7d3b">

Išvedimo į failus rezultatai:

<img width="280" alt="image" src="https://github.com/ElenaSutkute/V1.1/assets/145843117/5a56c8cb-790e-434b-938b-5996f407d785">   <img width="275" alt="image" src="https://github.com/ElenaSutkute/V1.1/assets/145843117/5c71c8ef-d95f-4931-8666-de802715941d">

# 1.1

Pakeitus struktūrą į klasę gauname tokius rezultatus:

<img width="263" alt="image" src="https://github.com/ElenaSutkute/V1.1/assets/145843117/dc78d3a9-13cf-4107-97e8-6046adae016f">

Atlikus eksperimentrus su flag'ais gauname tokius rezultatus:

<img width="413" alt="image" src="https://github.com/ElenaSutkute/V1.1/assets/145843117/592b8d41-3f77-46db-b9c7-a544ce481dd9">
