# PRUEBA---RA2
-----
## Ejercicio 1

### 1A. Solución:
No se centra ya que el contenedor site header, esta usando flexbox, con justify content. entonces el h1 y el menu se coloca cada uno en un lado.

### 1B. Solución: 

Para hacerlo con Flexbox, coloque el nav con position: absolute a la derecha y deje que el h1 se mantenga centrado.

CSS:
```
.site-header {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}

.main-nav {
  position: absolute;
  right: 0;
}

h1 {
  margin: 0;
}
```

Para hacerlo con Grid, Dividi la cabecera en 3 columnas. El h1 ocupa la del centro y el menú la ultima.

CSS:
```
.site-header {
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: center;
}

h1 {
  justify-self: center;
}

```

### 1C. Solución:

Lo que he hecho ha sido convertir el header en un grid de dos filas. En la primera fila solo el h1 centrado y en la segunda solo el nav centrado.

CSS:
```
.site-header {
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: auto auto;
  row-gap: 30px;
  justify-items: center;
}

h1 {
  grid-row: 1;
}

.main-nav {
  grid-row: 2;
}

```

### 1D. Solución:

Las reglas del CSS que he aplicado a .site-header. Ha sido un color de fondo, un espacio interior para que sea vea visualmente mas claro, un borde al boton y una sombra a la caja, para que sea visualmente más bonito.

CSS:
```
.site-header {
  background-color: #f2f2f2;
  padding: 20px 40px;
  border-bottom: 2px solid #ddd;
  box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}
```
## Ejercicio 2

### 2A. Solución:

Ahora incluimos un boton dentro de header.

HTML:
```
<header class="site-header">
  <button class="menu-btn">☰</button>

  <h1>Mi Sitio Web</h1>

  <nav class="main-nav">
      ...
  </nav>
</header>

```

### 2B. Solución:

Usamos flexbox para maquetar el diseño.

CSS:
```
.site-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.menu-btn {
  font-size: 24px;
  background: none;
  border: none;
  cursor: pointer;
}

h1 {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
}

.main-nav {
  margin-left: auto;
}
```
## Ejercicio 3

### 3A. Solución:

Yo voy a utilizar mi galeria de imagenes de el mini proyecto, y voy a hacer los cambios en la pagina web inventada.

HTML: 

```
<div class="galeria-grid">
  <figure>
    <img src="Imagenes/vista frontal.jpg" alt="Mustang frontal">
    <figcaption>Vista frontal del Ford Mustang</figcaption>
  </figure>
  <figure>
    <img src="Imagenes/llanta.jpeg" alt="Detalle de llanta de Mustang">
    <figcaption>Detalle de llanta deportiva</figcaption>
  </figure>
  <figure>
    <img src="Imagenes/circuito.jpg" alt="Mustang en circuito">
    <figcaption>Mustang en acción en circuito</figcaption>
  </figure>
  <figure>
    <img src="Imagenes/interior.jpg" alt="Interior deportivo de Mustang">
    <figcaption>Interior deportivo y tecnológico</figcaption>
  </figure>
  <figure>
    <img src="Imagenes/carretera.avif" alt="Mustang en carretera">
    <figcaption>Mustang en carretera abierta</figcaption>
  </figure>
  <figure>
    <img src="Imagenes/atardecer.jpeg" alt="Mustang al atardecer">
    <figcaption>Mustang al atardecer</figcaption>
  </figure>
</div>
```

### 3B. Solución:

Lo que vamos a  hacer, es crear el efecto de zoom suave, sombra y transicion animada.

CSS: 

```
.galeria-grid img {
  width: 200px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  border-radius: 6px;
}

.galeria-grid img:hover {
  transform: scale(1.1);
  box-shadow: 0 6px 12px rgba(0,0,0,0.3);
}
```

### 3C. Solución:

Vamos a poner el target, que lo que hace es abrir un enlace en una pestaña nueva.

HTML: 
```
<div class="galeria-grid">

  <a href="Imagenes/vista frontal.jpg" target="_blank">
    <img src="Imagenes/vista frontal-mini.jpg" alt="Mustang frontal">
  </a>

  <a href="Imagenes/llanta.jpeg" target="_blank">
    <img src="Imagenes/llanta-mini.jpeg" alt="Detalle de llanta">
  </a>

  <a href="Imagenes/circuito.jpg" target="_blank">
    <img src="Imagenes/circuito-mini.jpg" alt="Mustang en circuito">
  </a>

  <a href="Imagenes/interior.jpg" target="_blank">
    <img src="Imagenes/interior-mini.jpg" alt="Interior deportivo">
  </a>

  <a href="Imagenes/carretera.avif" target="_blank">
    <img src="Imagenes/carretera-mini.avif" alt="Mustang en carretera">
  </a>

  <a href="Imagenes/atardecer.jpeg" target="_blank">
    <img src="Imagenes/atardecer-mini.jpeg" alt="Mustang al atardecer">
  </a>

</div>
```

**Hecho por: Jhonatan Cano León**
