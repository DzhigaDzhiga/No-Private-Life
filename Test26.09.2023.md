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


### Вывести имена и фамилии студентов, которые учатся на курсе "Математика"
```sql
SELECT firstname, lastname 
FROM students WHERE age > 21;
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/3c6879c0-91b3-46fc-92a7-ce6b0e781326)
