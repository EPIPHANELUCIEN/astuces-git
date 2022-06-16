![[travailler_en_equipe.png]]

-travailler a plusieur sur un projet (repository)
-grerer les conflits 
-comment cree des branches manipuler suprimer
-comment faire un commit depus vs code
-l'utiliter des fichier readme et .gitignore


# la procedure etape par etape
dans notre cas on a un master et un second
pour eviter les problemes de comprension le master vas travailler directement ssur git et le second en local apres avoir cloner le file master et coder et faire un comit et et push en ligne sur le travail du master
### *le master *
aller sur github debu en ligne
 -cree un repository
 -uploader son fichier a linterieur
 -une fois uploader on vas commit le le changement (le bouton vert apres avoir uploader)
ensuite il envois le lien du dossier au second
 par mail par exemple

### *le second*
pour recuperer le fichier du master le second vas 
 -ouvrir son git bash et cloner le repository du master du master
   *se placer la ou il veut que le dossier a cloner soit par exemple le destop (cd desktop)
   *git clone liendudossier 
   *ainsi le le repository du master a ete recuperer
pou editer notre commit avec vscode
  -on se palce dans le dossier onfait un git bash here
  -on ouvre vscode avec "code ."
  -et on commence l'edition
[dans le cas ou le second a fait des modification du cote peut il actuliser celuis du master ?]
 -avec son vs code il peut modifier le code du repository du master
 -faire des commite en local [git add .] et [git commit -m "changement de bgr"]
 -mais il ne peut pas lenvoyer sur le repository du master en ligne avec le git donc le code [git push -u origin] ne marchera pas ;il faut dabors une autorisation du master
pou editer notre commit avec vscode
 
### *le master *
comment faire donner l'autorisation du projet
 -le master ouvre la page de notre repository 
 -il selectionne setings ; colaborators et add collaborator
 ![[Capture1.jpg]]
 ![[Capture2.jpg]]
 -ensuite on cherche le nom d'utilisateur desiere et on l'ajoute
  ~une fois effectuer on a un lien dinvitation qui est cree et qui peut etre copier et envoyer au second par mail par exemple
  
### *le second*
le second recois le lien , il l'ouvre et acept l'invitation du master
 .
desormai le le second peut maintenant faire un [git push -u origin] sans probleme
faison notre commit depuis vs code
 -on ouvre un nouveau terminal sur vscode 
 -on selectionne git bash (avec ce dernier on pouras effectuer les operations git tout en etant sur vs code)
   ~[git add .]
   ~[git commit -m "changement bgr"]
   ~[git push -u origin main]
-ainsie le la modification a ete effectuer par le second (le projet est diriger par deux personne maintenant et chaque commit est visible sur github)

### *le master *
suppossons que le master a envie de cree un read me
 -c'est un fichier qui vas vous indiquer la procedue a suivre
 -il permet aussi a aider les gens de ce conserner repository a comprendre le projet
 -si il n'a pa ete mis au paravent il pouras etre mis par le master au repository 
 editert son contenue ( le read me) anexc les sustemes de notation # ## ###
 
## [avant de continuer un projet on dois recuperer la version la plus recente possible du projet ] aucas ou le master a fait une modification et il faut aussi eviter de modifier le meme fichier que le master si non au niveaude commit on auras une erreur
pour recuperer un mise asjour sur depos distant
 ~[git pull] en dautres termes les modifications effectuer par le master
 ~et dans ce cas on se rend compt que il ya un fichier readme.md qui s'est ajouter
  +il faut savoir que c'est a partir du readme que les instructions du projet seront ercrite et permetra la communication entre le master et le second
  (ca peut etre des mots de passe; des instructions ;des notes js;)
  
  +ilm faut savoir que le git ignore est un fichier danlequel on vas indiquer a gitbash les elements a ne pas les tenir en compte lors du commit
   >supossonque l'on a fait notre [git pull]
   >et dans le dossier conserner on cree un fichier notes.txt avec du text comme contenu (et on souhaite pas que ce fichier fasse partie de notre commit )
   >on ouvre notre fichier [.gitignore] et on precise comme suit 
       /notes.txt    (dans ce cas tous le fichier nomer notes.txt seras exclu lors du prochaint commit)
	   dossier/*   (dans ce cas il ignore tous les elemen du dosiier nomer [dossier])
   >

### *la creation de branche*
pour cree une branche il suffit de faire 
 [git branche nom_branche]

## *[[Fichier indispensable]]*
[readme.txt]
[.gitignore]
## *[[Gerer les brances en local console]]*
![[Capture3.jpg]]
### *git branch*
-permet de lister toutes les branches presentes
-celuit en vert permet de monter sur quel branche on se trouve

### *git branch nom_branche*
permet de cree une branche nomer [nom_branche]

### *git checkout nom_branche*
-pour nous mettre sur notre branche que l'on vien de cree [nom_branche]
-ainsie maintenat si on fait un [git_branche] on verra que maintenant c'est la branche [nom_branche] qui est en vert.

### *git branch -d nom_branche*
permet de suprimer la branche nomer [nom_branche] (en locale)

### *git push --set-upstream origin nom_branche*
ainsie on a cree la branche [nom_branche] en ligne sur notre projet
-la brache permet de reprendre tout le contenue du repository et de le metre dans un autre espace et 
-ainsi le second qui avait cree la branche adesomais laposibilite de de faire ses commits sans affecter la branche principale
![[Capture4.jpg]]

## *[[Gerer les branches sur un depos distant console]]*
### *git push --set-upstream origin nom_branche*
ainsie on a cree la branche [nom_branche] en ligne sur notre projet
-la brache permet de reprendre tout le contenue du repository et de le metre dans un autre espace et 
-ainsi le second qui avait cree la branche adesomais laposibilite de de faire ses commits sans affecter la branche principale
![[Capture4.jpg]]

### *git push origin --delete nom_branche*
 permet de suprimer la branche  [nom_branche] en depot distant (c'est a dire en ligne sur github)
 
### *git branch -a*
permet de voir la liste de toutes les brances sur depat distant .
## *[tavaillons ur une notre branche nom_branche en depot distant]*
 on fait nos modifications avec le vs code
 on ouvre git bash ( de preference avec vscode ) et on fait
   [git add .]
   [git commit -m "changement_dans_new_branche"]
   [git push -u origin nom_branche ]ainsi on verra apparaitre sur git hub sur notre branche  [nom_branche] en ligne la modification faite
   
   nb 
   si le master se rend sur de lepository du projet et leselectionne on auras
   ![[Capture5.jpg]]
   on peut voir en 1 le nom du repositiry en 2 la branche sur laquel on se trouve en 3 le nombre brance existant 
   si on clic sur le 2 on auras
   ![[Capture6.jpg]]
   il presente ici les brnaces du repository
   
## *[[Travailler avec un depot distant]]*
### *git pull --rebase*
 il permet de fudionner fusionner toutes aures brances a la branche principale.(pas trop recommander mieux vaut utilser l'interface de github qui es beaucoup plus simple)
 
#### sur etition de branches ur le site git hub
![[Capture7.jpg]]
le1 pour supprimer la branche 
le 2pour la modifier branche
le 3 pour verifier regarder ce qui a ete faite au niveau de la branche
 
 *selectionnos le 3 a la partie verification du code (juste en bas de la page)
 ![[Capture8.jpg]]
 le 1 nous montre que le background a ete modifier 
  le rouge designe ce qui a ete suprimer et le vert ce qui a ete ajouter (idem pour le 2)
  
  *toujours jur la meme page le master peu y lesser un commentaire(4) et faire le merge(5)
 ![[Capture9.jpg]]
 
 *il faut savoir que c'est toujour sur cette page que il ya la gestion de confit (les conflits surviennent generalement )
 
## *[[Trouver qui a fait quoi ]]* dans la gestion des conflits
il ya gestion de conflit lorsque par exemple un second modifie un fichier du repository master dans une nouvelle branche. et que maintenant le master veut faire un merge des deux branches(on suppose que second [colner le repository master; cree sa branche ; faire un commit et un push sur sa nouvelle branche] a au paravent ) 

### *resolution de conflit*
 ![[Capture8.jpg]]
comme le montre la figure ci dessus le second a modifier deux element dans le css 

pour gerer le conflit on se rend sur la page d'dition de branche et on selectionne la branche desirer et on clique sur [new pull request];
![[Capture10.jpg]]

![[Capture11.jpg]]
le 1 nous indique le point de conflit  (on peut suprimer ce que l'on ne veut pas garder)
le 2 ne nous indique pas de conflit parceque il n'interfere pas avec un fichier deja exixtan 

(a3) designe la partie a suprimer et  on commit le changement
![[Capture13 2.jpg]]![[Capture14.jpg]]

![[Capture15.jpg]]
si le merged apparait en violet c'est bon signe

## *qui a fait quoi*
permet de savoir quel  utilisateur a effetuer quel changement sur un fichier donner

pour se faire on se place dabord sur la branche prin cipale [git checkout main]
 et on cherche a savoir qui a fait quoi sur un fichier donner (dans notre cas on le fait avec le fichier style.css)
 [git blame style.css]
 
 ![[Capture16 2.jpg]]
 ![[Capture17.jpg]]
 #### *appuier sur le clavier ''q" pour quiter l'affichage*
#### *git blame -L 10, 20 style.css*
utlie pour par exemple les proget avec un fichier de 600 ligne il permet d'afficher uniquement la ligne 10 a 20
## *[[Commit son projet git]]*
### *git add .*
### *git commit -m message*
### *git push origin main*

