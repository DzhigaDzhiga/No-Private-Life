## Задание №5 19.09.2023
№1
```sql
SELECT person.id, person.name, "age", "gender", "address", pizzeria.id, pizzeria.name, "rating" FROM "person", "pizzeria"
ORDER BY person.id ASC;
```
![image](https://github.com/DzhigaDzhiga/-/assets/144116592/6326ffa0-0661-419c-b93d-80ee2818222e)
№2
```sql
SELECT person.id, person.name, "age", "gender", "address", pizzeria.id, pizzeria.name, "rating" FROM "person", "pizzeria"
ORDER BY pizzeria.id ASC;
```
![image](https://github.com/DzhigaDzhiga/-/assets/144116592/1dda72cd-a27a-4550-aef7-48990822d2ec)
