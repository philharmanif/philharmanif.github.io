# philharmanif.github.io

Site web de la Philharmanif.

## Ajouter une chanson au parolier

Les chansons sont dans `parolier/chansons.json`. **Ne l'écris pas à la main** : les retours à la ligne et les guillemets y sont vite source d'erreurs. Passe plutôt par l'outil :

1. Ouvre `tools/paroles/index.html` dans ton navigateur (double-clic, il n'a pas besoin de serveur).
2. Remplis les champs : titre, texte (parolier), musique, arrangement et paroles. Tous sont facultatifs sauf le titre : un champ vide n'est pas affiché sur le site.
3. Dans les paroles, sélectionne du texte et clique sur **B** ou **I** pour le gras ou l'italique. Une ligne vide sépare deux couplets.
4. Clique sur **Copier** pour récupérer la ligne générée.
5. Colle-la dans `parolier/chansons.json`, entre les crochets, à la suite des autres chansons.
6. Vérifie que la **dernière** chanson du fichier n'a pas de virgule à la fin.

## Tester en local

Le parolier charge `chansons.json`, ce qui ne marche pas en ouvrant la page par double-clic. Lance un petit serveur à la racine du dépôt :

```
py -m http.server 8000
```

puis ouvre http://localhost:8000/parolier/.

## Structure

```
index.html          page d'accueil
parolier/           les paroles (index.html + chansons.json)
tools/paroles/      l'outil pour écrire une entrée de chansons.json
orchestre/          à venir
chorale/            à venir
pics/               logo et favicon
```
