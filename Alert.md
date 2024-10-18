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
<div
        class="container_alert container_alert_open"
        id="container_alert1"
        onclick="closeDialog('container_alert1')"
      >
        <div class="content_alert" onclick="stopPropagation(event)">
          <!-- COMPONENTE CARD -->
          <div class="card" style="height: 400px; max-height: 400px">
            <div class="card_title">Título</div>
            <div class="card_text">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Quaerat,
              nostrum quia. Rem adipisci excepturi eaque dolorum magni sint
              natus veritatis alias blanditiis molestiae eius, laborum, beatae,
              rerum sequi iusto magnam.Lorem ipsum dolor sit amet consectetur
              adipisicing elit. Quaerat, nostrum quia. Rem adipisci excepturi
              eaque dolorum magni sint natus veritatis alias blanditiis
              molestiae eius, laborum, beatae, rerum sequi iusto magnam.
            </div>
            <div class="card_section">
              <button
                class="btn btn_small btn_secondary_lighten"
                onclick="closeDialog('container_alert1')"
              >
                <span> Cerrar </span>
              </button>
            </div>
          </div>
          <!-- ... -->
        </div>
      </div>
      <div class="content-btn">
        <button onclick="openDialog('container_alert1')" class="btn">
          <span>open</span>
        </button>
      </div>
    </main>
    <script>
      function openDialog(status) {
        var el = document.querySelector(`#${status}`);
        console.log(el);
        el.classList.remove("container_alert_close");
        el.classList.add("container_alert_open");
      }
      function closeDialog(status) {
        var el = document.querySelector(`#${status}`);
        console.log(el);
        el.classList.remove("container_alert_open");
        el.classList.add("container_alert_close");
      }
      function stopPropagation(event) {
        event.stopPropagation();
      }
    </script>
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
