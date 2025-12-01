# Capítulo V: Implementación del Producto, Validación y Despliegue
## 5.1. Gestión de Configuración de Software

La gestión de configuración de software es crucial para nuestro trabajo, ya que nos permite mantener un control preciso sobre los elementos del proyecto, como el código fuente, los documentos de diseño y los activos digitales. Esto asegura que todos los miembros del equipo trabajen con la misma versión de los archivos y facilita la colaboración entre desarrolladores, diseñadores y otros profesionales involucrados en el proyecto.

### 5.1.1. Configuración del Entorno de Desarrollo de Software

A continuación se presentan las herramientas y estándares adoptados por el equipo para el desarrollo colaborativo del sistema:

| Actividad | Herramienta / Guía | Propósito | Tipo de acceso / Enlace |
| :---- | :---- | :---- | :---- |
| Gestión de Requisitos | Convenciones Gherkin | Redacción legible de requisitos en formato Given/When/Then. | [https://cucumber.io/docs/gherkin/](https://cucumber.io/docs/gherkin/) |
| Diseño UX/UI del Producto | Figma | Prototipado y diseño responsivo. | [https://figma.com/](https://figma.com/) |
| Desarrollo Frontend | HTML, CSS, JavaScript, Vue | Construcción de la interfaz web. | [https://vuejs.org/guide/introduction.html](https://vuejs.org/guide/introduction.html) |
| Desarrollo Backend | C# + ASP.NET Core | Implementación de servicios y lógica del backend. | [https://learn.microsoft.com/en-us/aspnet/core](https://learn.microsoft.com/en-us/aspnet/core) |
| IDE | Rider + WebStorm | Desarrollo, pruebas y depuración. | [https://www.jetbrains.com/rider](https://www.jetbrains.com/rider) [https://www.jetbrains.com/webstorm](https://www.jetbrains.com/webstorm) |
| Estándares de Código | Google HTML/CSS Style Guide, Vue Style Guide, MDN Guidelines, W3C JavaScript Style Guide, Google JavaScript Style Guide, C# Coding Conventions, Microsoft ASP.NET Core Guidelines | Aplicación de buenas prácticas de desarrollo en frontend y backend. | [https://developer.mozilla.org/](https://developer.mozilla.org/) [https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style) |
| Control de Versiones | Git + GitHub | Control de versiones y trabajo colaborativo. | [https://github.com/](https://github.com/) |
| Despliegue de Software | GitHub Pages | Despliegue continuo de la aplicación para entornos de prueba y validación. | [https://render.com/](https://render.com/) |

### 5.1.2. Gestión del Código Fuente

* **Flujo de trabajo GitFlow**

  Se implementará el modelo de ramas propuesto por Vincent Driessen en su artículo “A successful Git branching model”, conocido como GitFlow. Este modelo organiza el trabajo en las siguientes ramas:

  * **main:** Rama principal, contiene siempre código en producción.
  * **develop:** Rama principal de desarrollo, donde se integran las funcionalidades antes de pasar a producción.
  * **feature/*:** Ramas creadas desde `develop` para desarrollar nuevas funcionalidades.
    * Convención de nombres: `feature/<nombre-descriptivo-corto>`
      * **Ejemplo:** `feature/login-auth`
  * **release/*:** Ramas creadas desde `develop` cuando se prepara una nueva versión para producción.
    * Convención de nombres: `release/<versión>`
      * **Ejemplo:** `release/1.2.0`

* **Convenciones de Commits**
  Se utilizará el estándar Conventional Commits para los mensajes de commit. Esto facilitará la automatización en procesos de integración continua y la generación de changelogs.
  * **feat:** agregar funcionalidad de inicio de sesión
  * **fix:** corregir excepción de referencia nula en el servicio de usuario
  * **chore:** actualizar dependencias

### 5.1.3. Estilo y Convenciones del Código Fuente

* **Frontend (Landing Page - HTML, CSS, JavaScript)**
  * **Convenciones generales:**
    * **Idioma:** Todo el código, incluyendo nombres de variables, funciones y clases, debe escribirse en inglés.
    * **Indentación:** 2 espacios.
    * **Formato de archivos:** `.html`, `.css`, `.js`
    * **Estilos de código adoptados:**
      * [W3Schools HTML Style Guide](https://www.w3schools.com/html/html5_syntax.asp)
      * [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html)

  * **Convenciones de nombres:**
    * **Clases CSS:** kebab-case (ej., `main-container`)
    * **IDs HTML:** camelCase (ej., `mainContent`)
    * **Variables JS:** camelCase (ej., `userName`)
    * **Funciones JS:** camelCase (ej., `handleClick()`)

* **Aplicación Web Frontend (Vue.js + JavaScript)**
  * **Convenciones generales:**
    * **Idioma:** El código debe estar en inglés.
    * **Estructura de carpetas:** Segregación por módulos y componentes.
    * **Indentación:** 2 espacios.
    * **Formato de archivos:** `.vue`, `.js`, `.css`
    * **Estilos de código adoptados:**
      * [Vue.js Style Guide (Official)](https://vuejs.org/guide/reusability/style-guide.html)
      * [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)

  * **Convenciones de nombres:**
    * **Componentes Vue:** PascalCase (ej., `UserProfile.vue`)
    * **Variables y funciones JS:** camelCase (ej., `userName`, `handleSubmit()`)
    * **Nombres de archivos:** kebab-case (ej., `user-profile.vue`)
    * **Props:** camelCase en JS, kebab-case en plantillas HTML (ej., `userProfile` → `user-profile`)
    * **Eventos personalizados:** kebab-case (ej., `user-logged-in`)
    * **Clases CSS:** kebab-case

### 5.1.4. Configuración de Despliegue de Software

Esta sección detalla los pasos necesarios para desplegar con éxito los productos digitales que componen la solución: la landing page, la aplicación web (frontend) y los servicios web (backend), partiendo de sus respectivos repositorios.

* **Frontend (Landing Page - HTML, CSS, JavaScript)**
  * **Tecnología base:**
    * **Lenguajes:** HTML5, CSS3, JavaScript
    * **Hosting:** GitHub Pages

  * **Configuración y despliegue:**

    *Repositorio de código:* La Landing Page se desarrolla con HTML, CSS y JavaScript puros. Todos los archivos del proyecto deben subirse a un repositorio público en GitHub. Es obligatorio que el archivo `index.html` esté ubicado en la raíz del repositorio (`/`) para que GitHub Pages lo detecte correctamente como punto de entrada del sitio. Pasos de despliegue en GitHub Pages:

    * Acceder al repositorio en GitHub.
    * Ir a la sección Settings del repositorio.
    * En el menú lateral, seleccionar Pages.
    * En el campo Source elegir:
      * **Branch:** `main`
      * **Folder:** `/` (root)
    * Guardar los cambios.

      *Publicación:* GitHub generará automáticamente una URL pública donde la Landing Page estará disponible, con el formato: `https://<username>.github.io/<repository>/`

      *Actualizaciones:* Cualquier nuevo commit en la rama `main` se desplegará automáticamente en GitHub Pages.

* **Aplicación Web Frontend (Vue.js + JavaScript)**
  * **Tecnología base:**
    * **Framework:** Vue 3
    * **Herramienta de build:** Vite / Vue CLI (`npm run build`)
    * **Hosting:** GitHub Pages

  * **Configuración y despliegue:**

    *Repositorio de código:* El proyecto frontend está alojado en GitHub. El directorio de salida del build (`/dist`) contiene los archivos estáticos que deben publicarse.

    *Build:* Ejecutar `npm run build` para generar los archivos estáticos listos para producción.

    *Despliegue en GitHub Pages:* Para publicar el contenido del directorio `/dist` en GitHub Pages se puede usar la herramienta `gh-pages` (npm) o realizar un despliegue manual mediante una rama `gh-pages`. También se puede configurar un workflow de GitHub Actions para automatizar el proceso. Las URLs de los servicios REST del backend deben configurarse como variables de entorno (p. ej., `VITE_API_URL`) y no deben estar hardcodeadas.

    Pasos (resumen):
    * Acceder al repositorio en GitHub.
    * Ir a Settings → Pages.
    * En Source elegir `main` / `/` y guardar.

    *Publicación:* GitHub generará automáticamente la URL pública para el sitio.

    *Actualizaciones:* Los commits en `main` se desplegarán automáticamente si el pipeline está configurado.

## 5.2. Implementación de la Landing Page, Servicios y Aplicaciones

### 5.2.1. Sprint 1

El primer sprint es un hito importante en nuestro proceso ágil. Durante este periodo nos centramos en implementar las funcionalidades prioritarias identificadas en la planificación inicial. Esto implica traducir los requisitos y especificaciones en código funcional, desarrollando iterativamente las bases de nuestro producto.

#### 5.2.1.1. Planificación del Sprint 1

La planificación del sprint es una reunión en la que el equipo define las actividades para el siguiente sprint: qué trabajo se hará, cuánto tiempo tomará y quién será responsable. El objetivo es establecer un plan claro y alcanzable que fomente la colaboración y asegure que todos estén alineados con los objetivos y prioridades.

| Sprint \# | Sprint 1 |
| :---- | :---- |
| **Antecedentes de la Planificación** |  |
| **Fecha** | 15-09-2025 |
| **Hora** | 2:00 PM |
| **Lugar** | Discord (Reunión virtual) |
| **Preparado por** | Ever Giusephi Carlos Lavado, Abraam Bernabe Acosta Elera |
| **Asistentes (a la reunión de planificación)** | Ever Giusephi Carlos Lavado / Abraam Bernabe Acosta Elera / Mike Dylan Guillen Giraldo / Guillermo Arturo Howard Robles / Gerardo Valentín Palacín Lazo / David Ignacio Vivar Cesar |
| **Resumen de la Revisión Sprint 1** | El proyecto inicia con un enfoque en establecer las bases de la aplicación de trazabilidad de licores. El equipo se comprometió a entregar una base sólida que incluye una landing page funcional y la documentación inicial del proyecto. Se definieron la estructura del repositorio y las primeras definiciones de la arquitectura del sistema. |
| **Resumen de la Retrospectiva Sprint 1** | Al ser el primer sprint del proyecto, no existe una retrospectiva previa. El equipo estableció las primeras normas de trabajo colaborativo, decidió usar metodologías ágiles con reuniones diarias cortas y definió los canales principales de comunicación mediante Discord y WhatsApp para coordinación rápida. |
| **Objetivo del Sprint 1** | Nuestro enfoque es establecer una presencia web profesional y crear las bases técnicas del proyecto de trazabilidad de licores. Esperamos que esto entregue confianza inicial y validación del concepto a nuestros segmentos objetivo (transportistas, distribuidores y gerentes de tiendas). Esto se confirmará cuando tengamos una landing page funcional desplegada que presente claramente la propuesta de valor y los visitantes comprendan el beneficio en menos de 30 segundos. |
| **Velocidad del Sprint 1** | Para este sprint se estableció una velocidad de 25 Story Points, considerando que es el primer sprint y el equipo está en proceso de adaptación a la metodología de trabajo. |
| **Suma de Story Points** | La suma total de Story Points para las User Stories incluidas en este Sprint 1 es de 23 Story Points. |

#### 5.2.1.2. Líderes de Aspecto y Colaboradores

| Miembro del equipo (Apellido, Nombre) | Usuario GitHub | Aspecto 1: Líder (L) / Colaborador (C) - Desarrollo de User Stories | Aspecto 2: Líder (L) / Colaborador (C) - Desarrollo de Entrevistas | Aspecto 3: Líder (L) / Colaborador (C) - Mockups | Aspecto 4: Líder (L) / Colaborador (C) - Landing Page | Aspecto 5: Líder (L) / Colaborador (C) - Desarrollo Capítulos 1 y 2 |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Carlos Lavado, Ever Giusephi | FischlTx | L | C | C | C | C |
| Acosta Elera, Abraam Bernabe | abraam16 | C | L | C | C | C |
| Guillen Giraldo, Mike Dylan | FulLHous | C | C | L | C | C |
| Howard Robles, Guillermo Arturo | Guillermo Howard |  | C | C | C | L |
| Palacín Lazo, Gerardo Valentín | GeraldP03 | C | C | C | C | L |
| Vivar Cesar, David Ignacio | DarkBeider20 | C | C | C | C | C |

#### 5.2.1.3. Backlog del Sprint 1

| User Story |  | Work-Item / Tarea |  |  |  | Asignado |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Id | Título | Id | Título | Descripción | Estimación (Horas) | Asignado a |
| **US-33** | Notificación de pedido en tránsito | W001 | Diseño del mockup de la landing page | Crear wireframes y diseño visual de la landing page | 8 | Guillermo Howard |
|  |  | W002 | Estructura HTML de la landing page | Implementar estructura HTML semántica | 6 | Ever Carlos |
|  |  | W003 | Estilos CSS responsivos | Implementar CSS responsivo para todos los dispositivos | 8 | Mike Guillen |
|  |  | W004 | Integración del formulario de contacto | Implementar formulario de contacto funcional | 4 | David Vivar |
| **US-45** | Suscripción a un plan de servicio | W005 | Sección de planes de suscripción | Crear sección visual de planes en la landing page | 6 | Guillermo Howard |
|  |  | W006 | Validación de formularios | Implementar validación en JavaScript para formularios | 4 | Gerardo Palacín |
| **US-51** | Oferta de pruebas gratuitas | W007 | Call-to-Action para prueba gratuita | Diseñar e implementar botones de CTA para prueba gratuita | 3 | Ever Carlos |
|  |  | W008 | Configuración del repositorio en GitHub | Configurar estructura de carpetas y ajustes iniciales | 4 | Abraam Acosta |
| **Config** | Configuración inicial del proyecto | W009 | Documentación README | Crear documentación inicial del proyecto en `README.md` | 6 | Mike Guillen |
|  |  | W010 | Configuración del entorno de desarrollo | Configurar herramientas y dependencias de desarrollo | 5 | Abraam Acosta |
|  |  | W011 | Pruebas y validación | Realizar pruebas de las funcionalidades implementadas | 8 | Gerardo Palacín |
|  |  | W012 | Desplegar la landing page | Configurar y desplegar la landing page | 4 | David Vivar |

#### 5.2.1.4. Evidencia de Desarrollo para la Revisión del Sprint

Durante este sprint, el equipo avanzó significativamente en la implementación del proyecto. Se completaron la estructura y el diseño de la landing page, integrando secciones principales como navegación, testimonios, funcionalidades, formulario de contacto, redes sociales y servicios. Además, se documentaron los commits y las ramas utilizadas, garantizando trazabilidad y colaboración efectiva entre los miembros del equipo. A continuación se muestra la evidencia de los entregables y contribuciones principales.

#### 5.2.1.5. Evidencia de Ejecución para la Revisión del Sprint

![EEFSR1](../src/assets/chapter5/sprints/sprint1/execution-evidence-for-sprint-review1.png)

![EEFSR2](../src/assets/chapter5/sprints/sprint1/execution-evidence-for-sprint-review2.png)

![EEFSR3](../src/assets/chapter5/sprints/sprint1/execution-evidence-for-sprint-review3.png)

![EEFSR4](../src/assets/chapter5/sprints/sprint1/execution-evidence-for-sprint-review4.png)

#### 5.2.1.6. Evidencia de Documentación de Servicios para la Revisión del Sprint

Para esta entrega no se utilizaron APIs, por lo que no fue necesaria documentación de servicios implementados durante el sprint.

#### 5.2.1.7. Evidencia de Despliegue de Software para la Revisión del Sprint

Durante este sprint, el equipo desplegó con éxito la landing page utilizando la plataforma GitHub Pages. El propósito fue asegurar que la solución estuviera disponible en línea para revisión y validación, cumpliendo con estándares de entrega continua y visibilidad del progreso del proyecto.

![SDEFSR1](../src/assets/chapter5/sprints/sprint1/software-deployment-evidence-for-sprint-review1.png)

![SDEFSR2](../src/assets/chapter5/sprints/sprint1/software-deployment-evidence-for-sprint-review2.png)

#### 5.2.1.8. Perspectivas sobre la Colaboración del Equipo durante el Sprint

Durante este sprint, las actividades de implementación se llevaron a cabo de forma colaborativa y organizada. El equipo utilizó herramientas como GitHub para la gestión de versiones y asignación de tareas, y Discord para la comunicación y coordinación diaria. Cada miembro asumió responsabilidades específicas según el backlog y los aspectos definidos en la planificación, participando activamente en desarrollo, revisión de código y validación de entregables.

Se promovió la revisión cruzada de avances, el registro detallado de commits y la documentación de cambios. Las reuniones periódicas permitieron resolver dudas, ajustar prioridades y asegurar que todos los miembros estuvieran alineados con los objetivos del sprint. Esta dinámica facilitó la integración continua y la entrega oportuna de los resultados esperados.

![TCIDS](../src/assets/chapter5/sprints/sprint1/team-collaboration-insights-during-sprint.png)

## 5.2.2 Sprint 2

### 5.2.2.1. Planificación del Sprint 2

| Sprint \# | Sprint 2 |
| ----- | ----- |
| Antecedentes de la Planificación |  |
| Fecha | 2025-11-11 |
| Hora | 07:00 pm (GMT-5) |
| Lugar | Modalidad remota mediante la plataforma Discord |
| Preparado por | Howard Robles, Guillermo Arturo |
| Asistentes (a la reunión de planificación) |  |
| Resumen de la Revisión Sprint 1 | Durante el Sprint 1 se logró implementar casi en su totalidad la Landing Page del sistema GlassGo, desarrollando secciones clave como el header, footer, sección de beneficios y preguntas frecuentes, así como la integración inicial de estilos globales y tipografía. Quedó faltante la funcionalidad de cambio de idioma, la cual será prioridad para el siguiente sprint. El equipo cumplió con los entregables establecidos, respetando el diseño de mockups y la guía de estilos. Se identificaron oportunidades de mejora en la velocidad de desarrollo y gestión de tiempos. |
| Resumen de la Retrospectiva Sprint 1 | Durante el Sprint 1, el equipo logró avanzar de forma coordinada y efectiva en el desarrollo de la landing page, sin enfrentar mayores dificultades. Cada integrante cumplió puntualmente con las secciones asignadas, lo que permitió avanzar según lo planificado. La adopción de convenciones comunes en el código y el diseño contribuyó a mantener la coherencia del producto y facilitó la integración entre partes. Como mejora para el siguiente sprint, se acordó implementar revisiones diarias (daily reviews) que permitan alinear mejor los avances, detectar bloqueos tempranos y mejorar la comunicación continua entre miembros. |
| Objetivos del Sprint & User Stories |  |
| Objetivo del Sprint 2 | Nuestro enfoque está en brindar información clara y detallada a los visitantes de la plataforma, así como habilitar la gestión de inventario, configuración de perfil, notificaciones, resumen de datos y gestión de ventas para los usuarios del sistema interno. Creemos que esto proporciona mayor comprensión del propósito de la solución a los visitantes y mejora la eficiencia operativa de los administradores de restaurantes y proveedores. Esto se confirmará cuando los visitantes puedan explorar contenido relevante desde el acceso público, y los usuarios autenticados naveguen por el panel principal y accedan a los módulos de gestión de inventario, configuración de perfil, notificaciones, resumen de datos y ventas del sistema. |
| Velocidad del Sprint 2 | 30 |
| Suma de Story Points | 28 |

### 5.2.2.2. Líderes de Aspecto y Colaboradores

Durante el Sprint 2 se definió el desarrollo e integración de los módulos principales del frontend de la aplicación web interna GlassGo, abarcando funcionalidades clave como la gestión de productos, pedidos, inventario y compras. Estas implementaciones buscan optimizar los procesos internos y mejorar la trazabilidad del inventario, brindando mayor eficiencia a los administradores de restaurantes y su personal.

Con el fin de mantener una coordinación efectiva y una comunicación fluida entre los integrantes del equipo, se estructuró la matriz de liderazgo y colaboración (LACX), donde se asignó un líder (L) encargado de cada funcionalidad y colaboradores (C) que brindan apoyo en su implementación.

| Miembro del equipo (Apellido, Nombre) | Usuario GitHub | Perfil & Referencias | Pagos & Suscripciones | Fidelidad & Engagement | Planificación de Servicios | Administración del Sistema | Ejecución, Monitoreo y Servicio | Panel & Analíticas |
| ----- | ----- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Carlos Lavado Ever Giusephi | sephi-dev05 | C | L | L | C | C | C | C |
| Palacín Lazo Gerardo Valentín | GeraldP03 | C | C | C | C | C | L | C |
| Howard Robles Guillermo Arturo | GuillermoPromac | C | C | C | C | C | C | L |
| Acosta Elera Abraham Bernabe | abraam16 | L | C | C | C | C | C | C |
| Vivar Cesar David Ignacio | DarkBeider20 | C | C | C | C | L | C | C |
| Guillen Giraldo Mike Dylan | FulLHous | C | C | C | L | C | C | C |

### 5.2.2.3. Backlog del Sprint 2

El objetivo principal de este sprint es desarrollar la interfaz frontend de los dashboards para administradores de restaurantes y proveedores, enfocándose en una estructura clara, navegación eficiente y visualización adecuada de datos críticos.

![][image3]

Trello: [https://trello.com/invite/b/68ffe2b4ec71fc75648c1f28/ATTIdf711a197aade6d0da1e65a2032e1c37292FD061/sprint-backlog-2](https://trello.com/invite/b/68ffe2b4ec71fc75648c1f28/ATTIdf711a197aade6d0da1e65a2032e1c37292FD061/sprint-backlog-2)

### 5.2.2.4. Evidencia de Desarrollo para la Revisión del Sprint

En esta sección se presentan los avances realizados durante el Sprint 2, centrados en el desarrollo de los módulos principales de la aplicación web interna de GlassGo.

El objetivo fue implementar funcionalidades clave para la gestión de productos, pedidos, inventario y compras, con el fin de mejorar la eficiencia operativa y la trazabilidad de los recursos dentro de los restaurantes.

Durante este sprint se avanzó en la autenticación de usuarios, el diseño del panel principal y la implementación inicial de varios módulos funcionales.

1. Aplicación Web (Frontend): La siguiente tabla resume los commits realizados en el repositorio UI-Topic-Frontend, que incluyen la implementación de la gestión de productos, inventario y resumen.

|  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

### 5.2.2.5. Evidencia de Ejecución para la Revisión del Sprint

A continuación se presenta el video del frontend de la aplicación web interna. Este demuestra la interacción de los usuarios autenticados con los módulos principales del sistema, incluyendo la navegación por el sidebar, la gestión de productos, el seguimiento de alertas y el control de inventario.

### 5.2.2.6. Evidencia de Documentación de Servicios para la Revisión del Sprint

Durante este sprint se avanzó en el desarrollo del frontend interno de GlassGo, habilitando múltiples rutas navegables para los usuarios autenticados (administradores de restaurante y proveedores), en una estructura basada en Vue Router, Domain-Driven Design y componentes cargados dinámicamente. Aunque aún no se han documentado endpoints REST con OpenAPI, se listan a continuación los recursos navegables disponibles que forman parte del ecosistema de consumo de servicios web del sistema.

Descripción del logro:

- Finalización del Landing Page e implementación multilenguaje.
- Desarrollo modular del frontend con rutas específicas por rol (restaurante y proveedor).
- Estructura basada en Vue Router, DDD y carga lazy de componentes.
- Integración visual con PrimeVue y buenas prácticas de separación por contextos.

|  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- |

### 5.2.2.7. Evidencia de Despliegue de Software para la Revisión del Sprint

### 5.2.2.8. Perspectivas sobre la Colaboración del Equipo durante el Sprint

Durante el sprint se aplicaron estrategias de colaboración que permitieron un desarrollo fluido y organizado del proyecto. Entre las prácticas aplicadas destacan:

- Creación de ramas específicas por funcionalidad o sección, siguiendo la convención `feature/[nombre-de-seccion]`, lo que facilitó trabajo paralelo sin conflictos y mantuvo el repositorio estructurado.
- Responsabilidad distribuida: cada integrante fue responsable del desarrollo de una o más secciones del frontend.
- Commits frecuentes y atómicos para un seguimiento detallado del progreso.
- Integración de funcionalidades mediante Pull Requests hacia la rama `develop`, permitiendo control de calidad mediante revisiones cruzadas.
- Comunicación constante vía Discord para coordinación diaria, resolución de dudas y toma de decisiones técnicas.
- Buenas prácticas de control de versiones con mensajes claros en los commits y revisiones colaborativas mediante PRs.
- Enfoque en la calidad del código: estructuras consistentes, estándares de codificación y coherencia en estilos y convenciones.

### 5.2.3.1. Planificación del Sprint 3

| Sprint \# | Sprint 3 |
| ----- | ----- |
| Antecedentes de la Planificación |  |
| Fecha | 2025-11-12 |
| Hora | 08:00 pm (GMT-5) |
| Lugar | Modalidad remota mediante la plataforma Discord |
| Preparado por | Howard Robles Guillermo Arturo |
| Asistentes (a la reunión de planificación) |  |
| Resumen de la Revisión Sprint 2 | Durante el Sprint 2 se logró una mejora significativa en la experiencia de inicio para nuevos usuarios, al rediseñar e integrar la landing page con el frontend principal de la aplicación web GlassGo. Se avanzó considerablemente en el desarrollo del módulo frontend, incorporando funcionalidades clave como la gestión de inventario, notificaciones, analíticas y suscripciones para los perfiles de administradores y proveedores. El equipo demostró una sólida coordinación y colaboración en la implementación de estos componentes, respetando los lineamientos definidos en la planificación. Como oportunidad de mejora, se identificó la necesidad de fortalecer aún más la alineación del equipo con los objetivos priorizados del sprint, para asegurar una entrega aún más consistente en próximos ciclos. |
| Resumen de la Retrospectiva Sprint 2 | Durante el Sprint 2, el equipo mantuvo una comunicación fluida y una coordinación efectiva, lo cual permitió avanzar de forma sólida en varios módulos clave del frontend. La integración continua, las revisiones cruzadas de código y la claridad en las responsabilidades asignadas fueron aspectos destacados que facilitaron un buen ritmo de trabajo. Como oportunidad de mejora, se identificó la necesidad de reforzar el seguimiento y cumplimiento de los objetivos prioritarios, así como de mejorar la estimación de tiempos en algunos flujos más complejos. También se resaltó la importancia de alinear aún más los esfuerzos individuales con los objetivos de entrega colectivos. |
| Objetivos del Sprint & User Stories |  |
| Objetivo del Sprint 3 | Nuestro enfoque es presentar de forma efectiva la propuesta de valor a nuevos visitantes, habilitar la gestión de recetas y pedidos, mejorar la sección de ventas para administradores de restaurantes, incorporar la gestión de órdenes para proveedores y permitir a ambos segmentos realizar el pago de su suscripción. Además, proporcionar mediante la API de la plataforma puntos de acceso para que los desarrolladores frontend implementen funcionalidades relacionadas con pedidos, ventas, recetas, inventario, perfil y comentarios. Esto aumentará la confianza de los visitantes y mejorará los flujos de usuario y la operatividad de administradores y proveedores. |
| Velocidad del Sprint 3 | 38 |
| Suma de Story Points | 35 |

### 5.2.3.2. Líderes de Aspecto y Colaboradores

Durante el Sprint 3 se definió el desarrollo e integración de los módulos principales del frontend y del backend, abarcando funcionalidades clave como la gestión de productos, pedidos, inventario y compras. Estas implementaciones buscan optimizar los procesos internos y mejorar la trazabilidad del inventario.

| Miembro del equipo (Apellido, Nombre) | Usuario GitHub | Perfil & Referencias | Pagos & Suscripciones | Fidelidad & Engagement | Planificación de Servicios | Administración del Sistema |
| ----- | ----- | :---- | :---- | :---- | :---- | :---- |
| Carlos Lavado Ever Giusephi | sephi-dev05 | C | L | L | C | C |
| Palacín Lazo Gerardo Valentín | GeraldP03 | C | C | C | C | C |
| Howard Robles Guillermo Arturo | GuillermoPromac | C | C | C | C | C |
| Acosta Elera Abraham Bernabe | abraam16 | L | C | C | C | C |
| Vivar Cesar David Ignacio | DarkBeider20 | C | C | C | C | L |
| Guillen Giraldo Mike Dylan | FulLHous | C | C | C | L | C |

### 5.2.3.3. Backlog del Sprint 3

El objetivo principal de este sprint es consolidar una experiencia funcional completa para los distintos perfiles de usuario dentro de la plataforma GlassGo. Se prioriza la mejora de la landing page para comunicar eficazmente la propuesta de valor a nuevos visitantes, así como la habilitación de módulos clave como la gestión de ventas, recetas y pedidos para administradores, y la gestión de órdenes para proveedores.

Asimismo, se trabajará en la integración del flujo de pagos por suscripción y en la provisión de APIs REST documentadas, permitiendo al frontend consumir endpoints de forma eficiente para construir las vistas requeridas. Este enfoque busca mejorar la usabilidad, la operatividad y la cohesión entre frontend y backend, facilitando la validación funcional de la plataforma y avanzando hacia su adopción por parte de los usuarios finales.

![][image4]

Trello: [https://trello.com/invite/b/68ffe30942dcb480aedf84d2/ATTI14ff021bc259e9ac94812c42ae4680e22318D9BD/sprint-backlog-3](https://trello.com/invite/b/68ffe30942dcb480aedf84d2/ATTI14ff021bc259e9ac94812c42ae4680e22318D9BD/sprint-backlog-3)

### 5.2.3.4. Evidencia de Desarrollo para la Revisión del Sprint

Servicios Web (Backend):

En el backend de la plataforma se realizaron avances enfocados en la gestión de recetas, suministros y lotes. Se implementaron operaciones CRUD para recetas y el manejo detallado de sus insumos, además de validar y reforzar la integridad de datos mediante objetos de valor. Se añadieron configuraciones para entornos de desarrollo y producción y se mejoraron definiciones de columnas en la base de datos para optimizar el manejo de fechas, precios y cantidades. Se desarrollaron servicios y controladores que facilitan la interacción con los recursos, permitiendo una gestión eficiente y segura de los datos relacionados con el inventario y las operaciones del sistema.

### 5.2.3.5. Evidencia de Ejecución para la Revisión del Sprint

A continuación se muestra un video con los avances realizados durante el Sprint 3, en el cual se trabajó en la landing page y en el desarrollo del frontend y backend.

### 5.2.3.6. Evidencia de Documentación de Servicios para la Revisión del Sprint

Durante este sprint se completó al 100% el desarrollo del Landing Page, consolidando su estructura visual, diseño responsivo, traducción multilenguaje y funcionalidades de navegación. Asimismo, se avanzó en la construcción del frontend del sistema, incluyendo componentes clave como el menú lateral, el dashboard inicial, el módulo de gestión de insumos y la arquitectura modular en Angular bajo DDD (Domain-Driven Design).

Aunque aún no se desplegaron todos los endpoints REST, se documentan recursos y avances relevantes del sprint, junto con evidencia de despliegue y repositorio de código.

Descripción del logro:

- Finalización del Landing Page (100%).
- Implementación de diseño responsivo, i18n y redirecciones funcionales.
- Estructura de frontend modular iniciada (sidebar, dashboard y componentes base).
- Aplicación de buenas prácticas de organización por bounded contexts.
- Integración visual basada en Vue con PrimeVue y Primeflex.

### 5.2.3.7. Evidencia de Despliegue de Software para la Revisión del Sprint

Durante este sprint se realizaron actividades de despliegue y pruebas de los servicios desarrollados, asegurando que las funcionalidades estén operativas y accesibles para los usuarios finales.

### 5.2.3.8. Perspectivas sobre la Colaboración del Equipo durante el Sprint

Se mantuvo el uso de ramas específicas para cada sección o funcionalidad (`feature/[nombre-de-seccion]`), permitiendo un trabajo paralelo organizado.

Cada miembro asumió la responsabilidad de desarrollar uno o más bounded contexts del backend. Se realizaron commits frecuentes, registrando avances de manera continua y detallada. Las funcionalidades desarrolladas se integraron mediante Pull Requests hacia la rama `develop`. Se mantuvo comunicación constante vía Discord para coordinar avances y resolver dudas en tiempo real. Se aplicaron buenas prácticas de programación, control de versiones y colaboración en equipo.
