# La méthode Scrum

## Introduction

Cette méthode issue du manifeste agile est destinée à faciliter la gestion de projet. Créée en 1993 elle a depuis largement fait ses preuves et se positionne comme l'une des plus connue et utilisée. Elle repose sur un système d'itération (sprints). Pour chaque itération de développement du projet une nouvelle version est livrée. Elle se doit de répondre aux critères fonctionnels définis lors de la préparation du sprint. 

L'avantage premier de phases de développement courtes ainsi que de la livraison d'une version minimale du produit est de permettre au client d'obtenir rapidement une version minimale de son projet. Cette version est dés lors soumise aux tests et aux retours de ce dernier, permettant des ajustages en cours de développement. Contrairement aux méthodes utilisées précédement qui ne livraient que la version finie du projet, impliquant une phase de développement longue durant laquelle le client n'était pas amené à ajuster ses demandes (ajout ou suppression de fonctionnalité, bug rencontrés, expérience utilisateur en berne) au cours de la phase de développement, qui résultait en des coûts plus élevés et un temps de réalisation plus long. 

## Lexique

**Backlog:** Le backlog est un recueil des besoins du client. Il contient la liste des fonctionnalités du projet ainsi que les Users Stories. Chaque élément du backlog est classé par ordre de priorité. Une première version est créée à l'initialisation du projet, il doit être maintenu et régulièrement mis à jour par le Product Owner.

**US / Users Stories:** Ou Spécifications. Elles décrivent les interactions des utilisateurs avec le programme de façon détaillée. Par exemple "En tant qu'utilisateur non enregistré j'ai la possibilité de m'inscrire ou de me connecter".

**Planning Poker:** Il s'agit ici pour l'équipe de développement d'estimer le temps nécessaire à la réalisation d'une fonctionnalité en tenant compte de l'avis de chacun des membres de l'équipe.

**Sprint: (iterations)** Phase de développement intensive qui consiste à réaliser pour une durée déterminée le planning des fonctionnalités à implanter établi au préalable lors de la préparation du sprint. 

## Les rôles

- **Le product owner**: il s’agit du pont entre le client et l’équipe technique. Le product owner est chargé de définir le projet avec précision pour répondre au mieux aux attentes des clients et aux besoins des utilisateurs. Le product owner a également comme rôle de définir les fonctionnalités présentes lors de chaque livraison ainsi que de la validation des dites fonctionnalités pour une mise en production à la fin de chaque sprint.

- **Le scrum master:** ou le facilitateur. Il est là pour veiller au bon déroulement du projet selon ses objectifs ainsi de la réalisation des différentes activités en s’appuyant sur sa maîtrise de la méthode Scrum. Il se défini plutôt tel qu’un coach qu’un manager, le scrum master n’a pas un niveau hiérarchique supérieur aux membres de l’équipe, il s’agit même très souvent de l’un de ces membres. 

- **L'équipe de développement:** elle traduit la demande fonctionnelle en réalisation technique. Elle comprend les développeurs, designers et testeurs. 

## Déroulement

### Étape 1: préparer le projet

- Préparer le Backlog: cette tâche incombe au product owner, il doit traduire en terme de fonctionnalités / users stories, la demande du client. Il n'est pas nécessaire de produire directement une version complète du backlog, il peut être agrémenté au cours des sprints et doit être régulièrement maintenu à jour. 

- Architecture du projet: il s'agit ici de réaliser un plan souple du projet, en dessiner les grandes lignes mais permettre une flexibilité au cours des sprints. 

- Déterminer le temps aloué à chaque sprint (4 semaines maximum). Cette durée doit être réfléchie et pertinente: en effet elle sera maintenue tout au long de la réalisation du projet. Maintenir un rythme régulier permet de favoriser les automatismes et créer des repères temporels pour l'équipe de développement. 

### Étape 2: planification du sprint

En accord avec le product owner, il s'agit ici pour l'équipe de développement de sélectionner les éléments prioritaires et réalisables au sein d'une itération.

Une fois les fonctionnalités sélectionnées, un planning poker (technique d'estimation des tâches prenant en compte l'avis de chaque membre de l'équipe de développement) est réalisé, des story points sont attribués, ces story points sont basés sur la suite de Fibonacci: 0, 0.5, 1, 2, 3, 5, 8, 13, 20, 40, 100.

- 1 point équivaut à une fourchette de 2 à 4h de développement
- 3 points équivalent à 4 - 8h de développement
- 5 points équivalent à 8 - 16h de développement
- 7 points équivalent à 16 - 24h de développement
- 9 points équivalent à plus de 24h de développement

Ensuite, l'équipe de développement découpe en tâches les fonctionnalités sélectionnées. Ces tâches sont ensuite encodées dans le Sprint Backlog (système de ticket similaire à trello, il peut s'agir du logiciel Jira) et ajoutées au tableau des tâches physique (il s'agit souvent d'un mur sur lequel on appose les post-it correspondants aux tâches).


### Étape 3: le sprint

**Stand up meeting:** Durant le sprint, l'équipe de développement devra se plier au rituel quotidien de la "mêlée". Ou stand up meeting. Il s'agit d'une réunion de synchronisation rassemblant l'équipe de développement, le scrum master ainsi que le product owner. Elle se réalise **debout** en 15 minutes maximum à une heure définie (elle se doit d'être la même pour chaque jour dans l'esprit d'instaurer un cadre et une régularité) devant le tableau physique des tâches. Chaque membre de l'équipe doit répondre à 3 questions:

- "Qu'ai je fais hier?"
- "Quels sont les blocages que j'ai rencontré?"
- "Qu'est ce que je compte faire aujourd'hui?"

C'est l'occasion pour le **Scrum master** d'identifier les difficultés rencontrées et de veiller à les résoudre. Par exemple en sugérant la tutelle sous pair-programming d'un junior par un médior ou un sénior.

C'est également l'occasion de mettre à jour le tableau physique des tâches. La tâche est considérée comme terminée lorsque le code est commité, documenté, testé unitairement et par les testeurs en intégration, revu par un pair. 

### Étape 4: la Sprint review

À la fin de chaque sprint une revue est organisée. Quelles tâches ont été terminées, les fonctionnalités prévues ont elles été bien implantée? 
C'est le Product owner qui a alors la tâche d'accepter ou refuser une fonctionnalité candidate qu'il n'estimerait pas prête à la release. 

Ensuite, l'équipe de développement calcule sa **vélocité**. En additionnant les points d'estimations attribués aux fonctionnalités qui ont été acceptées. 

### Étape 5: Rétrospective

Animée par le Scrum Master, c'est l'occasion de faire le bilan du sprint. Qu'est ce qui a fonctionné ou  non? Quels étaient les obstacles rencontrés et quelles sont les solutions à y apporter lors du prochain sprint? 

Chaque membre de l'équipe reçoit une pile de post-it pour y écrire ce qu'il a relevé du sprint de positif, négatif ou confus. Ensuite il s'agit de rassembler par thématiques les post-it similaires.
Ensuite chaque membre participant se voit alouer 3 post-it qui servent de vote pour le thème du prochain sprint.

Les dysfonctionnalités ne peuvent pas toutes être réglées lors d'un seul sprint. Le but est l'amélioration continue des processus de développement de l'équipe ainsi que le bien être au sein de celle ci. Pour ce faire la sélection d'un seul problème par sprint et sa résolution est privilégié. 
