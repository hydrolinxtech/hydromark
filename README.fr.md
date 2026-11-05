# HydroMark — complément Markdown pour OneNote avec un assistant IA

[English](README.md) · [简体中文](README.zh.md) · [繁體中文](README.zh-TW.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · [Español](README.es.md) · [Português](README.pt.md) · [Русский](README.ru.md) · [Deutsch](README.de.md) · **Français** · [हिन्दी](README.hi.md) · [العربية](README.ar.md) · [Support](SUPPORT.fr.md)

**HydroMark est un complément (add-in) Markdown WYSIWYG pour Microsoft OneNote sous Windows.** Écrivez du Markdown sur une page OneNote, dès la frappe, il est rendu instantanément en contenu OneNote natif — titres, listes, tableaux, listes de tâches, blocs de code, formules LaTeX et diagrammes Mermaid. Aucun export, aucune capture d'écran, aucun changement d'application. Depuis la **v1.1.0**, un **assistant IA** intégré écrit des articles rendus, des tableaux et des opérations de page directement dans vos notes.

> ⚠️ **Ceci est un dépôt open source qui contient une partie du code et de la documentation du projet HydroMark.** Il accueille aussi les annonces produit et les retours de la communauté (Issues et Discussions). Voir [Licence et code source](#licence-et-code-source) ci-dessous.

---

## Qu'est-ce que HydroMark ?

![HydroMark dans OneNote : le ruban HydroMark, le Markdown rendu sur la page, le panneau de table des matières et le panneau Assistant IA](assets/hydromark-onenote.png)

HydroMark est un **complément Markdown pour OneNote** : un complément Windows qui intègre un véritable éditeur Markdown dans Microsoft OneNote. Vous continuez à écrire dans les bloc-notes, le canevas et la synchronisation cloud de OneNote, mais vous obtenez le flux de travail Markdown que vous voulez vraiment — tapez `## Heading` puis une espace, et la page affiche un titre rendu au lieu de la syntaxe brute.

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
| **IA**            | Intégrée — 14 fournisseurs, apportez votre propre clé API           |
| **Langues**       | English · 简体中文 · 繁體中文 · 日本語 · 한국어 · Español · Português · Русский · Deutsch · Français · हिन्दी · العربية |

## ✨ Fonctionnalités

| Fonctionnalité          | Ce qu'elle fait                                                    | Raccourci       |
| ----------------------- | ------------------------------------------------------------------ | --------------- |
| 🤖 **Assistant IA**     | Écrit articles, tableaux & exécute les actions du complément dans la page | `Alt+A`    |
| ✍️ **Rendu instantané** | Titres, listes et plus se formatent pendant la frappe              | `#` / `-` + Espace |
| 🔁 **Source ↔ rendu**   | Bascule entre Markdown brut et rendu, par page ou par paragraphe   | —               |
| 📥 **Coller Markdown**  | Transforme un Markdown copié en note finie                         | `Ctrl+Shift+V`  |
| 💻 **Coloration du code**| Plus de 200 langages, 100+ thèmes, copie en un clic                | —               |
| ∑ **Mathématiques LaTeX**| Formules en ligne & en bloc comme équations OneNote natives       | `$…$`           |
| 📊 **Diagrammes**       | 26+ types Mermaid / ZenUML : flux, séquence, Gantt, carte mentale… | —               |
| ▱ **Tableaux**          | Bascule pleine largeur ↔ ajusté au contenu, conservée              | `Alt+W`         |
| ☑️ **Listes de tâches** | Cases cliquables, export en `- [x]` / `- [ ]`                       | —               |
| ⌨️ **Commandes slash**  | Palette de commandes pour insérer des blocs rapidement             | `/`             |
| 🖍️ **Blocs de mise en évidence** | Met en avant visuellement les notes importantes            | —               |
| 📑 **Sommaire & largeur**| Table des matières auto ; largeur manuelle / auto                | —               |
| 🌙 **Mode sombre**      | Contenu, boîtes de dialogue & barre IA suivent OneNote             | —               |
| 🔄 **Import / Export**  | Fichiers Markdown entrants et sortants (images optionnelles)        | `F8`            |

### 🤖 Assistant IA — la fonctionnalité phare (nouveau dans la 1.1.0)

La plupart des barres latérales IA vous remettent un mur de texte à copier-coller. L'assistant de HydroMark **écrit dans vos notes** :

- **Exécute des actions du complément, pas seulement du chat** — insère un article entièrement rendu, construit des tableaux, exécute des opérations de page (rendu, export, table des matières, largeur de page) ; les résultats des actions sont renvoyés dans la conversation pour que le modèle puisse confirmer ou se corriger.
- **Des tableaux sur commande, avec la largeur demandée** — `insert_table` prend en charge les dispositions pleine largeur de page et **ajustées au contenu** ; le parcours IA partage le même moteur de tableaux que le basculement de largeur `Alt+W`.
- **Apportez votre propre modèle** — 14 fournisseurs intégrés (OpenAI, DeepSeek, Kimi, Zhipu, Qwen…), Base URL personnalisée pour tout le reste. Votre clé API reste sur votre machine ; aucun serveur intermédiaire.
- **Multimodal** — collez une capture d'écran dans le chat et référencez-la avec des modèles multimodaux.
- **Suivi de la langue** — posez votre question en français, obtenez une réponse en français ; en anglais, une réponse en anglais.
- **Inclus dans toutes les licences** — l'essai gratuit de 14 jours et tous les niveaux payants. Ouvrez-le avec `Alt+A` ou le groupe **AI** du ruban.

### 📝 Rendu Markdown

- **Rendu Markdown instantané** — tapez `#` ou `-` puis une espace : la ligne est déjà formatée ; les autres blocs restent rendus par Entrée ou F5 (WYSIWYG).
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

## 🚀 Pour commencer

1. **Téléchargez** l'installateur multilingue unique depuis [https://hydromark.hydrolinx.top/download](https://hydromark.hydrolinx.top/download) (nécessite Windows 7+ et OneNote **bureau** 2013+).
2. **Lancez** l'installateur — il s'adapte automatiquement à OneNote 32 bits et 64 bits, il n'y a pas de package x86 / x64 séparé à choisir.
3. **Ouvrez OneNote** et repérez l'onglet **HydroMark** dans le ruban.
4. **Écrivez du Markdown** — tapez `## ` puis une espace pour un titre, `- ` puis une espace pour une liste ; les autres blocs se rendent avec Entrée ou `F5`.
5. **Configurez d'abord l'IA** — ouvrez **Paramètres → Modèle IA**, choisissez un fournisseur et saisissez votre clé API (clé à apporter soi-même ; 14 fournisseurs intégrés). Ouvrez ensuite **l'assistant IA** avec `Alt+A` (ou le groupe **AI** du ruban) et laissez-le écrire articles et tableaux directement dans la page.
6. **Exportez** la page courante vers `.md` avec `F8`.

Un essai complet de 14 jours démarre automatiquement — sans carte bancaire. Pour le guide complet, voir la [documentation](https://hydromark.hydrolinx.top/documentation).

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
- Téléchargement : https://hydromark.hydrolinx.top/download
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

Ceci est un **dépôt open source**. Il contient une partie du code source et de la documentation du projet HydroMark ; le reste du projet n'est pas stocké ici.

Vous êtes invité à :

- Lire, étudier et réutiliser le code et la documentation de ce dépôt
- Ouvrir des issues et participer aux discussions pour nous aider à nous améliorer
- Utiliser le nom HydroMark lorsque vous présentez ou évaluez le projet

Merci de ne pas utiliser le nom et la marque HydroMark dans des produits ou services dérivés, afin de ne pas induire les utilisateurs en erreur sur l'origine.

© HydroLinx. HydroMark et son logo sont des marques de HydroLinx.

---

*HydroMark — Markdown, comme OneNote aurait dû le proposer. Désormais avec un assistant IA qui fait la saisie.*
