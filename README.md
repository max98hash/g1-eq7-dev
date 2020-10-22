# Définition

- **Un utilisateur** est une personne physique capable de créer et gérer des projet.

# Architecture

// TODO décrire architecture Hexagonale

```
src
|- Domain
|    |- Entity
|    |- Port
|- App
|    |- useCase
|- Infra
|- UI

```

# Backlog

| ID  | Description                                                                                                                                                                                                                                                                           | Difficulté | Importance | Sprint |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| ---------- | ---------- | ------ |
| 1   | **En tant qu'** utilisateur **je souhaite** pouvoir créer un projet. Un projet comporte un nom, une date de début, une date de fin estimée (possiblement null? ), un depot git, une description, un état **afin de** pouvoir saisir et plannifier mes issues, tasks, tests et release | 1          |            |        |
| 2   | **En tant que qu'** utilisateur **je souhaite** créer des issues (descrition, type, id généré automatiquement, état = "ouvert" par défaut) **afin de** pouvoir les organiser et réaliser leur suivie.                                                                                 | 1          |            |        |
| 3   | **En tant qu'** utilisateur, **je souhaite** pouvoir modifier l'état d'une issue à l'aide d'une liste d'état (OUVERT, EN COURS, TESTABLE, TESTEE, CLOTUREE)                                                                                                                           | 1          |            |        |
| 4   | **En tant qu'** utilisateur, **je souhaite** créer des tâches (id, description, lien avec issues, état par défaut en TODO) **afin de** de pouvoir ensuite les réaliser                                                                                                                | 1          |            |        |
| 5   | **En tant qu'** utilisateur, **je souhaite** pouvoir gérer mes tâches sous la forme d'un kanban (TODO, DOING, TOTEST, DONE) **afin d'** assurer le suivi des tâches.                                                                                                                  | 2          |            |        |
| 6   | **En tant qu'** utilisateur, **je souhaite** pouvoir créer différents sprints (date de début, date de fin, id générér automatiquement ) afin de pouvoir plus tard plannifier mes différentes issues.                                                                                  | 1          |            |        |
| 7   | **En tant qu’** utilisateur, **je souhaite** pouvoir ajouter une issue dans un sprint à l'aide d'un drag & drop ou à l'aide d'une liste **afin de** plannifier mes issues.                                                                                                            | 1          |            |        |
| 22  | **En tant qu'** utilisateur **je souhaite** pouvoir drag & drop une issues dans des colonnes FACILE, MOYENNE, DUR **afin de** pouvoir généré la difficulté de chaque issue                                                                                                            | 2          |            |        |
| 26  | **En tant que** PO **je souhaite** pouvoir drag & drop une issue dans des colonnes d'importance HAUTE, MOYENNE, FAIBLE **afin de** pouvoir générer l'importance de chaque issue                                                                                                       | 2          |            |        |
| 8   | **En tant qu’** utilisateur **je souhaite** pouvoir créer un Pert pour le projet global et un pour chaque sprint **afin de** pourvoir organiser le développement                                                                                                                      | 5          |            |        |
| 9   | **En tant qu'** utilisateur **je souhaite** pouvoir organiser mes tâches chronologiquement dans un diagramme via un drag and drop **afin de** visualiser un calendrier des tâches                                                                                                     | 3          |            |        |
| 10  | **En tant qu’** utilisateur **je souhaite** pouvoir créer un profil (nom, prénom, mail) **afin de** pouvoir assigner un profil à des tâches                                                                                                                                           | 1          |            |        |
| 11  | **En tant qu'** utilisateur, **je souhaite** pouvoir enregistrer des tests E2E **afin de** pouvoir valider le fonctionnement du front mais aussi garantir son intégration avec le back-office                                                                                         | 2          |            |        |
| 12  | **En tant qu'** utilisateur, **je souhaite** pouvoir créer une page release qui contiendrait le nom, la version, lien vers le fichier, la vidéo, la page d'installation, la liste des issues présentes dans la release,la date **afin de** pouvoir les integrer                       | 2          |            |        |
| 13  | **En tant qu'** utilisateur, **je souhaite** pouvoir signaler un bug présent sur la release directement sur l'application **afin de** pouvoir faire les corrections ultérieurement                                                                                                    | 1          |            |        |
| 14  | **En tant qu'** utilisateur, **je souhaite** pouvoir uploader une vidéo de démonstration sur une release **afin de** l'expliquer et montrer son fonctionnement                                                                                                                        | 1          |            |        |
| 15  | **En tant qu'** utilisateur je souhaite** pourvoir télécharger une release présente sur la page des releases **afin de** pouvoir la partager ou l'integrer à son projet                                                                                                               | 1          |            |	 |
| 16  | **En tant qu'** utilisateur **je souhaite** pouvoir ajouter un test (nom, tâches associées) dans mon projet via un bouton **afin de** pouvoir définir si les tâches associées sont terminées ou non                                                                                   | 1          |            |        |
| 17  | **En tant qu'** utilisateur **je souhaite** définir si un test du projet est : "Pas encore exécuté", "Réussi" ou "Échoué" **afin de** savoir l'avancement de nos tests                                                                                                                | 1          |            |        |
| 18  | **En tant qu'** utilisateur **je souhaite** lier mon test à un fichier de test sur github **afin de** récupérer son scénario et sa description pour l'ajouter à notre test                                                                                                            | 3          |            |        |
| 19  | **En tant qu'** utilisateur **je souhaite** ajouter à mon test, via un bouton ou une zone de drag and drop, une vidéo de son  exécution **afin de** pouvoir revoir rapidement le test sans le relancer, ou voir le test d'une ancienne version                                        | 1          |            |        |
| 20  | **En tant qu'** utilisateur **je souhaite** pouvoir définir chaque étape d'une tâche comme effectuée ou non grâce à une case cochable **afin d'** actualiser son pourcentage d'avancement                                                                                             | 3          |            |        |
| 21  | **En tant qu'** utilisateur **je souhaite** consulter une liste de toutes les releases (nom,version) sur la page de releases **afin de** récupérer l'historique et faire mon  choix                                                                                                   | 1          |            |        |
| 23  | **En tant qu'** utilsateur **je souhaite** visualiser sur la page d'acceuil du projet son avancement (tâches à effectuer cette semaine, % de complétion du sprint, des tâches, des issues, des tests) **afin d'** avoir une vision globale de l'avancement du projet                  | 1          |            |        |
| 24  | **En tant qu'** utilsateur **je souhaite** ajouter une note (titre, description) à la page d'accueil du projet **afin de** servir comme mémo ou message important à faire passer aux autres developpeurs                                                                              | 2          |            |        |
