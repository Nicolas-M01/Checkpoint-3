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


# Partie 3 : Analyse du stockage
## Q.2.3.1 Quels sont les systèmes de fichiers actuellement montés ?  
``ext2 et ext4``  

## Q.2.3.2 Quel type de système de stockage ils utilisent ?  
Il utilise LVM  

## Q.2.3.3 Ajouter un nouveau disque de 8,00 Gio au serveur et réparer le volume RAID  
`Disque ajouté :`  
![Capture d'écran 2025-01-17 120536](https://github.com/user-attachments/assets/e867f5a4-bb39-412e-b0aa-779a0c55aea9)  
`Disque monté et RAID1 fonctionnel`  
`mdadm --add /dev/md0 /dev/sdb1` fonctionne aussi  
`mdadm --detail /dev/md0`  
![Capture d'écran 2025-01-17 122023](https://github.com/user-attachments/assets/a92fb50d-5130-420d-b804-180798f46bc9)  

## Q.2.3.4 Ajouter un nouveau volume logique LVM de 2 Gio qui servira à héberger des sauvegardes. Ce volume doit être monté automatiquement à chaque démarrage dans l'emplacement par défaut : /var/lib/bareos/storage.  
![Capture d'écran 2025-01-23 191058](https://github.com/user-attachments/assets/ab57de7f-35cb-4c9a-8f41-f90f042e8840)  
**Création du volume logique avec ``lvcreate --name LVMSave --size 2G cp3-vg``**  
**Création de la partition en ext4:**  
![Capture d'écran 2025-01-23 191125](https://github.com/user-attachments/assets/b59bcd0b-8922-41f1-bd58-63cad9cd24cf)  
**Montage**  
![Capture d'écran 2025-01-23 191245](https://github.com/user-attachments/assets/bb1921c5-8d25-4f3f-ad46-7d77a01ff571)  
**envoie des UUID avec un "LABEL" dans `/etc/fstab`**  
![Capture d'écran 2025-01-23 191353](https://github.com/user-attachments/assets/42ab9996-7c84-4d5f-a845-503d165b8377)
**Modif d enotre partition pour être montée au redémarrage:**  
![Capture d'écran 2025-01-23 191635](https://github.com/user-attachments/assets/c92d73aa-ffa8-46fd-81b1-10502c3d5eb3)




## Q.2.3.5 Combien d'espace disponible reste-t-il dans le groupe de volume ?  

---

# Partie 4 : Sauvegardes  

## Q.2.4.1 Expliquer succinctement les rôles respectifs des 3 composants bareos installés sur la VM.   
* bareos-dir : Il s'installe surle serveur. Il gère la planification, le contrôle et le lancement des sauvegardes. Il gère les autres composants.  
* bareos-sd : Il permet d'effectuer les sauvegardes sur différents supports par par un storage deamon.  
* bareos-fd : Installé sur chaque machine devant être sauvegardée. collecte les infos et renvoie à bareos-sd.  

---

# Partie 5 : Filtrage et analyse réseau  
## Q.2.5.1 Quelles sont actuellement les règles appliquées sur Netfilter ?  
Il laisse passer les paquets ICMPv4.  
Il laisse passer les paquets ICMPv6.  
Il laisse passer les paquets à destination du port ssh par TCP.  

## Q.2.5.2 Quels types de communications sont autorisées ?  


## Q.2.5.3 Quels types sont interdit ?  
Les paquets invalides en entrée sont abandonnés.

## Q.2.5.4 Sur nftables, ajouter les règles nécessaires pour autoriser bareos à communiquer avec les clients bareos potentiellement présents sur l'ensemble des machines du réseau local sur lequel se trouve le serveur.  


---

# Partie 6 : Analyse de logs  
## Q.2.6.1 Lister les 10 derniers échecs de connexion ayant eu lieu sur le serveur en indiquant pour chacun :  
![Capture d'écran 2025-01-17 132738](https://github.com/user-attachments/assets/bed32dd2-e6ec-43a5-9b63-ccb7d0fc442b)


## La date et l'heure de la tentative  
17/01/2025 à 8H36 et 12H04.  

## L'adresse IP de la machine ayant fait la tentative  











