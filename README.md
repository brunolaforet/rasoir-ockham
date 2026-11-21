# rasoir-ockham

> *Numquam ponenda est pluralitas sine necessitate.*  
> — Guillaume d'Ockham, commentaire des *Sentences* (XIVe siècle).
>
> *Entia non sunt multiplicanda praeter necessitatem.*  
> — Formule la plus célèbre, qui ne figure pas dans ses écrits : elle date du XVIIe siècle (John Punch, 1639).
>
> Paraphrase en français actuel : « Il ne faut jamais multiplier les éléments sans nécessité. »

Un skill au format [Agent Skills](https://agentskills.io) (Claude, Codex, Gemini CLI, Cursor…) qui applique le rasoir d'Ockham : retirer ce qui est superflu (dépendances, étapes, options, sections, affirmations) sans toucher à la fonction principale. À efficacité égale, la solution la plus simple gagne.

Il fonctionne sur le code, les architectures web (PWA, WordPress), les workflows, la stratégie marketing et le copywriting.

## Ce que fait le skill

Claude suit une méthode en 6 étapes :

1. Formuler le besoin réel en une ligne, avec les contraintes dures.
2. Inventorier chaque élément (dépendance, outil, étape, option, section, affirmation).
3. Rendre un verdict par élément : **supprimer**, **fusionner**, **différer** ou **garder**.
4. Appliquer la clôture de Chesterton : si on ignore pourquoi un élément existe, on ne le coupe pas, on pose la question.
5. Présenter la version épurée.
6. Documenter les coupes.

### Trois modes d'intensité

| Mode | Ce que fait Claude |
|---|---|
| **Audit** (par défaut sur un existant) | Liste les coupes proposées, ne modifie rien |
| **Proposition** | Fournit la version épurée à côté de l'original |
| **Application** | Modifie directement, uniquement sur demande explicite |

### Ce qui n'est jamais coupé sans accord explicite

Sécurité et validation des entrées, accessibilité, mentions légales et RGPD, comportement hors-ligne quand c'est la promesse du produit, balises SEO de base, tests et garde-fous, voix de marque.

### Format de sortie

Besoin en une ligne, tableau des coupes (`Élément | Verdict | Raison | Risque`), version épurée, puis bilan chiffré avant/après.

## Exemples d'usage

- « Applique le rasoir d'Ockham à cette architecture de PWA. »
- « Simplifie ce workflow : formulaire → Zapier → Airtable → Make → e-mail. »
- « C'est trop compliqué, vise une version minimale de cette offre. »
- « Taille ce texte d'accueil sans perdre le ton. »

## Installation

### Claude.ai ou application Claude

1. Télécharge `rasoir-ockham.zip` depuis la page [Releases](../../releases).
2. Ouvre **Customize > Skills** (selon l'interface : **Settings > Capabilities**).
3. Clique sur **+**, puis **Create skill**, puis **Upload a skill**.
4. Sélectionne le fichier `rasoir-ockham.zip`, puis active le skill.

### Claude Code

Copie le dossier `rasoir-ockham/` (celui qui contient `SKILL.md`) dans :

- `~/.claude/skills/` pour l'utiliser dans tous tes projets ;
- `.claude/skills/` à la racine d'un projet pour le limiter à ce projet.

### Autres outils compatibles Agent Skills

Le format `SKILL.md` est un standard ouvert, repris par plusieurs outils (Codex, Gemini CLI, Cursor, GitHub Copilot, OpenCode, Windsurf, Cline…). Le skill ne contient que des instructions, sans script ni outil spécifique : copie le dossier `rasoir-ockham/` à l'emplacement prévu par la documentation de ton outil.

> Testé sur Claude. Pour les autres outils, la compatibilité vient de leur documentation et peut varier selon la version.

## Utiliser sans skills (ChatGPT, Gemini, Mistral…)

Si ton outil ne gère pas les skills, la méthode reste utilisable :

1. Ouvre `rasoir-ockham/SKILL.md` et copie tout ce qui suit l'en-tête (à partir de `# rasoir-ockham`).
2. Colle-le au début d'une conversation, ou dans les instructions personnalisées (GPT, Gem, projet).
3. Demande ensuite : « Applique le rasoir d'Ockham à ceci : … ».

Le déclenchement automatique (via la `description`) ne fonctionne qu'avec les outils qui gèrent les skills ; ailleurs, tu invoques la méthode toi-même.

## Structure du dépôt

```
.
├── README.md
├── LICENSE
└── rasoir-ockham/
    └── SKILL.md
```

## Crédits

Skill conçu avec l'aide de Gemini, puis amélioré avec Claude, par Bruno Laforêt ([@brunolaforet](https://github.com/brunolaforet)).

## Licence

[MIT](LICENSE) : tu peux l'utiliser, le modifier et le redistribuer librement, en conservant la mention de copyright.
