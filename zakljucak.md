# ZAKLJUČAK

Napomena: Korišćeni dataset je sintetizovan (veštački generisan), a ne prikupljen 
od stvarnih članova teretane, što je detaljnije objašnjeno u opisu dataseta.

Klasterizacijom, i k-means i hijerarhijskim pristupom, i za muški i za 
ženski deo dataseta, dobijene su dve jasno izdvojene grupe članova teretane. 
Manju grupu čine napredni vežbači koji treniraju duže i češće, imaju nizak 
procenat telesne masti i veći unos vode, dok veću grupu čine umereni vežbaci 
sa kraćim i ređim treninzima i višim procentom masti. Obe metode klasterizacije 
su, nezavisno jedna od druge, došle do identične podele (razlika je svega 
par članova/članica), što pokazuje da otkrivena podela nije slučajna. Dodatna 
provera kroz poređenje sa stvarnim nivoom iskustva članova (Experience_Level), 
koji uopšte nije korišćen u klasterizaciji, pokazala je da se napredni 
klaster poklapa sa naprednim vežbačima, što dodatno potvrđuje da su dobijeni
klasteri smisleni. Pokušana je i podela na tri klastera (k=3), ali pokazalo
se da ne donosi značajnu dodatnu vrednost - napredna grupa ostaje ista, dok
se preostala grupa samo dodatno deli po nekom drugom kriterijumu (intenzitetu
treninga kod muškaraca, godinama kod žena) bez jasne veze sa 
iskustvom. Na osnovu svega, zaključujem da je k=2 najispravniji i najjasniji izbor
za oba dela dataseta.

DODATNA ANALIZA: Klasterizacija sa uključenim Workout_Type (OHC)

Sprovedena je dodatna analiza u kojoj je promenljiva 
Workout_Type (tip treninga: Cardio, HIIT, Strength, Yoga) uključena u 
klasterizaciju putem One-Hot Encoding (OHC) transformacije, umesto da bude 
izostavljena kao u osnovnoj analizi.

Rezultati pokazuju da uključivanje Workout_Type drastično menja dobijene
klastere. Optimalan broj klastera prema silhouette analizi postaje 
k=4 (umesto k=2 u osnovnoj analizi), i svaki klaster savršeno odgovara 
tačno jednom tipu treninga - i za muški i za ženski deo dataseta, kod obe 
metode klasterizacije (k-means i hijerarhijska/Ward).

Ostali fizički parametri (godine, težina, BPM, procenat masti, trajanje i 
učestalost treninga) pokazuju veoma male razlike između klastera, za 
razliku od osnovne analize gde su te razlike bile značajno izraženije
(jasno razdvajanje na "umerene" i "posvećene" vežbače).

Kao rezultat, klasterizacija sa uključenim Workout_Type praktično 
rekonstruiše već poznatu kategorizaciju po tipu treninga, umesto da 
otkrije novu, fiziološki zasnovanu podelu članova - što je bio cilj 
osnovne analize. Zbog toga se osnovna analiza (bez Workout_Type) smatra 
ispravnijom za kategorizaciju članova teretane.