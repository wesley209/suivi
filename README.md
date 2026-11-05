# Programme IA — suivi de progression

Application web pour suivre, semaine après semaine, un programme personnel de préparation à l’intelligence artificielle : **24 semaines, 10 heures par semaine, 240 heures au total**.

Le programme vise à renforcer les bases (mathématiques, programmation, apprentissage automatique) et à produire un portfolio vérifiable, en vue de candidater à un Master en informatique orienté IA.

## Objectif

Un programme de six mois demande de la régularité. Cette application sert à :

- **voir l’avancement d’un coup d’œil** : une courbe compare les heures réellement travaillées au rythme prévu ;
- **savoir quoi faire cette semaine** : cinq séances de deux heures, du lundi au vendredi ;
- **garder une trace** : notes par semaine, liens vers les projets, notions à reprendre ;
- **ne rien oublier du dossier** : projet final, CV académique, relevés, recommandations, Statement of Purpose, test d’anglais.

## Le programme

| Mois | Thème | Livrable |
|------|-------|----------|
| 1 | Fondamentaux mathématiques et Python | Résoudre des exercices de base et écrire des programmes Python simples |
| 2 | Algèbre linéaire, probabilités et statistiques | Comprendre les notions mathématiques du machine learning et analyser un jeu de données |
| 3 | Calcul différentiel et data science | Analyse reproductible (mini-projet 1 : données agricoles) |
| 4 | Machine learning | Plusieurs modèles comparés avec leurs limites (mini-projet 2 : scikit-learn) |
| 5 | Deep learning | Modèle neuronal simple avec PyTorch (mini-projet 3 : images ou textes) |
| 6 | Projet final et préparation académique | Projet complet sur GitHub : code, documentation, résultats, limites |

### Rythme hebdomadaire

| Jour | Travail | Durée |
|------|---------|-------|
| Lundi | Mathématiques : cours, exemples, exercices | 2 h |
| Mardi | Python et programmation | 2 h |
| Mercredi | Mathématiques : approfondissement et problèmes | 2 h |
| Jeudi | Informatique et IA : théorie et implémentation | 2 h |
| Vendredi | Projet pratique, révision et bilan | 2 h |

Le week-end sert uniquement à rattraper une séance manquée.

## Fonctionnalités

- Courbe des heures cumulées face au rythme prévu, avec marqueur de la semaine en cours
- Vue « Cette semaine » avec les cinq séances à cocher
- Les 24 semaines regroupées par mois, avec compteur de séances et livrable à valider
- Notes libres par semaine
- Suivi des trois mini-projets et du projet final, avec lien GitHub
- Listes de contrôle du projet final et du dossier de candidature
- Carnet d’erreurs : notions mal comprises à reprendre
- Ressources gratuites et conseils de travail
- Export et import de la progression au format JSON
- Thème clair et sombre selon les réglages du système, interface adaptée au mobile

## Utilisation

Aucune installation ni compilation : l’application tient dans un seul fichier, `index.html`.

### En local

Ouvrir `index.html` dans un navigateur, ou lancer un petit serveur :

```bash
npx serve .
```

### Déploiement sur Vercel

**Avec le dépôt GitHub**

1. Pousser le projet sur GitHub.
2. Sur [vercel.com/new](https://vercel.com/new), importer le dépôt.
3. Framework : *Other*. Laisser vide la commande de build et le dossier de sortie.
4. Cliquer sur *Deploy*.

**Avec la CLI**

```bash
npm i -g vercel
vercel
```

N’importe quel hébergeur de sites statiques (GitHub Pages, Netlify, Cloudflare Pages) convient aussi.

## Données et confidentialité

- Toute la progression est stockée dans le `localStorage` du navigateur. **Aucune donnée n’est envoyée à un serveur.**
- Les données sont propres à chaque navigateur, chaque appareil et chaque adresse (URL). Elles disparaissent si l’on vide les données de navigation ou en navigation privée.
- Safari peut effacer les données d’un site peu visité : ouvrir l’application au moins une fois par semaine.
- **Réglages → Exporter (JSON)** crée une sauvegarde ; **Importer** la restaure, y compris sur un autre appareil.

## Structure du projet

```
.
├── index.html   # interface, styles et logique
└── README.md
```

Technologies : HTML, CSS et JavaScript natifs, sans dépendance. Seules les polices Bricolage Grotesque et Instrument Sans sont chargées depuis Google Fonts, avec des polices système en repli.

## Personnaliser le programme

Le contenu du programme est défini en haut du script, dans les constantes de `index.html` :

- `MONTHS` : mois, livrables et semaines
- `DAYS` : séances de la semaine
- `PROJECTS`, `FINAL`, `DOSSIER` : projets et listes de contrôle

Modifier ces tableaux suffit pour adapter le parcours (autre durée, autres thèmes, autres projets).

## Limites

- Pas de synchronisation automatique entre appareils.
- Un seul programme et un seul utilisateur par navigateur.

## Avertissement

Ce programme est une préparation personnelle. Il ne garantit ni admission, ni bourse. Les critères d’admission, tests d’anglais, dates et financements doivent être vérifiés sur les sites officiels au moment de candidater, par exemple :

- [Admissions master, Stanford CS](https://www.cs.stanford.edu/admissions/masters-admissions)
- [Stanford CS229 — Machine Learning](https://cs229.stanford.edu/) (référence pour les prérequis)

## Ressources gratuites

- [Khan Academy](https://www.khanacademy.org/math) : mathématiques, probabilités, statistiques
- [3Blue1Brown](https://www.3blue1brown.com/) : algèbre linéaire et calcul en images
- [CS50](https://cs50.harvard.edu/x/) : programmation et bases de l’informatique
- [Stanford Engineering Everywhere](https://see.stanford.edu/) : cours universitaires
- [PyTorch Tutorials](https://pytorch.org/tutorials/) : introduction au deep learning
- [NumPy](https://numpy.org/learn/) : documentation officielle
- [scikit-learn](https://scikit-learn.org/stable/) : documentation et guides
