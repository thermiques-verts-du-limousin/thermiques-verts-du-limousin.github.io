# thermiques-verts-du-limousin.github.io

## Contribuer au projet
### Prérequis
* Installer ruby on rail
* Installer Jekyll

`gem install bundler jekyll`

* Installer git
* Cloner le dépôt
`git clone https://github.com/thermiques-verts-du-limousin/thermiques-verts-du-limousin.github.io.git`

### Utilisation
* Se rendre dans le dossier racine du projet
`cd thermiques-verts-du-limousin.github.io`
* Démarrer le serveur
`bundle exec jekyll serve`
* Pour tester une modification, compiler les fichiers de sortie
`jekyll build`
* Visualiser le résultat en visitant l'adresse [http://localhost:4000/](http://localhost:4000/)

## Ajouter des données
### Ajouter un lien
Se rendre dans le dossier \_data puis links. Ajouter le lien dans le fichier adéquate :
* links_club_school_federation : liens regroupants les sites de fédérations, clubs et écoles
* links_space_area : liens donnant des inforations sur les espaces aériens
* links_technical_documentation : liens sur la documentation technique et théorique concernant le vol libre
* links_weathercast : liens vers les sites de prévisions météo
* links_wind_captors : liens vers les sites d'affichage des valeurs mesurées par les balises

Les champs à ajouter sont les suivants :
``` yml
- name: **Nom du lien à afficher** obligatoire
  url: **URL du lien** obligatoire
  description: **Informations complémentaires** optionnel
```

### Ajouter un vol
Se rendre dans le fichier \_flights. Créer un nouveau fichier de la forme `AAAA-MM-JJ_Prenom_Nom.md`.
Le fichier doit avoir cette structure :
```md
---
saison: 2018-2019 (Exemple) __obligatoire__
date: 01/05/2019 (Exemple) __obligatoire__
pilote: _Nom du pilote_ __obligatoire__
distance: _En km_
points:
departement: 23 (Exemple)
flightType: Dist 3 pts / triangle / triangle FAI / ...
wing: _Voile du pilote_
CFD: Oui / Non suivant déclaration CFD
url_ffvl: _URL du vol sur la CFD_
#other_url: _Si vol accessible sur un autre site, URL du vol sur ce site en enlevant le # en début de ligne_
#other_url_site_name: _Si vol accessible sur un autre site, nom du site en enlevant le # en début de ligne_
---
```
