# Hubket

Aplicación web para gestionar tickets de soporte TIC. Está hecha con HTML, CSS y JavaScript, sin dependencias ni servidor; se ejecuta directamente en el navegador.

## Funcionalidades

- Crear tickets con título, descripción, tipo, prioridad y responsable.
- Tipos disponibles: Incidente, Requerimiento, Problema y Cambio.
- Estados: Abierto, En progreso, Resuelto y Cerrado.
- Prioridades: Baja, Media, Alta y Crítica.
- Responsables: Juan, Matías y Dalmiro.
- Cambiar la prioridad, el responsable y el estado desde la tabla.
- Filtrar los tickets por estado, tipo, prioridad y responsable.
- Ver los tickets en la tabla, en este orden: N° de Ticket, Tipo, Título, Prioridad, Responsable, Estado, Creado y Aging.
- Consultar el tiempo transcurrido en Aging. Para tickets de prioridad Crítica, el dato se muestra en amarillo desde los 15 minutos, naranja desde los 30 minutos y rojo desde los 60 minutos.
- Consultar el resumen de tickets por estado y el tiempo promedio de resolución.

## Seguimiento del tiempo

- Mientras el ticket está abierto o en progreso, Aging muestra cuánto tiempo pasó desde su creación y se actualiza cada minuto.
- Al marcarlo como Resuelto o Cerrado, se registra la fecha y Aging muestra cuánto tardó desde su creación.
- Si se reabre, el seguimiento vuelve a correr desde la creación.

## Cómo usarla

Abrí `index.html` en un navegador. No hace falta instalar nada.

Los tickets se guardan en el `localStorage` del navegador. Permanecen disponibles al recargar la página en ese navegador y equipo; no se sincronizan automáticamente entre dispositivos.

Los tickets guardados antes de incorporar el tipo se muestran como tipo Incidente.

## Archivos

| Archivo | Contenido |
|---|---|
| `index.html` | Estructura de Hubket, formulario y tabla de tickets |
| `styles.css` | Diseño de la página y estilos de prioridad, estado y Aging |
| `app.js` | Creación, persistencia, filtros, cambios de estado y cálculos de tiempo |
