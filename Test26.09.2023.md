## Контрольная работа 26.09.2023.
### №1 Вывести все записи из таблицы "Студенты"
```sql
SELECT * FROM students;
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/937b1cd7-cb2d-4bba-9366-f06800f044d0)

### №2 Вывести имена и фамилии всех студентов старше 21 года
```sql
SELECT firstname, lastname 
FROM students WHERE age > 21;
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/3c6879c0-91b3-46fc-92a7-ce6b0e781326)

### №3 Вывести список всех курсов
```sql
SELECT coursename FROM courses;
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/56ef62b2-7988-40a1-b735-0b22f1c05f23)

### №4 Вывести имена и фамилии студентов, которые учатся на курсе "Математика"
```sql
SELECT firstname, lastname FROM students
JOIN studentcourses ON studentcourses.studentid = students.studentid
WHERE courseid = (SELECT courseid FROM courses WHERE coursename = 'Математика');
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/0a7a2bb2-0ed4-42e3-b17b-e30a3d08fcd5)

### №5 Вывести имена и фамилии студентов, возраст которых составляет 20 лет, и которые учатся на курсе "История"
```sql
SELECT firstname, lastname FROM students
JOIN studentcourses ON studentcourses.studentid = students.studentid
WHERE courseid = (SELECT courseid FROM courses WHERE coursename = 'История') AND age = 20;
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/178335af-f917-480a-9e2e-b131ad49f6df)

### №6 Вывести количество студентов на каждом курсе
```sql
SELECT coursename, (SELECT COUNT(studentid) FROM studentcourses
WHERE c.courseid = studentcourses.courseid) FROM courses c
ORDER BY count DESC; 
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/ff4f2742-e8e7-4c04-ad26-3c4e4717e2aa)

### №7 Вывести средний возраст студентов
```sql
SELECT AVG(age) AS age FROM students;
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/f44285ca-1d28-4695-a546-437ee4e5643e)

## №8 Вывести имена и фамилии студентов, которые не учатся ни на одном из курсов
```sql
SELECT firstname, lastname, studentid FROM students
WHERE studentid not IN (SELECT studentid FROM studentcourses);
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/d81a5e4d-f8c1-4908-ab42-78d63a9aa984)

## №9 Вывести список курсов и количество студентов на каждом курсе, даже если на курсе нет студентов
```sql
SELECT coursename, (SELECT count(studentid) FROM studentcourses
WHERE c.courseid = studentcourses.courseid) FROM courses c
ORDER BY count DESC; 
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/ab0044f9-1b17-4c64-8b95-006b5f736bf5)

## №10 Вывести имена и фамилии студентов, которые не старше 22 лет и учатсяна курсе "Биология"
```sql
SELECT firstname, lastname FROM students
JOIN studentcourses ON studentcourses.studentid = students.studentid
WHERE courseid = (select courseid FROM courses WHERE coursename = 'Биология') AND age >= 22;
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/1324953a-fec8-43e6-8774-175af12289f6)



