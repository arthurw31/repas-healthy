# 🥗 Repas Healthy

App d'inspiration pour repas sains — version "healthy" au sens : **protéiné, avec des glucides, bon volume alimentaire, peu de gras**.

En ligne : https://repas-healthy.vercel.app

## Fonctionnalités

- **🎲 Inspiration** — générateur d'idées avec 4 modes :
  - *Assiette composée* : protéine + préparation + féculent + légume + façon légume + sauce
  - *Plat complet* : un plat + un dessert
  - *Menu entier* : entrée/apéro + plat + dessert
  - *Apéro dinatoire* : 2 froids + 2 chauds + 1 dip, sans doublon
  - Verrouillage 🔒 / relance 🔄 par élément, filtres ⏱️ Rapide · 🌞 De saison · 🥗 Léger (écarte les options grasses)
  - 👍/👎 sur chaque élément : l'app apprend tes goûts (tirage pondéré)
- **📅 Ma semaine** — 7 dîners sans répétition ni deux fois la même protéine d'affilée, filtres appliqués, verrouillage par jour
- **🛒 Liste de courses** — générée depuis la semaine, groupée (protéines / féculents / légumes / ingrédients par plat), cases cochables + articles libres
- **📖 Journal** — ✅ marque un repas comme mangé ; l'app évite de reproposer les mêmes plats pendant 7 jours
- **⭐ Favoris** — garde les combos qui te plaisent
- **📚 Bibliothèque** — listes modifiables (ajout / suppression / réinitialisation) + **export/import JSON** pour transférer ses données entre appareils
- **📱 PWA** — installable sur téléphone, fonctionne hors ligne (service worker)

## Technique

Page statique sans build ni dépendance : `index.html` + `sw.js` + `manifest.webmanifest` + `icon.svg`. Données en localStorage. Les items sont tagués (`rapide`, `gras`, `saison`, `dip`) dans `TAGS` ; les items ajoutés par l'utilisateur passent tous les filtres.
