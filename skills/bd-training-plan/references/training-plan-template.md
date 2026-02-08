# Template : Plan d'Entrainement

Utilise ce template pour generer le fichier Markdown du plan d'entrainement. Remplis chaque section en fonction du profil de l'athlete et du sport choisi.

---

```markdown
# Plan d'entrainement [Sport] - [Objectif]

> Genere le [date] | Sport : [sport] | Niveau : [niveau]

## Profil athlete

| Parametre | Valeur |
|-----------|--------|
| Nom | [prenom] |
| Niveau | [debutant / intermediaire / avance] |
| Objectif | [objectif specifique] |
| Performance visee | [temps cible, allure, ou objectif de performance] |
| Volume hebdo max | [Xh — calcule depuis la grille de disponibilites] |
| Equipement | [equipement disponible] |
| Contraintes / blessures | [blessures, limitations physiques] |
| Contraintes planning | [resume des seances fixes et indisponibilites] |
| Evenement cible | [nom + date, ou "forme generale"] |
| Duree du plan | [X semaines] |

## Organisation type de la semaine

Grille construite a partir des disponibilites declarees par l'athlete.

| Jour | Matin | Midi | Soir |
|------|-------|------|------|
| Lun | [seance ou -] | [seance ou -] | [seance ou -] |
| Mar | [seance ou -] | [seance ou -] | [seance ou -] |
| Mer | [seance ou -] | [seance ou -] | [seance ou -] |
| Jeu | [seance ou -] | [seance ou -] | [seance ou -] |
| Ven | [seance ou -] | [seance ou -] | [seance ou -] |
| Sam | [seance ou -] | [seance ou -] | [seance ou -] |
| Dim | [seance ou -] | [seance ou -] | [seance ou -] |

> Les seances marquees Fix: sont imposees et non deplacables.
> Les creneaux `-` ne sont jamais utilises.

## Vue d'ensemble (macro-cycle)

| Phase | Semaines | Objectif | Volume hebdo |
|-------|----------|----------|--------------|
| Preparation generale | S1-SX | Construire la base aerobique | Xh |
| Preparation specifique | SX-SY | Developper les qualites specifiques | Xh |
| Pre-competition | SY-SZ | Simuler les conditions de course | Xh |
| Affutage | SZ-fin | Fraicheur maximale pour le jour J | Xh (-30%) |

## Semaines detaillees

### Semaine N - Phase : [nom] | Objectif : [objectif semaine]

| Jour | Creneau | Seance | Volume | Intensite | Details |
|------|---------|--------|--------|-----------|---------|
| Lun | [matin/midi/soir] | [type] | [volume] | [intensite] | [description detaillee] |
| ... | ... | ... | ... | ... | ... |

> **Convention par sport :**
> - **Course a pied** : Volume = distance (ex: 10km), Intensite = allure (ex: 5'00/km). Pour les fractionnes, decrire dans Details (ex: "8x400m a 3'50/km, recup 200m trot").
> - **Velo** : Volume = duree (ex: 1h30), Intensite = zone (Z1-Z5).
> - **Natation** : Volume = distance (ex: 2000m), Intensite = allure (ex: 1'50/100m) ou zone (Z2-Z3).

**Volume total semaine : Xh (dont Xkm CAP, Xm natation) | Charge : [legere/moderee/elevee/decharge]**

> Le volume total est toujours en heures/minutes (temps total d'entrainement). Pour la CAP, convertir distance x allure en duree pour le cumul. Ajouter le detail km CAP et metres natation entre parentheses.

> Repeter ce bloc pour chaque semaine du plan.

## Points de reevaluation

Des checkpoints integres au plan pour ajuster si necessaire :

| Semaine | Questions a se poser | Action si probleme |
|---------|---------------------|--------------------|
| S4 | Fatigue excessive ? Douleurs ? Progression ressentie ? | Reduire volume de 20% la semaine suivante |
| S8 | Objectif toujours realiste ? Motivation ? Forme physique ? | Ajuster l'objectif ou le volume |
| S[fin-2] | Confiance ? Sensations ? Stress ? | Alleger si besoin, priorite a la fraicheur |

## Gestion des contraintes

[Section a adapter selon les blessures/contraintes declarees — omettre si aucune contrainte]

### [Nom de la contrainte]

- **Precautions** : [ce qu'il faut faire]
- **Signaux d'alerte** : [quand s'arreter]
- **Alternatives** : [seances de remplacement si douleur]

## Conseils complementaires

### Recuperation
- [conseils adaptes au niveau et au sport]

### Nutrition
- [grandes lignes, pas de regime detaille]

### Mental
- [preparation mentale si evenement cible]

---

> **Avertissement** : Ce plan d'entrainement a ete genere par une intelligence artificielle. Il ne constitue en aucun cas un avis medical ni un conseil sportif professionnel. Son contenu peut contenir des erreurs ou des recommandations inadaptees a votre situation personnelle. Avant de suivre ce programme, consultez un medecin et/ou un entraineur diplome. L'utilisation de ce plan se fait sous votre entiere responsabilite.
```

---

## Notes pour l'agent

- Toujours remplir la colonne **Intensite** pour chaque seance : allure (min/km) pour la CAP, zone (Z1-Z5) pour le velo, allure ou zone pour la natation
- Les semaines de decharge doivent etre clairement identifiees
- Le **volume hebdo max** est calcule en sommant les durees max de tous les creneaux declares — c'est le plafond absolu
- Ne jamais depasser le volume hebdo max sans le signaler
- La section "Organisation type de la semaine" est obligatoire — elle montre comment les disponibilites de l'athlete se traduisent en seances
- Les points de reevaluation sont obligatoires, pas optionnels
- La section "Gestion des contraintes" n'apparait que si l'athlete a declare des contraintes physiques
- La section "Conseils complementaires" reste concise (5-10 lignes max par sous-section)
