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
![image](https://github.com/DzhigaDzhiga/-/assets/144116592/e18321bd-cb29-438c-b3d8-e01a514d21e1)

