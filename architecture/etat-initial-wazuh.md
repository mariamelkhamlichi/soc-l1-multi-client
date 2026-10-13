# État initial de Wazuh

## Date d'observation

13 octobre 2026 — état observé pendant la séance 2.

## Services

Les composants suivants sont actifs sur `wazuh-manager` :

- Wazuh Manager ;
- Wazuh Indexer ;
- Wazuh Dashboard ;
- Filebeat.

Le tableau de bord est accessible depuis Kali à l'adresse interne :

```text
https://192.168.10.20
```

## Agents observés

| ID | Nom | Adresse IP | Système | Statut observé |
|---:|---|---|---|---|
| 001 | raspberry | 192.168.10.1 | Debian GNU/Linux 11 | Actif après démarrage de `master` |
| 002 | kali | 192.168.10.10 | Kali GNU/Linux 2026.1 | Actif |
| 003 | kali-B | 192.168.10.11 | Kali GNU/Linux 2026.1 | Déconnecté |

## Interprétation SOC L1

Cet état est un point de référence et non un résultat d'incident. L'analyste
doit vérifier les agents déconnectés avant de conclure à une absence de logs.
La disponibilité de la collecte sera suivie avant l'exécution des scénarios.

## Limites

Les alertes et agents déjà présents peuvent provenir d'une configuration
antérieure du laboratoire. Ils ne sont pas encore attribués aux trois clients
Atlas et ne doivent pas être présentés comme des résultats du projet.

Après le démarrage de `master` et la vérification du service `wazuh-agent`,
l'agent `raspberry` est passé à l'état actif dans Wazuh. La collecte Linux
est donc disponible pour la suite du projet.
