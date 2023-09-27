## Контрольная работа 26.09.2023.
### Вывести все записи из таблицы "Студенты"
```sql
SELECT * FROM students;
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/937b1cd7-cb2d-4bba-9366-f06800f044d0)

### Вывести имена и фамилии всех студентов старше 21 года
```sql
SELECT firstname, lastname 
FROM students WHERE age > 21;
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/3c6879c0-91b3-46fc-92a7-ce6b0e781326)

###  Вывести список всех курсов
```sql
SELECT coursename FROM courses;
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/56ef62b2-7988-40a1-b735-0b22f1c05f23)


### Вывести имена и фамилии студентов, которые учатся на курсе "Математика"
```sql
SELECT firstname, lastname FROM students
JOIN studentcourses ON studentcourses.studentid = students.studentid
WHERE courseid = (SELECT courseid FROM courses WHERE coursename = 'Математика');
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/0a7a2bb2-0ed4-42e3-b17b-e30a3d08fcd5)

###  Вывести имена и фамилии студентов, возраст которых составляет 20 лет, и которые учатся на курсе "История"
```sql
SELECT firstname, lastname FROM students
JOIN studentcourses ON studentcourses.studentid = students.studentid
WHERE courseid = (SELECT courseid FROM courses WHERE coursename = 'История') AND age = 20;
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/178335af-f917-480a-9e2e-b131ad49f6df)

###   Вывести количество студентов на каждом курсе
```sql
SELECT coursename, (SELECT COUNT(studentid) FROM studentcourses
WHERE c.courseid = studentcourses.courseid) FROM courses c; 
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/e514527a-da1a-42d4-919a-0ebc94aacdd3)


### Вывести средний возраст студентов
```sql
SELECT AVG(age) AS age FROM students;
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/f44285ca-1d28-4695-a546-437ee4e5643e)

## Вывести имена и фамилии студентов, которые не учатся ни на одном из курсов
```sql
SELECT firstname, lastname, studentid FROM students
WHERE studentid not IN (SELECT studentid FROM studentcourses);
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/d81a5e4d-f8c1-4908-ab42-78d63a9aa984)

## Вывести список курсов и количество студентов на каждом курсе, даже если на курсе нет студентов
```sql
SELECT coursename, (SELECT count(studentid) FROM studentcourses WHERE c.courseid = studentcourses.courseid) FROM courses c;
```



