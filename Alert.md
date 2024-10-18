# Documentación del Componente Alert

---

## Descripción general:

### Este componente es un contenedor simple, que muestra un mensaje de alerta en la interfaz de usuario(UI). Permite notificar a todos los usuarios sobre información importante que requiera atención.

---

### Tipo de componente:

- **Estructural (HTML)**
- **Estilo (CSS)**

### Atributos:

- **Class: "container" // Clase que aplica atributos generales al contenedor del mensaje de alerta.**

### Métodos:

- **(No se aplican métodos en este componente, ya que es un documento estático sin interactividad. Si se agregan funcionalidades en JavaScript, se documentarán aquí.)**

## Dependencias

#### CSS:

- **/public/alert.css: Estilos específicos para el componente de alerta.**
- **/public/global.css: Estilos globales para la aplicación.**

---

## Guía de uso:

| class     | descrip                               | uso               |
| --------- | ------------------------------------- | ----------------- |
| container | Contenedor para el mensaje de alerta. | Class="container" |

#

HTML

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Alert</title>
    <link rel="stylesheet" href="/public/alert.css" />
    <link rel="stylesheet" href="/public/global.css" />
  </head>
  <body>
    <main>
      <div class="container">Alert</div>
    </main>
  </body>
</html>
```

CSS

```css
:root {
  --primary-color: #0bb79e;
  --primary-color-lighten: #a3d339;

  --secondary-color: #ff6427;
  --secondary-color-lighten: #ff9912;
  --tertiary-color: #05a6dd;
  --tertiary-color-lighten: #5fd6f2;

  --success-color: #5cb85c;
  --warning-color: #fcd432;
  --error-color: #dc3545;

  --text-transform-btn: uppercase;
  --weight-btn: 600;
  --letter-spacing-btn: 1.5px;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html,
body {
  height: 100%;
  width: 100%;
  font: 100% sans-serif;
}
main {
  height: 100%;
}
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
  background-color: #f1f1f1;
}
```
