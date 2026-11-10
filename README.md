# Mini-projet R1.02

Site d’équipe en HTML et CSS. Pour le voir sur ton PC, ouvre `index.html` dans ton navigateur après avoir cloné le dépôt.

## Travailler avec VS Code sur Windows

### 1. Rejoindre le dépôt

1. Accepte l’invitation GitHub avec ton propre compte. Installe **Git** et **VS Code** sur ton PC si nécessaire.
2. Dans VS Code, fais **Ctrl + Maj + P** et cherche **Git: Clone**. Colle `https://github.com/ArthurPhisbien/mini_Projet_R1.02.git`.
3. Si GitHub te demande de te connecter, utilise le compte qui a accepté l’invitation. Choisis le dossier où ranger le projet, puis clique sur **Ouvrir**. Pour voir le site, ouvre `index.html` dans ton navigateur.

### 2. Créer une branche pour ta tâche

1. Clique sur le nom de la branche en bas à gauche et sélectionne **main**, la version commune du site.
2. Ouvre **Contrôle de code source** avec **Ctrl + Maj + G**. Dans le menu **…**, choisis **Pull** pour mettre `main` à jour.
3. Clique de nouveau sur le nom de la branche → **Créer une branche**. Donne-lui un nom comme `prenom/page-contact` et vérifie qu’il s’affiche en bas à gauche avant de coder.

Répartissez les fichiers. Par exemple, une personne travaille sur `contact.html` et `css/contact.css`, une autre sur `equipe.html` et `css/equipe.css`. Prévenez-vous quand vous touchez aux fichiers communs comme `index.html`.

### 3. Enregistrer et envoyer tes changements

1. Enregistre tes fichiers, puis ouvre **Contrôle de code source**. Clique sur un fichier pour voir les différences et sur le **+** pour l’inclure dans ton prochain commit.
2. Écris un message comme « Ajouter la page contact », puis clique sur **Commit**. Ton commit est enregistré sur ton PC.
3. Clique sur **Publier la branche** au premier envoi. Pour les envois suivants, utilise **… → Push**. Tu peux pousser plusieurs fois pendant la même tâche.

### 4. Récupérer les changements

**Pull** récupère les changements de la branche sur laquelle tu es. Pour récupérer la version commune, termine ton commit en cours, passe sur **main**, puis fais **… → Pull**. Si tu veux aussi intégrer cette version à une tâche en cours, retourne sur ta branche, fais **Ctrl + Maj + P → Git: Merge Branch**, puis choisis **main**.

Si VS Code signale un conflit, ouvre le fichier indiqué, compare les deux versions et décide avec ton camarade quoi garder. Enregistre, ajoute le fichier avec **+**, puis termine le commit de fusion.

### 5. Proposer ta partie pour le site commun

Une fois ta branche poussée, ouvre le dépôt sur GitHub → **Pull requests → New pull request**. Choisis **base: main** et **compare: ta branche**, puis vérifie les fichiers modifiés et crée la demande. Après relecture et fusion, chacun pourra récupérer le résultat avec un **Pull** sur `main`.

Tu peux aussi créer et relire les pull requests depuis VS Code avec l’extension **GitHub Pull Requests and Issues**.

## Équivalent dans le terminal

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
