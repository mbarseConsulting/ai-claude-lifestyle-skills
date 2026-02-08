# 🏃‍♂️ AI Claude Lifestyle Skills

_Collection de skills Claude pour le lifestyle, sport et bien-être._

## Vue d'ensemble

**AI Claude Lifestyle Skills** est une collection de skills personnalisés pour Claude AI, spécialisés dans le coaching sportif, la nutrition et le bien-être. Ces skills permettent de créer des plans d'entraînement structurés, des programmes nutritionnels personnalisés et des routines de vie saine adaptées à vos besoins.

Le projet exploite le **système de skills Claude** pour fournir des agents spécialisés capables de générer des plans professionnels, d'ajuster les programmes selon vos retours et de vous accompagner dans vos objectifs lifestyle.

## 🚀 Installation

### Option 1 : Installation manuelle

1. Téléchargez le skill souhaité depuis [Releases](../../releases)
2. Dans Claude.ai, allez dans **Settings > Skills**
3. Cliquez sur **Import skill** et uploadez le fichier `.zip`

### Option 2 : Depuis les sources

1. Clonez ce repo :

```bash
git clone https://github.com/[username]/ai-claude-lifestyle-skills.git
```

2. Compressez le dossier du skill :

```bash
cd ai-claude-lifestyle-skills
zip -r coach-sportif.zip coach-sportif/
```

3. Importez dans Claude (voir Option 1, étape 2-3)

## 📖 Utilisation

### Coach Sportif

**Créer un plan d'entraînement :**

```
Créer un plan d'entraînement pour un 10km en 40min dans 1 mois, avec coach-sportif
```

**Ajuster un plan existant :**

```
J'ai une douleur au genou, ajuste mon plan avec coach-sportif
```

**Exemples de plans :**

- [Plan Triathlon M en 2h05](examples/triathlon-m-2h05.md)
- [Plan 10km sub-40](examples/10km-40min.md)

## 🛠️ Structure des skills

```
ai-claude-lifestyle-skills/
├── coach-sportif/
│   ├── SKILL.md                 # Point d'entrée du skill
│   ├── references/
│   │   ├── coach-persona.md     # Persona du coach
│   │   ├── training-plan-template.md
│   │   ├── generation-rules.md
│   │   ├── qa-checks.md
│   │   └── athlete-profile-template.md
│   └── artefact/                # Plans générés (optionnel)
└── examples/                    # Exemples de plans
```

## 🤝 Contribution

Les contributions sont bienvenues ! Pour ajouter un nouveau skill ou améliorer les existants :

1. Fork le projet
2. Créez une branche (`git checkout -b feature/nouveau-skill`)
3. Commitez vos changements
4. Push vers la branche (`git push origin feature/nouveau-skill`)
5. Ouvrez une Pull Request

## 📄 Licence

[MIT](LICENSE) - Utilisez librement pour vos projets personnels ou professionnels.

## ⚠️ Disclaimer

Ces skills génèrent des plans d'entraînement et conseils à titre informatif uniquement. Ils ne constituent en aucun cas un avis médical ou un conseil professionnel. Consultez toujours un médecin et/ou un entraîneur diplômé avant de débuter un programme d'entraînement.

## 🔗 Liens utiles

- [Documentation Claude Skills](https://docs.anthropic.com/claude/docs/skills)
- [Claude.ai](https://claude.ai)
