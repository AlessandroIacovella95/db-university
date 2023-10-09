# EX QUERY JOIN

<br>

## QUERY 1

```sql
-- Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

SELECT *
FROM `students`
INNER JOIN `degrees`
ON `degrees`.`id` = `students`.`degree_id`

WHERE `degrees`.`name` = 'Corso di Laurea in Economia';
```

<br>

## QUERY 2

```sql
-- Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

SELECT *
FROM `departments`
INNER JOIN `degrees`
ON `departments`.`id`= `degrees`.`department_id`

WHERE `departments`.`name`= 'Dipartimento di Neuroscienze'
AND `degrees`.`level` = 'magistrale';
```

<br>

## QUERY 3

```sql
-- Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

SELECT *
FROM  `courses` AS `c`
INNER JOIN `course_teacher` AS `ct`
ON `c`.`id` = `ct`.`course_id`

INNER JOIN `teachers` AS `t`
ON `t`.`id` = `ct`.`teacher_id`

WHERE `t`.`id` = 44;
```

<br>

## QUERY 4

```sql
-- Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome

SELECT *
FROM `students`

INNER JOIN `degrees`
ON  `degrees`.`id`= `students`.`degree_id`

INNER JOIN  `departments`
ON `departments`.`id` = `degrees`.`department_id`

ORDER BY `students`.`surname` ASC, `students`.`name` ASC;
```

<br>

## QUERY 5

```sql
-- Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

SELECT *
FROM `degrees`

INNER JOIN `courses`
ON `degrees`.`id`= `courses`.`degree_id`

INNER JOIN `course_teacher`
ON `courses`.`id` = `course_teacher`.`course_id`

INNER JOIN `teachers`
ON `teachers`.`id` = `course_teacher`.`teacher_id`;
```

<br>

## QUERY 6

```sql
-- Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)

SELECT *
FROM `teachers`

INNER JOIN `course_teacher`
ON `teachers`.`id` = `course_teacher`.`teacher_id`

INNER JOIN `courses`
ON `courses`.`id`= `course_teacher`.`course_id`

INNER JOIN `degrees`
ON `degrees`.`id` = `courses`.`degree_id`

INNER JOIN `departments`
ON `departments`.`id` = `degrees`.`department_id`

WHERE `departments`.`name`= "Dipartimento di Matematica";
```
