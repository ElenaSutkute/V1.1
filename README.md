Šiame darbe buvo atliktas "rule-of-three". Štai pagrindiniai pakitimai, užtikrinantys taisyklės realizavimą:
Destruktorius (~Duomenys()): 
    Sunaikinta atmintį Container* nd. Užtikrina tinkamą išteklių valdymą. 

Kopijavimo Konstruktorius (Duomenys(const Duomenys& other)): 
    Atlieka gilų Container objekto kopijavimą, priskiria naują atmintį nukopijuotam objektui. 

Kopijavimo Priskyrimo Operatorius (Duomenys& operator=(const Duomenys& other)): 
    Atlaisvina esamus išteklius ir atlieka gilų Container objekto kopijavimą. 

Perkėlimo Konstruktorius (Duomenys(Duomenys&& other) noexcept): 
    Perleidžia “atsakingumą” už Container objekto atmintį iš other į dabartinį objektą. 

Perkėlimo Priskyrimo Operatorius (Duomenys& operator=(Duomenys&& other) noexcept): 
    Tvarko atsakingumą už išteklius ir vengia išteklių nuotėkio. 
