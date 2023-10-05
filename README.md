# Esercizio di oggi: db-university

## Traccia:

Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università:

- Sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
- Ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
- Ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
- Ogni Corso può essere tenuto da diversi Insegnanti;
- Ogni Corso prevede più appelli d'Esame;
- Ogni Studente è iscritto ad un solo Corso di Laurea;
- Ogni Studente può iscriversi a più appelli di Esame;
- Per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente.
  Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.
