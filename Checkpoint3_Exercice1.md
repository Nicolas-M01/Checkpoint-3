# Partie 1 : Gestion des utilisateurs  

## Q.1.1.1 Créer l'utilisateur Lionel Lemarchand avec les même attribut de société que Kelly Rhameur.  
Création du user  
![Capture d'écran 2025-01-23 183228](https://github.com/user-attachments/assets/dcbd352a-c5b0-4398-a658-2a509b61241e)  
![Capture d'écran 2025-01-23 183848](https://github.com/user-attachments/assets/ec67cba3-6c98-4751-8efb-e16a858feb20)  
![Capture d'écran 2025-01-23 183948](https://github.com/user-attachments/assets/c201f630-99b9-408c-89b3-0c0460ba2a2c)  

Intégration dans les mêmes OU que l'ancienne personne  
![Capture d'écran 2025-01-17 095136](https://github.com/user-attachments/assets/a0ec3af8-e131-490f-ba5a-679aea4fe63b)  



## Q.1.1.2 Créer une OU DeactivatedUsers et déplace le compte désactivé de Kelly Rhameur dedans.  
La photo est claire (petite flèche noire montre la désactivation)  
![Capture d'écran 2025-01-17 100053](https://github.com/user-attachments/assets/71a2607f-e230-4919-9dd9-e86f39a831b6)  

## Q.1.1.3 Modifier le groupe de l'OU dans laquelle était Kelly Rhameur en conséquence.  
Suppression de Kelly Rhameur de son ancien groupe au profit de Lionel Lemarchand.  
![Capture d'écran 2025-01-17 100612](https://github.com/user-attachments/assets/1f394401-bd5f-4322-9452-467fbd390e62)  

## Q.1.1.4 Créer le dossier Individuel du nouvel utilisateur et archive celui de Kelly Rhameur en le suffixant par -ARCHIVE.  
![Capture d'écran 2025-01-17 101028](https://github.com/user-attachments/assets/0738190a-a338-40df-8b6a-144a78cdd3b3)  

---

# Partie 2 : Restriction utilisateurs  
## Q.1.2.1 Faire en sorte que l'utilisateur Gabriel Ghul ne puisse se connecter que du lundi au vendredi, de 7h à 17h.  
![Capture d'écran 2025-01-17 102418](https://github.com/user-attachments/assets/bdd9f86f-2205-4e85-833a-d116aabf0def)  

## Q.1.2.2 De même, bloquer sa connexion au seul ordinateur CLIENT01.  

![Capture d'écran 2025-01-23 185416](https://github.com/user-attachments/assets/76ec6a80-f18c-4a12-8090-062139151b55)




## Q.1.2.3 Mettre en place une stratégie de mot de passe pour durcir les comptes des utilisateurs de l'OU LabUsers.  
`Création groupe "LabUsers" et intégration de tous les sous-groupes dedans`  
![Capture d'écran 2025-01-17 111056](https://github.com/user-attachments/assets/6ed4313c-8aa8-465e-b889-07fa522a9288)  

`Nouvelle Police de password et intégration du groupe LabUsers`  
![Capture d'écran 2025-01-17 111119](https://github.com/user-attachments/assets/6a2964c8-4994-4d36-a45f-d5736862e5db)  
``Lancement de "dsac.exe pour accéder à la politique de mdp``  
![Capture d'écran 2025-01-17 110003](https://github.com/user-attachments/assets/d5c8084f-04b5-42ca-9786-2725912f6a67)

`GPO en place pour le groupe LabUsers`  
![Capture d'écran 2025-01-17 111204](https://github.com/user-attachments/assets/93f7db76-b37e-4b7d-8204-551febdff63f)

# Partie 3 : Lecteurs réseaux  
## Q.1.3.1 Créer une GPO Drive-Mount qui monte les lecteurs E: et F: sur les clients.  
Nouvelle GPO
![Capture d'écran 2025-01-23 190126](https://github.com/user-attachments/assets/6b1c75f2-cc0a-424e-8644-99e31444dfc8)  
![Capture d'écran 2025-01-23 190220](https://github.com/user-attachments/assets/a1068125-ab8f-4e38-810c-fa79191b2b69)  
![Capture d'écran 2025-01-23 190314](https://github.com/user-attachments/assets/5d9615be-5f2c-43fb-b60c-ed80b9e93a0c) 


















