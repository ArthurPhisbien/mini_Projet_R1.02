# Mini-projet R1.02

Site d’équipe en HTML et CSS. Pour le voir sur ton PC, ouvre `index.html` dans ton navigateur après avoir cloné le dépôt.

## Travailler avec VS Code sur Windows

1. **Rejoindre le projet (une fois).** Accepte l’invitation GitHub. Dans VS Code, fais **Ctrl + Maj + P → Git: Clone**, colle `https://github.com/ArthurPhisbien/mini_Projet_R1.02.git`, puis ouvre le dossier cloné. Si on te demande de te connecter, utilise le compte invité.
2. **Commencer une tâche.** En bas à gauche, sélectionne `main`, la version commune. Fais **Ctrl + Maj + G → … → Pull** pour la mettre à jour. Clique ensuite sur `main` → **Créer une branche**, par exemple `lea/page-contact`. Chacun code sur sa branche.
3. **Envoyer ton travail.** Dans **Ctrl + Maj + G**, clique sur le **+** à côté des fichiers voulus, écris un message et clique sur **Commit**. Ça enregistre une version sur ton PC. Clique sur **Publier la branche** la première fois, puis **… → Push** les fois suivantes pour envoyer tes commits sur GitHub.
4. **Partager une partie terminée.** Sur GitHub, ouvre **Pull requests → New pull request**. Choisis ta branche dans **compare** et `main` dans **base**. Une fois la demande relue et fusionnée, chacun peut passer sur `main` et faire **Pull** pour récupérer le résultat.

<details>
<summary>Voir les commandes équivalentes dans le terminal</summary>

### Première fois

Accepte l’invitation GitHub, puis lance ces commandes depuis le dossier où tu veux placer le projet.

```bash
git clone https://github.com/ArthurPhisbien/mini_Projet_R1.02.git
cd mini_Projet_R1.02
```

### Pour chaque nouvelle tâche

Pars de la version commune à jour et crée une branche avec un nom unique. Remplace `prenom/page-equipe` par ton prénom et ta tâche.

```bash
git switch main
git pull --ff-only
git switch -c prenom/page-equipe
```

Répartissez-vous les pages ou sections. Par exemple, une personne peut travailler sur `equipe.html` et `css/equipe.css`, une autre sur `contact.html` et `css/contact.css`. Coordonnez les changements dans `index.html` et `css/style.css`, qui servent de base commune.

### Envoyer ton travail

Après tes modifications, vérifie les fichiers concernés et fais ton premier push.

```bash
git status
git add equipe.html css/equipe.css
git commit -m "Ajouter la page équipe"
git push -u origin prenom/page-equipe
```

Adapte les chemins à tes fichiers. Pour les prochains envois sur cette branche, fais un commit puis `git push`. Tu peux envoyer tes commits au fur et à mesure.

Pour intégrer ton travail, ouvre une **pull request** sur GitHub depuis ta branche vers `main`. Après la fusion, le prochain `git pull --ff-only` sur `main` récupère la version commune.

### Récupérer les changements pendant une tâche

Enregistre d’abord tes modifications dans un commit. Depuis ta branche de travail, récupère puis intègre les changements déjà fusionnés dans `main`.

```bash
git fetch origin
git merge origin/main
```

Si Git signale un conflit, ouvre les fichiers signalés, garde les lignes voulues, puis ajoute les fichiers corrigés avec `git add` et termine avec `git commit`.

</details>
