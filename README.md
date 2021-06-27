# 2020p3web-own-rest-api-JanDostal
## Schéma
![Konceptuální model](/IMG_20210622_144920.jpg)
## Modely
### Třídy
Akce | Metoda | Endpoint | Výsledek
---- | ------ | -------- | --------
Vytvořit novou třídu | POST | /api/classes + body | Created, Bad Request
Smazat třídu | DELETE | api/classes/{id}/deletion | No content, Not found
Upravit třídu | PUT | api/classes/{id} + body | Ok, No content, Not found, Bad request
Získat třídu podle id | GET | api/classes/{id} | Class - Ok, Not found
Získat seznam tříd podle parametrů | GET | api/classes[grade][educationLevel][codeDesignation?] | ICollection<Class> - Ok, No content, Bad request
Získat seznam tříd, které už byly ukončeny | GET | api/classes/ended | ICollection<Class> - Ok, No content
Získat počet tříd dle parametrů | GET | api/classes[grade?][educationLevel?][codeDesignation?]/count | int - Ok, Bad request
Získat počet studentů v třídě dle id třídy | GET | api/classes/{id}/students | int - Ok, Not found
### Studenti
