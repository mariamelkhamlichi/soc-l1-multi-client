# SOC L1 Multi-Client

Projet de portfolio professionnel simulant le travail d'une analyste SOC L1
dans un laboratoire local isolé.

## Contexte

Atlas Cyber Services est un SOC fictif supervisant Banque Atlas, Industrie
Atlas et PME Atlas.

## État actuel

- architecture VirtualBox documentée ;
- réseau interne `SOC_LAB` configuré ;
- Wazuh, Kali Linux, Linux et Windows préparés ;
- premier playbook SSH rédigé.

## Sécurité et périmètre

Les travaux sont réalisés uniquement dans un laboratoire local contrôlé.
Aucune infrastructure réelle, adresse IP publique ou donnée confidentielle
n'est ciblée ou utilisée.

## Structure

- `architecture/` : architecture du laboratoire ;
- `cadrage/` : périmètre et objectifs ;
- `playbooks/` : procédures de triage SOC L1 ;
- autres dossiers : livrables à venir.

Les résultats sont simulés et seront complétés progressivement au fil des
séances.
