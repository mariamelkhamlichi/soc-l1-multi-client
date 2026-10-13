\# Playbook — Brute Force SSH



\## 1. Objectif



Identifier, analyser et qualifier une série d’échecs de connexion SSH

sur un serveur Linux supervisé.



\## 2. Périmètre



Ce playbook s’applique aux serveurs Linux des clients Atlas Cyber Services

dans le laboratoire local SOC\_LAB.



\## 3. Déclencheur



Le playbook est déclenché lorsqu’un nombre inhabituel d’échecs

d’authentification SSH est détecté sur une période courte.



\## 4. Criticité initiale



Moyenne par défaut.



La criticité peut devenir élevée si :



\- une connexion réussie suit les échecs ;

\- un compte privilégié est ciblé ;

\- plusieurs serveurs sont concernés ;

\- une activité suspecte est observée après la connexion.





\## 5. Prérequis



\- accès aux alertes Wazuh ;

\- accès aux logs du serveur Linux ;

\- accès à `/var/log/auth.log` ou `/var/log/secure` ;

\- nom du client concerné ;

\- nom du serveur ciblé ;

\- heure de détection ;

\- procédure d’escalade L2 disponible.



\## 6. Informations à collecter



\- client concerné ;

\- serveur ciblé ;

\- adresse IP source ;

\- utilisateur ciblé ;

\- date et heure ;

\- nombre d’échecs ;

\- éventuelle connexion réussie ;

\- méthode d’authentification ;

\- autres hôtes ciblés ;

\- activité observée après une connexion réussie.



\## 7. Sources de données



\- alertes Wazuh ;

\- logs SSH Linux ;

\- journaux système ;

\- historique des connexions ;

\- inventaire des actifs ;

\- Threat Intelligence autorisée.





\## 8. Étapes de triage L1



1\. Identifier le client concerné.

2\. Identifier le serveur Linux ciblé.

3\. Vérifier l’heure de début et de fin de l’activité.

4\. Compter les échecs d’authentification.

5\. Identifier l’utilisateur ciblé.

6\. Identifier l’adresse IP source.

7\. Rechercher une connexion réussie après les échecs.

8\. Vérifier si le compte est privilégié.

9\. Rechercher d’autres serveurs ciblés.

10\. Rechercher une activité suspecte après une connexion réussie.

11\. Vérifier si l’activité peut être liée à une tâche autorisée.

12\. Collecter les preuves dans le ticket.

13\. Déterminer la qualification finale.





\## 9. Qualifications possibles



\### Faux positif



L’activité est liée à une erreur connue, un test autorisé ou une tâche

d’administration documentée.



\### Activité bénigne



Les échecs sont limités, aucune connexion ne réussit et l’utilisateur

confirme une erreur de saisie.



\### Tentative d’attaque



De nombreux échecs sont observés, sans connexion réussie ni activité

postérieure confirmée.



\### Incident confirmé



Une connexion réussie suit les échecs ou une activité suspecte est observée

après l’authentification.



\## 10. IOC à collecter



\- adresse IP source ;

\- utilisateur ciblé ;

\- serveur ciblé ;

\- date et heure ;

\- adresse IP de destination ;

\- preuve de connexion réussie ;

\- commandes exécutées après connexion ;

\- autres hôtes concernés.



\## 11. Actions L1 autorisées



\- collecter et préserver les logs ;

\- rechercher les événements associés ;

\- documenter la chronologie ;

\- vérifier l’identité de l’actif ;

\- enrichir une adresse IP de test ;

\- recommander une réinitialisation de compte ;

\- recommander un blocage selon la procédure validée ;

\- préparer une escalade vers L2.



\## 12. Actions interdites sans validation



\- supprimer des logs ;

\- modifier directement un compte ;

\- isoler un serveur sans procédure ;

\- bloquer une adresse sans autorisation ;

\- lancer des tests contre une adresse IP publique ;

\- exécuter une charge utile offensive.





\## 13. Conditions d’escalade vers L2



Escalader immédiatement si :



\- une connexion SSH réussie suit les échecs ;

\- un compte administrateur est ciblé ;

\- plusieurs serveurs sont touchés ;

\- une activité suspecte suit la connexion ;

\- un mouvement latéral est possible ;

\- un actif critique ou des données sensibles sont concernés ;

\- l’adresse IP est identifiée comme malveillante avec un niveau de confiance élevé.



\## 14. Conditions de clôture



La clôture est possible si :



\- aucune connexion réussie n’est observée ;

\- l’activité est expliquée et autorisée ;

\- un seul actif est concerné ;

\- aucun événement suspect associé n’est trouvé ;

\- la justification est documentée ;

\- le ticket contient toutes les preuves nécessaires.



\## 15. Informations obligatoires dans le ticket



\- identifiant du ticket ;

\- client ;

\- serveur ciblé ;

\- utilisateur ;

\- adresse IP source ;

\- période observée ;

\- nombre d’échecs ;

\- connexion réussie ou non ;

\- chronologie ;

\- logs analysés ;

\- IOC ;

\- analyse ;

\- qualification ;

\- décision ;

\- recommandations ;

\- analyste ;

\- heures SLA.



\## 16. SLA de laboratoire



\- prise en charge : 15 minutes ;

\- qualification initiale : 30 minutes ;

\- escalade si nécessaire : 60 minutes ;

\- clôture ou mise en attente : 4 heures.



\## 17. Erreurs à éviter



\- conclure sans vérifier les logs ;

\- oublier de rechercher une connexion réussie ;

\- ne pas vérifier si le compte est privilégié ;

\- confondre une erreur utilisateur avec une attaque ;

\- bloquer automatiquement une adresse ;

\- utiliser un IOC réel inutilement ;

\- oublier de documenter les horaires ;

\- présenter une hypothèse comme une preuve.

