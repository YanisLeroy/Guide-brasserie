# Guide "Comment créer sa brasserie de A à Z"

## Comment installer RelaxedJS et commencer à contribuer (Avec Docker) ?

Attention : N'oubliez pas de vérifier que votre compte utilisateur fasse bien partie du groupe "docker" pour pouvoir exécuter Docker sans être en super-administrateur avec sudo. Si ce n'est pas le cas, tapez la commande suivante :
``` shell script
    sudo usermod -aG docker $USER
```

1. Clonez le dépot Git.
``` shell script
    git clone https://github.com/YanisLeroy/Guide-brasserie.git
```

2. Construisez l'image Docker de RelaxedJS.
``` shell script
    cd Guide-brasserie && docker build -t relaxed
```

3. Pour simplifier l'utilisation, créez un alias pour la commande.
``` shell script
    alias relaxed="docker run -it --rm -u $(id -u):$(id -g) -v $(pwd):$(pwd) -w $(pwd) --name relaxed relaxed $@"
```

4. Vous pouvez maintenant modifier les fichiers PUG et générer des PDF avec RelaxedJS très simplement.
``` shell script
    relaxed Standards-raccordement/index.pug --no-sandbox
```

## Comment installer RelaxedJS et commencer à contribuer (Avec NodeJS) ?

1. Installer NodeJS
``` shell script
    curl-sL https://deb.nodesource.com/setup_8.x |sudo-Ebash- 
    sudo apt install -y nodejs
```

2. Installer Git
``` shell script
    apt-get install git
```

3. Installer RelaxedJS
```shell script 
    npm i -g relaxedjs
```

4. Vous pouvez maintenant modifier les fichiers PUG et générer des PDF avec RelaxedJS très simplement.
``` shell script
    relaxed Standards-raccordement/index.pug
```
