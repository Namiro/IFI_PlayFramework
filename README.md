# IFI PlayFramework

Pour commencer, clonez ce projet sur votre poste :
```
mkdir -p $HOME/ifiplayframework
cd $HOME/ifiplayframework
git clone https://github.com/Namiro/IFI_PlayFramework.git
cd $HOME/ifiplayframework/IFI_PlayFramework
```

## TP : Application CRUD
  Il s'agit d'une application Play classique CRUD en Scala, soutenue par une base de données JDBC en mémoire. Elle utilise ANORM pour l'accès à la Base de Données, pagination classique, et l'intégration avec un framework CSS (Twitter Bootstrap).

  Ce tp consiste à implémenter les actions Create, Update et Delete.

Votre but est d'appeler les méthodes des services pour pouvoir implémenter ces actions.

Pour vous faciliter les choses, une base de début est fourni.


# Builder et lancer l'application :

Pour cela, il suffit de taper la commande
```
.\sbt-dist\bin\sbt.bat run
```
ou
```
./sbt run
```

Celle ci va lancer notre serveur sbt. (ctrl+D pour éteindre)

Accéder ensuite à l'url :

[http://localhost:9000/]

An SQL script will be run on your database, cliquer sur "Apply this script now!" afin de peupler notre base de données qu'on utilisera dans ce tp


###### 1. Ajouter un étudiant :

1. Créer dans le controleur l'action "create" qui s'occupe d'afficher le formulaire d'ajout "createForm.scala.html" qui prend en paramètres studentForm et programService.options .

2. Ajouter le chemin de cette action dans le fichier routes (c'est une requête http GET) .

3. Ajouter cette action au boutton "Add a new student" dans la view "list.scala.html"

4. Compléter l'action save du controleur afin de pouvoir enregistrer un nouveau étudiant (utiliser la fonction insert du studentService)

5. Ajouter le chemin de cette action dans le fichier routes (c'est une requête http POST) .

6. Ajouter cette action au boutton "Create this student" dans la view "createForm.scala.html"

7. Ajouter l'action du bouton "Cancel" qui nous retourne vers la liste des étudiants dans la view "createForm.scala.html".

###### 2. Mettre à jour un étudiant :

1. Ajouter le chemin de l'action edit dans le fichier routes (c'est une requête http GET) .

2. Ajouter le lien vers cette action dans la view "list.scala.html" pour pouvoir afficher le formulaire d'édition quand on clique sur le nom d'un étudiant.

3. Compléter l'action update du controleur afin de pouvoir mettre à jour un étudiant (utiliser la fonction update du studentService)

4. Ajouter le chemin de l'action update dans le fichier routes (c'est une requête http POST) .

5. Ajouter cette action au boutton "Save this student" dans la view "editForm.scala.html"

6. Ajouter l'action du bouton "Cancel" qui nous retourne vers la liste des étudiants dans la view "editForm.scala.html".

###### 3. Supprimer un étudiant :

1. Créer dans le controleur l'action "delete" qui s'occupe de supprimer un étudiant(utiliser la fonction delete de studentService)

2. Ajouter le chemin de l'action delete dans le fichier routes (c'est une requête http POST) .

3. Ajouter cette action au boutton "Delete this student" dans la view "editForm.scala.html"
