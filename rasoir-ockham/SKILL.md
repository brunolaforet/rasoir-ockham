---
name: rasoir-ockham
description: "Appliquer le rasoir d'Ockham au code, aux architectures web (PWA, WordPress), aux workflows, à la stratégie marketing et au copywriting pour retirer les entités, dépendances, étapes ou affirmations superflues sans perdre la fonction principale. À utiliser quand l'utilisateur demande de simplifier, auditer, tailler, alléger, dégraisser, viser une version minimale ou un MVP, réduire la sur-ingénierie ou dit « c'est trop compliqué », ou invoque le rasoir d'Ockham."
---
# rasoir-ockham

Retire toute complexité superflue (technique, stratégique, rédactionnelle) en conservant intact chaque élément indispensable. À égalité d'efficacité, la solution la plus simple gagne.

## Quand l'utiliser

* L'utilisateur invoque Ockham ou demande de simplifier, alléger, tailler, dégraisser.
* Audit d'une architecture, d'une PWA, d'un site WordPress, d'un workflow ou d'une pile d'outils.
* Resserrage d'un positionnement, d'une offre, d'un copywriting ou d'options de décision.

## Mode d'intensité

Déduis le mode de la demande. En cas de doute, prends le plus prudent.

1. **Audit** : liste les coupes proposées, ne modifie rien. (Mode par défaut pour un fichier ou un système existant.)
2. **Proposition** : fournis la version épurée à côté de l'original, l'utilisateur valide.
3. **Application** : modifie directement, seulement si l'utilisateur le demande explicitement.

## Étapes

1. **Besoin réel :** formule en une ligne l'objectif concret et les contraintes dures, avant de toucher à quoi que ce soit.
2. **Inventaire :** liste chaque dépendance, outil, étape, option, section ou affirmation.
3. **Verdict par élément :**
   * **Supprimer** : sa disparition ne casse rien de mesurable.
   * **Fusionner** : doublonne un autre élément.
   * **Différer** : utile plus tard, pas pour l'objectif actuel.
   * **Garder** : son retrait casse le résultat principal ou une garantie (voir « Ne jamais couper »).
   Test : « si je retire X, qu'est-ce qui casse concrètement, et quel est le coût de le réintroduire ? »
4. **Clôture de Chesterton :** si tu ignores pourquoi un élément existe, ne le coupe pas. Signale-le et pose la question.
5. **Voie par défaut :** présente la version épurée, avec une porte de sortie explicite seulement s'il existe un vrai arbitrage.
6. **Documenter les coupes :** dis brièvement ce qui est retiré ou fusionné et pourquoi la version allégée tient.

## Format de sortie

* **Besoin :** une ligne.
* **Coupes :** tableau `Élément | Verdict | Raison | Risque`.
* **Version épurée :** le livrable (code, texte, schéma, liste d'étapes).
* **Bilan :** avant/après chiffré (lignes, dépendances, étapes, mots, options), ce qui prouve le gain.

Pour une demande courte, condense : besoin, version épurée, deux ou trois coupes clés.

## Ne jamais couper sans accord explicite

* Sécurité, validation des entrées, gestion des secrets.
* Accessibilité (contrastes, alternatives textuelles, navigation clavier).
* Mentions légales, RGPD, consentement.
* Comportement hors-ligne ou de repli quand c'est la promesse du produit.
* Balises SEO de base (title, meta description, hiérarchie des titres, canonical).
* Tests, sauvegardes et garde-fous qui préviennent une panne.
* Voix de marque en copywriting : tailler ne veut pas dire aplatir le ton.

## Exemples avant/après

**Code / PWA**
* Avant : ajout d'une bibliothèque de dates (30 ko) pour afficher « samedi 21 novembre ».
* Après : `Intl.DateTimeFormat('fr-FR', {...})` natif. Dépendance en moins, même résultat.

**Workflow**
* Avant : formulaire → Zapier → Airtable → Make → e-mail.
* Après : formulaire → e-mail de notification. Airtable et les deux automatisations ne servaient pas l'objectif (être prévenu d'un contact).

**Copywriting**
* Avant : « Nous sommes une agence innovante et passionnée qui accompagne ses clients vers l'excellence digitale. »
* Après : « Je crée votre site en 10 jours, prêt à générer des demandes de devis. » Une promesse vérifiable remplace trois adjectifs creux.

**Offre**
* Avant : 5 formules, 12 options, 3 niveaux de support.
* Après : 2 formules et une option. Le choix devient une décision de 30 secondes.

## Pièges

* Minimalisme n'est pas suppression d'une exigence : ne coupe pas ce qui prévient une panne, une faille ou une fonction cœur.
* Ockham est une heuristique, pas une loi. Si simplifier fait perdre en exactitude (diagnostic, fait vérifiable, contrainte réglementaire), dis-le au lieu de couper.
* Préfère des suppressions et remplacements concrets à des conseils vagues du type « fais simple ».
* Reste net et direct : pas de dissertation philosophique.
