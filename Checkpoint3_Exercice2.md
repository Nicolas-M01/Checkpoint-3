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
![Capture d'écran 2025-01-17 114641](https://github.com/user-attachments/assets/9dcc5c46-9848-44d3-8ec0-5ea49cb1044a)  


## Q.2.2.2 Autoriser l'accès à distance à ton compte personnel uniquement.  
![Capture d'écran 2025-01-17 114815](https://github.com/user-attachments/assets/e35b400c-377d-4d38-ac6f-dc7033940714)  


## Q.2.2.3 Mettre en place une authentification par clé valide et désactiver l'authentification par mot de passe  
![Capture d'écran 2025-01-17 115243](https://github.com/user-attachments/assets/82a22722-1ce3-4d0a-a4b2-5f9da18814fd)
![Capture d'écran 2025-01-17 115333](https://github.com/user-attachments/assets/41b83377-cefc-4b3a-805e-90b39d388ffd)
![Capture d'écran 2025-01-17 114641](https://github.com/user-attachments/assets/3af00595-c7df-4931-90e9-e6b3af0f2ee9)  


---
