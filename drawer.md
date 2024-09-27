# Componenete Navigator Drawer

---

## El navigator drawer es un menu lateral que permite navegar por la app y se despliega en modo movil o pequeño, en modo escritorio permanece abierto.

---

## Descripción general:

**El navigator drawer es un menu lateral que permite navegar por la app y se despliega en modo movil o pequeño, en modo escritorio permanece abierto.**

## Guia de uso

`#drawer`: Panel lateral oculto que se desliza desde el lado izquierdo. Define el estilo, tamaño, y posición del Drawer.

`#drawer_toggle`:Checkbox oculto que controla si el drawer está abierto o cerrado. Se usa para activar o desactivar el Drawer mediante un input.

`#drawer_open`: Label que muestra el ícono de menú (☰) para abrir el drawer. Usado como botón para abrir el Drawer, estilizado como menú.

`#drawer_close`: Label que muestra el ícono de cerrar (✖) dentro del drawer. Usado como botón para cerrar el Drawer.

`#drawer_overlay`: Capa oscura que aparece cuando el drawer está abierto. Cubre el contenido principal y cierra el Drawer al hacer clic.

HTML

```html
<header>
  <nav>
    <label for="drawer_toggle" id="drawer_open"> &#9776; </label>
    <input type="checkbox" name="drawer_close" id="drawer_toggle" />
    <div id="drawer">
      <label for="drawer_toggle" id="drawer_close"> &#10005; </label>
      <ul class="vertical_list">
        <li><a>Inicio de sesión</a></li>
        <li><a>Trámites veterinarios</a></li>
        <li><a>Trámites de áreas verdes</a></li>
        <li><a>Estado de trámites</a></li>
        <li><a>Historial de trámites finalizados</a></li>
        <li><a>Otras consultas</a></li>
        <li><a>Perfil</a></li>
        <li><a>Cerrar sesión</a></li>
      </ul>
    </div>
    <label for="drawer_toggle" id="drawer_overlay"> </label>
  </nav>
</header>
<aside id="sidebar">
  <ul class="vertical_list">
    <li><a>Inicio de sesión</a></li>
    <li><a>Trámites veterinarios</a></li>
    <li><a>Trámites de áreas verdes</a></li>
    <li><a>Estado de trámites</a></li>
    <li><a>Historial de trámites finalizados</a></li>
    <li><a>Otras consultas</a></li>
    <li><a>Perfil</a></li>
    <li><a>Cerrar sesión</a></li>
  </ul>
</aside>
```

CSS

```css
header {
  background-color: var(--primary-color);
  color: #f1f1f1;
  padding: 15px;
  height: 60px;
  position: sticky;
  top: 0;
  box-shadow: 10px 4px 4px rgba(0, 0, 0, 0.2);
}
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
nav > input[type="checkbox"] {
  display: none;
}
#drawer_open {
  font-size: 20px;
  cursor: pointer;
}
#drawer {
  position: fixed;
  top: 0;
  left: -320px;
  background: var(--primary-color);
  height: 100%;
  width: 300px;
  max-width: 300px;
  transition: left 0.5s ease;
  z-index: 3;
  box-shadow: 6px 4px 4px rgba(0, 0, 0, 0.1);
}
#drawer_overlay {
  position: absolute;
  background-color: rgba(0, 0, 0, 0.3);
  z-index: 2;
  display: block;
  inset: 0;
  width: 0;
}
#drawer_toggle:checked + #drawer {
  left: 0;
}
#drawer_toggle:checked ~ label#drawer_overlay {
  width: 100%;
}
#drawer_close {
  position: absolute;
  top: 15px;
  right: 15px;
  cursor: pointer;
  font-size: 20px;
}
#sidebar {
  width: 300px;
  height: 100%;
  background-color: var(--primary-color);
  color: #f1f1f1;
  position: fixed;
  top: 0;
  left: 0;
  display: block;
}
main {
  width: calc(100% - 300px);
  max-width: calc(100% - 300px);
  margin-left: 300px;
}
.vertical_list {
  display: block;
  padding: 15px;
  list-style-type: none;
  margin: 60px 0px 0px 0px;
  padding: 0;
  align-items: center;
}
.vertical_list > li > a {
  text-decoration: none;
  padding: 15px;
  display: block;
  transition: background-color 0.5s ease;
  cursor: pointer;
}
.vertical_list > li > a:hover {
  background-color: rgba(0, 0, 0, 0.1);
}
@media only screen and (max-width: 1000px) {
  #sidebar {
    display: none;
  }
  main {
    width: 100%;
    max-width: 100%;
    margin: 0px;
  }
}
```
