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


### Вывести средний возраст студентов
```sql

```
