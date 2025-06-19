# 🎨 Guide  CSS

CSS (*Cascading Style Sheets*) permet de **styliser** les pages web HTML. Voici un guide complet pour maîtriser les fondements du CSS.

---

## 📌 1. Qu’est-ce que CSS ?

- **CSS** permet de contrôler la mise en forme (couleur, taille, position, etc.) des éléments HTML.
- Il peut être écrit :
  - en **interne** dans `<style>` ;
  - en **externe** via un fichier `.css` ;
  - ou en **ligne** via l’attribut `style`.

---

## 🧱 2. Sélecteurs

### Sélecteurs de base

```css
h1 { color: red; }
#monId { font-weight: bold; }
.maClasse { font-style: italic; }
```

### Sélecteurs combinés

```css
div p       /* tous les <p> dans un <div> */
div > p     /* <p> enfants directs de <div> */
div + p     /* premier <p> suivant un <div> */
```

### Sélecteurs d’attributs

```css
input[type="text"] { border: 1px solid gray; }
a[href^="https"] { color: green; }
```

---

## 🎨 3. Propriétés de style

### Couleur et arrière-plan

```css
color: red;
background-color: #f2f2f2;
background-image: url("image.jpg");
background-size: cover;
```

### Police

```css
font-family: Arial, sans-serif;
font-size: 16px;
font-weight: bold;
text-align: center;
text-decoration: underline;
```

### Bordure et ombre

```css
border: 1px solid black;
border-radius: 5px;
box-shadow: 2px 2px 5px gray;
```

---

## 📐 4. Marges et paddings

```css
margin: 10px;         /* marge extérieure */
padding: 20px;        /* marge intérieure */
margin: 10px 5px;     /* vertical horizontal */
margin: 10px 5px 15px 0; /* top right bottom left */
```

---

## 📏 5. Dimensions

```css
width: 200px;
height: auto;
max-width: 100%;
```

---

## 🧭 6. Positionnement

```css
position: static | relative | absolute | fixed | sticky;
top: 0;
left: 10px;
z-index: 10;
```

---

## 🧩 7. Display & Box Model

```css
display: block | inline | inline-block | none | flex | grid;
visibility: hidden;
overflow: hidden | scroll | auto;
```

### Box model

- **Content** → **Padding** → **Border** → **Margin**

---

## 🧮 8. Flexbox

```css
display: flex;
justify-content: center | space-between | space-around;
align-items: center | stretch | flex-start | flex-end;
flex-direction: row | column;
flex-wrap: wrap;
```

### Exemple

```css
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

---

## 📊 9. Grid

```css
display: grid;
grid-template-columns: 1fr 1fr;
grid-gap: 10px;
grid-template-areas: "header header" "menu main";
```

---

## 🧙 10. Pseudo-classes et pseudo-éléments

```css
a:hover { color: red; }
input:focus { border-color: blue; }
li:first-child { font-weight: bold; }

p::before {
  content: "👉 ";
}
```

---

## 🎯 11. Media Queries (responsive)

```css
@media screen and (max-width: 768px) {
  body {
    background-color: lightgray;
  }
}
```

---

## 🧪 12. Transitions et animations

```css
transition: all 0.3s ease;

@keyframes slideIn {
  from { transform: translateX(-100px); }
  to { transform: translateX(0); }
}

.element {
  animation: slideIn 1s ease-in-out;
}
```

---

## 🧰 13. Variables CSS

```css
:root {
  --main-color: #3498db;
}

body {
  color: var(--main-color);
}
```

---

## 📋 14. Priorité CSS

| Niveau            | Spécificité |
|-------------------|-------------|
| Élément (`div`)   | 0-0-1       |
| Classe (`.a`)     | 0-1-0       |
| ID (`#id`)        | 1-0-0       |
| Inline style      | 1-0-0-0     |
| `!important`      | prioritaire |

---

## 📌 15. Bonnes pratiques

- Utiliser une feuille de style externe (`style.css`)
- Éviter les styles en ligne (`style=""`)
- Organiser les règles par section : base, layout, composants
- Utiliser des **classes réutilisables**
- Préférer les **unités relatives** (`em`, `rem`, `%`) plutôt que fixes (`px`)

---

## 🚀 Conclusion

CSS est un langage puissant pour structurer visuellement vos interfaces. Sa maîtrise est essentielle pour construire des sites modernes, **accessibles**, et **responsive**.

> 🧠 *Maîtrisez les bases, puis explorez les frameworks comme Bootstrap ou Tailwind pour aller plus loin.*
