# Documentación del UI KIT

---

## Este es un documento que expone lo que debe llevar cada componente según su modelo atómico, considerando html, css y js.

---

# Componente: "Button"

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
<div class="textfield">
  <input name="nombre" id="nombre" type="text" placeholder="Nombre" />
  <label for="nombre">Nombre</label>
</div>
```

CSS

```css
div {
  padding: 10px;
  border: 1px solid black;
}
```

# Componente: "Input"

## descripción general:

El siguiente código crea un campo de texto con una etiqueta descriptiva. La etiqueta ayuda a los usuarios a entender qué información deben ingresar en el campo.

- **Tipo de componente**
- **Atributos**
- **Métodos**

## Dependencias

## Guia de uso

| class             | descrip                                                   | uso                                 |
| ----------------- | --------------------------------------------------------- | ----------------------------------- |
| textfield         | Se utiliza para agrupar los elementos del campo de texto. | class="textfield"                   |
| texfield_outlined | Se utiliza para agrupar los elementos del campo de texto. | class="textfield texfield_outlined" |

JS

```Javascript
function holaMundo(){
console.log("Hola mundo")
}
```

HTML

```html
<div class="textfield">
  <input name="nombre" id="nombre" type="text" placeholder="Nombre" />
  <label for="nombre">Nombre</label>
</div>
```

CSS

```css
.textfield {
  position: relative;
  width: 100%;
  background-color: inherit;
}
.textfield input::placeholder {
  opacity: 0;
}
.textfield > input {
  width: 100%;
  height: 60px;
  font-size: 1.2em;
  padding: 10px;
  outline: none;
  border-bottom: 1px solid #ccc;
  border-left: none;
  border-right: none;
  border-top: none;
}

.texfield_outlined > input {
  border: 1px solid #ccc;
  border-color: #cccccc;
  border-radius: 0.2em;
}

.textfield label {
  position: absolute;
  left: 10px;
  top: 50%;
  transform: translateY(-50%);
  font-size: 1.2em;
  color: #818181;
  letter-spacing: 1px;
  transition: 0.3s;
  font-family: "Roboto", sans-serif;
  font-weight: 600;
}

.textfield input:focus + label,
.textfield input:not(:placeholder-shown) + label {
  top: 0;
  font-size: 0.8em;
  color: var(--primary-color);
  background: inherit;
  padding: 7px;
}

.textfield input:focus {
  border-bottom: 2px solid var(--primary-color);
}

.texfield_outlined input:focus {
  border: 2px solid var(--primary-color);
}
```

# Componente: "Textarea"

## descripción general:

Es un elemento que permite a los usuarios escribir y editar texto en varias líneas, ofrecen más espacio y flexibilidad para la entrada de texto extensiva.

- **Tipo de componente**
- **Atributos**
- **Métodos**

## Dependencias

## Guia de uso

| class             | descrip                                                          | uso                                 |
| ----------------- | ---------------------------------------------------------------- | ----------------------------------- |
| textfield         | Elemento HTML utilizado para crear un campo de texto multilínea. | class="textfield"                   |
| texfield_outlined | Elemento HTML utilizado para crear un campo de texto multilínea. | class="textfield texfield_outlined" |

JS

```Javascript

```

HTML

```html
<div class="textfield">
  <textarea
    name="c"
    id="comentario"
    rows="4"
    placeholder="Comentario"
    style="resize: none"
  ></textarea>
  <label for="comentario">Comentario</label>
</div>
```

CSS

```css
.textfield textarea::placeholder {
  opacity: 0;
}
.textfield > textarea {
  width: 100%;
  height: 120px;
  font-size: 1.2em;
  padding: 10px;
  outline: none;
  border-bottom: 1px solid #ccc;
  border-left: none;
  border-right: none;
  border-top: none;
}

.texfield_outlined > textarea {
  border: 1px solid #ccc;
  border-color: #cccccc;
  border-radius: 0.2em;
}

.textfield label {
  position: absolute;
  left: 10px;
  top: 50%;
  transform: translateY(-50%);
  font-size: 1.2em;
  color: #818181;
  letter-spacing: 1px;
  transition: 0.3s;
  font-family: "Roboto", sans-serif;
  font-weight: 600;
}

.textfield textarea:focus + label,
.textfield textarea:not(:placeholder-shown) + label {
  top: 0;
  font-size: 0.8em;
  color: var(--primary-color);
  background: inherit;
  padding: 7px;
}

.textfield textarea:focus {
  border-bottom: 2px solid var(--primary-color);
}

.texfield_outlined textarea:focus {
  border: 2px solid var(--primary-color);
}
```

## checkbox

#### Descripción

El código anterior crea un checkbox con una etiqueta descriptiva. La etiqueta ayuda a los usuarios a entender qué opción están seleccionando.

Se genera una serie de checkboxes con etiquetas asociadas. Cada `input` de tipo `checkbox` está enlazado a un `label` a través del atributo `for`, que debe coincidir con el `id` del `input`.

La clase `checkbox` agrupa los elementos y aplica estilos CSS específicos para los checkboxes, personalizando su apariencia y comportamiento cuando son seleccionados o al pasar el mouse sobre ellos.

| clase                      | descripcion                                         | uso                               |
| -------------------------- | --------------------------------------------------- | --------------------------------- |
| checkbox                   | checkbox simple                                     | class="checkbox"                  |
| checkbox_primary           | el checkbox toma el color primario                  | class="checkbox primary           |
| checkbox_primary_lighten   | el checkbox toma el color primario pero mas claro   | class="checkbox primary_lighten   |
| checkbox_secondary         | el checkbox toma el color secundario                | class="checkbox secondary         |
| checkbox_secondary_lighten | el checkbox toma el color secundario pero mas claro | class="checkbox secondary_lighten |
| checkbox_tertiary          | el checkbox toma el color terciario                 | class="checkbox tertiary          |
| checkbox_tertiary_lighten  | el checkbox toma el color terciario pero mas claro  | class="checkbox tertiary_lighten  |

### Plantilla de ejemplo

```HTML
<div class="checkbox primary">
<input type="checkbox" name="checkbox" id="checkbox1">
<label for="checkbox1">checkbox 1</label>
</div>
```

- `div`: en el div de ir la clase
- `id` & `for` deben tener el mismo atributo
  tiene menú contextual
