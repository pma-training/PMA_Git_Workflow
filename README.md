# Overview of the PMA Git Worklow
An explanation of the PMA Git Workflow and how the PMA-DM and Country Organizations interact on GitHub (_Français ci-dessous_)

_Video:_ [Overiview of PMA Git Worklow](https://www.youtube.com/watch?v=0SCo4vHbjvY&list=PLaCCIQf3NY979c70cnegKx8Cmo3Wltkia&index=15&t=0s)

### Summary 
Provides an overview of the PMA GitHub Workflow and how the PMA DM Organization and the Country Organizations interact

#### By the end of this video, you should be able to:
- Understand the PMA Git Workflow
- Understand the relationship between PMA GitHub Organizations

### PMA DM Organization
Where all the template .do files are stored
- Access: All PMA data management staff, both in partner countries and in Baltimore
- Repository Privacy Settings: All repositories are private
- Branch Types:
  - Master Branch - The most recent versions of the .do files
  - .do file Update Branch - Where Baltiomre-based data managers make updates to .do files
- Branch Settings: All branches are protected so they cannot be deleted

### PMA Country Organization
Direct copies of the PMA DM Organization intended for country use, created through forking the repository
- Access: All data management staff in the specific country and all PMA Baltimore data management staff
- Repository Privacy Settings: All repositories are private
- Branch Types:
  - Master Branch – the most recent versions of the .do files
  - .do file Update Branch – Where country data managers make updates to .do files
    - Any change that will need to occur in multiple rounds
  - Round Branch – Created each time a new round of data collection starts
- Branch Settings: All branches are protected so they cannot be deleted

### Specific Workflows
#### Workflow if a .do file is updated in the PMA DM Organization:
1. Create a .do file update branch
2. Go to Stata, make updates to .do files, and commit updates following PMA commit standards
3. Submit a pull request from the .do file update branch to the master branch in the PMA DM Organization
    - Repository manager approves the pull request after review
4. Submit a pull request from the master branch in the PMA DM Organization to the master branch in each PMA Country Organization
    - Lead Baltimore DM for each country submits pull request
    - Lead Baltimore DM for the country OR Lead Country DM approves pull request after review
5. IF DATA COLLECTION IS IN PROGRESS
    - In PMA Country Organization, merge changes from master to round branch

#### Workflow if a .do file is updated in the PMA Country Organization:
1. Create a .do file update branch
2. Go to Stata, make updates to .do files, and commit updates following PMA commit standards
3. Submit a pull request from the .do file update branch to the master branch in the PMA Country Organization
    - Lead Baltimore DM for the country approves the pull request after review
4. IF DATA COLLECTION IS IN PROGRESS
    - In PMA Country Organization, merge changes from master to round branch
5. Submit a pull request from the master branch in the PMA Country Organization to the master branch in the PMA DM Organization
    - Lead Baltimore DM for the country OR Lead Country DM submits the pull request
    - Baltimore-based repository manager approves the pull request
6. Submit a pull request from the master branch in the PMA DM Organization to the master branch in each PMA Country Organization (not including the country that created the original edit)
    - Lead Baltimore DM for each country submits pull request
    - Lead Baltimore DM for the country OR Lead Country DM approves pull request after review
7. IF DATA COLLECTION IS IN PROGRESS
    - In PMA Country Organization, merge changes from master to round branch

### Glossary of terms:
| Term | Definition |
| ---- | ---------- |
| Branch | A branch is a parallel version of a repository that allows you to work freely without disrupting the master version of a file. PMA uses branches to update .do file content and prepare .do files for round specific data collection |
| Commit | A commit is a way to save a change to a file that also stores information on what changes were made, when and by who. PMA uses commits to systematically document changes to .do files |
| Fork | A fork is a copy of a repository that lives in a separate account or organization. Forks allow changes to be made to a repository without affecting the original, while maintain a link between the two so that pull requests can be submitted between the two. PMA forks all repositories from the PMA_DM Organization to the Country Organizations, allowing for .do file updates to be shared across organizations |
| Master | The default branch that is made each time a new repository is created. At PMA, the master branch contains the template of any give .do file. No changes should be made in the master branch |
| Merge | Takes the changes from one branch and applies them into another branch, often via a pull request. PMA uses merges to share updates to the .do file templates |
| Organization | A workspace where teams can collaborate across many projects at once. PMA uses organizations to organize .do files by purpose and country. |
| Private Repository | A repository that can only be viewed or contributed to by their creator and specified collaborators. All PMA repositories are private so no external person can access personally identifying information stored in .do files. |
| Pull Request | Proposed changes to a repository submitted by a user and accepted or rejected by the repository’s collaborators. PMA uses pull requests to integrate updates to .do files into the templates and share between countries. |
| Repository | Contains all of the project files and documentation and stores each file’s revision history. Can have multiple collaborators. PMA keeps its .do files in repositories that are organized by survey type and action |
| Tag | Active points to commits that do not move. PMA tags the final commit before releasing data products so the version of the specific .do file can be easily referenced for future use |


_________________________________________________________________

# Vue d'ensemble du flux de travail
Explication du déroulement des opérations de PMA Git et comment les Organizations PMA_DM et des pays interagissent sur GitHub

_Vidéo:_ [Vue d'ensemble du flux de travail](https://www.youtube.com/watch?v=HhrqsvtGlr8&list=PLaCCIQf3NY97bYG9q4ha8mEUlM8W7kJpE&index=15&t=0s)

### Résumé  
Aperçu du déroulement des opérations de PMA sur GitHub et comment les Organizations PMA_DM et des pays interagissent

#### A la fin de la vidéo, vous devriez être en mesure de :
- Comprendre le déroulement des opérations Git de PMA
- Comprendre la relation entre les différentes Organizations de PMA sur GitHub 


### Organisation PMA DM
Lieu où tous les modèles des dofiles sont stockés
- Accès : L’ensemble du personnel de gestion des données de PMA, autant dans les pays partenaires qu’à Baltimore 
- Paramètres de confidentialité du repository : Tous les repositories sont privés
- Types de Branches :
  - Master Branch – les dernières versions (les plus récentes) des .do files  
  - Branch de mise à jour des .do files – Là où les gestionnaires de données à Baltimore effectuent les mises à jour des .do files. 
- Paramètres des Branches : Toutes les branches sont protégées pour ne pas être effacées. 


### Orgnaisation de pays PMA
- Accès : L’ensemble du personnel de gestion des données du pays concerné et l’ensemble du personnel de données PMA à Baltimore
- Paramètres de confidentialité du repository : Tous les repositories sont privés
- Types de Branches :
  - Master Branch – les dernières versions (les plus récentes) des .do files  
  - Branch de mise à jour des dofiles – Là où les gestionnaires de données des pays effectuent les mises à jour des .do files
    - Toute modification devant avoir lieu sur plusieurs vagues 
  - Branch de la vague d’enquête – Créée à chaque fois qu’une nouvelle vague de collecte de données commence 
- Paramètres des Branches : Toutes les branches sont protégées pour ne pas être effacées


### Flux de travials spécifiques
#### Flux de travail si un .do file est mis à jour dans l'Organisation PMA_DM :
1. Créez une branch de mise à jour du .do file
2. Allez sur Stata, effectuez les mises à jour du .do file, et engagez (commit) ces mises à jour conformément aux standards de PMA 
3. Envoyez une pull request à partir de la branch de mise à jour du .do file vers la master branch dans l’Organization PMA_DM 
    - Le/la gestionnaire du repository autorise la pull request après l’avoir examinée
4. Envoyez une a pull request de la master branch de l’Organization PMA_DM vers la master branch de chaque Organization de pays
    - Le/la gestionnaire de données de chaque pays à Baltimore envoie la pull request
    - Le/la gestionnaire de données du pays à Baltimore OU le/la gestionnaire de données principal(e) dans le pays autorise la pull request après l’avoir examinée
5. SI LA COLLECTE DES DONNÉES EST EN COURS
    - Dans l’Organization de pays, fusionnez (merge) les modifications de la master à la branch de la vague d’enquête


#### Flux de travail si un .do file est mis à jour dans une Organisation de pays:
1. Créez une branch de mise à jour du .do file
2. Allez sur Stata, mettez à jour les .do files, et engagez (commit) les mises à jour conformément aux standards de PMA 
3. Envoyez une pull request à partir de la branch de mise à jour du dofile vers la master branch dans l’Organization du pays 
    - Le/la gestionnaire de données du pays à Baltimore approuve la pull request après l’avoir examinée
4. SI LA COLLECTE DES DONNÉES EST EN COURS
    - Dans l’Organization du pays, fusionnez (merge) les modifications de la master à la branch de la vague d’enquête
5. Envoyez une pull request de la master branch dans l’Organization du pays vers la master branch de l’Organization PMA_DM
    - Le/la gestionnaire de données du pays à Baltimore OU le/la gestionnaire de données principal(e) dans le pays concerné envoie la pull request
    - Le/la gestionnaire du repository basé(e) à Baltimore autorise la pull request
6. Envoyez une pull request de la master branch dans l’Organization PMA_DM vers la master branch dans chaque Organization de pays (excepté le pays qui a créé la modification) 
    - Chaque gestionnaire de données de pays à Baltimore envoie une pull request
    - Le/la gestionnaire de données du pays à Baltimore OU le/la gestionnaire de données principal(e) dans le pays autorise la pull request après l’avoir examinée
7. SI LA COLLECTE DES DONNÉES EST EN COURS
    - Dans l’organization du pays PMA, fusionnez (merge) les modifications de la master à la branch de la vague d’enquête


### Glossaire :
| Terme | Definition |
| ---- | ---------- |
| Branch | Version parallèle d’un repository permettant de travailler librement sans perturber la version master d’un fichier. PMA utilise des branches pour mettre à jour le contenu des dofiles et les préparer pour la collecte de données d’une vague d’enquête spécifique. |
| Commit | Manière de sauvegarder une modification d’un fichier en stockant aussi des informations sur les changements qui ont été faits, quand et par qui. PMA utilise des commits pour documenter systématiquement les modifications des .do files |
| Fork | Copie d’un repository vivant dans un compte ou une Organization séparé(e). Les forks permettent d’apporter des modifications à un repository sans en affecter l’original, tout en maintenant un lien entre les deux pour que des pull requests puissent être envoyées entre les deux. PMA créer une « fork »  entre tous les repositories de l’Organization PMA_DM et les Organizations des pays, permettant ainsi de partager les mises à jour des .do files entre les Organizations |
| Master | Branch par défaut générée à chaque fois qu’un nouveau repository est créé. À PMA, la master branch contient le modèle de chaque .do file. Aucune modification ne devrait être apportée à la master branch |
| Merge | Applique les modifications d’une branch à une autre branch, souvent via une pull request. PMA utilise la fonction merge pour partager des mises à jour de modèles de .do files |
| Organization | Espace de travail où les équipes peuvent collaborer sur différents projets en même temps. PMA utilise des organizations pour organiser ses .do files selon leur objectif et par pays |
| Private Repository | Un repository qui ne pouvant être visionné que par son créateur ou ses collaborateurs, ou auquel seuls son créateur et des collaborateurs spécifiés peuvent contribuer. Tous les repositories de PMA sont privés pour qu’aucune personne externe ne puisse avoir accès aux données personnelles stockées dans les .do files |
| Pull Request | Modifications proposées pour un repository par un(e) utilisateur/trice et acceptées ou rejetées par les collaborateurs du repository. PMA utilise les pull requests pour intégrer les mises à jour des .do files aux modèles et les partager entre les pays. |
| Repository | Contient tous les fichiers et la documentation du projet, et stocke l’historique de révision de chaque fichier. Peut avoir plusieurs collaborateurs. PMA garde ses .do files dans des repositories organisés par type d’enquête et d’action |
| Tag | Points actifs des commits qui ne bougent pas. PMA attribue un tag au commit final avant de publier les produits de données pour que la version spécifique d’un .do file soit référencée et puisse être facilement utilisée plus tard |
