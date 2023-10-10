## Задание №5 19.09.2023
### №1
```sql
SELECT person.id, person.name, "age", "gender", "address", pizzeria.id, pizzeria.name, "rating" FROM "person", "pizzeria"
ORDER BY person.id ASC;
```
![image](https://github.com/DzhigaDzhiga/-/assets/144116592/58207d3c-7e40-4688-b76f-97dbcbe6d769)

```sql
SELECT person.id, person.name, "age", "gender", "address", pizzeria.id, pizzeria.name, "rating" FROM "person", "pizzeria"
ORDER BY pizzeria.id ASC;
```
![image](https://github.com/DzhigaDzhiga/-/assets/144116592/e18321bd-cb29-438c-b3d8-e01a514d21e1)

### №2
```sql
SELECT "order_date" AS action_date, "name" FROM "person_order", "person"
WHERE "order_date" IN (SELECT "visit_date" FROM "person_visits") AND person_order.person_id = person.id
ORDER BY "order_date" ASC;
```
![image](https://github.com/DzhigaDzhiga/-/assets/144116592/eb89b9e4-4139-4d63-bf79-04664ef25571)

```sql
SELECT "order_date" AS action_date, "name" FROM "person_order", "person"
WHERE "order_date" IN (SELECT "visit_date" FROM "person_visits") AND person_order.person_id = person.id
ORDER BY "name" DESC;
```
![image](https://github.com/DzhigaDzhiga/-/assets/144116592/5c0169aa-edaf-40ef-8141-32b2f8da7d9a)

### №3
```sql
SELECT "order_date", ("name" || ' (age:' || "age" || ')') AS person_information FROM "person_order"
JOIN "person" ON "person_id" = person.id
ORDER BY "order_date" ASC, "person_information" ASC;
```
![image](https://github.com/DzhigaDzhiga/-/assets/144116592/2493fb1e-19e6-49a6-9493-f89e9e648b6e)

### №4
```sql
SELECT order_date, (name || ' (age:' || age || ')') AS person_information FROM person_order NATURAL JOIN person
ORDER BY order_date ASC, person_information ASC;
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/fe00065a-fbb0-4fe3-9b39-8f070b1741e4)

### №5
```sql
SELECT name FROM pizzeria
WHERE id NOT IN
(SELECT pizzeria_id FROM person_visits);
```
![image](https://github.com/DzhigaDzhiga/No-Private-Life/assets/144116592/8271141f-8000-4590-883f-9620f9ccaa15)


## Задание №6 20.09.2023
### №1
```sql

```
