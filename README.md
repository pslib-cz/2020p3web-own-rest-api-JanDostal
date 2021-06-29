# 2020p3web-own-rest-api-JanDostal
## Schéma
![Konceptuální model](/IMG_20210622_144920.jpg)
## Modely
### Třídy
Akce | Metoda | Endpoint | Výsledek
---- | ------ | -------- | --------
Vytvořit novou třídu | POST | api/classes + body | Created, Bad Request
Smazat třídu | DELETE | api/classes/{id} | No content, Not found
Upravit třídu | PUT | api/classes/{id} + body | Ok, No content, Not found, Bad request
Získat třídu podle id | GET | api/classes/{id} | Class - Ok, Not found
Získat seznam tříd podle parametrů | GET | api/classes[grade?][educationLevel?][codeDesignation?] | ICollection\<Class\> - Ok, No content, Bad request
Získat seznam tříd, které už byly ukončeny, podle úrovně vzdělání | GET | api/classes{educationLevel}/ended | ICollection\<Class\> - Ok, No content, Bad request
Získat počet studentů v třídě dle id třídy | GET | api/classes/{id}/students | int - Ok, Not found
### Studenti
Akce | Metoda | Endpoint | Výsledek
---- | ------ | -------- | --------
Vytvořit nového studenta | POST |/api/students + body | Created, Bad Request
Smazat studenta | DELETE | api/students/{pin} | No content, Not found
Upravit studenta | PUT | api/students/{pin} + body | Ok, No content, Not found, Bad request
Získat studenta podle rodného čísla | GET | api/students/{pin} | Student - Ok, Not found
Získat seznam studentů, kterým už bylo 18 let, dle id třídy | GET | api/classes/{id}/students/adult | ICollection\<Student\> - Ok, No content, Not found
Získat seznam studentů v dané třídě dle id třídy | GET | api/classes/{id}/students | ICollection\<Student\> - Ok, No content, Not found
