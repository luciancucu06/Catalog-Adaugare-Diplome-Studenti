# Catalog Studenti

Aplicatie de consola dezvoltata in limbajul C destinata gestiunii evidentei studentilor, notelor si situatiei academice. Proiectul a fost realizat ca parte a activitatii practice universitare, avand ca scop aprofundarea structurilor de date, gestiunii dinamice a memoriei si lucrului cu fisiere in C.

---

## Functionalitati

- Adaugare, afisare, modificare si stergere inregistrari studenti (operatii CRUD).
- Gestionarea datelor de identificare (nume, prenume, grupa, numar matricol/ID).
- Inregistrarea notelor si calcularea automata a mediilor.
- Sortarea studentilor dupa criterii multiple (alfabetic, dupa medie sau grupa).
- Cautare si filtrare dupa nume, grupa sau identificator.
- Salvarea si incarcarea datelor pe disc (persistenta prin fisiere text sau binare).
- Eliberarea completa si corecta a memoriei alocate dinamic la iesirea din program.

---

## Tehnologii si Concepte Utilizate

- **Limbaj:** C (standard C99 / C11)
- **Mediu de dezvoltare:** Microsoft Visual Studio 2022 (compilator MSVC)
- **Structuri de date:** `struct` pentru definirea entitatii student, vectori alocati dinamic sau liste inlantuite.
- **Gestiunea memoriei:** Alocare si realocare dinamica prin functiile standard (`malloc`, `calloc`, `realloc`, `free`), prevenind memory leak-urile.
- **I/O si Persistenta:** Prelucrarea fluxurilor de intrare/iesire si a fisierelor (`stdio.h`: `fopen`, `fclose`, `fread`, `fwrite`, `fprintf`, `fscanf`).
- **Modularizare:** Organizare pe module separate cu fisiere sursa (`.c`) si headere (`.h`).

---

## Structura Proiectului

```text
Catalog Studenti/
|-- Catalog Studenti.sln          # Solutia Visual Studio
|-- Catalog Studenti/
|   |-- Catalog Studenti.vcxproj  # Configuratia proiectului C/C++
|   |-- main.c                    # Punctul de intrare si bucla meniului principal
|   |-- student.h                 # Definitiile structurilor si prototipurile functiilor
|   |-- student.c                 # Implementarea operatiilor pe studenti si calcul medii
|   |-- file_io.h                 # Prototipuri pentru salvare/incarcare date
|   |-- file_io.c                 # Implementarea persistentei pe disc
|   `-- studenti.dat / .txt       # Fisierul de date pentru persistenta (dupa caz)
`-- README.md
