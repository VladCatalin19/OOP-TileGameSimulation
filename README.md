# OOP-TileGameSimulation
Object Oriented Programming Project

-------------------------------------------------------------------------------
Vlad Marius-Cătălin 325CD
Anul II Semestrul I
Tema1 Programare Orientată pe Obiect
-------------------------------------------------------------------------------

    1. Implementare
    Pe lângă pachetele fileio și main, am creat mai multe pachete ajutatoare:

 - heroes:
    Conține o clasă abstractă "hero" ce conține atributele generale și simple
ale eroilor, precum HP, XP, metodele respective acestor atribute și metode 
abstracte care țin de executarea celor două abilitati ale fiecărui erou.

 - heroes.properties:
    Aici se găsesc clase pentru implementarea conceptelor de modificatori de
teren și rasă, efectele fiecărui erou și o clasă abstractă care este centra-
lizată pe calcularea damage-ului și generarea efectelor fiecărei abilități.

 - map:
    Pachetul conține clase ce țin de harta jocului. Fiecare celulă a hărții
este caracterizata printr-un tip de teren si o de lista de eroi ce se afla
în celula respectivă.

 - tilegame:
    Aici se află clase care se ocupă de deschiderea unei ferestre și afișarea
hărții, eroilor și animațiile acestora.

 - tilegame.gfx:
    Pachetul se ocupă de partea de grafică. Aici se încarcă texturile și se de-
senează scena.



    2. Executia programului
    În primul rând, se citesc harta și eroii jocului din fișierul de intrare.
În fiecare rundă se citesc mișcările eroilor, se aplică "damage over time",
dacă există, se mută eroii în pozițiile cerute și se execută luptele, dacă
există eroi în aceeași celulă. După terminarea rundelor, se scrie în fișie-
rul de ieșire datele despre eroii jocului.



    3. Design Patterns
    În cadrul acestei teme am folosit mai multe design pattern-uri:
- factory și singleton pentru crearea de eroi pe baza intrării din fișierul
sursă;
- strategy pentru implementarea abilităților eroilor pentru a asigura indepen-
dența acestora față de rasele eroilor;
- visitor pentru a itera prin celulele hărții și de a pune eroii să se lupte;
