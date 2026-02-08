# Regles de generation du plan

## Calcul du volume

**Calculer le volume hebdo max disponible** en sommant les durees max de tous les creneaux declares. C'est le plafond absolu du volume hebdomadaire. L'afficher dans l'en-tete du plan comme "Volume hebdo max".

Le volume hebdomadaire DOIT rester sous ce plafond.

## Intensite

Chaque seance d'entrainement DOIT inclure un **indicateur d'intensite** — suivre les conventions par sport definies dans `training-plan-template.md`.

## Periodisation

- Inclure des semaines de decharge toutes les 3-4 semaines
- Inclure des checkpoints de reevaluation (obligatoires, pas optionnels)

## Construction depuis la grille de disponibilites

La grille est le squelette — le plan est construit autour, pas l'inverse :

1. Chaque seance DOIT etre placee dans un creneau declare disponible (jour + moment de la journee)
2. Le sport assigne a une seance DOIT correspondre a ce que l'athlete a declare possible pour ce creneau (ex: si seul "course" est possible mardi matin, pas de natation)
3. Les seances fixes sont non-negociables : les garder telles quelles
4. Les creneaux indisponibles (`-`) ne sont jamais utilises — sans exception
5. Distribuer la charge intelligemment sur les creneaux disponibles : alterner les disciplines, respecter la recuperation entre seances dures, placer les seances cles sur les creneaux avec le plus de temps disponible
6. Inclure un tableau resume "Organisation type de la semaine" montrant la grille avec les seances assignees avant le detail hebdomadaire
