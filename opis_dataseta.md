
# Gym Members Exercise Dataset - klasterizacija članova teretane

U fajlu `gym_members_exercise_tracking.csv` dati su podaci o članovima teretane 
koji sadrže analize obrazaca treninga i fizičkih performansi. Dataset je 
preuzet sa platforme Kaggle (Gym Members Exercise Dataset, autor: Vala Khorasani, 
https://www.kaggle.com/datasets/valakhorasani/gym-members-exercise-dataset). 
Podaci su o 973 člana teretane. Bitno je napomenuti da je dataset sintetizovan 
(veštački generisan), a ne prikupljen od stvarnih članova teretane - ovo ne 
umanjuje vrednost analize, s obzirom da je cilj rada demonstracija metodologije 
klasterizacije. Promenljive su:

- Age - Starost člana (godine)
- Gender - Pol (Male, Female)
- Weight (kg) - Telesna težina
- Height (m) - Telesna visina
- Max_BPM - Maksimalan broj otkucaja srca tokom treninga
- Avg_BPM - Prosečan broj otkucaja srca tokom treninga
- Resting_BPM - Broj otkucaja srca u mirovanju
- Session_Duration (hours) - Trajanje treninga u satima
- Calories_Burned - Broj sagorenih kalorija tokom treninga
- Workout_Type - Tip treninga (Yoga, HIIT, Cardio, Strength)
- Fat_Percentage - Procenat telesne masti
- Water_Intake (liters) - Dnevni unos vode u litrima
- Workout_Frequency (days/week) - Broj treninga nedeljno
- Experience_Level - Nivo iskustva (1 - početnik, 2 - srednji, 3 - napredni)
- BMI - Indeks telesne mase

NAPOMENE

- Klasterizacija se sprovodi odvojeno za muške i ženske članove,zbog značajnih razlika 
u telesnim parametrima između polova.