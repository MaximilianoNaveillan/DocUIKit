# Documentación del UI KIT

---

## Este es un documento que expone lo que debe llevar cada componente según su modelo atómico, considerando html, css y js.

---

# Componente:

## descripción general:

- **Tipo de componente**
- **Atributos**
- **Métodos**

## Dependencias

## Guia de uso

| class               | descrip                           | uso                             |
| ------------------- | --------------------------------- | ------------------------------- |
| btn                 | botón simple de texto             | class="btn"                     |
| btn-primary-lighten | botón de color primário aligerado | class="btn btn-primary-lighten" |
| text_icon           | ...                               | class="btn text_icon"           |

JS

```Javascript
function holaMundo(){
console.log("Hola mundo")
}
```

HTML

```html
<div>
  <div>...</div>
</div>
```

CSS

```css
div {
  padding: 10px;
  border: 1px solid black;
}
```

# Componente: Banner

## Descripción general: Este componente está situado debajo de la barra de navegación y su principal función es indicarle al usuario en qué interfaz se encuentra.

- **Tipo de componente:**
  Este es el componente banner.
- **Atributos:**
  El componente está situado debajo de la barra de navegación, ofrece al usuario información sobre en qué interfaz se encuentra, también incluye el ícono de acuerdo a dicha interfaz según los íconos especificados en el menú principal.
- **Métodos:**
  No cuenta con métodos en JS.

## Dependencias

## Guia de uso

| class          | descrip                                                                        | uso                    |
| -------------- | ------------------------------------------------------------------------------ | ---------------------- |
| banner         | corresponde al contenedor de las etiquetas que componen el banner              | class="banner"         |
| banner_icon    | corresponde al ícono que muestra el banner según dónde se encuentre el usuario | class="banner_icon"    |
| banner_text    | corresponde al texto que se muestra en el banner                               | class="banner_text"    |
| banner_colores | corresponde a la imagen de la paleta de colores al final del banner            | class="banner_colores" |

HTML

```html
<div class="banner">
  <div class="banner_icon">
    <span><img src="./public/icn_veterinaria.svg" alt="ícono" /></span>
  </div>
  <div class="banner_text">
    <span>El banner indica que estás en <b>(Indicar sección)</b></span>
  </div>
  <img
    class="banner_colores"
    src="./public/paleta-colores.png"
    alt="Barra de colores"
  />
</div>
```

CSS

```css
.banner {
  width: 100%;
  height: 100px;
  max-height: 100px;
  background-color: #fff;
  box-shadow: 4px 4px 10px rgba(0, 0, 0, 0.6);
  display: grid;
  grid-template-areas:
    "icono texto texto texto texto texto texto texto texto texto texto"
    "icono texto texto texto texto texto texto texto texto texto texto"
    "banner banner banner banner banner banner banner banner banner banner banner";
  padding: 0;
  gap: 0;
}
.banner_icon {
  grid-area: icono;
  height: 90px;
  max-height: 90px;
  margin: auto;
  justify-content: center;
  align-content: center;
}
.banner_text {
  grid-area: texto;
  color: #818181;
  font-size: 16px;
  align-content: center;
}
.banner_colores {
  grid-area: banner;
  width: 100%;
  height: 10px;
  max-height: 10px;
}
```
