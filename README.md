# Documentación del UI KIT

## Componente: "Input"

### descripción general:

El siguiente código crea un campo de texto con una etiqueta descriptiva. La etiqueta ayuda a los usuarios a entender qué información deben ingresar en el campo.

- *Tipo de componente*
- *Atributos*
- *Métodos*

## Guia de uso

| class             | descrip                                                   | uso                                 |
| ----------------- | --------------------------------------------------------- | ----------------------------------- |
| textfield         | Se utiliza para agrupar los elementos del campo de texto. | class="textfield"                   |
| texfield_outlined | Se utiliza para agrupar los elementos del campo de texto. | class="textfield texfield_outlined" |

HTML

html
<div class="textfield">
  <input name="nombre" id="nombre" type="text" placeholder="Nombre" />
  <label for="nombre">Nombre</label>
</div>


JSX

JSX
import "./FormStyle.css";

function InputField() {
  return (
    <>
      <div className="textfield">
        <input name="nombre" id="nombre" type="text" placeholder="Nombre" />
        <label htmlFor="nombre">Nombre</label>
      </div>
    </>
  );
}

export default InputField;


CSS

css
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


# Componente: "Textarea"

## descripción general:

Es un elemento que permite a los usuarios escribir y editar texto en varias líneas, ofrecen más espacio y flexibilidad para la entrada de texto extensiva.

- *Tipo de componente*
- *Atributos*
- *Métodos*

## Dependencias

## Guia de uso

| class             | descrip                                                          | uso                                 |
| ----------------- | ---------------------------------------------------------------- | ----------------------------------- |
| textfield         | Elemento HTML utilizado para crear un campo de texto multilínea. | class="textfield"                   |
| texfield_outlined | Elemento HTML utilizado para crear un campo de texto multilínea. | class="textfield texfield_outlined" |

HTML

html
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


CSS

css
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


## checkbox

#### Descripción

El crea un checkbox con una etiqueta descriptiva. La etiqueta ayuda a los usuarios a entender qué opción están seleccionando.

Se genera una serie de checkboxes con etiquetas asociadas. Cada input de tipo checkbox está enlazado a un label a través del atributo for, que debe coincidir con el id del input.

La clase checkbox agrupa los elementos y aplica estilos CSS específicos para los checkboxes, personalizando su apariencia y comportamiento cuando son seleccionados o al pasar el mouse sobre ellos.

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

HTML
<div class="checkbox primary">
<input type="checkbox" name="checkbox" id="checkbox1">
<label for="checkbox1">checkbox 1</label>
</div>


- div: en el div de ir la clase
- id & for deben tener el mismo atributo
  tiene menú contextual

## Componente: Tabla

#### Descripción

El componente Tabla es una estructura de datos organizada en filas y columnas que permite mostrar información de manera clara y legible. Este componente incluye un encabezado con títulos de columna y un cuerpo donde se listan los datos correspondientes. Además, cuenta con funcionalidades que mejoran la experiencia de usuario, como la opción de destacar una fila activa y efectos visuales al pasar el cursor sobre cualquier fila.

| clase      | descripcion                                                                              | uso                  |
| ---------- | ---------------------------------------------------------------------------------------- | -------------------- |
| table      | Abarcara toda la tabla                                                                   | class="table"      |
| active-row | se destacan con un estilo especial, indicando que son importantes o están seleccionadas. | class="active-row" |

HTML

HTML
 <div class="container">
      <table class="table">
        <thead>
          <tr>
            <th>ID</th>
            <th>Nombre</th>
            <th>Edad</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>1</td>
            <td>John</td>
            <td>25</td>
          </tr>
          <tr class="active-row">
            <td>2</td>
            <td>Jane</td>
            <td>30</td>
          </tr>
          <tr>
            <td>3</td>
            <td>Doe</td>
            <td>35</td>
          </tr>
        </tbody>
      </table>
    </div>


- *`table`*: Permitiendo organizar los datos en un formato tabular.
- Encabezado: La sección thead está estilizada con un fondo de color para diferenciarse visualmente del cuerpo de la tabla.
- *Celdas*: Las celdas (th y td) tienen un espaciado adecuado para garantizar una buena legibilidad.

CSS

CSS
.table {
  width: 100%;
  border-collapse: collapse;
  font-size: 1em;
  text-align: left;
  background-color: #fff;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
}

.table thead tr {
  background-color: #009879;
  color: #ffffff;
  text-align: left;
  font-weight: bold;
}

.table th,
.table td {
  padding: 12px 15px;
}

.table tbody tr {
  border-bottom: 1px solid #dddddd;
}

.table tbody tr:nth-of-type(even) {
  background-color: #f3f3f3;
}

.table tbody tr:last-of-type {
  border-bottom: 2px solid #009879;
}

.table tbody tr.active-row {
  font-weight: bold;
  color: #009879;
}

.table tbody tr:hover {
  background-color: #f1f1f1;
  cursor: pointer;
}


- *Efectos visuales*: Se usan colores alternados en las filas y un cambio de fondo cuando el usuario interactúa con ellas, además de destacar una fila activa con la clase active-row.

Este componente es útil para mostrar listados de información y puede ser personalizado fácilmente cambiando los estilos de acuerdo con las necesidades del proyecto.
