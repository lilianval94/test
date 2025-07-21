# Récap mini projet de Naji
Consigne -> 1 page web :
- avec un formulaire avec 5 6 champs pour créer une personne
- je valide avec ce formulaire avec "Formik"
- quand formulaire validé, afficher la ligne dans le tableau
- je peux cliquer sur n'importe quelle ligne pour modifier le champs (sauf id)
- quand tout est bon, sauvegarder la ligne dans une bdd avec CRUD

DATABASE :
Dans un terminal quand tout est bon : pg_ctl -D C:\PosgtreSQL\data start
-> sachant qu'avant j'avais fait avant : postgres --single -D C:\PosgtreSQL\data template1
-> puis j'ai créer le role postgres et l'ai rendu admin et superuser
-> j'ai créé la database "M981117"
-> puis j'ai rendu postgres owner de cette db et j'ai "grant all privileges"
-> derrière j'ai restart pour relancé le serveur
-> sur pgadmin, il faut bien remplir les champs avec le bon nom, username, mdp pour la création d'une db

Stack :
	- Frontend : React
		○ Formik
		○ Ag grid
		○ Easy Peasy
	- Backend : Spring
		○ Spring boot starter web
		○ Spring boot starter data jpa
		○ Spring boot starter security
		○ Postgresql
		○ Spring boot starter webflux
		○ Lombok
		○ Swagger models jakarta
		○ Swagger annotations
		○ Log4j
	- BDD : Postegresql

---------------------------------------------------------------------------

TO DO : FORMIK FORMULAIRE
	- Créer la classe User (nom STRING, prénom STRING, age INT, sexe ENUM, dateNaissance DATE)
	- Créer le formulaire avec "Formik" avec 5 6 champs pour créer un user
	- Pouvoir valider la création du formulaire
	- Bien vérifier que les champs sont valides
	- Si pas valide alors afficher un message d'erreur rouge au dessus du submit avec liste de ce qui va pas
	- Si valide alors création d'un objet User
	
TO DO : EASY PEASY STORE
	- Créer un store pour gérer un crud d'une liste d'objets User
	- Dans le component tableau, avoir un useEffect qui update la liste en continue
	
TO DO : AG GRID TABLEAU
	- Cette liste doit être affichée dans un tableau "ag grid" avec toutes les colonnes d'un user
	- Ajouter des filtres pour chaque colonne
	- Chaque ligne du tableau doit être modifiable en cliquant dessus
	- Toujours bien vérifier la validité d'une cellule du tableau à la modification
	- Ajouter pagination du tableau (5, 10, 50)
	- Ajouter une colonne Delete avec un bouton avec image poubelle blanche sur fond rouge, et la rendre fonctionnelle avec le store par id quand y'aura la bdd
TODO : BDD
	- Le formulaire doit sauvegarder dans une bdd un nouveau User avec un id
	- Le tableau doit lire la table User de la bdd pour afficher la liste
	- Une modification du tableau doit se faire sur la bdd aussi
	- Le delete du tableau doit être fonctionnel

BONUS
	- Ajouter une modale pour valider un Delete ou une création avec le formulaire
Ajouter des tests, je sais pas sur quoi mais voilà<img width="1277" height="1418" alt="image" src="https://github.com/user-attachments/assets/6f549b48-a2c9-4d79-8241-37b95e8fe389" />
