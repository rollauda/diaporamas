---
title: marp
layout: default
nav_order: 40
published: false
---

## prévisualisation
Vous pouvez activer la prévisualisation du code HTML dans Marp Markdown avec `markdown.marp.enableHtml` option dans le json. 
→ shift+cmd+P : `ouvrir les paramètres json`

## Sans le plugin vscodium
Pour installer Marp et intégrer des présentations Marp dans un site Jekyll avec le thème Just the Docs, vous pouvez suivre les étapes suivantes :

1. Tout d'abord, installez Marp en utilisant la commande suivante dans le terminal : 

```
npm install -g @marp-team/marp-cli
```

2. Créez un fichier Markdown pour votre présentation Marp en utilisant un éditeur de texte. Par exemple, créez un fichier `presentation.md`.

3. Dans votre fichier Markdown, incluez les méta-données suivantes en haut du fichier :

```yaml
---
marp: true
---
```

Ces méta-données indiquent à Marp de traiter le fichier comme une présentation.

4. Écrivez votre présentation en utilisant la syntaxe Marp. Vous pouvez trouver des exemples de syntaxe sur le site Web de Marp.

5. Exportez votre présentation au format HTML en exécutant la commande suivante dans le terminal :

```
marp presentation.md --html
```

Cela créera un fichier HTML pour votre présentation.

6. Intégrez votre présentation dans votre site Jekyll. Vous pouvez utiliser la balise `<iframe>` pour intégrer votre présentation dans une page de votre site.

7. Si vous utilisez le thème Just the Docs, vous pouvez intégrer votre présentation dans une page en créant un fichier Markdown pour la page et en incluant le code HTML suivant :

```html
<iframe src="/path/to/presentation.html" width="100%" height="600px" frameborder="0"></iframe>
```

Assurez-vous de remplacer `/path/to/presentation.html` par le chemin d'accès réel à votre fichier HTML de présentation.

8. Construisez et visualisez votre site Jekyll pour voir votre présentation intégrée.

## avec le plugin

Pour intégrer la syntaxe de Marp dans une page Markdown d'un site statique Jekyll avec l'extension Marp pour VSCode, suivez les étapes ci-dessous :

1. Installez l'extension Marp pour VSCode. Pour cela, ouvrez Visual Studio Code, accédez à la vue des extensions (Ctrl + Maj + X) et recherchez "Marp".

2. Créez une nouvelle page Markdown dans votre site Jekyll, ou ouvrez une page existante.

3. Ajoutez les métadonnées YAML pour votre page Jekyll en haut du fichier, comme suit :

```yaml
---
layout: default
title: Ma page Marp
---

```

4. Écrivez votre contenu de page en utilisant la syntaxe de Marp. Par exemple :

```markdown
---
marp: true
---

# Titre de la présentation

Contenu de la présentation

---

## Deuxième diapositive

Contenu de la deuxième diapositive

---
```

Notez que les métadonnées YAML "marp: true" indiquent à Marp de traiter la page comme une présentation.

5. Enregistrez votre fichier.

6. Générez la présentation en utilisant l'extension Marp pour VSCode. Pour cela, ouvrez le fichier de présentation et appuyez sur Ctrl + Maj + P (ou Cmd + Maj + P sur Mac) pour ouvrir la palette de commandes. Recherchez "Marp : Exporter en HTML" et sélectionnez cette option.

7. Marp exportera la présentation sous forme de fichier HTML et l'enregistrera dans le même dossier que votre fichier Markdown.

8. Intégrez la présentation dans votre page Jekyll en utilisant la balise `<iframe>` suivante :

```html
<iframe src="/path/to/presentation.html" width="100%" height="600px" frameborder="0"></iframe>
```

Assurez-vous de remplacer "/path/to/presentation.html" par le chemin d'accès réel à votre fichier HTML de présentation.

9. Construisez et visualisez votre site Jekyll pour voir votre présentation intégrée.

Il est important de noter que pour intégrer la présentation dans votre page Jekyll, vous devrez répéter les étapes 6 à 9 chaque fois que vous modifiez la présentation.