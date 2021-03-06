# Pour traduire la documentation de vue-loader

### Workflow de travail

Cette branche de travail `working` est volontairement mise en avant et doit uniquement être mise à jour dans le sens :

`vuejs/vue-loader:master` --> `vuejs-fr/vue-loader:working`.

Nous traduisons les fichiers directement dans le dossier `en` sans les renommer. Cela permet lors de la mise à jour de la documentation via l'utilisation des commandes :

```
git fetch upstream
git merge working upstream/master
```

d'obtenir des conflits **sur les pages déjà traduites** et ainsi maintenir la documentation à jour en fonction des modifications à travers **les documents déjà traduits**.

Note : `git remote add upstream https://github.com/vuejs/vue-loader.git` est nécessaire au préalable pour utiliser les commandes ci-dessus.

### Traduction

Pour savoir ce qui est [en cours de traduction](https://github.com/vuejs-fr/vue-loader/issues/2) ou [comment traduire un fichier](https://github.com/vuejs-fr/vue-loader/issues/1), référez vous aux issues correspondantes.

### Reverssement

Quand un fichier traduit est validé par pull request, on le met à jour dans le dossier `fr` de `vuejs-fr/vue-loader:master` puis on propose une pull request au site principal :

`vuejs-fr/vue-loader:master` --> `vuejs/vue-loader:master`

ainsi le dossier officiel hébergeant la documentation possède bien le dossier `fr` en français et le dossier `en` en anglais.

Note : il peut être intéressant de faire une pull request par ficher validé et donc de créer une branche dérivée de `vuejs-fr/vue-loader:master` pour faire la pull request (`vuejs-fr/vue-loader:master` --> `vuejs-fr/vue-loader:only_one_changed_file_from_master` --> `vuejs/vue-loader:master`)
