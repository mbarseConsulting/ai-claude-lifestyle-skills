# Verification du plan (QA)

Apres production du plan, **le relire** et executer TOUS les checks suivants. Afficher un rapport de verification au format ci-dessous. Si un check echoue, **corriger le plan immediatement** et re-executer les checks en erreur jusqu'a ce que tout passe.

## Checks a effectuer

1. **Volume hebdo — calcul arithmetique** : Pour chaque semaine, calculer la **duree totale estimee** en additionnant les durees de toutes les seances. Pour les seances dont le volume est en distance (CAP, natation), estimer la duree : `duree = distance x allure`. Exemple : 10km a 5'00/km = 50min. Pour les fractionnes, estimer la duree totale incluant echauffement + blocs + recup (souvent indiquee dans Details). Verifier que ce cumul correspond au total affiche dans la ligne "Volume total semaine". Tolerance : +/- 5min. **Le volume total semaine est toujours exprime en heures/minutes** (c'est le temps total d'entrainement), jamais en km.
2. **Volume hebdo — plafond** : Verifier qu'aucune semaine ne depasse le volume hebdo max declare dans le profil (sauf mention explicite).
3. **Creneaux — jour** : Chaque seance doit etre placee un jour ou l'athlete a declare au moins un creneau disponible. Aucune seance le jour de repos (sauf semaine de course).
4. **Creneaux — moment de la journee** : Chaque seance doit etre dans le bon creneau (matin/midi/soir) tel que declare par l'athlete.
5. **Creneaux — sport** : Le sport de chaque seance doit correspondre a ce que l'athlete a declare possible pour ce creneau. Exemple : si le creneau est "CAP", pas de natation.
6. **Creneaux — duree max** : Aucune seance ne depasse la duree max declaree pour son creneau.
7. **Seances fixes** : Toutes les seances marquees `Fix:` dans le profil sont presentes chaque semaine, au bon jour et creneau, avec la bonne duree.
8. **Intensite** : Chaque seance (hors repos) a une intensite renseignee dans la colonne Intensite, au bon format selon le sport (voir conventions dans `training-plan-template.md`). Une seance CAP avec uniquement une zone (ex: "Z2") sans allure est une erreur.
9. **Decharges** : Il y a une semaine de decharge toutes les 3-4 semaines. Le volume de decharge est reduit de 30-40% par rapport a la semaine precedente.
10. **Progression** : Le volume augmente de facon progressive entre les decharges (max +10%/semaine hors relance post-decharge).
11. **Checkpoints** : La section "Points de reevaluation" existe et contient au moins 3 checkpoints.
12. **Duree du plan** : Le nombre de semaines correspond a l'ecart entre la date de debut et la date de l'evenement.
13. **Contraintes / blessures** : Si le profil declare des blessures ou contraintes, verifier qu'aucune seance ne les viole (pas de charge sur zone blessee sans adaptation explicite).

## Format du rapport de verification

Afficher le rapport a l'athlete apres production du plan :

```
## Verification du plan

| # | Check | Statut | Detail |
|---|-------|--------|--------|
| 1 | Volume calcul | OK/ERREUR | [detail si erreur : semaine X, calcule Xh, affiche Yh] |
| 2 | Volume plafond | OK/ERREUR | [detail si erreur] |
| 3 | Creneaux jour | OK/ERREUR | [detail si erreur] |
| 4 | Creneaux moment | OK/ERREUR | [detail si erreur] |
| 5 | Creneaux sport | OK/ERREUR | [detail si erreur] |
| 6 | Creneaux duree | OK/ERREUR | [detail si erreur] |
| 7 | Seances fixes | OK/ERREUR | [detail si erreur] |
| 8 | Zones intensite | OK/ERREUR | [detail si erreur] |
| 9 | Decharges | OK/ERREUR | [detail si erreur] |
| 10 | Progression | OK/ERREUR | [detail si erreur] |
| 11 | Checkpoints | OK/ERREUR | [detail si erreur] |
| 12 | Duree du plan | OK/ERREUR | [detail si erreur] |
| 13 | Contraintes | OK/ERREUR | [detail si erreur] |
```

- Si toutes les lignes sont OK : afficher "Plan valide." et presenter le resume a l'athlete.
- Si des erreurs sont detectees : corriger le plan et re-executer les checks en erreur. Repeter jusqu'a ce que tout passe. Afficher le rapport final corrige.
