# \# Architecture du laboratoire SOC L1 Multi-Client

# 

# \## 1. Nom du projet

# 

# SOC L1 Multi-Client — Atlas Cyber Services

# 

# \## 2. Objectif

# 

# Simuler l'activité d'une analyste SOC L1 dans un laboratoire local isolé.

# 

# \## 3. Environnement de virtualisation

# 

# \- Hyperviseur : VirtualBox

# \- Réseau : SOC\_LAB

# \- Type de réseau : Internal Network

# \- Sous-réseau : 192.168.10.0/24

# \- Accès Internet des machines de laboratoire : non requis

# 

# \## 4. Machines principales

# 

# | Machine | Rôle | Adresse SOC\_LAB |

# |---|---|---|

# | Kali Linux | Analyse et génération de trafic autorisé | 192.168.10.10 |

# | Wazuh Manager | SIEM et collecte des événements | 192.168.10.20 |

# | master | Serveur Linux supervisé | 192.168.10.1 |

# | windows | Poste Windows supervisé | 192.168.10.40 |

# 

# \## 5. Règles de sécurité

# 

# \- Laboratoire local uniquement.

# \- Aucun test contre une infrastructure réelle.

# \- Aucune adresse IP publique ciblée.

# \- Aucune donnée confidentielle utilisée.

# \- Snapshots créés avant les modifications.

# \- Les machines vulnérables restent isolées d'Internet.

# 

# \## 6. État initial

# 

# \- Réseau SOC\_LAB opérationnel.

# \- Wazuh accessible depuis Kali, Windows et master.

# \- Les adresses IP sont configurées.

# \- Les tests de connectivité sont concluants.

