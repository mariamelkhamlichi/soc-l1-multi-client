# Agents Wazuh actifs

## État observé

Après configuration du réseau `SOC_LAB` et correction de l'adresse du manager
dans l'agent Windows, les agents utiles au projet sont actifs dans Wazuh.

| Agent | Adresse IP | Système | Statut |
|---|---|---|---|
| kali | 192.168.10.10 | Kali GNU/Linux | Actif |
| windows | 192.168.10.40 | Windows 10 Pro | Actif |
| raspberry / master | 192.168.10.1 | Debian GNU/Linux 11 | Variable selon l'état de la VM |

## Interprétation SOC L1

La collecte Windows est maintenant disponible pour les événements de sécurité,
PowerShell et Sysmon. La collecte Linux sera disponible lorsque `master` est
allumée et que son service `wazuh-agent` fonctionne.

L'agent `kali-B` reste hors périmètre du projet et n'est pas utilisé.
