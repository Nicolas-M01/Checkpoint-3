# Partie 1 : Gestion des utilisateurs  

## Q.2.1.1 Sur le serveur, créer un compte pour ton usage personnel.  
En root :  
`adduser velarion` : création du compte.  
 Le dossier perso se crée et nous rentrons un mot de passe.  



## Q.2.1.2 Quelles préconisations proposes-tu concernant ce compte ?  
Il est recommandé de rentrer l'utilisateur dans un groupe avec des droits restreints pour se connecter en root uniquement si besoin.  
Garder un système à jour : `sudo apt update && sudo apt upgrade -y`  
Faire des sauvegardees régulièrement.  
Fermer la session lorsque l'on quite son poste.  

---

# Partie 2 : Configuration de SSH  

## Q.2.2.1 Désactiver complètement l'accès à distance de l'utilisateur root.  
![Capture d'écran 2025-01-17 114525](https://github.com/user-attachments/assets/4139d1f6-eb50-43b2-86ea-b5483baf3305)  

## Q.2.2.2 Autoriser l'accès à distance à ton compte personnel uniquement.  


## Q.2.2.3 Mettre en place une authentification par clé valide et désactiver l'authentification par mot de passe  


---
