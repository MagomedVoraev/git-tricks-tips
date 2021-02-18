# Git Tricks - Tips

## Pour supprimer le README.md d'un projet pushé, tout en gardant l'historique des commits :

- clonez une copie du repo, au cas où ça tourne mal : `git clone <adresse ssh> <ma_copie_du_repo>`
- descendez dans le repo puis supprimez le remote : `git remote remove origin`
- sur GIthub, créez un nouveau repo sur votre compte perso
- lancez un parcours de l'historique de la branche pour retirer le README de tous les commits : `git filter-branch -f --index-filter 'git rm --cached --ignore-unmatch README.md'`
- si vous avez plusieurs branches dans votre repo et que vous voulez les pusher (vous pouvez décider de ne pusher que main), il faudra répéter l'opération pour chaque branche que vous souhaitez pusher
- ajouter le remote `origin` avec l'adresse ssh de votre nouveau repo
- pushez le tout sur votre repo : `git push -u origin main`
- retournez vérifier en ligne sur votre repo perso qu'il n'y a bien plus aucune trace d'un quelconque README
- s'il reste un README quelque part, nos bots le détecteront en quelques minutes, vous aurez environ une heure pour changer de nom, quitter le pays et prendre rdv avec un bon chirurgien pour faire en sorte qu'aucune caméra de circulation ne vous repère (ou faîtes comme moi, vivez à la campagne, y'a pas de caméras de circulation)



## Pour supprimer / enlever les modifications faites à un repo git sur son hote 

- `git stash` => cela va supprimer tout ce qui a été modifié / fait depuis le dernier pull / push



## Pour créer une section about me tout en haut de la page sur GitHub

[Le lien : About your profile README](https://docs.github.com/en/github/setting-up-and-managing-your-github-profile/managing-your-profile-readme#about-your-profile-readme)


## GitHub training / learning

- [git-cheat-sheet](https://training.github.com/downloads/fr/github-git-cheat-sheet.pdf)

- [git-school](http://git-school.github.io/visualizing-git/)

- [learn-git-branching](https://learngitbranching.js.org/?locale=fr_FR)