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




