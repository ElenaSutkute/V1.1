1. Visų pirma programa paklausia, ar norime, kad duomenys būtų saugomi list tipo konteineryje ar vector tipo. Kad pasitinkti tipą, reikia įvesti raidę l, jei norite, kad būtų naudojamas list ir v, jei vector. Tada yra klausiama, ar sugeneruoti failus ir ar norime studentus rūšiuoti pagal jų galutinį pažymų, jei norite jį pasirinkti, įveskite raidę v, ar pagal pavardes, įrašyti raidę p. Atsakius taip bus sugeneruoti 5 tekstiniai failai: 1000, 10 000, 100 000, 1 000 000 ir 10 000 000 srudentų. Sugeneravus failą, į ekraną yra išvedamas laikas, per kurį failas buvo sugeneruotas. Baigus generuoti failus yra skaitomi duomenys iš pasirinkto failo. Norint pakeisti failą, iš kurio bus skaitoma, reikia atlikti pakeitimus 252 ir 254 eilutėse faile my_lib.cpp. Kai duomenys yra nuskaityti, studentai yra surūšiuojami pagal paradžioje pasirinkt1 būdą, paskaičiuojamas studentų galutinis pažymys pagal vidurkį ir studentai yra suskirtomi į du failus: Moksliukai, kurių vidurkis yra >=5 ir Vargšiuksi, kurių vidurkis <5. Eigoje yra skaičiuojami visų šių operacijų įvykdymo laikai, ši veiksmas vykdomas 5 kartus, kad patikrinti vykdymo laiko patikimumą.
2. Visų pirma, paklausiama ar norite nuskaityti duomenis iš failo. Galimi atsakymai yra tik taip arba ne.
   2.1. Įvedus taip, duomenys yra nuskaitomi iš failo kursiokai.txt. Jei vedant pažymius į tekstinį failą buvo padarytos klaidos,   studento nebus galutiniame sąraše ir bus parašyta kelintas studentas turi klaidų savo pažymių tarpe.
   2.2. Įvedus ne, reikia pasirinkti kiek norėsite vesti studentų. Galima vesti tik skaičius.
   

Pakeitimai buvo atliekami remiantis 2 strategija, kadangi joje rūšiavimas list tipo konteineryje pagerėjo dvigubai. Buvo pasirinkta modifikuoti vector tipo konteinerį su funkcija partition, kadangi ji parodė gerus rezultatus. Vector tipo konteineryje naudojant partition funkciją rūšiavimas pagal vidurkį pagreitėjo 8 kartus, o pagal pavardę pagreitėjo dvigubai. Tyrimas buvo atliktas nagrinėjant 1 000 000 studentų failą.

Konteinerio tipas ir rūšiavimo kriterijus:

Vektoriuje pagal vidurkį 
<img width="401" alt="image" src="https://github.com/ElenaSutkute/v1.0/assets/145843117/34e36817-3abf-46fc-8e31-f94ac28568c5">


Vektoriuje pagal pavardę 
<img width="464" alt="image" src="https://github.com/ElenaSutkute/v1.0/assets/145843117/da2080ce-2b39-4a79-9a03-f2e48bcccf3c">


List'e pagal vidurkį 
<img width="457" alt="image" src="https://github.com/ElenaSutkute/v1.0/assets/145843117/49fa4d34-6299-42b7-8e16-a61a3ad41bd7">


List'e pagal pavardę
<img width="458" alt="image" src="https://github.com/ElenaSutkute/v1.0/assets/145843117/562b6edf-067c-45c4-961e-fef1eebaea88">
