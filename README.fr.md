# HydroMark — complément Markdown pour OneNote avec un assistant IA

[English](README.md) · [简体中文](README.zh.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Русский](README.ru.md) · [Deutsch](README.de.md) · **Français** · [Support](SUPPORT.fr.md)

**HydroMark est un complément (add-in) Markdown WYSIWYG pour Microsoft OneNote sous Windows.** Écrivez du Markdown sur une page OneNote, appuyez sur Entrée, et il est rendu instantanément en contenu OneNote natif — titres, listes, tableaux, listes de tâches, blocs de code, formules LaTeX et diagrammes Mermaid. Aucun export, aucune capture d'écran, aucun changement d'application. Depuis la **v1.1.0**, un **assistant IA** intégré écrit des articles rendus, des tableaux et des opérations de page directement dans vos notes.

> ⚠️ **Ce dépôt est partiellement open source : une partie du code et de la documentation y est publiée.** Il accueille aussi les annonces produit et les retours de la communauté (Issues et Discussions). Voir [Licence et code source](#licence-et-code-source) ci-dessous.

---

## Qu'est-ce que HydroMark ?

HydroMark est un **complément Markdown pour OneNote** : un complément Windows qui intègre un véritable éditeur Markdown dans Microsoft OneNote. Vous continuez à écrire dans les bloc-notes, le canevas et la synchronisation cloud de OneNote, mais vous obtenez le flux de travail Markdown que vous voulez vraiment — tapez `## Heading`, appuyez sur Entrée, et la page affiche un titre rendu au lieu de la syntaxe brute.

Tout est rendu avec les **éléments natifs de OneNote, et non des images**, de sorte que vos notes Markdown restent modifiables, consultables dans OneNote, disponibles hors ligne et synchronisées avec OneNote sur téléphone, tablette et web. Appuyez sur `F8` pour exporter une page vers `.md`.

Depuis la **v1.1.0**, le complément inclut également un **assistant IA**. Contrairement aux barres latérales IA qui vous donnent du texte à copier-coller, l'IA de HydroMark écrit dans la page : elle insère des articles entièrement rendus, construit des tableaux et exécute des actions du complément telles que le rendu, l'export, la table des matières et la largeur de page — les résultats étant renvoyés au modèle pour qu'il puisse confirmer ou se corriger.

**À qui s'adresse-t-il :** aux développeurs et équipes techniques, aux étudiants et chercheurs, aux équipes produit et opérations — toute personne qui écrit du Markdown mais conserve ses notes dans OneNote.

## Aperçu rapide

| Élément           | Détail                                                              |
| ----------------- | ------------------------------------------------------------------- |
| **Produit**       | HydroMark — complément Markdown pour OneNote avec un assistant IA   |
| **Catégorie**     | Plugin OneNote / extension OneNote / complément COM Office          |
| **Plateforme**    | Windows 7 et versions ultérieures                                   |
| **Application hôte** | OneNote **bureau** 2013+ (2016 / 2019 / 2021 / Microsoft 365)    |
| **Environnement d'exécution** | .NET Framework 4.8+                                      |
| **Non pris en charge** | OneNote pour Windows 10 (UWP / Microsoft Store), macOS, mobile  |
| **Essai**         | Essai complet de 14 jours, sans carte bancaire                      |
| **IA**            | Intégrée — 15 fournisseurs, apportez votre propre clé API           |
| **Languages**     | 简体中文 · English · 日本語 · 한국어 · Deutsch · Français · Español · Русский |

## ✨ Fonctionnalités

### 🤖 Assistant IA — la fonctionnalité phare (nouveau dans la 1.1.0)

La plupart des barres latérales IA vous remettent un mur de texte à copier-coller. L'assistant de HydroMark **écrit dans vos notes** :

- **Exécute des actions du complément, pas seulement du chat** — insère un article entièrement rendu, construit des tableaux, exécute des opérations de page (rendu, export, table des matières, largeur de page) ; les résultats des actions sont renvoyés dans la conversation pour que le modèle puisse confirmer ou se corriger.
- **Des tableaux sur commande, avec la largeur demandée** — `insert_table` prend en charge les dispositions pleine largeur de page et **ajustées au contenu** ; le parcours IA partage le même moteur de tableaux que le basculement de largeur `Alt+W`.
- **Apportez votre propre modèle** — 15 fournisseurs intégrés (OpenAI, DeepSeek, Kimi, Zhipu, Qwen…), Base URL personnalisée pour tout le reste. Votre clé API reste sur votre machine ; aucun serveur intermédiaire.
- **Multimodal** — collez une capture d'écran dans le chat et référencez-la avec des modèles multimodaux.
- **Suivi de la langue** — posez votre question en français, obtenez une réponse en français ; en anglais, une réponse en anglais.
- **Inclus dans toutes les licences** — l'essai gratuit de 14 jours et tous les niveaux payants. Ouvrez-le avec `Alt+A` ou le groupe **AI** du ruban.

### 📝 Rendu Markdown

- **Rendu Markdown en temps réel** — tapez du Markdown, appuyez sur Entrée, il est formaté instantanément (WYSIWYG).
- **Vue double source / rendu** — basculez à tout moment entre le Markdown brut et le rendu, par page ou par paragraphe.
- **Collez du Markdown de n'importe où** — `Ctrl+Shift+V` transforme un bloc Markdown copié depuis une page web, un document ou une réponse d'IA en une note finalisée.
- **Coloration syntaxique du code** — coloration syntaxique pour plus de 200 langages, plus de 100 thèmes, copie en un clic.
- **Mathématiques LaTeX** — formules en ligne et en bloc rendues comme équations OneNote natives.
- **Diagrammes Mermaid / ZenUML** — plus de 26 types de diagrammes : organigramme, séquence, classe, état, Gantt, carte mentale, UML et plus encore.
- **Tableaux avec basculement pleine largeur ↔ ajusté au contenu** — `Alt+W` bascule tout tableau dans les deux sens ; l'état ajusté au contenu est conservé.
- **Listes de tâches** — les cases à cocher restent cliquables et s'exportent comme `- [x]` / `- [ ]`.
- **Commandes slash** — appuyez sur `/` pour ouvrir une palette de commandes et insérer des blocs plus rapidement.
- **Blocs de mise en évidence** — mettez visuellement en avant les notes importantes.
- **Table des matières et largeur de page** — générez ou masquez automatiquement une table des matières ; largeur de page manuelle ou automatique.
- **Adaptation complète au mode sombre** — le contenu rendu, les boîtes de dialogue et la barre latérale IA suivent tous le thème de OneNote.
- **Import / export transparent** — fichiers Markdown en entrée, fichiers Markdown en sortie (images facultatives).

## Questions fréquentes

**Existe-t-il un complément Markdown pour OneNote ?**
Oui — HydroMark est un complément (add-in) Markdown conçu spécifiquement pour Microsoft OneNote bureau sous Windows.

**Puis-je utiliser l'IA pour écrire des notes dans OneNote ?**
Oui. HydroMark inclut un assistant IA qui insère des articles et des tableaux Markdown rendus directement dans la page OneNote active, et peut déclencher des actions du complément telles que le rendu, l'export ou la table des matières.

**HydroMark fonctionne-t-il avec OneNote pour Windows 10, Mac ou mobile ?**
Non. HydroMark prend en charge OneNote **bureau** 2013 et versions ultérieures (2016 / 2019 / 2021 / Microsoft 365) sous Windows 7+. La version UWP / Microsoft Store de OneNote, macOS et mobile ne sont **pas** pris en charge.

**HydroMark est-il un plugin OneNote ou une application séparée ?**
C'est un complément OneNote, pas une application de prise de notes séparée. Il s'installe dans OneNote et ajoute un onglet **HydroMark** au ruban ; vos notes restent dans vos bloc-notes existants.

**Le contenu Markdown reste-t-il natif dans OneNote ?**
Oui. Le rendu utilise les éléments natifs de OneNote plutôt que des images, de sorte que les notes restent modifiables, consultables et synchronisables sur tous les clients OneNote. Les pages peuvent toujours être exportées vers `.md`.

**Comment l'installer ?**
Téléchargez l'installateur multilingue unique depuis le site web, exécutez-le et ouvrez OneNote — un onglet **HydroMark** apparaît dans le ruban. L'installateur s'adapte automatiquement à OneNote 32 bits et 64 bits.

**Est-ce gratuit ?**
Il existe un essai complet de 14 jours. Ensuite, les licences sont par appareil (e-mail + clé) : offres Individual et Family, Basic et Pro, à vie ou annuelle.

## 🌐 Liens officiels

- Site web (anglais) : https://hydromark.hydrolinx.top
- Site web (中文) : https://hydromark.hydrolinx.cn
- Documentation : https://hydromark.hydrolinx.top/documentation
- Tarifs : https://hydromark.hydrolinx.top/pricing
- Journal des modifications : https://hydromark.hydrolinx.top/changelog

## 💬 Commentaires et assistance

C'est le meilleur moyen de nous contacter :

- 🐛 **Rapports de bugs et demandes de fonctionnalités** → ouvrez une [Issue](../../issues)
- 💡 **Idées et discussions générales** → utilisez les [Discussions](../../discussions)
- 📧 **E-mail** → support@hydrolinx.top
- 📖 **Guide d'assistance** → [SUPPORT.fr.md](SUPPORT.fr.md)

Avant d'ouvrir une issue, veuillez rechercher les issues existantes pour éviter les doublons, et inclure votre version de Windows / OneNote ainsi que les étapes de reproduction.

## 🗺️ Feuille de route

Nous améliorons activement HydroMark. À court terme :

- Des actions IA plus intelligentes — résumés intelligents, étiquetage automatique et davantage d'opérations du complément que l'assistant peut exécuter
- Plus de types de diagrammes et de modèles de blocs
- Une intégration OneNote plus large

Suivez la page [Releases](../../releases) pour les notes de mise à jour.

## Licence et code source

HydroMark est un **logiciel propriétaire**. Le code source n'est **pas open source** et n'est pas distribué via ce dépôt. Tous droits réservés.

Vous êtes invité à :

- Lire la documentation et les annonces ici
- Ouvrir des issues et participer aux discussions pour nous aider à nous améliorer

Vous ne pouvez **pas**, sans autorisation écrite explicite :

- Copier, modifier ou redistribuer le code source de HydroMark
- Utiliser le nom / la marque HydroMark dans des produits dérivés

© HydroLinx. Tous droits réservés.

---

*HydroMark — Markdown, comme OneNote aurait dû le proposer. Désormais avec un assistant IA qui fait la saisie.*
