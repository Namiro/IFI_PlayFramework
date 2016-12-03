# IFI PlayFramework

Pour commencer, clonez ce projet à l'adresse suivante sur votre poste :

# Builder et lancer l'application :

Pour cela, il suffit de taper la commande

`./sbt run`

si sous windows tapez

`sbt run`

Celle ci va lancer notre serveur sbt. (ctrl+D pour éteindre)

Accéder ensuite à l'url :

`http://localhost:9000/`

An SQL script will be run on your database, cliquer sur "Apply this script now!" afin de peupler notre base de données qu'on utilisera dans ce tp

# ADD A STUDENT :
1-Créer dans le controleur l'action create qui affiche le formulaire de création. ( prend en paramètre studentForm et programService.options)

2- Ajouter l'action du bouton "add a new student" qui va vous envoyer au formulaire de création :
requête http  get qui fais appel à la fonction create du contrôleur

3-Compléter la fonction save du contrôleur pour enregistrer un nouveau étudiant, avec un message de succés.

4-Ajouter l'action du button "Create this student" qui crée l’étudiant :
requête http post qui fais appel à la fonction save du contrôleur

5-Ajouter l'action du bouton "Cancel" qui nous retourne vers la liste des étudiants :
requête http post qui fais appel à la fonction list du contrôleur

# EDIT AN EXISTING STUDENT :

1- Ajouter la requête http get qui fais appel a l'action edit du contrôleur quand on clique sur un étudiant de la liste (affiche le formulaire d’édition)

2-Compléter la fonction update du contrôleur qui met à jour un étudiant (fonction update de studentService), avec un message de succés.

3- Ajouter l'action du bouton "Save this student" requête http post qui fait appel à la fonction save du contrôleur.

4-Ajouter l'action du bouton "Cancel" qui nous retourne vers la liste des étudiants :
requête http post qui fais appel à la fonction list du contrôleur

# DELETE A STUDENT :

1- Ajouter dans le controleur, l'action qui gère la suppresion d'un étdudiant à partir de son id.
2-Ajouter l'action du bouton "Delete this student" requête http post qui fais appel a la fonction delete(id) du contrôleur

# RECHERCHE :

1- Ajouter l'action du bouton Filter by name pour rechercher un étudiant qui fait appel à la fonction list du contrôleur
