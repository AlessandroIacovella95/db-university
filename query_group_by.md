# EX QUERY GROUP BY

<br>

## QUERY 1

```sql
-- Contare quanti iscritti ci sono stati ogni anno

SELECT COUNT(*) as numero_studenti, YEAR(`enrolment_date`) as anno
FROM `students`
GROUP BY YEAR(`enrolment_date`);
```

<br>

## QUERY 2

```sql
-- Contare gli insegnanti che hanno l'ufficio nello stesso edificio

SELECT COUNT(*) as numero_insegnanti, `office_address`
FROM `teachers`
GROUP BY `office_address`;
```

<br>

## QUERY 3

```sql
-- Calcolare la media dei voti di ogni appello d'esame

SELECT ROUND(AVG(`vote`)) as media_voto, `exam_id`
FROM `exam_student`
GROUP BY `exam_id`;
```

<br>

## QUERY 4

```sql
--Contare quanti corsi di laurea ci sono per ogni dipartimento

SELECT COUNT(*) as numero_corsi_laurea, `department_id` as numero_dipartimento
FROM `degrees`
GROUP BY `department_id`;
```
