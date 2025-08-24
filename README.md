# Laboratorio 3 – IC8057: Introducción al Desarrollo de Páginas Web

**Nombre:** Josué Torres Narvaez  
**Carné:** 2018084162  
**Curso:** IC-8057 – Introducción al Desarrollo de Páginas Web  
**Fecha:** 24/08/2025  

---

## Título del proyecto

### TechFuture 2025 – Evento Tecnológico

Este proyecto consiste en el desarrollo de una página web estática, refinando la del Laboratorio 2, para aplicar conceptos avanzados de **CSS3** como *selectores, pseudo-clases, el modelo de caja, posicionamiento, Flexbox y Grid*, siguiendo las buenas prácticas vistas en clase.

---

## Estructura del proyecto y CSS

El proyecto se organizó en una nueva rama llamada `lab3-selectores-boxmodel` y se crearon los siguientes archivos CSS, enlazados en el orden correcto:

- **styles/base.css:** Contiene la propiedad `box-sizing: border-box`, variables CSS y estilos tipográficos globales.  
- **styles/layout.css:** Contiene la maquetación de la página, incluyendo el uso de `display: flex` para la navegación y `display: grid` para el listado de expositores.  
- **styles/components.css:** Estilos para componentes reutilizables como `.btn`, `.card` y el control de `overflow`.  
- **styles/overrides.css:** Utilizado para demostrar la especificidad con la regla `!important`.  

---

## Selectores y Pseudo-clases aplicadas

Se implementaron los siguientes selectores y pseudo-clases, como se indica en la rúbrica:

- **Selectores de tipo:** `header`, `nav`, `section`, `img` y otros.  
- **Selectores de clase:** `.card` para los expositores y `.btn` para el botón de envío.  
- **Selectores de ID:** `#agenda`, `#expositores`, `#registro`, `#ubicacion` y `#patrocinadores`.  
- **Selectores de atributo:** `a[target="_blank"]`, `img[alt]`, `input[type="email"]`.  

**Combinadores:**

- **Descendiente:** `.card p` → estilizar los párrafos dentro de las tarjetas.  
- **Hijo directo:** `header > nav` → estilizar la navegación.  
- **Adyacente:** `nav a + a` → agregar un separador entre enlaces de navegación.  
- **Hermanos:** `ol li ~ li` → estilizar los elementos de la lista de patrocinadores a partir del segundo.  

**Pseudo-clases:**

- **De estado:** `:hover`, `:active`, `:focus-visible` → botón de envío.  
- **Estructurales:** `:nth-child(odd)` para colorear filas alternas en la tabla, `:last-child` para el último elemento y `:not()` para excluir el primer elemento de la lista de ubicación.  

---

## Demostración de Especificidad

- Se utilizó una regla con `!important` en `overrides.css` para sobrescribir el color de fondo del badge **"Experto TOP"** en las tarjetas de expositores.  
- Se agregó un estilo en línea en el HTML del título de **Expositores** (`<h2 style="...">`), que convive con su clase, demostrando su alta especificidad.  

---

## Otros conceptos aplicados

- **Box Model:** Se definió `box-sizing: border-box` globalmente, con márgenes y paddings adecuados. Se observó el colapso de márgenes entre el título `h2` y las tarjetas `.card`.  
- **Overflow:** Se implementó `overflow: auto` en un párrafo de la tarjeta del expositor.  
- **Flexbox y Grid:** `display: flex` para la barra de navegación y `display: grid` con `repeat()` y `minmax()` para los expositores.  
- **Positioning:** `position: relative` en el contenedor `.card` y `position: absolute` en el badge para ubicarlo en la esquina superior derecha.  

---

## Despliegue en Netlify

El proyecto fue versionado en una rama dedicada de GitHub y se creó un nuevo deploy en Netlify para esta rama.

- **Repositorio en GitHub:** [JosueTorresN/Lab2](https://github.com/JosueTorresN/Lab2.git) (rama `lab3-selectores-boxmodel`)  
- **Sitio en Netlify:** [Deploy en Netlify](https://tu-nuevo-deploy.netlify.app) *(reemplazar con el enlace correcto)*  

---

## Conclusiones

- Se lograron aplicar correctamente las técnicas avanzadas de **CSS3**, demostrando un control preciso sobre la presentación visual del sitio.  
- La organización en múltiples archivos CSS facilita la escalabilidad y el mantenimiento del proyecto.  
- El uso de **selectores complejos y pseudo-clases** permite un estilo más dinámico y eficiente, reduciendo la necesidad de clases extra en el HTML.  
