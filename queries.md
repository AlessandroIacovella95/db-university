# EX QUERY

<br>

## QUERY 1

```sql
-- Selezionare tutti gli studenti nati nel 1990

SELECT *
FROM `students`
WHERE YEAR(date_of_birth) = "1990";
```

## QUERY 2

```sql
-- Selezionare tutti i corsi che valgono più di 10 crediti

SELECT *
FROM `courses`
WHERE `cfu` > 10;
```

## QUERY 3

```sql
-- Selezionare tutti gli studenti che hanno più di 30 anni

SELECT *, (YEAR(CURRENT_DATE()) - YEAR(date_of_birth) -(RIGHT(CURRENT_DATE(),5) < RIGHT(date_of_birth,5))) AS età
FROM students
WHERE YEAR(CURRENT_DATE()) - YEAR(date_of_birth)-(RIGHT(CURRENT_DATE(),5) < RIGHT(date_of_birth,5)) >= 30
```

## QUERY 4

```sql
-- Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea

SELECT *
FROM `courses`
WHERE`period` = "I semestre" AND `year`= "1";
```

## QUERY 5

```sql
-- Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020

SELECT *
FROM `exams`
WHERE DATE(date) = "2020/06/20" AND TIME(hour) > "14%";
```

## QUERY 6

```sql
-- Selezionare tutti i corsi di laurea magistrale

SELECT *
FROM `degrees`
WHERE `level`LIKE "magistrale";
```

## QUERY 7

```sql
-- Da quanti dipartimenti è composta l'università?

SELECT COUNT(*) as num_departments
FROM `departments`;
```

## QUERY 8

```sql
-- Quanti sono gli insegnanti che non hanno un numero di telefono?

SELECT COUNT(*) as num_teachers
FROM `teachers`
WHERE `phone` IS NULL;
```
