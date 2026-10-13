\# Document de cadrage



\## 1. Intitulé du projet



SOC L1 Multi-Client — Qualification des alertes, Threat Intelligence et investigation d’incidents



\## 2. Organisation fictive



Atlas Cyber Services est un SOC fictif supervisant trois clients :



\- Banque Atlas ;

\- Industrie Atlas ;

\- PME Atlas.



\## 3. Objectif général



Simuler le travail quotidien d’une analyste SOC L1 dans un laboratoire local isolé.



\## 4. Objectifs opérationnels



\- recevoir et qualifier des alertes ;

\- analyser des logs Linux et Windows ;

\- identifier des IOC ;

\- enrichir les IOC avec la Threat Intelligence ;

\- associer les preuves à MITRE ATT\&CK ;

\- appliquer des playbooks ;

\- rédiger des tickets ITSM ;

\- suivre les SLA ;

\- décider d’une clôture ou d’une escalade vers L2 ;

\- préparer une passation de shift ;

\- proposer des améliorations de règles.



\## 5. Périmètre technique



\- VirtualBox ;

\- réseau interne SOC\_LAB ;

\- Wazuh ;

\- Kali Linux ;

\- serveur Linux ;

\- machine Windows ;

\- Sysmon si disponible ;

\- Zeek si les ressources le permettent ;

\- modèle de ticket ITSM ;

\- données de test uniquement.



\## 6. Limites et règles de sécurité



\- aucune infrastructure réelle ciblée ;

\- aucune adresse IP publique attaquée ;

\- aucun système non contrôlé utilisé ;

\- aucune donnée confidentielle ;

\- aucune charge utile dangereuse ;

\- résultats limités au laboratoire ;

\- snapshots réalisés avant les modifications.



\## 7. Scénarios prévus



1\. Brute force SSH.

2\. Brute force Active Directory.

3\. PowerShell suspect.

4\. Scan réseau.

5\. Phishing simulé.



\## 8. Livrables



\- architecture du laboratoire ;

\- inventaire des sources de logs ;

\- cinq playbooks ;

\- cinq tickets ITSM ;

\- cinq rapports d’investigation ;

\- matrice MITRE ATT\&CK ;

\- matrice d’escalade ;

\- tableau SLA ;

\- modèle de passation de shift ;

\- rapport de faux positifs ;

\- modèle de veille ;

\- rapport final ;

\- présentation ;

\- README GitHub.

