# Archive Génie Industriel — ENIT

Site statique (HTML + CSS pur, aucun JavaScript) pour partager cours,
examens et corrections avec les étudiants du département.

## Structure

```
index.html        → page d'accueil
1ere-annee.html   → matières de 1ère année (S1 + S2)
2eme-annee.html   → matières de 2ème année (S1 + S2)
style.css         → style commun à toutes les pages
```

## 1. Héberger sur GitHub Pages (gratuit)

1. Créez un dépôt sur GitHub (par exemple `archive-gi`).
   Astuce : si vous le nommez `VOTRE-PSEUDO.github.io`, le site sera
   directement à l'adresse `https://VOTRE-PSEUDO.github.io`.
2. Uploadez les 4 fichiers à la racine du dépôt
   (bouton **Add file → Upload files** sur GitHub, aucun outil requis).
3. Dans le dépôt : **Settings → Pages → Source : Deploy from a branch**,
   branche `main`, dossier `/ (root)` → **Save**.
4. Après 1 à 2 minutes, le site est en ligne à
   `https://VOTRE-PSEUDO.github.io/archive-gi/`.

Chaque modification poussée sur `main` met le site à jour automatiquement.

## 2. Lier vos fichiers Google Drive

Le plus simple et le plus maintenable : **un dossier Drive par matière et
par type** (ex. `GI1 / Analyse / Examens`). Ainsi, quand vous ajoutez un
PDF dans le dossier, le site n'a pas besoin d'être modifié.

Pour obtenir un lien :

1. Dans Google Drive, clic droit sur le dossier (ou fichier) → **Partager**.
2. Accès général : **Tous les utilisateurs disposant du lien → Lecteur**.
3. **Copier le lien**.
4. Dans le fichier HTML, remplacez le `#` correspondant :

```html
<td class="links"><a href="https://drive.google.com/drive/folders/XXXXXXXX">Ouvrir</a></td>
```

Si un document n'est pas encore disponible :

```html
<td class="links"><span class="na">—</span></td>
```

## 3. Ajouter / modifier une matière

Ouvrez `1ere-annee.html` ou `2eme-annee.html`, copiez un bloc `<tr> ... </tr>`
existant, changez le nom de la matière et les liens. C'est tout.

Les noms de matières actuels sont des **exemples** : remplacez-les par le
vrai programme du département.

## 4. Avant la mise en ligne

- [ ] Remplacer l'e-mail de contact dans `index.html` (section « À propos »)
- [ ] Adapter la liste des matières au vrai programme
- [ ] Remplacer tous les liens `#` par les liens Drive
- [ ] Mettre à jour la date « Dernière mise à jour » dans le pied de page
