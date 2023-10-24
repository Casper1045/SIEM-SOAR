# Attaque par Force Brute sur Serveur SSH

Ce référentiel contient les détails d'une attaque par force brute sur un serveur SSH dans une machine virtuelle Azure. L'objectif est de comprendre comment une telle attaque peut être menée et comment elle peut être détectée à l'aide de Microsoft Azure Sentinel.

## Description de l'Attaque

L'attaque par force brute est une menace courante où un attaquant tente de deviner le mot de passe d'un serveur SSH en essayant différentes combinaisons de mots de passe jusqu'à ce qu'il réussisse à se connecter. Voici les étapes de l'attaque :

1. **Reconnaissance** : L'attaquant identifie l'adresse IP publique de la machine virtuelle Azure cible.

2. **Exploration des Vulnérabilités** : L'attaquant analyse la configuration SSH de la machine virtuelle et identifie qu'elle autorise les connexions SSH par mot de passe.

3. **Accès Initial** : L'attaquant commence à exécuter une attaque de force brute contre le serveur SSH en essayant de deviner le mot de passe de l'utilisateur. Il utilise des outils automatisés pour tester une série de mots de passe couramment utilisés.

4. **Persistance** : Si l'attaquant parvient à deviner le mot de passe, il obtient un accès SSH à la machine virtuelle. Il peut installer des backdoors ou d'autres méthodes pour assurer un accès continu à la VM.

5. **Privilèges Élevés** : Une fois à l'intérieur, l'attaquant peut essayer d'augmenter ses privilèges en exploitant des vulnérabilités connues sur la VM ou en essayant d'obtenir des privilèges administratifs.

6. **Mouvement Latéral** : L'attaquant peut tenter de se déplacer latéralement pour explorer d'autres parties du réseau Azure en utilisant l'accès obtenu.

7. **Collecte d'Informations** : L'attaquant collecte des informations sur les ressources et les données sensibles sur la machine virtuelle et sur le réseau Azure.

8. **Exfiltration de Données** : L'attaquant exfiltre des données sensibles de la VM vers un emplacement externe sous son contrôle.

## Fichiers d'Attaque

![image](https://github.com/Casper1045/SIEM-SOAR/assets/61239359/86087b63-f549-4e67-a033-a76f4f720a0e)


## Utilisation de Microsoft Azure Sentinel

Nous utilisons Microsoft Azure Sentinel pour détecter et surveiller cette attaque. Les règles de détection ont été configurées pour identifier les activités anormales liées à l'attaque par force brute.

