# Mode d'emploi — Outil de Composition de Groupes EPS

**Collège Jean Jaurès, Gençay** — Académie de Poitiers

---

## 🎯 Objectif de l'outil

L'outil **Groupes EPS** automatise la composition des groupes de travail en cours d'EPS selon plusieurs critères : niveaux de performance, bonifications, contraintes de vigilance (aménagements, difficultés physiques) et paires d'élèves (pairs d'entraide, conflits à éviter).

Il génère :
- Des groupes équilibrés ou homogènes au choix
- Un PDF de synthèse et un export Excel pour les archives
- Une **feuille de terrain imprimable** pour vos notes au gymnase (présence, performance, observations)
- Un **projet sauvegardable** contenant plusieurs compositions (une par APSA/séquence)

**Point clé** : l'outil ne remplace pas votre diagnostic pédagogique ; il exécute vos décisions de positionnement et applique vos contraintes automatiquement, gain de temps assuré.

---

## ⚠️ Donnees sensibles et RGPD

L'outil ne transmet aucune donnée à un serveur extérieur. Les fichiers de projet contiennent des données nominatives (noms, prénoms, vigilances liées à la santé). **À conserver obligatoirement sur le réseau de l'établissement, jamais sur clé USB personnelle.**

Pour les vigilances, privilégiez les intitulés neutres — « Aménagement type A » plutôt qu'un diagnostic détaillé.

---

## 📋 Avant de commencer

**Préparation recommandée** :
1. Récupérez la **liste des élèves de votre classe** (export Pronote en Excel ou CSV)
2. Listez les **critères de positionnement** que vous avez en tête (tests diagnostiques, pratique en club…)
3. Identifiez les **vigilances** (PAI, inaptitude partielle, handicap moteur…)
4. Notez les **paires** (binômes d'entraide, conflits connus)

**Configuration technique** :
- Ouvrez `groupes_eps.html` dans un navigateur moderne (Chrome, Firefox, Safari, Edge)
- Connexion internet requise au premier lancement (téléchargement des bibliothèques PDF/Excel)
- Ensuite : fonctionne en mode hors ligne
- Enregistrez le fichier dans vos favoris pour un accès rapide

---

## 🚀 Étape 1 : Importer la classe

### Importer un fichier Excel/CSV

1. Cliquez sur **« Déposer ici le fichier de la classe »** (zone pointillée en haut)
2. Choisissez votre fichier Excel ou CSV (extraction Pronote acceptée)
3. Une fenêtre « Correspondance des colonnes » s'affiche : indiquez quelle colonne correspond à Nom, Prénom, Âge/Date de naissance, Sexe
4. Cliquez **« Importer les élèves »**

L'outil détecte automatiquement les colonnes — vous ne devez que confirmer. Les dates de naissance sont converties en âge.

### Ajouter des élèves à la main

- Cliquez **« + Ajouter un élève à la main »** si vous en avez oublié
- Le nom et le prénom sont obligatoires ; l'âge et le sexe sont facultatifs

### Tableau d'affichage

Vous voyez aussitôt la liste des élèves avec colonnes vides prêtes pour les critères.

---

## 🎓 Étape 2 : Définir vos critères

**Quatre onglets organisent les critères.**

### Onglet 1 : Bonifications

**Qu'est-ce que c'est ?** Une case cochée qui ajoute des points fixes au score d'un élève (pratique en club, leadership…). Points peuvent être négatifs (malus).

**Exemple** : « Pratique en club » = +2 points

**Comment faire** :
1. Entrez l'intitulé (ex. « Pratique en club »)
2. Entrez le nombre de points (positif ou négatif)
3. Cliquez **« Ajouter »**
4. Cochez les élèves concernés dans le tableau ci-dessus

**Conseil** : limitez-vous à 3–4 bonifications pour garder la lisibilité.

---

### Onglet 2 : Performances chiffrées

**Qu'est-ce que c'est ?** Le résultat d'un test diagnostique (temps au 50 m, distance en demi-fond…) saisi élève par élève. Converti automatiquement en points.

**Deux modes de conversion** :

#### A) Classement automatique (le plus simple)
- Le meilleur reçoit le maximum de points, le plus faible 0, les autres sont échelonnés proportionnellement
- Aucun barème à définir
- Idéal si vous avez des résultats bruts sans paliers de référence

#### B) Barème à paliers (plus fin)
- Vous définissez des seuils : « à partir de 1500 m → 2 pts », « à partir de 2000 m → 4 pts »…
- L'outil attribue les points selon le palier atteint
- Idéal si vous avez des référentiels (évaluations officielles, barèmes académiques)

**Comment faire** :

1. Entrez l'intitulé (ex. « 50 m nage libre »)
2. Entrez l'unité (s, m, tours…)
3. Entrez le **points max** (ex. 10)
4. Choisissez le **sens** :
   - *« Valeur haute = meilleure »* pour une distance, un nombre de tours
   - *« Valeur basse = meilleure »* pour un temps
5. Choisissez la **conversion** (classement auto ou barème)
6. Cliquez **« Ajouter »**

**Si vous avez choisi un barème**, vous devez définir les paliers :
- Dans le tableau qui s'affiche, cliquez **« + Ajouter un palier »**
- Remplissez seuil et points (ex. `1500` en unité → `2` pts)
- Attention au sens : pour les temps, un palier à 9,5 s avec 5 pts s'active si l'élève a 9,5 s **ou mieux** (9,2 s) ; pour les distances, un palier à 1500 m s'active si l'élève atteint 1500 m **ou plus**

**Saisir les performances dans le tableau**
- Dans le tableau des élèves, colonnes grisées « Performance » : entrez les valeurs brutes
- Format accepté :
  - Nombres simples : `12,4` ou `12.4` (automne reconnaît virgule et point)
  - Temps au format mm:ss : `2:35` (2 minutes 35 secondes = 155 secondes)
- Les points s'affichent automatiquement dans la colonne **Score**

**Conseil** : si vos résultats varient beaucoup d'une année à l'autre, privilégiez le classement automatique (moins de maintenance).

---

### Onglet 3 : Vigilances

**Qu'est-ce que c'est ?** Un signalement : PAI, asthme d'effort, inaptitude partielle, handicap moteur… Ils requièrent une règle de **répartition** entre les groupes.

**Trois modes de répartition** :

1. **Répartir dans tous les groupes** → Aucun groupe n'a + de 1 élève d'écart pour cette vigilance
   - Exemple : 5 asthmatiques, 4 groupes → 1-1-2-1 répartition
   - Utilité : que chaque enseignant encadrant ait une compétence d'accompagnement identique

2. **Regrouper dans un même groupe** → Tous les élèves avec cette vigilance dans le même groupe
   - Exemple : 3 élèves à mobilité réduite dans le groupe A uniquement
   - Utilité : faciliter la surveillance rapprochée ou les aménagements matériels

3. **Sans contrainte** → Pas de règle ; laisse l'algorithme libre
   - Utilité : si c'est un simple signalement sans implication pédagogique

**Comment faire** :

1. Entrez un intitulé **neutre** (ex. « Aménagement type A », plutôt que « Asthme »)
2. Sélectionnez la règle de répartition
3. Cliquez **« Ajouter »**
4. Cochez les élèves concernés dans le tableau

**Conseil** : les noms de vigilances restent **confidentiels entre vous et l'équipe**. Ne les imprimez jamais sur un document destiné aux élèves ou aux parents. Les exports PDF/Excel portent uniquement le code de vigilance (ex. « Aménagement type A »), jamais le diagnostic.

---

### Onglet 4 : Paires d'élèves

**Qu'est-ce que c'est ?** Des contraintes fortes : « toujours ensemble » ou « à séparer ».

**Deux types** :

1. **Toujours ensemble** → Binôme d'entraide, élève accompagnant un camarade
   - L'outil les place dans le même groupe coûte que coûte (sauf verrouillage contradictoire)

2. **À séparer** → Conflits connus, dynamique de classe problématique
   - L'outil les met dans des groupes différents

**Comment faire** :

1. Sélectionnez les deux élèves dans les listes déroulantes
2. Choisissez le type de contrainte
3. Cliquez **« Ajouter »**

**Important** : les paires sont appliquées **en dernier**, après la composition initiale. Si une paire ne peut pas être satisfaite (par exemple, deux élèves verrouillés dans des groupes différents avec une contrainte « ensemble »), un **bandeau d'avertissement rouge** s'affiche au-dessus des groupes avec les noms précis.

**Conseil** : les paires surpassent l'équilibre des niveaux — utilisez-les avec parcimonie (max. 3–4 pour une classe de 24).

---

## 🔀 Étape 3 : Composer les groupes

### Choisir une séquence/APSA

En tête de l'étape 3, vous voyez :
- Un sélecteur **« Séquence / APSA »** avec la liste de vos compositions (une par séance thématique)
- Boutons **« + Nouvelle »**, **« ⧉ Dupliquer »**, **« ✎ Renommer »**, **« ✕ Supprimer »**

**Workflow typique** :
1. Créez une composition pour chaque APSA/séquence (natation, badminton, athlétisme…)
2. Les groupes de natation ne sont pas forcément les mêmes que ceux de badminton
3. Dupliquez une composition existante comme point de départ si vous voulez faire une légère variation

### Réglages de composition

**Nombre de groupes** : 2 à 10 (souvent 4)

**Type de groupes** :
- **Homogènes** (par défaut) → Le groupe A rassemble les scores les plus élevés, le groupe D les plus faibles. Idéal pour l'EPS : une progression pédagogique claire, l'enseignant peut adapter le contenu à chaque groupe.
- **Équilibrés** (hétérogènes) → Chaque groupe a une moyenne de score proche. Idéal si vous cherchez des groupes "justes" pour tous, avec des élèves de différents niveaux qui s'entraident.

**Options** :
- Cochez **« Équilibrer filles / garçons »** si votre classe est mixte et que vous voulez du 50/50 par groupe (au mieux)

### Composer

1. Ajustez le nombre de groupes et le type
2. Cliquez **« Composer les groupes »**

L'outil affiche aussitôt les groupes sous forme de **« chasubles »** colorées (A, B, C…) avec :
- L'effectif par groupe
- La moyenne de score
- Le compteur filles/garçons
- Les puces de vigilance

**Rien n'est figé** : vous pouvez glisser-déposer un élève d'un groupe à l'autre pour l'ajuster à la main.

### Verrouiller des élèves

Le bouton 🔓/🔒 à côté de chaque élève vous permet de le **figer dans son groupe**. Lors d'une recomposition, les élèves verrouillés restent à leur place — utile si vous avez une raison pédagogique de les maintenir stables d'une semaine à l'autre.

### Recomposer (hors verrouillés)

Cliquez **« ↻ Recomposer »** pour composer à nouveau sans toucher aux élèves verrouillés. Pratique après chaque test de diagnostic : vous gardez vos « points d'appui » stables et adaptez les autres.

### Avertissements de paires

Si une contrainte de paire **ne peut pas être satisfaite**, un bandeau rouge s'affiche :
> ⚠ **Contraintes de paires non satisfaites :** [élève A] et [élève B] devraient être **ensemble**

Vous devez alors :
- Déverrouiller l'un des deux élèves et le déplacer à la main, ou
- Revoir la contrainte de paire elle-même

---

## 📊 Étape 4 : Exports et feuille de terrain

### PDF de synthèse (📄)

- **Contenu** : tableau récapitulatif des groupes (effectif, score moyen, mixité, vigilances) + un tableau détaillé par groupe avec tous les noms
- **Usage** : archives, communication à l'équipe, préparation de la séance
- **Fichier** : `groupes_EPS_[classe]_[APSA].pdf`

### Excel (⬇)

- **Feuille 1** : synthèse (groupe, effectif, score…)
- **Feuilles 2+** : une par groupe (noms, scores, performances brutes, vigilances)
- **Usage** : si vous devez faire du traitement de données, récupérer les scores bruts, etc.
- **Fichier** : `groupes_EPS_[classe]_[APSA].xlsx`

### Feuille de terrain (📋)

**La vraiment utile au quotidien.**

- **Format** : A4 paysage, une page par groupe
- **Contenu** : liste des élèves du groupe, colonnes pour plusieurs séances (date, présence, performance, observations)
- **Usage** : imprimez-la sur un porte-bloc ; remplissez-la en direct au gymnase
- **Paramètre** : en haut de la barre d'actions, ajustez le nombre de séances (1 à 6)

**Colonnes** :
- **Prés.** (Présence) : P (présent), D (dispensé), A (absent)
- **Perf.** (Performance) : notez votre évaluation du jour (temps, distance, note…)
- **Observations** : remarques pédagogiques, progrès, points de vigilance

**Point de vigilance** : les élèves signalés par une puce • ont une vigilance donnée. C'est un rappel pour vous ; ne montrez jamais cette feuille à un élève ou un parent sans adapter.

---

## 💾 Sauvegarde et reprise du travail

### Enregistrer un projet

1. Entrez le nom de votre classe (ex. « 5e B »)
2. Cliquez **« ⬇ Enregistrer le projet »**
3. Un fichier `.json` se télécharge avec vos élèves, critères, paires et **toutes les séquences/APSA**

**À faire** : sauvegardez ce fichier sur votre espace personnel du serveur de l'établissement (jamais sur clé USB perso).

### Reprendre un projet

1. Cliquez **« ⬆ Reprendre un projet »**
2. Sélectionnez votre fichier `.json`
3. Tous vos élèves, critères et compositions sont restaurés
4. Vous êtes ramené à la composition active

**Upgrade automatique** : si vous aviez un projet de l'ancienne version (v1), il est converti à la v2 automatiquement à la première ouverture. Vous recevez un message de confirmation.

---

## 🛠️ Conseils pratiques et pièges courants

### Les performances brutes doivent être fiables
- Si vous utilisez un barème, assurez-vous que les seuils correspondent à votre niveau de classe (ne copier pas bêtement les Brochures nationales sans adapter)
- Les tests doivent être **homogènes** (conditions identiques pour tous, équité des passations)

### Regrouper les vigilances n'est pas neutre
- Si vous regroupez 3 élèves à mobilité réduite dans le même groupe, cet enseignant aura plus de charge — est-ce prévu ?
- Consultez l'équipe (CPE, infirmière) avant de regrouper les vigilances

### Les paires surpassent les niveaux
- Si vous mettez deux copains très faibles en « ensemble » et qu'ils se distraient, pensez à cette contrainte avant de blâmer la composition
- C'est un choix pédagogique : une paire d'entraide a du sens ; une paire pour ne pas les séparer et qu'ils se motivent est une hypothèse à vérifier

### Modifier les critères après composition
- Si vous changez un barème **après** avoir composé, les scores se mettent à jour mais les groupes ne bougent pas
- Il faut cliquer « Recomposer » pour réappliquer les niveaux nouveaux
- C'est volontaire (pas de recomposition surprise) ; dites-vous que c'est un contrôle qualité

### L'outil suggère ; vous décidez
- Aucun algorithme n'est neutre ; l'outil ne remplace pas votre diagnostic pédagogique
- Si le résultat vous semble bancal, ajustez à la main, verrouille ce que vous tenez, recomposez le reste
- Le glisser-déposer est votre ami

---

## ❓ Questions fréquentes

**Q. Je n'ai pas de connexion internet la première fois. Que faire ?**  
R. Ouvrez la page une première fois en wifi/connexion filaire. Les bibliothèques (PDF, Excel) se téléchargent. Après, vous pouvez travailler en mode hors ligne.

**Q. Puis-je supprimer une séquence/APSA sans perdre les autres ?**  
R. Oui. Sélectionnez la séquence, cliquez « Supprimer » — les autres séquences restent intactes dans le fichier sauvegardé.

**Q. Les vigilances sont-elles visibles dans les exports ?**  
R. Oui, dans le PDF et l'Excel, avec le nom neutre que vous avez choisi (ex. « Aménagement type A »). Ne partagez ces documents qu'avec l'équipe pédagogique.

**Q. Je veux modifier un élève (nom mal orthographié…). Comment faire ?**  
R. Cliquez directement sur la cellule du tableau — vous pouvez éditer le nom, l'âge, le sexe en ligne.

**Q. Puis-je imprimer directement ?**  
R. Oui : bouton 🖨 en haut de l'étape 4. C'est l'impression classique du navigateur, avec mise en page dédiée (groupes côte à côte).

**Q. Les données élèves restent-elles confidentielles ?**  
R. Absolument. L'outil fonctionne **entièrement dans votre navigateur** — rien n'est envoyé à un serveur. Les fichiers de projet restent sur votre ordinateur ou votre espace réseau.

---

## 📞 Support et questions

Pour toute question technique ou pédagogique sur l'outil, adressez-vous à :
- **[Principal adjoint / Référent pédagogique]** : questions pédagogiques sur la composition
- **[Responsable informatique établissement]** : questions techniques, stockage sécurisé des fichiers

---

## Résumé du workflow (1ère utilisation)

1. ✓ Importer le fichier de la classe
2. ✓ Créer 3–4 bonifications (pratique, leadership…)
3. ✓ Créer 2–3 performances (tests diagnostiques)
4. ✓ Créer 1–2 vigilances (aménagements…)
5. ✓ Créer 2–4 paires si pertinent
6. ✓ Créer une composition « Séquence 1 »
7. ✓ Composer avec réglages par défaut (homogène, 4 groupes)
8. ✓ Ajuster à la main si besoin
9. ✓ Exporter PDF + feuille de terrain
10. ✓ Enregistrer le projet

**Durée estimée** : 15–20 min.

---

**Bonne composition ! 🏊‍♂️⚽🏐**

Collège Jean Jaurès, Gençay  
Juillet 2026
