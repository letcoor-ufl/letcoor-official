# LETCOOR 1.0.0 — Documentație completă pentru utilizator

> Documentație realizată pe baza codului sursă real al **LETCOOR 1.0.0**, furnizat la 30 octombrie 2026.
> Această documentație descrie funcțiile expuse efectiv de aplicația Android/Windows și de interfața actuală.

---

## Cuprins

1. [Primii pași: conectarea dispozitivelor](#1-primii-pași-conectarea-dispozitivelor)
2. [Permisiuni importante, mai ales offline](#2-permisiuni-importante-mai-ales-offline)
3. [Crearea sau alăturarea la un grup](#3-crearea-sau-alăturarea-la-un-grup)
4. [Înțelegerea ecranului principal](#4-înțelegerea-ecranului-principal)
5. [Harta tactică](#5-harta-tactică)
6. [Crearea unei semnalări](#6-crearea-unei-semnalări)
7. [Crearea unui obiectiv](#7-crearea-unui-obiectiv)
8. [Crearea unui ordin](#8-crearea-unui-ordin)
9. [Crearea unui punct de adunare](#9-crearea-unui-punct-de-adunare)
10. [Trimiterea unei alerte de siguranță](#10-trimiterea-unei-alerte-de-siguranță)
11. [Interacțiunea cu un obiect deja publicat](#11-interacțiunea-cu-un-obiect-deja-publicat)
12. [Panoul „Comandament și activitate”](#12-panoul-comandament-și-activitate)
13. [Meniul grupului sau al echipei](#13-meniul-grupului-sau-al-echipei)
14. [Echipe](#14-echipe)
15. [Participanți și roluri](#15-participanți-și-roluri)
16. [Invitarea unui participant nou](#16-invitarea-unui-participant-nou)
17. [Operațiuni](#17-operațiuni)
18. [Campanii de roluri](#18-campanii-de-roluri)
19. [Sesiuni](#19-sesiuni)
20. [Partajarea datelor între echipe](#20-partajarea-datelor-între-echipe)
21. [Gestionarea grupului și a echipelor](#21-gestionarea-grupului-și-a-echipelor)
22. [Limite de publicare](#22-limite-de-publicare)
23. [Localizare](#23-localizare)
24. [Notificări](#24-notificări)
25. [Hărți offline](#25-hărți-offline)
26. [Conexiunea la rețea și funcționarea offline](#26-conexiunea-la-rețea-și-funcționarea-offline)
27. [Confidențialitate, blocare și recuperare](#27-confidențialitate-blocare-și-recuperare)
28. [Roluri disponibile](#28-roluri-disponibile)
29. [Sfaturi de pregătire înaintea unei activități](#29-sfaturi-de-pregătire-înaintea-unei-activități)
30. [Depanare](#30-depanare)
31. [Rezumat rapid](#31-rezumat-rapid)

---

# 1. Primii pași: conectarea dispozitivelor

LETCOOR utilizează un sistem de invitații între dispozitive. O invitație poate fi transmisă prin **cod QR**, **link**, partajare de sistem sau fișier, în funcție de platformă.

Pentru a maximiza șansele de conectare, mai ales **fără Internet**, pregătiți ambele dispozitive înainte de schimb.

## 1.1 Înainte de a scana codul QR sau de a deschide linkul

Pe ambele dispozitive:

1. Deschideți LETCOOR și păstrați aplicația în prim-plan în timpul primei conectări.
2. Activați **Wi‑Fi**.
3. Activați **Bluetooth**.
4. Acceptați solicitările Android/Windows referitoare la **dispozitive din apropiere**, Bluetooth, Wi‑Fi Direct sau rețeaua locală.
5. Dacă Android propune ca telefonul să devină vizibil prin Bluetooth, acceptați în timpul fazei de conectare.
6. Dacă Android solicită activarea serviciului de localizare pentru a permite detectarea radio, este recomandat să îl activați pentru compatibilitate cu API-urile de proximitate ale telefonului.
7. **Camera** este necesară numai pentru scanarea unui cod QR. Nu este necesară dacă utilizați un link.

> **Important:** autorizarea sau activarea serviciului de localizare Android pentru descoperirea prin proximitate nu activează automat partajarea poziției dvs. în LETCOOR. Partajarea localizării este o funcție separată și rămâne dezactivată până când o activați dvs.

## 1.2 Conectarea prin cod QR

### Pe dispozitivul care invită

1. Deschideți meniul grupului sau al echipei atingând numele din stânga sus.
2. Deschideți fila **Invită**.
3. Dacă sunt disponibile mai multe destinații, alegeți **grupul** sau **echipa** la care se va face alăturarea.
4. Deschideți **Partajează invitația**.
5. Selectați **Afișează codul QR**.
6. Lăsați codul QR afișat pe ecran.

Un cod QR poate fi compus din mai multe părți. LETCOOR le derulează automat. Este posibil să puneți derularea pe pauză sau să treceți manual la partea anterioară/următoare.

### Pe dispozitivul invitat

1. Pe ecranul de pornire, alegeți **Alătură-te cu o invitație**.
2. Apăsați butonul de scanare QR.
3. Autorizați camera dacă Android/Windows solicită acest lucru.
4. Îndreptați camera spre codul QR de pe celălalt dispozitiv.
5. Dacă QR-ul are mai multe părți, mențineți camera orientată spre ecran până când LETCOOR a citit toate părțile.
6. LETCOOR importă invitația și pregătește un **răspuns**.
7. Dispozitivul invitat afișează apoi un **link de răspuns** sau un **cod QR de răspuns** care trebuie trimis înapoi dispozitivului care invită.

### Trimiterea răspunsului înapoi către dispozitivul care invită

Pe dispozitivul care a creat invitația:

1. Rămâneți în **Invită**.
2. Deschideți **Primește răspunsul**.
3. Scanați codul QR de răspuns, lipiți linkul de răspuns sau utilizați mecanismul de partajare disponibil.
4. LETCOOR verifică răspunsul și apoi începe conectarea directă.

Aplicația afișează apoi starea încercării: pregătire pentru proximitate, conectare la Internet, căutare locală, conexiune stabilită sau expirarea timpului.

## 1.3 Conectarea prin link

Procedura este identică, dar fără cameră.

### Dispozitivul care invită

În **Invită > Partajează invitația**:

1. Alegeți **Link de invitație**.
2. Apăsați **Copiază linkul** sau butonul de partajare.
3. Trimiteți linkul celuilalt participant.

### Dispozitivul invitat

1. Deschideți **Alătură-te cu o invitație**.
2. Lipiți linkul în **Invitație de acceptat**, sau utilizați butonul pentru clipboard.
3. LETCOOR procesează automat un link valid.
4. Trimiteți apoi **linkul de răspuns** înapoi dispozitivului care vă invită.

### Dispozitivul care invită

În **Primește răspunsul**:

1. Lipiți linkul de răspuns sau scanați codul QR de răspuns.
2. LETCOOR verifică răspunsul.
3. Conexiunea începe automat.

## 1.4 De ce trebuie trimis un răspuns înapoi?

Fluxul bidirecțional permite ambelor dispozitive să cunoască informațiile necesare pentru încercarea de conectare. LETCOOR poate apoi încerca rutele disponibile și autentifica perechea înainte de admiterea în grup sau echipă.

## 1.5 Admiterea în grup și echipă

O invitație validă este semnată și vizează o destinație stabilită la crearea acesteia.

- O invitație de grup permite alăturarea la grupul corespunzător.
- O invitație provenită de la o echipă poate include accesul la **grupul părinte și la echipa celui care invită**.
- Cheile private ale grupului sau istoricul complet nu sunt incluse în codul QR.
- Admiterea este validată de protocolul LETCOOR după autentificare; nu există o validare manuală suplimentară pentru o invitație validă, decât dacă politica de admitere sau drepturile spațiului o împiedică.

---

# 2. Permisiuni importante, mai ales offline

LETCOOR utilizează mai multe funcții de sistem. Pentru utilizarea fără Internet, permisiunile de proximitate sunt deosebit de importante.

## 2.1 Bluetooth și Wi‑Fi Direct

În **Setări > Permisiuni**, LETCOOR oferă:

- **Bluetooth și Wi‑Fi Direct — Permite**
- **Cameră — Permite**
- **Localizare — Verifică**

Pe versiunile recente de Android, LETCOOR poate solicita în special permisiuni de sistem legate de:

- dispozitive din apropiere;
- scanare Bluetooth;
- conexiune Bluetooth;
- anunțare Bluetooth;
- Wi‑Fi Direct / dispozitive Wi‑Fi din apropiere;
- acces la rețeaua locală pe versiunile Android care îl impun.

Pe unele versiuni mai vechi de Android, descoperirea Bluetooth/Wi‑Fi poate depinde de permisiunea de localizare Android.

## 2.2 Localizare: două lucruri diferite

Trebuie făcută diferența între:

1. **Localizarea de sistem Android utilizată de anumite API-uri de descoperire prin proximitate.**
2. **Partajarea voluntară a poziției dvs. în LETCOOR.**

Puteți utiliza LETCOOR fără să vă publicați poziția pe hartă. Partajarea localizării se configurează separat din pictograma **Localizare**.

## 2.3 Cameră

Camera este utilizată numai pentru scanarea codurilor QR. Scanarea nu necesită microfonul.

Dacă accesul la cameră este refuzat:

- utilizați linkul de invitație;
- sau reautorizați camera în setările Android/Windows.

## 2.4 Notificări de sistem

Notificările de sistem pot fi activate din centrul de notificări LETCOOR. Acestea permit primirea de alerte native pentru anumite evenimente atunci când platforma permite acest lucru.

---

# 3. Crearea sau alăturarea la un grup

La prima pornire, dacă dispozitivul nu are încă niciun grup, LETCOOR afișează ecranul de pornire.

Aveți două opțiuni:

- **Creează un grup**
- **Alătură-te cu o invitație**

## 3.1 Crearea unui grup

1. Apăsați **Creează un grup**.
2. Introduceți **Numele grupului**.
3. Numele trebuie să conțină cel puțin 2 caractere.
4. Apăsați **Creează**.

Creatorul primește rolul de administrare al grupului și poate apoi crea echipe, invita participanți și gestiona spațiul în funcție de capabilitățile acordate de Core.

## 3.2 Alăturarea la un grup

1. Apăsați **Alătură-te cu o invitație**.
2. Importați linkul sau codul QR.
3. Urmați schimbul invitație/răspuns descris la începutul acestei documentații.

## 3.3 Nr. personal

Fiecare dispozitiv are un **Nr. personal** afișat în timpul integrării inițiale și în fila **Context**.

Acest număr servește drept identificator lizibil pentru utilizator în interfață. Identitatea criptografică reală se bazează pe identitatea dispozitivului LETCOOR, nu pe acest cod afișat.

---

# 4. Înțelegerea ecranului principal

LETCOOR utilizează o interfață **centrată pe hartă**, mai degrabă decât o succesiune de pagini clasice.

## 4.1 Antet

În partea de sus a ecranului:

- în stânga: **numele grupului sau al echipei selectate în prezent**;
- subtitlul indică **Grup** sau **Echipă**;
- poate apărea starea **Nesincronizat** dacă contextul funcționează fără sincronizare;
- un clopoțel deschide **Notificările**;
- butonul **Comandament** deschide panoul de comandament și activitate;
- un indicator afișează starea rețelei: Internet direct, releu, Wi‑Fi Direct, Wi‑Fi local, Bluetooth, LAN, sincronizare sau căutarea unei conexiuni.

## 4.2 Harta centrală

Harta afișează obiectele autorizate în contextul curent:

- ordine;
- semnalări;
- obiective;
- întâlniri / puncte de adunare;
- alerte de siguranță;
- prezența echipei;
- prezența exactă atunci când este autorizată;
- deplasări / trasee în funcție de drepturi și partajările active.

## 4.3 Legendă

Butonul `?` afișează legenda, inclusiv:

- Pericol;
- Obiectiv;
- Punct de adunare;
- Echipă.

## 4.4 Subsol

Partea de jos a ecranului indică:

- numărul de membri activi din context;
- numărul de obiecte active;
- existența eventuală a unei sesiuni în curs, iar în lipsa acesteia, Nr. dvs. personal.

## 4.5 Deschiderea meniului grupului sau al echipei

Atingeți numele contextului în stânga sus.

Panoul conține filele:

- **Context**
- **Echipe**
- **Participanți**
- **Invită**
- **Operațiuni**
- **Gestionare**
- **Setări**

Unele funcții apar numai dacă rolul dvs. are permisiunea corespunzătoare.

---

# 5. Harta tactică

## 5.1 Deplasarea pe hartă

Harta se utilizează ca o hartă tactilă clasică: deplasare și zoom.

## 5.2 Adăugarea unui obiect

Pentru a publica un obiect spațial:

1. Faceți o **apăsare lungă** în locul dorit.
2. LETCOOR deschide **Adaugă aici**.
3. Sunt afișate acțiunile autorizate pentru rolul dvs.

Opțiunile sunt:

- **Semnalare**
- **Obiectiv**
- **Ordin**
- **Punct de adunare**
- **Alertă de siguranță**

Acțiunile neautorizate în contextul dvs. nu sunt afișate.

## 5.3 Forme geografice

În funcție de tipul obiectului, LETCOOR permite:

- **Punct**;
- **Zonă circulară**;
- **Poligon**;
- **Traseu**.

Pentru o zonă circulară, raza poate fi reglată între **10 și 500 m**.

Pentru un poligon sau un traseu:

1. alegeți geometria;
2. apăsați **Desenează pe hartă**;
3. adăugați vârfurile pe hartă;
4. utilizați **Anulează ultimul**, **Finalizează** sau **Renunță**.

Numărul de puncte este limitat de interfață.

## 5.4 Durată / termen

Obiectele spațiale care nu sunt de siguranță pot primi o durată între **5 și 360 de minute**, în pași de 5 minute.

---

# 6. Crearea unei semnalări

1. Faceți o apăsare lungă pe hartă.
2. Alegeți **Semnalare**.
3. Selectați tipul.
4. Introduceți opțional un nume și o descriere.
5. Alegeți geometria și durata.
6. Apăsați **Publică**.

## Tipuri de semnalare disponibile

- Pericol
- Obstacol
- Rută blocată
- Trecere impracticabilă
- Trecere deschisă
- Adversar observat
- Grup observat
- Mișcare observată
- Problemă de echipament
- Personalizat

În funcție de rolul dvs., o semnalare poate fi publicată în cadrul echipei sau la nivelul grupului.

Cercetașii și responsabilii care au permisiunile necesare pot, printre altele, confirma, contesta, rezolva sau promova anumite semnalări.

---

# 7. Crearea unui obiectiv

1. Faceți o apăsare lungă pe hartă.
2. Alegeți **Obiectiv**.
3. Introduceți **Obiectiv de realizat**.
4. Alegeți tipul.
5. Alegeți prioritatea.
6. Selectați geometria.
7. Reglați termenul.
8. Apăsați **Publică**.

## Tipuri de obiectiv

- Atingerea unui punct
- Menținerea unei zone
- Capturarea unei zone
- Recuperarea unui obiect
- Ajungerea la un punct de întâlnire
- Observarea unei zone
- Personalizat

## Obiectiv de echipă sau obiectiv final al grupului

Atunci când rolul și contextul permit acest lucru, formularul vă permite să alegeți:

- **Întregul grup — obiectiv final**;
- **Această echipă — obiectiv de echipă**.

Obiectivul final este vizibil membrilor grupului și echipelor în conformitate cu regulile de autorizare ale Core.

## Priorități

Interfața oferă:

- P0 — Urgentă
- P1 — Ridicată
- P2 — Normală
- P3 — Scăzută

---

# 8. Crearea unui ordin

1. Faceți o apăsare lungă pe hartă.
2. Alegeți **Ordin**.
3. Introduceți instrucțiunea personalizată dacă este necesar.
4. Alegeți tipul de ordin.
5. Alegeți prioritatea.
6. Puteți lega ordinul de un **obiectiv** existent.
7. Puteți lega ordinul de un **punct de întâlnire** existent.
8. Dacă este necesar, LETCOOR permite crearea directă a unui obiectiv sau a unui punct de întâlnire în același loc și apoi revenirea la ordin.
9. Alegeți geometria și durata.
10. Apăsați **Publică**.

## Tipuri de ordin

- Deplasare
- Regrupare
- Menținerea poziției
- Înaintare
- Retragere
- Apărare
- Observare
- Securizarea unui obiectiv
- Personalizat

## Ordinul șefului de grup

Atunci când publicația este un ordin de comandament al grupului, șeful de grup alege **echipele destinatare**. Codul operațional prevede ca acest tip de ordin să fie destinat șefilor echipelor selectate.

## Ordin de echipă

Un șef de echipă poate crea ordine în cadrul echipei sale. Un ordin de echipă poate fi, de asemenea, legat de un ordin de comandament părinte atunci când această relație este disponibilă.

---

# 9. Crearea unui punct de adunare

1. Faceți o apăsare lungă pe hartă.
2. Alegeți **Punct de adunare**.
3. Dați-i un nume scurt.
4. Alegeți un **Punct** sau o **Zonă circulară**.
5. Reglați durata / termenul.
6. Publicați.

Punctul de adunare creează un punct de întâlnire care poate fi folosit și ca referință pentru un ordin.

---

# 10. Trimiterea unei alerte de siguranță

Alerta de siguranță este o publicație prioritară.

1. Faceți o apăsare lungă pe hartă.
2. Alegeți **Alertă de siguranță**.
3. Introduceți un mesaj dacă este necesar.
4. Alegeți tipul.
5. Apăsați **Trimite alerta**.

## Tipuri disponibile

- Rănire
- Oprirea activității
- Pericol
- Persoană dispărută
- Altă urgență

O alertă personalizată necesită un mesaj.

LETCOOR reamintește în interfață că alerta P0 trebuie utilizată în caz de pericol sau nevoie de ajutor.

În funcție de permisiuni, un responsabil poate apoi selecta **Marchează ca rezolvată**.

---

# 11. Interacțiunea cu un obiect deja publicat

Atingeți un obiect de pe hartă pentru a deschide fișa acestuia.

Acțiunile propuse depind de tipul obiectului și de permisiunile dvs.

## Semnalare

Acțiuni posibile:

- Confirmă
- Contestă
- Rezolvă
- Prelungește cu 15 min
- Anulează semnalarea
- Promovează la nivel de grup, atunci când semnalarea provine de la o echipă și rolul permite acest lucru

Pentru anumite obiecte operaționale, LETCOOR poate oferi și:

- **Confirmă pe teren**;
- **Votează pentru rezolvare**;
- **Semnalează trecerea deschisă**;
- **Elimină informația**.

## Obiectiv

Un utilizator cu permisiunea corespunzătoare poate modifica starea acestuia:

- În curs
- Finalizat
- Eșuat
- Anulat

## Ordin

Pot fi propuse răspunsuri în funcție de tipul ordinului:

- Primit
- Acceptat
- Finalizat
- Imposibil

Panoul simplificat **Operațiuni > Ordine** utilizează cel puțin confirmarea **Primit** atunci când ordinul necesită un răspuns.

## Alertă de siguranță

Responsabilul autorizat poate alege **Marchează ca rezolvată**.

---

# 12. Panoul „Comandament și activitate”

Butonul **Comandament** din partea de sus a ecranului deschide un panou separat destinat operațiunilor care nu sunt neapărat asociate unui punct de pe hartă.

Acesta conține până la trei file:

- **Notificări**
- **Publică**
- **Istoric**

Filele apar numai atunci când au conținut sau când o acțiune este autorizată.

## 12.1 Notificări

Afișează obiectele operaționale accesibile:

- ordin de comandament;
- ordin de echipă;
- obiectiv;
- obiectiv final al grupului;
- anunț;
- raport de verificat;
- semnalare verificată.

Fiecare card poate indica:

- text;
- tip;
- stare;
- echipă/grup;
- obiectiv sau punct de întâlnire asociat;
- echipe vizate;
- confirmări de primire;
- voturi;
- progres pe echipă.

În funcție de rolul dvs., butoanele pot oferi:

- Primit;
- Verifică pe teren;
- Elimină;
- Marchează ca citit;
- Declară finalizat;
- Votează finalizat;
- Votează imposibil;
- Votează rezolvat;
- Rezolvă.

## 12.2 Publică

LETCOOR afișează numai publicațiile autorizate pentru rolul și contextul dvs.

Tipurile interne gestionate în prezent de interfață includ:

- Ordin de comandament
- Ordin de echipă
- Obiectiv de echipă
- Obiectiv final al grupului
- Anunț
- Raport de verificat
- Semnalare verificată

Pentru un ordin de comandament, alegeți echipele destinatare.

Pentru un ordin de echipă, puteți selecta un ordin de comandament părinte.

Introduceți apoi descrierea și apăsați **Publică**.

Publicațiile create din acest panou utilizează în prezent în codul interfeței o durată operațională implicită de aproximativ 30 de minute.

## 12.3 Istoric

Afișează evenimentele înregistrate cu data, rezumatul și identificatorul obiectului.

---

# 13. Meniul grupului sau al echipei

Atingeți numele contextului în stânga sus.

## Fila Context

Afișează:

- selectorul **Grup sau echipă**;
- numărul de membri;
- numărul de dispozitive conectate;
- starea sesiunii;
- rolurile dvs.;
- tema Sistem / Luminos / Întunecat;
- limba;
- **Nr. personal**, care poate fi copiat.

Limbile expuse în prezent de interfață sunt: **Sistem, Français, English, العربية, Deutsch și Русский**. Interfața trece automat la direcția de la dreapta la stânga pentru arabă.

## Fila Echipe

Consultați [Echipe](#14-echipe).

## Fila Participanți

Consultați [Participanți și roluri](#15-participanți-și-roluri).

## Fila Invită

Consultați [Invitarea unui participant nou](#16-invitarea-unui-participant-nou).

## Fila Operațiuni

Consultați [Operațiuni](#17-operațiuni).

## Fila Gestionare

Consultați [Gestionarea grupului și a echipelor](#21-gestionarea-grupului-și-a-echipelor).

## Fila Setări

Conține în prezent:

- hărți offline;
- gestionarea permisiunilor Bluetooth/Wi‑Fi Direct;
- permisiunea pentru cameră;
- verificarea localizării.

---

# 14. Echipe

Fila **Echipe** afișează echipele grupului.

Pentru fiecare echipă, LETCOOR afișează în special:

- numele;
- numărul de membri;
- șeful echipei;
- lista participanților;
- starea accesului dvs. la echipă.

## Stări de acces

- **Sunteți membru · acces pregătit**
- **Calitate de membru înregistrată · recepționarea cheilor este în curs**
- **Nu faceți parte din această echipă**

Dacă sunteți membru și accesul este pregătit, apăsați **Deschide echipa mea**.

## 14.1 Crearea unei echipe

Această funcție apare pentru șeful de grup care are permisiunea corespunzătoare.

1. Introduceți **Numele echipei**.
2. Alegeți **Șeful echipei** dintre membrii grupului.
3. Selectați opțional membrii inițiali.
4. Puteți utiliza:
   - Selectează tot;
   - 10 persoane;
   - 15 persoane;
   - Deselectează tot.
5. Apăsați **Creează echipa și numește-i șeful**.

O echipă acceptă în formular cel mult 200 de membri inițiali, inclusiv șeful.

Membrii selectați părăsesc eventuala lor echipă anterioară din același grup pentru a se alătura celei noi.

Atunci când grupul are deja zece echipe sau mai multe, codul impune reguli suplimentare de dimensiune minimă: echipele active trebuie să aibă cel puțin patru membri pentru ca extinderea să poată continua.

## 14.2 Înlocuirea șefului echipei

Dacă acțiunea este autorizată:

1. deschideți echipa;
2. utilizați **Înlocuiește șeful echipei**;
3. alegeți un membru al grupului.

## 14.3 Praguri de validare

Responsabilii autorizați pot configura:

- voturile cercetașilor necesare pentru finalizare;
- voturile cercetașilor necesare pentru declararea imposibilității;
- voturile necesare pentru rezolvarea unei semnalări.

---

# 15. Participanți și roluri

Fila **Participanți** afișează membrii contextului selectat.

Puteți căuta un participant după Nr. personal sau identificator.

Atingeți un participant pentru a deschide acțiunile disponibile.

## 15.1 Roluri permanente și roluri de sesiune

Atunci când este disponibilă o sesiune, administratorul poate alege:

- **Permanent**;
- **Sesiune**.

Un rol permanent rămâne asociat membrului în conformitate cu regulile grupului/echipei.

Un rol de sesiune se aplică sesiunii selectate.

## 15.2 Atribuirea sau eliminarea unui rol

Rolurile pe care le puteți atribui apar sub formă de butoane.

Un buton activ indică faptul că rolul este deja prezent. Apăsarea acestuia permite eliminarea rolului atunci când aveți autoritatea necesară.

Există și o secțiune **Administrează un rol într-o echipă** care permite alegerea:

1. echipei țintă;
2. rolului;
3. **Atribuie rolul de echipă** sau **Elimină rolul de echipă**.

## 15.3 Atribuire de sesiune

Un administrator de sesiune poate seta participantul ca:

- Activ;
- În pauză;
- Plecat;
- Eliminat.

De asemenea, poate alege echipa de sesiune sau **Fără echipă**.

Apăsați **Aplică atribuirea**.

## 15.4 Eliminarea unui membru

Atunci când permisiunea este disponibilă, apare butonul **Elimină din acest grup sau din această echipă**.

## 15.5 Transferarea administrării grupului

Responsabilul autorizat poate selecta un alt participant și apoi utiliza **Transferă administrarea**.

Destinatarul va trebui apoi să accepte transferul din secțiunea **Gestionare**.

## 15.6 Blocarea unui dispozitiv

Secțiunea **Moderare** permite, atunci când rolul dvs. o autorizează:

- **Blochează acest dispozitiv**;
- afișarea dispozitivelor blocate;
- **Ridică blocarea**.

Un dispozitiv blocat continuă să fie refuzat la invitațiile noi până la ridicarea blocării.

---

# 16. Invitarea unui participant nou

Deschideți **Invită**.

## 16.1 Alegerea destinației

În funcție de rolul dvs., meniul **Destinație** vă permite să alegeți:

- grupul;
- o echipă.

Un administrator al grupului poate avea mai multe destinații în meniu.

## 16.2 Admitere deschisă / închisă

Interfața poate indica:

- **Admitere deschisă**;
- **Admitere închisă**.

Dacă rolul dvs. permite:

- **Deschide accesul**;
- **Închide accesul**.

O echipă poate moșteni și închiderea generală a grupului.

## 16.3 Partajarea invitației

LETCOOR permite:

- link;
- QR;
- copiere;
- partajare de sistem;
- fișier `.letcoor` pe platformele unde este disponibil butonul.

## 16.4 Primirea răspunsului

După ce celălalt dispozitiv importă invitația:

1. deschideți **Primește răspunsul**;
2. scanați sau lipiți linkul de răspuns;
3. LETCOOR pornește conexiunea.

Dacă încercările prin Internet și proximitate expiră, butonul **Reîncearcă** permite reluarea procesului.

## 16.5 Resetarea unei invitații

Butonul de resetare permite invalidarea/regenerarea schimbului curent atunci când rolul dvs. permite acest lucru.

---

# 17. Operațiuni

Fila **Operațiuni** permite alegerea unui grup sau a unei echipe și afișează apoi mai multe subfile în funcție de drepturi și conținut:

- **Ordine**
- **Anunțuri**
- **Roluri**
- **Partajare între echipe**
- **Sesiuni**
- **Istoric**

## 17.1 Ordine

Afișează ordinele active cu:

- tip;
- prioritate;
- text;
- starea răspunsului.

Atunci când este necesară o confirmare, butonul **Primit** permite confirmarea primirii din această vizualizare.

## 17.2 Anunțuri

Afișează anunțurile active.

Fiecare anunț poate include:

- tip;
- text;
- starea de fixare;
- butonul **Confirmă primirea**.

Un membru autorizat poate crea un anunț alegând:

### Tipuri

- Informație
- Important
- Informație de grup
- Informație de sesiune
- Regulă a activității
- Coordonare

### Expirare

- 15 min
- 1 h
- 4 h
- 24 h
- Fără expirare

O casetă permite **Fixarea anunțului**.

---

# 18. Campanii de roluri

Campaniile de roluri permit deschiderea temporară a unor locuri pentru un anumit rol.

Acestea se găsesc în:

**Meniul grupului/echipei > Operațiuni > Roluri**

## 18.1 Alăturarea la o campanie

O campanie deschisă afișează:

- rolul;
- starea sa;
- modul;
- numărul de locuri deja atribuite / capacitatea.

Apăsați **Alătură-te** pentru a solicita rolul.

## 18.2 Moduri de campanie

### Primele cereri valide — `FIRST_VALID`

Primele cereri eligibile sunt atribuite automat până la atingerea capacității disponibile.

Codul permite acest mod numai pentru rolurile considerate neprivilegiate.

### Validare de către un responsabil — `ADMIN_APPROVAL`

Cererile rămân în așteptare până la aprobarea de către un responsabil.

Administratorul vede **Cereri în așteptare** și poate apăsa **Aprobă** pentru fiecare participant.

## 18.3 Crearea unei campanii

Dacă rolul dvs. permite gestionarea campaniilor:

1. alegeți **Rolul**;
2. alegeți **Modul** propus pentru acel rol;
3. alegeți numărul de **Locuri** de la 1 la 64;
4. alegeți **Durata**:
   - 15 min;
   - 1 h;
   - 4 h;
   - 24 h;
5. apăsați **Deschide o campanie**.

## 18.4 Închiderea unei campanii

Un administrator autorizat poate apăsa **Închide**.

## 18.5 Retragerea cererii proprii

În **Istoric**, o cerere încă în așteptare poate afișa **Retrage cererea mea**.

## 18.6 Roluri disponibile pentru campanii

Codul expune campaniilor, în funcție de context și drepturile dvs.:

- Cercetaș de grup;
- Cercetaș de echipă;
- Releu;
- Acoperire;
- Asalt.

Rolul de Șef de grup nu este atribuit niciodată prin campanie.

---

# 19. Sesiuni

O sesiune reprezintă o perioadă operațională limitată în cadrul grupului.

## 19.1 Crearea unei sesiuni

Din **Gestionare**, dacă aveți permisiunea:

1. deschideți secțiunea **Sesiune**;
2. introduceți durata în minute;
3. durata maximă afișată este de **56 de zile**;
4. apăsați **Creează o sesiune**.

## 19.2 Consultarea sesiunilor

În **Operațiuni > Sesiuni**, LETCOOR afișează:

- data creării;
- starea: deschisă/încheiată sau starea atribuirii;
- echipa dvs., dacă există;
- sfârșitul planificat.

## 19.3 Gestionarea unei sesiuni

Responsabilul autorizat poate:

- adăuga **+ 1 h**;
- **Încheia** sesiunea.

## 19.4 Roluri și atribuiri în timpul unei sesiuni

În **Participanți**, puteți selecta o sesiune administrată, atribui roluri limitate la acea sesiune și repartiza participanții într-o echipă/stare.

---

# 20. Partajarea datelor între echipe

Această funcție este disponibilă dintr-o **echipă** în:

**Operațiuni > Partajare între echipe**

Nu oferă automat acces la conținutul privat al unei alte echipe. Utilizează o ofertă de partajare creată și acceptată în mod explicit.

## 20.1 Propunerea unei partajări

1. Alegeți **Echipa țintă**.
2. Alegeți **Datele partajate**.
3. Alegeți precizia.
4. Reglați frecvența.
5. Reglați expirarea.
6. Apăsați **Propune partajarea**.

## 20.2 Clase de date disponibile

- Prezența generală a echipei
- Semnal
- Starea echipei
- Poziție precisă
- Istoricul deplasărilor

## 20.3 Precizie

- Privire de ansamblu / agregată
- Aproximativă
- Precisă

Dacă este selectată **Poziție precisă**, precizia devine obligatoriu precisă în interfață.

## 20.4 Frecvență

Reglabilă între **5 și 300 de secunde**, în pași de 5 secunde.

## 20.5 Expirare

- 15 min
- 1 h
- 4 h
- 24 h

## 20.6 Acceptare sau revocare

Echipa destinatară autorizată poate apăsa **Acceptă**.

O ofertă sau o partajare poate fi **Revocată** de partea care are permisiunea corespunzătoare.

---

# 21. Gestionarea grupului și a echipelor

Fila **Gestionare** centralizează funcțiile administrative.

## 21.1 Selectarea unui spațiu

Selectorul **Grup sau echipă** permite alegerea spațiului care trebuie administrat.

## 21.2 Alăturarea la o echipă existentă

Atunci când acțiunea este autorizată, o echipă poate oferi:

- **Alătură-te**;
- **Recuperează accesul** atunci când calitatea de membru există, dar cheile trebuie recuperate.

## 21.3 Părăsirea unei echipe

Apăsați **Părăsește echipa** și verificați rezumatul înainte de confirmare.

## 21.4 Dizolvarea unei echipe

Un responsabil autorizat vede **Dizolvă echipa**.

Confirmarea indică faptul că:

- echipa va fi dizolvată pentru membrii săi;
- membrii rămân în grup;
- celelalte dispozitive aplică dizolvarea atunci când o primesc.

## 21.5 Părăsirea unui grup

Un membru obișnuit poate pregăti un plan de plecare și apoi îl poate confirma.

Dacă participantul conduce echipe, LETCOOR poate fi nevoit să dizolve acele echipe înainte de plecare, conform planului calculat de Core.

## 21.6 Dizolvarea unui grup

Șeful de grup autorizat poate utiliza **Dizolvă grupul**.

Confirmarea avertizează că grupul și echipele sale vor fi dizolvate. Dispozitivele offline vor trebui să se reconecteze pentru a primi dizolvarea.

## 21.7 Alăturarea la un grup nou sau la o echipă nouă

Pagina **Gestionare** conține și un bloc **Alătură-te unui grup sau unei echipe** cu același sistem de invitație ca la integrarea inițială.

## 21.8 Invitații în așteptare

Atunci când Core expune invitații de acceptat, acestea apar cu un buton **Acceptă** până la expirare.

## 21.9 Starea echipei

Responsabilul autorizat poate publica:

- Pregătită
- În deplasare
- Pe poziție
- În adunare
- Are nevoie de ajutor
- Deconectată

## 21.10 Politica de poziție exactă

Într-o echipă, un responsabil autorizat poate alege:

- **Permite**;
- **Refuză**

pentru politica de poziție exactă a echipei.

## 21.11 Transferul administrării

Dacă aveți un transfer de administrare în așteptare, secțiunea afișează **Acceptă transferul administrării**.

---

# 22. Limite de publicare

În **Gestionare**, responsabilii autorizați pot configura limitele de publicare ale grupului sau ale echipei.

Limitele pot fi definite:

- implicit;
- pentru un anumit membru.

Parametrii expuși în prezent:

- numărul de alerte de siguranță active;
- semnalări pe minut;
- semnalări la 4 minute.

Valorile formularului sunt cuprinse între 1 și 1000.

---

# 23. Localizare

Pictograma **Localizare** apare pe hartă atunci când platforma furnizează localizare nativă.

## 23.1 Activarea partajării

1. Deschideți **Localizare**.
2. Selectați **Partajează localizarea mea**.
3. Reglați precizia.

LETCOOR republică periodic prezența cât timp partajarea este activă și aplicația poate obține poziția.

## 23.2 Precizie

Cursorul merge de la **0 m la 1 km**.

- **0 m**: precizia disponibilă pe dispozitiv, fără deplasare adăugată de LETCOOR.
- valoare mai mare: poziția partajată este deplasată aleatoriu în interiorul razei alese.

## 23.3 Oprirea partajării

Selectați **Nu partaja localizarea mea**.

Partajarea este oprită și atunci când contextul se schimbă sau când aplicația întrerupe prezența conform ciclului său de viață.

## 23.4 Stări afișate

- Se obține localizarea…
- Partajare activă cu grupul dvs.
- Partajare în așteptarea reluării
- Localizare nepartajată

> Partajarea localizării nu este obligatorie pentru a vă alătura unui grup, a utiliza harta, a trimite ordine sau a utiliza rețeaua mesh.

---

# 24. Notificări

Atingeți **clopoțelul** din partea de sus a ecranului.

Centrul de notificări reunește:

- evenimente ale grupului;
- modificări ale conexiunii/transportului;
- notificări de sistem LETCOOR.

Indicatorul arată numărul de notificări necitite.

## 24.1 Citire

Notificările sunt marcate ca citite atunci când devin suficient de vizibile în listă sau când este consultată secțiunea corespunzătoare.

## 24.2 Navigare

Atingerea unei notificări poate deschide:

- secțiunea Participanți;
- Echipe;
- Operațiuni;
- un obiect de pe hartă;
- panoul Comandament.

## 24.3 Notificări de sistem

Setările clopoțelului permit activarea/dezactivarea notificărilor native de sistem atunci când platforma permite acest lucru.

---

# 25. Hărți offline

Deschideți:

**Meniul grupului/echipei > Setări > Hărți offline**

## 25.1 Selectarea unei zone

1. Apăsați **Selectează plăcile pe hartă**.
2. LETCOOR închide panoul și afișează o grilă pe hartă.
3. Atingeți celulele care trebuie păstrate.
4. Contorul indică numărul de celule selectate dintr-un maximum de 20.
5. Apăsați **Validează** pentru a reveni la setări sau **Anulează**.

## 25.2 Nivel de detaliu

Meniul **Detaliu** permite selectarea unui nivel de zoom de la 3 la 14.

O zonă prea mare la un nivel ridicat de detaliu poate fi refuzată. Interfața solicită atunci reducerea nivelului de detaliu sau alegerea unor celule mai mici.

## 25.3 Instalare

După selectarea celulelor:

1. apăsați **Instalează celulele selectate**;
2. urmăriți progresul;
3. puteți **Anula descărcarea**.

## 25.4 Ștergerea unei hărți

Hărțile instalate sunt listate cu nivelul de zoom și dimensiunea lor. Apăsați **Șterge** pentru a elibera spațiu.

---

# 26. Conexiunea la rețea și funcționarea offline

LETCOOR poate utiliza mai multe transporturi pentru aceeași rețea logică.

Interfața recunoaște în special:

- **Internet direct**;
- **Internet prin releu**;
- **Rețea locală (LAN)**;
- **Wi‑Fi local**;
- **Wi‑Fi Direct**;
- **Bluetooth**.

## 26.1 Mesh logic

LETCOOR nu impune ca fiecare membru să fie conectat direct la toți ceilalți.

Exemplu:

```text
Telefon A ↔ Telefon B ↔ Telefon C ↔ Telefon D
```

Un eveniment autorizat poate fi retransmis între perechi în funcție de topologie și de regulile de acoperire ale grupului/echipei.

Transportul fizic și identitatea LETCOOR sunt separate: o pereche rămâne identificată prin identitatea sa LETCOOR chiar dacă ruta de rețea se schimbă.

## 26.2 Fără Internet

Pentru a maximiza șansele de funcționare fără Internet:

- activați Wi‑Fi;
- activați Bluetooth;
- permiteți dispozitivele din apropiere;
- permiteți rețeaua locală dacă Android solicită acest lucru;
- acceptați vizibilitatea/asocierea de sistem atunci când LETCOOR o solicită;
- mențineți LETCOOR în prim-plan în timpul primei conectări;
- apropiați dispozitivele în timpul bootstrap-ului inițial;
- nu refuzați dialogurile de sistem necesare pentru comunicațiile radio de proximitate.

## 26.3 Starea transporturilor de proximitate

LETCOOR poate afișa separat:

- Wi‑Fi local;
- Wi‑Fi Direct;
- Bluetooth;

cu stări precum:

- permisiune necesară;
- activare necesară;
- inițializare;
- pregătit;
- căutare;
- pereche găsită;
- conectare;
- grup format;
- autentificare LETCOOR;
- conectat;
- recuperare;
- indisponibil.

## 26.4 Wi‑Fi Direct ocupat

Dacă Android indică faptul că Wi‑Fi Direct este ocupat, LETCOOR poate încerca o recuperare. Ecranul de informații Wi‑Fi Direct recomandă, printre altele, să verificați:

- dacă Wi‑Fi este activ;
- dacă partajarea conexiunii/hotspotul nu intră în conflict cu Wi‑Fi Direct;
- dacă nu există deja o altă căutare/conexiune Wi‑Fi Direct în curs.

## 26.5 Rețeaua poate schimba transportul

Starea din partea de sus a ecranului poate afișa diferite transporturi în timpul sesiunii. LETCOOR poate avea rute alternative către o pereche și poate utiliza ruta disponibilă în funcție de starea rețelei.

---

# 27. Confidențialitate, blocare și recuperare

LETCOOR aplică mai multe mecanisme de protecție atunci când datele private ale unui grup nu mai pot fi verificate cu ajutorul altor membri.

## 27.1 Blocare după absență

Codul interfeței prevede un ecran:

**Sesiune blocată după un minut de absență.**

Apăsați **Reconectează-te** pentru a recăpăta accesul.

## 27.2 Verificarea conexiunii cu membrii

Atunci când este necesară o recuperare de confidențialitate, LETCOOR afișează:

**Se verifică conexiunea cu membrii…**

Încearcă să găsească un membru accesibil și poate afișa detaliile transporturilor de proximitate.

## 27.3 Ștergere locală automată

Pentru anumite grupuri configurate cu recuperare automată, dacă reconectarea nu este posibilă în perioada prevăzută, datele locale ale grupului pot fi șterse **după verificare**.

Interfața actuală anunță un termen de douăzeci de minute pentru grupurile vizate.

Atunci când opțiunea este disponibilă, puteți:

- șterge/reseta datele locale;
- sau alege **Păstrează datele pe propriul meu risc**, ceea ce dezactivează ștergerea automată pentru acest context.

LETCOOR avertizează că păstrarea acestor date poate crește riscul în cazul compromiterii fizice a dispozitivului.

## 27.4 Protecție desktop

Pe desktop, vizualizarea privată poate fi ascunsă/estompată atunci când fereastra pierde focalizarea și apoi reîmprospătată înainte de a fi afișată din nou.

---

# 28. Roluri disponibile

Modelul de domeniu LETCOOR definește nouă roluri.

| Rol | Funcție generală în codul actual |
|---|---|
| **Administrator de grup** (`GROUP_ADMIN`) | Administrarea grupului, crearea echipelor și sesiunilor, gestionarea membrilor/rolurilor, campanii, dizolvare, transferul administrării, anunțuri. |
| **Coordonator de grup** (`GROUP_LEADER`) | Coordonare la nivel de grup, ordine/obiective/semnalări de grup, campanii și anunțuri în funcție de permisiuni. |
| **Șef de echipă** (`TEAM_LEADER`) | Ordine/obiective/puncte de întâlnire/starea echipei sale, partajare între echipe, anunțuri, campanii de echipă. |
| **Cercetaș de grup** (`GROUP_SCOUT`) | Semnalare și confirmare/promovare la nivel de grup în funcție de permisiuni. |
| **Cercetaș de echipă** (`TEAM_SCOUT`) | Raport/semnalare de echipă, confirmare și promovare în funcție de permisiuni. |
| **Releu** (`TRANSMITTER`) | Capacitate de retransmisie prevăzută de domeniu și publicarea anumitor prezențe rezumate în funcție de politică; acest rol nu acordă acces la datele private ale altor echipe. |
| **Acoperire** (`COVER`) | Etichetă operațională cu capabilitățile de bază ale membrului. |
| **Asalt** (`ATTACKER`) | Etichetă operațională cu capabilitățile de bază ale membrului. |
| **Membru** (`MEMBER`) | Capabilități de bază: semnalare normală în echipa sa atunci când este permisă, alertă de siguranță, răspuns la ordine, prezență autorizată și participare la campanii. |

> Permisiunile sunt calculate de Core și sunt aditive. Interfața afișează numai acțiunile autorizate efectiv. Apartenența la un grup nu oferă automat acces la datele private ale tuturor echipelor sale.

---

# 29. Sfaturi de pregătire înaintea unei activități

Pentru utilizare reală, în special într-o zonă unde Internetul poate fi slab:

1. Instalați aceeași versiune LETCOOR pe toate dispozitivele.
2. Creați grupul înainte de începerea activității.
3. Faceți ca participanții să se alăture cât timp sunt încă fizic aproape unii de alții.
4. Acceptați permisiunile de proximitate pe fiecare dispozitiv Android.
5. Activați Bluetooth și Wi‑Fi.
6. Testați cel puțin o conexiune fără date mobile dacă funcționarea offline este importantă.
7. Creați echipele și atribuiți șefii înainte de dispersare.
8. Deschideți o sesiune dacă doriți roluri/atribuiri de sesiune și istoricul corespunzător.
9. Descărcați hărțile offline necesare înainte de a pierde Internetul.
10. Verificați dacă participanții știu să deschidă:
    - Notificări;
    - Comandament;
    - echipa lor;
    - funcția Alertă de siguranță.
11. Activați partajarea localizării numai dacă doriți cu adevărat să o publicați.

---

# 30. Depanare

## Cele două dispozitive nu se văd offline

Verificați pe ambele dispozitive:

- Wi‑Fi activat;
- Bluetooth activat;
- permisiunile **Dispozitive din apropiere** acordate;
- permisiunea pentru rețeaua locală acordată dacă Android o solicită;
- aplicația vizibilă/detectabilă dacă sistemul cere confirmare;
- LETCOOR în prim-plan în timpul căutării inițiale.

Dacă Android deschide setările de localizare, activați serviciul de localizare pentru a maximiza compatibilitatea descoperirii. Acest lucru nu activează partajarea poziției LETCOOR.

## „Wi‑Fi Direct indisponibil” sau „ocupat”

- dezactivați temporar partajarea manuală a conexiunii/hotspotului;
- așteptați câteva secunde;
- relansați încercarea;
- verificați dacă nu este activă o altă aplicație sau conexiune Wi‑Fi Direct.

## Codul QR nu funcționează

- așteptați până când toate părțile codului QR au fost citite;
- apropiați ecranele;
- creșteți luminozitatea ecranului pe care este afișat QR-ul;
- utilizați cursorul de zoom al camerei;
- utilizați linkul în locul QR-ului dacă este necesar.

## Accesul la cameră este refuzat

- utilizați linkul;
- sau deschideți setările camerei Windows/Android din LETCOOR atunci când este disponibil butonul.

## Linkul este acceptat, dar conexiunea expiră

- verificați Internetul sau proximitatea;
- apropiați dispozitivele;
- activați Wi‑Fi și Bluetooth;
- acceptați dialogurile de sistem;
- apăsați **Reîncearcă** atunci când apare butonul.

## Sunt în grup, dar nu într-o echipă

Deschideți:

**Context > Echipe** sau **Gestionare**.

Dacă echipa permite alăturarea, utilizați **Alătură-te**. O invitație de echipă poate, de asemenea, admite direct participantul în grupul părinte și în echipa vizată, în funcție de tichetul primit.

## „Calitate de membru înregistrată · recepționarea cheilor este în curs”

Calitatea de membru este cunoscută, dar accesul criptografic la echipă nu este încă pregătit. Mențineți dispozitivele conectate pentru a permite recuperarea/sincronizarea cheilor. Dacă butonul **Recuperează accesul** apare în Gestionare, utilizați-l.

## Un obiect nu este vizibil

Verificați:

- grupul/echipa selectată;
- permisiunile dvs.;
- expirarea obiectului;
- sincronizarea rețelei;
- faptul că un obiect privat al unei echipe nu este automat vizibil celorlalte echipe.

## Localizarea nu este afișată

- verificați permisiunea de localizare;
- verificați dacă este selectat **Partajează localizarea mea**;
- verificați grupul curent;
- așteptați următoarea publicare periodică;
- verificați dacă politica echipei permite precizia necesară.

---

# 31. Rezumat rapid

## Pentru a intra în LETCOOR

```text
Dispozitiv care invită
  ↓
Invită
  ↓
QR sau link
  ↓
Dispozitivul invitat importă
  ↓
Dispozitivul invitat produce un răspuns
  ↓
Dispozitivul care invită scanează/lipește răspunsul
  ↓
Conexiune + autentificare + admitere
```

## Pentru a crea ceva pe hartă

```text
Apăsare lungă pe hartă
  ↓
Semnalare / Obiectiv / Ordin / Punct de adunare / Alertă de siguranță
  ↓
Completați formularul
  ↓
Alegeți zona / durata dacă este disponibilă
  ↓
Publică
```

## Pentru a gestiona un grup

```text
Numele grupului în stânga sus
  ↓
Context | Echipe | Participanți | Invită | Operațiuni | Gestionare | Setări
```

## Pentru o campanie de roluri

```text
Operațiuni
  ↓
Roluri
  ↓
Alege rolul + modul + locurile + durata
  ↓
Deschide o campanie
  ↓
Membrii se alătură
  ↓
Atribuire automată sau validare de către un responsabil, în funcție de mod
```

## Pentru funcționare fără Internet

```text
Wi‑Fi ACTIVAT
Bluetooth ACTIVAT
Permisiuni de proximitate acordate
Rețea locală permisă dacă este solicitată
Asociere/vizibilitate acceptată dacă este solicitată
Dispozitive apropiate la primul contact
LETCOOR deschis în prim-plan
```

LETCOOR poate apoi utiliza transporturile disponibile și retransmite informațiile autorizate între perechi în funcție de topologia rețelei mesh.

---

**LETCOOR 1.0.0 — Documentație pentru utilizator**
