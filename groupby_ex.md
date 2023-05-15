GROUP BY

## Contare quanti iscritti ci sono stati ogni anno

SELECT COUNT(id) AS yearly_enrollments, YEAR(enrolment_date) AS year FROM students GROUP BY YEAR(enrolment_date);

## Contare gli insegnanti che hanno l'ufficio nello stesso edificio

SELECT COUNT(id) AS teachers_amount, office_address FROM teachers GROUP BY office_address;

## Calcolare la media dei voti di ogni appello d'esame

SELECT AVG(vote) AS average_vote, exam_id FROM exam_student GROUP BY exam_id;

## Contare quanti corsi di laurea ci sono per ogni dipartimento

SELECT COUNT(degrees.id) AS department_degrees, departments.name AS department_name FROM degrees JOIN departments ON degrees.department_id = departments.id GROUP BY degrees.department_id;