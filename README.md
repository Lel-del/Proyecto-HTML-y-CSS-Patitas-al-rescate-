Esta es la primera fase de la presencia digital para la fundación Patitas al Rescate. Se ha diseñado y maquetado la página de inicio (index.html) utilizando una estética inspirada en interfaces de videojuegos RPG clásicos de 8/16 bits, cumpliendo con la restricción técnica de no utilizar JavaScript.

**Características Implementadas**:
Estética RPG Retro: Uso de tipografías monoespaciadas, bordes definidos, sombras sólidas, paleta de colores oscuros con verdes brillantes (#4ade80, #22c55e) y renderizado de imágenes pixeladas para simular un menú de juego.

-Carrusel de Fotos CSS Puro: Sistema de transición automática alojado en el banner principal (header) que rota entre 3 imágenes de rescates reales (@keyframes moverFotos) cada 3.3 segundos, con un ciclo total de 10 segundos de manera infinita sin alterar el flujo de la página.

-Estructura Semántica y Limpia: Separación estricta de componentes mediante HTML5 nativo (<nav>, <header>, <main>, <section>, <article>, <footer>).

-Sección de Misión y Visión: Bloques de información interactivos mediante CSS con sutiles efectos de escalado (transform: scale(1.05)) y sombreado de texto al pasar el cursor.

-Sección Destacada: Espacio dedicado al "Perrito del Mes" con un contenedor estructurado para dar prioridad visual a casos específicos de adopción.

```
PROYECTO/
│
├── index.html          # Código de la estructura de la página de inicio (Home)
│
├── css/
│   └── style.css       # Estilos nativos (Tipografías, animaciones, layout retro)
│
└── media/
    └── img/            # Recursos visuales (iconos, fondos y fotos de mascotas)

```

Al tratarse de una maqueta estática construida puramente con HTML5 y CSS3 nativo, no requiere ningún tipo de compilación, servidores locales complejos ni dependencias de Node.js.

-Descargar o clonar este repositorio en tu equipo local.

-Asegurarte de que las imágenes correspondientes (nutellin.jpg, domi.jpg, maopidi.jpg, Toby.jpeg, icono.jpg, fondo.gif) se encuentren dentro de la ruta media/img/.

-Hacer doble clic sobre el archivo index.html para abrirlo directamente en cualquier navegador web moderno (Edge, Chrome, Firefox, Safari).

-(Opcional recomendado para desarrollo): Si utilizas Visual Studio Code, puedes ejecutar la extensión Live Server para previsualizar los cambios en tiempo real.

**Formulario de Contacto (contacto.html)**
Se ha implementado la interfaz de mensajería y soporte técnico para el gremio de rescate, estructurando un sistema de entrada de datos adaptativo enfocado en la usabilidad del usuario.

**Características Implementadas**
Diseño de Formulario en Rejilla: Uso de CSS Grid adaptativo que organiza los campos en una sola columna para dispositivos móviles y se despliega automáticamente en dos columnas (grid-template-columns: 1fr 1fr) en pantallas de escritorio.

Validación de Estados en CSS: * Interactividad: Cambio de color de bordes al enfocar los campos (:focus).

Validación Nativa: Detección en tiempo real de campos obligatorios correctos o incorrectos mediante las pseudoclases :required:valid y :required:invalid sin depender de scripts externos.

Maquetación de Estados Simulados: Creación de clases estáticas específicas (.error y .success) para visualizar cómo responderá la interfaz ante alertas del sistema o envíos exitosos de información.

Corrección Estructural: Limpieza y cierre simétrico de las etiquetas semánticas del bloque de información directa y del pie de página (<footer>).

Aquí tienes la sección correspondiente para el Catálogo de Adopciones, lista para anexar a tu archivo README.md.

**Catálogo de Compañeros (adopciones.html)**
Se ha estructurado el sistema de visualización de personajes (mascotas rescatadas) simulando un menú de selección de equipo o inventario RPG, distribuyendo dinámicamente las tarjetas según la resolución de la pantalla.

**Características Implementadas**
Rejilla Responsiva Completa: Configuración avanzada de CSS Grid estructurada a través de media queries progresivas para garantizar simetría visual en cualquier dispositivo:

Móviles: 1 columna (1fr) para priorizar la lectura en vertical.

Tablets (min-width: 600px): Rejilla de 2 columnas.

Pantallas medianas (min-width: 900px): Rejilla de 3 columnas.

Escritorio ancho (min-width: 1200px): Rejilla máxima de 4 columnas de tamaño idéntico.

Componente Tarjeta RPG: Cada bloque de personaje cuenta con una estructura semántica (<article>) que encapsula:

Un Contenedor de Imágenes Simétrico (.tarjeta-img-box) con altura fija y centrado dinámico mediante Flexbox, usando object-fit: cover para evitar la deformación de las fotos.

Una etiqueta de estado flotante (.badge-estado) posicionada de manera absoluta (position: absolute) en la esquina superior izquierda.

Un bloque de estadísticas del compañero con resaltado de palabras clave mediante etiquetas <strong>.

Estados de Disponibilidad: * Activo: Tarjetas interactivas con animaciones de desplazamiento vertical suave al posicionar el cursor (transform: translateY(-4px)) y botones vinculados a la bitácora de detalles (perfil.html).

Reubicado / Adoptado: Bloques visualmente atenuados mediante filtros nativos de desaturación y brillo en CSS (filter: grayscale(80%) brightness(50%)), modificando el cursor y bloqueando la interacción mediante propiedades de desactivación para simular un estado no seleccionable.

