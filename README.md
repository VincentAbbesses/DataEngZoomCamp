## DataEngZoomCamp

#### Connexion à GitHub :

1/ Créer un répertoire  
2/ Générer une clé ssh sur la machine locale  

`ssh-keygen -t rsa -b 4096 -C "vincent.pm.erb@gmail.com"`

Une paire de clé (privée + publique) est crée dans le dossier ~/.ssh  
Copier la clé publique (id_rsa_pub)  
  
3/ Ajouter la clé publique sur GitHub (onglet Settings/SSH and GPG keys)  

New SSH key  
Coller la clé publique   

4/ Cloner répertoire sur machine locale  
`git clone git@github.com:VincentAbbesses/DataEngZoomCamp.git`  


#### Connexion à GCP : 

1/ Créer un projet sur GCP  
2/ Créer une paire de clés SSH sur la machine locale   
* aller dans le dossier ~/.ssh
* `ssh-keygen -t rsa -f ~gcp -C vincent -b 2048`  (filename = gcp, user = vincent, on choisit arbitrairement)


3/ Sur GCP, dans ComputeEngine/Metadata, ajouter la clé SSH publique nouvellement créée  
4/ Créer une VM  (Ubuntu, 30go), copier l'external IP  
5/ Se connecter en ssh : `ssh -i ~/.ssh/gcp vincent@35.233.59.0` (user(ssh)@externalIP)  
6/ Connexion avec la machine GCP établie

Note : pour se connecter plus facilement, créer un fichier nommé `config` dans .ssh :
`Host de-zoomcamp
    HostName 35.233.59.0
    User vincent
    IdentityFile /home/syd/.ssh/gcp`
On peut alors se connecter à la machine en lancant la commande `ssh de-zoomcamp`

7/ Commandes utiles : `htop`, `gcloud --version`

#### Configurer instance GCP

1/ Télécharger anaconda 
* wget https://repo.anaconda.com/archive/Anaconda3-2024.10-1-Linux-x86_64.sh
* bash anaconda.....sh
2/ installer docker
* apt install docker.io
* pour éviter d'avoir à taper sudo systématiquement :
** sudo groupadd docker
** sudo gpasswd -a $USER docker



3/ Cloner le répertoire github

 
 GCP 
# 1/ Create project
# 2/ generate SSH keys (on ubuntu)

# 3/ Create VM Enable compute engine API
# 4/ Connect to VM with SSH
# 5/ Install Anaconda
# wget https://repo.anaconda.com/archive/Anaconda3-2024.10-1-Linux-x86_64.sh 





