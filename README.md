# Guide "Comment créer sa brasserie de A à Z"

## Comment installer RelaxedJS et commencer à contribuer ?

1. Clonez le dépot Git.
``` shell script
    git clone https://github.com/YanisLeroy/Guide-brasserie.git
```

2. Construisez l'image Docker de RelaxedJS.
``` shell script
    cd Guide-brasserie && sudo docker build -t relaxed
```

3. Pour simplifier l'utilisation, créez un alias pour la commande.
``` shell script
    alias relaxed="sudo docker run -it --rm -u $(id -u):$(id -g) -v $(pwd):$(pwd) -w $(pwd) --name relaxed relaxed $@"
```

4. Vous pouvez maintenant modifier les fichiers PUG et générer des PDF avec RelaxedJS très simplement.
``` shell script
    relaxed Standards-raccordement/index.pug --no-sandbox
```