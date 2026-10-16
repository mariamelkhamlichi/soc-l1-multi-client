# Collecte Windows validée

## Observation

L'agent `windows` (`192.168.10.40`) transmet correctement ses événements à
Wazuh.

## Événement de référence

- type : résumé SCA de configuration ;
- règle : `19005` ;
- niveau : `9` ;
- politique : CIS Microsoft Windows 10 Enterprise Benchmark v1.12.0 ;
- contrôles : 394 ;
- contrôles réussis : 115 ;
- contrôles échoués : 275 ;
- score observé : 29 %.

## Qualification

Cet événement est une information de conformité et de configuration. Il ne
constitue pas, à lui seul, un incident de sécurité confirmé.

## Lien avec le projet SOC L1

La collecte Windows est validée. Les événements de sécurité, PowerShell et
Sysmon pourront maintenant être exploités pour les scénarios du projet.
