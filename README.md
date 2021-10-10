# Projet de première année d'école d'ingénieur
## Preuve de concept de spyware basique en python

Le but du projet était de voir s'il était possible de récupérer des données sur un ordinateur distant en étant un débutant en matière de logiciels malveillants.
Le projet est divisé en deux parties :
- Une partie "client" qui exécute les actions malveillantes.
- Une partie "serveur" qui récupère les données exfiltrées par le client et les sauvegarde.

Le client est capable d'effectuer une capture de l'écran, d'enregistrer à travers le micro, de capturer une vidéo via la webcam ou de voler le mot de passe administrateur à l'aide d'un faux formulaire de saisie de mot de passe.
Il est également capable d'exécuter des instructions python à la volée à l'aide d'une fonction *exec*, ce qui permet de lui ajouter des fonctionnalités supplémentaires à l'exécution.

Le programme était peu, voir pas détecté par les antivirus au moment des tests (cf images). Cela s'explique par l'utilisation de modules python tout à fait légitimes :
la capture d'écran est faite grâce au module *pyscreenshot*, la capture audio grâce au module *python-sounddevice*, la capture vidéo grâce au module *opencv-python* et la faux formulaire grâce à *tkinter*.

Il est cependant important de noter que la capture vidéo allume la LED intégrée à la plupart des webcams, notifiant son utilisation. De plus, toutes les données sont exfiltrées en clair vers le serveur, sans aucune protection, il serait donc aisé de détecter le trafic illégitime avec un sniffer réseau.
