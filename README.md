# projetpyt
# les instructions d'installation
apt-get update && sudo apt-get install python-pip python3-pip python-dev python3-dev
sudo pip install virtualenvwrapper

# Editer le fichier ~/.bashrc et ajouter ce code
VIRTUALENVWRAPPER=/usr/local/bin/virtualenvwrapper.sh
if [ -f ${VIRTUALENVWRAPPER} ]
then
	export WORKON_HOME=~/.virtualenvs
	source ${VIRTUALENVWRAPPER}
else
    echo Impossible de trouver le fichier VirtualEnvWrapper ${VIRTUALENVWRAPPER} introuvable
    echo Vérifiez la localisation du fichier et changer la variable VIRTUALENVWRAPPER dans votre fichier .bashrc 
    echo Lancez la recherche en tapant (peut prendre un certain temps) : find / -name virtualenvwrapper.sh
fi

# Préparation de l'environnement
user$ python --version
Python 2.7.9
user$ mkvirtualenv --python=python3 mon_env
(mon_env) user$ python --version
Python 3.4.2
(mon_env) user$ deactivate
user$ workon mon_env
(mon_env) user$ pip install ipython

   # problème entre la version 2 et 3
(mon_env) user$ cat > version.py
import sys
print(sys.version)
(mon_env) user$ python version.py 
3.4.2 (default, Oct  8 2014, 10:45:20) 
[GCC 4.9.1]
(mon_env) user$ /usr/bin/python version.py 
2.7.9 (default, Jun 29 2016, 13:08:31) 
[GCC 4.9.2]

projet python
