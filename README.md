# 2020p3web-own-rest-api-JanDostal
## Schéma
![Konceptuální model](/IMG_20210622_144920.jpg)
## Modely
### Třídy
Akce | Metoda | Endpoint | Výsledek
---- | ------ | -------- | --------
Vytvořit novou třídu | POST | api/Classes + body | Created, Bad Request
Smazat třídu | DELETE | api/Classes/{id} | No content, Not found
Upravit třídu | PUT | api/Classes/{id} + body | Ok, Not found, Bad request
Získat třídu podle id | GET | api/Classes/{id} | Class - Ok, Not found
Získat seznam tříd podle parametrů | GET | api/Classes[grade?][educationLevel?][codeDesignation?] | ICollection\<Trida\> - Ok, No content, Bad request
Získat seznam tříd, které už byly ukončeny, podle úrovně vzdělání | GET | api/Classes{educationLevel}/ended | ICollection\<Trida\> - Ok, No content, Bad request
Získat počet studentů v třídě dle id třídy | GET | api/Classes/{id}/students | int - Ok, Not found
Získat seznam studentů, kterým už bylo 18 let, dle id třídy | GET | api/Classes/{id}/Students/adult | ICollection\<Student\> - Ok, No content, Not found
Získat seznam studentů v dané třídě dle id třídy | GET | api/Classes/{id}/Students | ICollection\<Student\> - Ok, No content, Not found
### Studenti
Akce | Metoda | Endpoint | Výsledek
---- | ------ | -------- | --------
Vytvořit nového studenta | POST |/api/Students + body | Created, Bad Request
Smazat studenta | DELETE | api/Students/{pin} | No content, Not found
Upravit studenta | PUT | api/Students/{pin} + body | Ok, Not found, Bad request
Získat studenta podle rodného čísla | GET | api/Students/{pin} | Student - Ok, Not found
