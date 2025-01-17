# Partie 1 : Gestion des utilisateurs  

## Q.1.1.1 
Création du user  
![Capture d'écran 2025-01-17 094956](https://github.com/user-attachments/assets/2d47a554-d8a4-4944-8d03-4e4ea860ce8d)  
Intégration dans les mêmes OU que l'ancienne personne  
![Capture d'écran 2025-01-17 095136](https://github.com/user-attachments/assets/a0ec3af8-e131-490f-ba5a-679aea4fe63b)  
Intégration dans le même groupe `GrpUsersDirectionDesRessourcesHumaines`  
![Capture d'écran 2025-01-17 095659](https://github.com/user-attachments/assets/a79abb8f-1b27-45aa-8c81-fff9e959a83b)

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
``Créer groupe "Bloquage CLIENT01`` et ajouter Gabriel.Ghul.  
![Capture d'écran 2025-01-17 103204](https://github.com/user-attachments/assets/f94f33a0-3474-4184-a524-d1cca4a7a625)  
``Créer GPO``  
![Capture d'écran 2025-01-17 104957](https://github.com/user-attachments/assets/0f5b131a-85a2-4781-92fa-ad28129573eb)  
``Attribuer groupe à la restriction``  
![Capture d'écran 2025-01-17 105124](https://github.com/user-attachments/assets/6ff16829-0f07-4068-b3d3-c6da9ac6c7c8)  
``Activer GPO de force``  
![Capture d'écran 2025-01-17 105257](https://github.com/user-attachments/assets/227b4ff4-0d40-46ed-979d-5881b02dac8e)




## Q.1.2.3 Mettre en place une stratégie de mot de passe pour durcir les comptes des utilisateurs de l'OU LabUsers.  





# Partie 3 : Lecteurs réseaux  

## Q.1.3.1 Créer une GPO Drive-Mount qui monte les lecteurs E: et F: sur les clients.  
