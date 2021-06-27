# 2020p3web-own-rest-api-JanDostal
## Schéma
![Konceptuální model](/IMG_20210622_144920.jpg)
## Třídy
Akce | Metoda | Endpoint | Výsledek
---- | ------ | -------- | --------
Vytvořit novou třídu | POST | /api/classes + body | Created, Bad Request
Smazat třídu | DELETE | api/classes/{id} | Ok, Not found
Upravit třídu | PUT | api/classes/{id}/[educationalStage][graduationYear][originYear][codeDesignation?] | Ok, No Content, Not found, Bad request

## Studenti
