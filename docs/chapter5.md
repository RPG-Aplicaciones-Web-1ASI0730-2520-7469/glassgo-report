# Chapter V: Product Implementation, Validation & Deployment
## 5.1. Software Configuration Management

Software configuration management is crucial for our work, as it allows us to maintain precise control over the elements of our project, such as source code, design documents, and digital assets. This ensures that all team members are working with the same version of the files and facilitates collaboration among developers, designers, and other professionals involved in the project.

### 5.1.1. Software Development Environment Configuration

The following are the tools and standards adopted by the team for collaborative system development:

| Activity | Tool / Guide | Purpose | Access Type / Link |
| :---- | :---- | :---- | :---- |
| Requirements Management | Gherkin Conventions | Readable requirement writing in Given/When/Then format. | [https://cucumber.io/docs/gherkin/](https://cucumber.io/docs/gherkin/) |
| Product UX/UI Design | Figma | Prototyping and responsive design. | [https://figma.com/](https://figma.com/) |
| Frontend Dev | HTML, CSS, JavaScript, Vue | Building the web interface. | [https://vuejs.org/guide/introduction.html](https://vuejs.org/guide/introduction.html) |
| Backend Dev | C# + ASP.NET Core | Implementation of services and backend logic. | [https://learn.microsoft.com/en-us/aspnet/core](https://learn.microsoft.com/en-us/aspnet/core) |
| IDE | Rider + WebStorm | Development, testing, and debugging. | [https://www.jetbrains.com/rider](https://www.jetbrains.com/rider) [https://www.jetbrains.com/webstorm](https://www.jetbrains.com/webstorm) |
| Code Standards | Google HTML/CSS Style Guide, Vue Style Guide, MDN Guidelines, W3C JavaScript Style Guide, Google JavaScript Style Guide, C# Coding Conventions, Microsoft ASP.NET Core Guidelines | Application of best development practices in frontend and backend. | [https://developer.mozilla.org/](https://developer.mozilla.org/) [https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style) |
| Version Control | Git + GitHub | Version control and collaborative work. | [https://github.com/](https://github.com/) |
| Software Deployment | GitHub Pages | Continuous deployment of the application for testing and validation environments. | [https://render.com/](https://render.com/) |

### 5.1.2. Source Code Management

* **GitFlow Workflow**

  The branching model proposed by Vincent Driessen in his article “A successful Git branching model,” known as GitFlow, will be implemented. This model organizes work into the following branches:

  * **main:** Main branch, always contains production code.  
  * **develop:** Main development branch, where features are integrated before going to production.  
  * **feature/\*:** Branches created from develop to develop new features.  
    * Naming convention: feature/<short-descriptive-name>  
      * **Example:** feature/login-auth  
  * **release/\*:** Branches created from develop when preparing a new version for production.  
    * Naming convention: release/<version>  
      * **Example:** release/1.2.0  

* **Commit Conventions**  
  The Conventional Commits standard will be used for commit messages. This will facilitate automation in continuous integration processes and changelog generation.  
  * **feat:** add login functionality  
  * **fix:** correct null pointer exception on user service  
  * **chore:** update dependencies

### 5.1.3. Source Code Style & Conventions

* **Frontend (Landing Page - HTML, CSS, JavaScript)**  
  * **General Conventions:**  
    * **Language:** All code, including variable names, functions, and classes, is written in English.  
    * **Indentation:** 2 spaces.  
    * **File Format:** .html, .css, .js  
    * **Adopted Code Style:**  
      * [W3Schools HTML Style Guide](https://www.w3schools.com/html/html5_syntax.asp)  
      * [Google HTML/CSS Style Guide](https://google.github.io/styleguide/htmlcssguide.html)

  * **Naming Conventions:**  
    * **CSS Classes:** kebab-case (e.g., main-container)  
    * **HTML IDs:** camelCase (e.g., mainContent)  
    * **JS Variables:** camelCase (e.g., userName)  
    * **JS Functions:** camelCase (e.g., handleClick())

* **Frontend Web App (Vue.js + JavaScript)**  
  * **General Conventions:**  
    * **Language:** Code is entirely in English.  
    * **Folder Structure:** Segregation by modules and components.  
    * **Indentation:** 2 spaces.  
    * **File Format:** .vue, .js, .css  
    * **Adopted Code Style:**  
      * [Vue.js Style Guide (Official):](https://vuejs.org/guide/reusability/style-guide.html)  
      * [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)

  * **Naming Conventions:**  
    * **Vue Components:** PascalCase (e.g., UserProfile.vue)  
    * **JS Variables and Functions:** camelCase (e.g., userName, handleSubmit())  
    * **Files:** kebab-case (e.g., user-profile.vue)  
    * **Props:** camelCase in JavaScript, kebab-case in HTML templates (e.g., prop: userProfile, usage: user-profile)  
    * **Custom Events:** kebab-case (e.g., user-logged-in)  
    * **CSS Classes:** kebab-case

### 5.1.4. Software Deployment Configuration

This section details the necessary steps to successfully deploy the digital products that make up the solution: the landing page, the web application (frontend), and the Web Services (backend), starting from their respective source code repositories.  
* **Frontend (Landing Page - HTML, CSS, JavaScript)**  
  * **Base Technology:**  
    * **Languages:** HTML5, CSS3, JavaScript  
    * **Hosting:** GitHub Pages

  * **Configuration and Deployment:**

    *Source Code Repository:* The Landing Page is developed using pure HTML, CSS, and JavaScript. All project files must be uploaded to a public repository on GitHub. It is mandatory for the index.html file to be located at the root of the repository (/) for GitHub Pages to correctly detect it as the entry point of the site. Deployment steps on GitHub Pages:

    * Access the repository on GitHub.  
    * Go to the repository's Settings section.  
    * In the sidebar menu, select Pages.  
    * In the Source field, choose:  
      * **Branch:** main  
      * **Folder:** / (root)  
    * Save the changes.

      *Publication:* GitHub will automatically generate a public URL where the Landing Page will be available, in the format: https://\<username\>.github.io/\<repository\>/

      Updates: Any new commit to the main branch will be automatically deployed by GitHub Pages, without the need for additional actions.

* **Frontend Web App (Vue.js + JavaScript)**  
  * **Base Technology:**  
    * **Framework:** Vue 3  
    * **Build Tool:** Vite / Vue CLI (npm run build)  
    * **Hosting:** GitHub Pages

  * **Configuration and Deployment:**

    *Source Code Repository:* The frontend project is hosted on GitHub. The output directory of the build (/dist) contains the files that need to be published.

    *Build:* The command is executed; npm run build. This generates the static files ready for production.

    *Deployment on GitHub Pages:* To publish the content of the /dist directory on GitHub Pages, you can use the gh-pages tool (npm) or perform a manual deployment via a gh-pages branch. A GitHub Actions workflow can also be set up to automate the process. Environment Variables: The URLs of the backend REST services are configured as environment variables (e.g., VITE_API_URL) and are not hardcoded. Differentiated environments:

    * Access the repository on GitHub.  
    * Go to the repository's Settings section.  
    * In the sidebar menu, select Pages.  
    * In the Source field, choose:  
      * **Branch:** main  
      * **Folder:** / (root)  
    * Save the changes.

      *Publication:* GitHub will automatically generate a public URL where the Landing Page will be available, in the format: *https://\<username\>.[github.io/](http://github.io/)\<repository\>/*

      *Updates:* Any new commit to the main branch will be automatically deployed by GitHub Pages, without the need for additional actions.

## 5.2. Landing Page, Services & Applications Implementation

### 5.2.1. Sprint 1

The first sprint is an important milestone in our agile development process. During this period, we focused on implementing the priority features and functionalities identified in the initial planning. This involves translating the requirements and specifications into functional code, iteratively developing the foundations of our product.

#### 5.2.1.1. Sprint Planning 1

Sprint planning is a meeting in agile methodology where the team plans the activities for the next sprint. It defines what work will be done, how long it will take, and who will be responsible. The goal is to establish a clear and achievable plan for the team, fostering collaboration and ensuring that everyone is aligned on objectives and priorities.

| Sprint \# | Sprint 1 |
| :---- | :---- |
| **Sprint Planning Background** |  |
| **Date** | 15-09-2025 |
| **Time** | 2:00 PM |
| **Location** | Discord (Virtual Meeting) |
| **Prepared By** | Ever Giusephi Carlos Lavado, Abraam Bernabe Acosta Elera |
| **Attendees (to planning meeting)** | Ever Giusephi Carlos Lavado / Abraam Bernabe Acosta Elera / Mike Dylan Guillen Giraldo / Guillermo Arturo Howard Robles / Gerardo Valentín Palacín Lazo / David Ignacio Vivar Cesar |
| **Sprint 1 - 1 Review Summary** | The project begins with a focus on establishing the foundations of the liquor traceability application. The team is committed to delivering a solid base that includes a functional landing page and the initial project documentation. The repository structure and the first definitions of the system architecture were established. |
| **Sprint 1 - 1 Retrospective Summary** | As this is the first sprint of the project, there is no previous retrospective. The team established the first collaborative work norms, decided to use agile methodologies with short daily meetings, and defined the main communication channels through Discord and WhatsApp for quick coordination. |
| **Sprint 1 Goal** | Our focus is on establishing a professional web presence and creating the technical foundations of the liquor traceability project. We believe this delivers initial confidence and validation of the concept to our target segments (transport operators, distributors, and store managers). This will be confirmed when we have a functional landing page deployed that clearly presents the value proposition and visitors can understand the benefit of the solution in less than 30 seconds. |
| **Sprint 1 Velocity** | For this sprint, a velocity of 25 Story Points was established, considering that it is the first sprint and the team is in the process of adapting to the working methodology. |
| **Sum of Story Points** | The total sum of Story Points for the User Stories included in this Sprint 1 is 23 Story Points. |

#### 5.2.1.2. Aspect Leaders and Collaborators

| Team Member (Last Name, First Name) | GitHub Username | Aspect Name 1: User Stories Development Leader (L) / Collaborator (C) | Aspect Name 2: Interview Development Leader (L) / Collaborator (C) | Aspect Name 3: Mockups Development Leader (L) / Collaborator (C) | Aspect Name 4: Landing Page Development Leader (L) / Collaborator (C) | Aspect Name 5: Development of Chapters 1 and 2 Leader (L) / Collaborator (C) |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Carlos Lavado, Ever Giusephi | FischlTx | L | C | C | C | C |
| Acosta Elera, Abraam Bernabe | abraam16 | C | L | C | C | C |
| Guillen Giraldo, Mike Dylan | FulLHous | C | C | L | C | C |
| Howard Robles, Guillermo Arturo | Guillermo Howard |  | C | C | C | L |
| Palacín Lazo, Gerardo Valentín | GeraldP03 | C | C | C | C | L |
| Vivar Cesar, David Ignacio | DarkBeider20 | C | C | C | C | C |

#### 5.2.1.3. Sprint Backlog 1

| User Story |  | Work-Item / Task |  |  |  | Status |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Id | Title | Id | Title | Description | Estimation (Hours) | Assigned To |
| **US-33** | Order Notification in Transit | W001 | Landing Page Mockup Design | Create wireframes and visual design of the landing page | 8 | Guillermo Howard |
|  |  | W002 | Landing Page HTML Structure | Implement semantic HTML structure | 6 | Ever Carlos |
|  |  | W003 | Responsive CSS Styles | Implement responsive CSS for all devices | 8 | Mike Guillen |
|  |  | W004 | Contact Form Integration | Implement functional contact form | 4 | David Vivar |
| **US-45** | Subscription to a Service Plan | W005 | Subscription Plans Section | Create visual section of plans on landing page | 6 | Guillermo Howard |
|  |  | W006 | Form Validation | Implement JavaScript validation for forms | 4 | Gerardo Palacín |
| **US-51** | Offering Free Trials | W007 | Call-to-Action for Free Trial | Design and implement CTA buttons for free trial | 3 | Ever Carlos |
|  |  | W008 | GitHub Repository Setup | Configure folder structure and initial settings | 4 | Abraam Acosta |
| **Config** | Initial Project Setup | W009 | README Documentation | Create initial project documentation in [README.md](http://readme.md/) | 6 | Mike Guillen |
|  |  | W010 | Development Environment Setup | Configure development tools and dependencies | 5 | Abraam Acosta |
|  |  | W011 | Testing and Validation | Conduct testing of implemented functionalities | 8 | Gerardo Palacín |
|  |  | W012 | Deploy Landing Page | Configure and deploy the landing page | 4 | David Vivar |

#### 5.2.1.4. Development Evidence for Sprint Review

During this Sprint, the team made significant progress in the implementation of the project. The structure and design of the landing page were completed, integrating the main sections such as navigation, testimonials, functionalities, contact form, social media, and services. Additionally, the commits and branches used were documented, ensuring traceability and effective collaboration among team members. Below is the evidence of the main deliverables and contributions made during the Sprint.

#### 5.2.1.5. Execution Evidence for Sprint Review

![EEFSR1](../src/assets/chapter5/sprints/sprint1/execution-evidence-for-sprint-review1.png)

![EEFSR2](../src/assets/chapter5/sprints/sprint1/execution-evidence-for-sprint-review2.png)

![EEFSR3](../src/assets/chapter5/sprints/sprint1/execution-evidence-for-sprint-review3.png)

![EEFSR4](../src/assets/chapter5/sprints/sprint1/execution-evidence-for-sprint-review4.png)

#### 5.2.1.6. Services Documentation Evidence for Sprint Review

For this delivery, no APIs were used, so documentation on services implemented during the Sprint was not required.

#### 5.2.1.7. Software Deployment Evidence for Sprint Review

During this Sprint, the team successfully deployed the landing page using the GitHub Pages platform. The goal was to ensure that the solution was available online for review and validation, complying with continuous delivery standards and visibility of project progress.

![SDEFSR1](../src/assets/chapter5/sprints/sprint1/software-deployment-evidence-for-sprint-review1.png)

![SDEFSR2](../src/assets/chapter5/sprints/sprint1/software-deployment-evidence-for-sprint-review2.png)

#### 5.2.1.8. Team Collaboration Insights during Sprint

During this Sprint, the implementation activities were carried out collaboratively and in an organized manner. The team used tools like GitHub for version management and task assignment, and Discord for daily communication and coordination. Each member took on specific responsibilities according to the backlog and aspects defined in the planning, actively participating in development, code review, and validation of deliverables.

Cross-review of progress, detailed commit logging, and documentation of changes made were promoted. Periodic meetings allowed for resolving doubts, adjusting priorities, and ensuring that all members were aligned with the Sprint objectives. This dynamic facilitated continuous integration and timely delivery of expected results.

![TCIDS](../src/assets/chapter5/sprints/sprint1/team-collaboration-insights-during-sprint.png)

5.2.2 Sprint 2

5.2.2.1. Sprint Planning 2

| Sprint \# | Sprint 2 |
| ----- | ----- |
| Sprint Planning Background |  |
| Date | 2025-11-11 |
| Time | 07:00 pm (GMT-5) |
| Location | Modalidad remota mediante la plataforma Discord |
| Prepared By | Howard Robles, Guillermo Arturo |
| Attendees (to planning meeting) |  |
| Sprint 1 Review Summary | Durante el Sprint 1 se logró implementar casi en su totalidad la Landing Page del sistema GlassGo, desarrollando secciones clave como el header, footer, sección de beneficios y preguntas frecuentes, así como la integración inicial de estilos globales y tipografía. Quedó faltante la funcionalidad de cambio de idioma, la cual será prioridad para el siguiente sprint. El equipo cumplió con los entregables establecidos, respetando el diseño de mockups y la guía de estilos. Se identificaron oportunidades de mejora en la velocidad de desarrollo y gestión de tiempos. |
| Sprint 1 Retrospective Summary | Durante el Sprint 1, el equipo logró avanzar de forma coordinada y efectiva en el desarrollo de la landing page, sin enfrentar mayores dificultades. Cada integrante cumplió puntualmente con las secciones asignadas, lo que permitió avanzar según lo planificado. La adopción de convenciones comunes en el código y el diseño contribuyó a mantener la coherencia del producto y facilitó la integración entre partes. Como mejora para el siguiente sprint, se acordó implementar revisiones diarias (daily reviews) que permitan alinear mejor los avances, detectar bloqueos tempranos y mejorar la comunicación continua entre miembros. |
| Sprint Goal & User Stories |  |
| Sprint 2 Goal | Nuestro enfoque está en brindar información clara y detallada a los visitantes de la plataforma, así como habilitar la gestión de inventario, configuración de perfil, notificaciones, resumen de datos y gestión deventas para los usuarios del sistema interno. Creemos que esto proporciona mayor comprensión del propósito de la solución a los visitantes y mejora la eficiencia operativa de insumos de los administradores de restaurantes y proveedores. Esto se confirmará cuando los visitantes puedan explorar contenido relevante desde el acceso público, y los usuarios autenticados naveguen por el panel principal y accedan a los módulos de gestión de inventario, configuración de perfil, notificaciones, resumen de datos y ventas del sistema. |
| Sprint 2 Velocity | 30 |
| Sum of Story Points | 28 |

5.2.2.2 Aspect Leaders and Collaborators

Aspect Leaders and Collaborators

Durante el Sprint 2, se ha definido el desarrollo e integración de los módulos principales del frontend de la aplicación web interna GlassGo , abarcando funcionalidades clave como la gestión de productos, pedidos, inventario y compras. Estas implementaciones buscan optimizar los procesos internos y mejorar la trazabilidad del inventario, brindando mayor eficiencia a los administradores de restaurantes y su personal.

Con el fin de mantener una coordinación efectiva y una comunicación fluida entre los integrantes del equipo, se estructuró la matriz de liderazgo y colaboración (LACX), donde se asignó un líder (L) encargado de cada funcionalidad y colaboradores (C) que brindan apoyo en su implementación.

| Team Member (Last Name, First Name) | GitHub Username | Profile & References  | Paymets & Subscriptions  | Loyalty & Engagerment  | Service Planning  | System Administration  | Service Execution & Monitoring | Dashboard & Analytics |
| ----- | ----- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Carlos Lavado Ever Giusephi | sephi-dev05 | C | L | L | C | C | C | C |
| Palacín Lazo Gerardo Valentín  | GeraldP03 | C | C | C | C | C | L | C |
| Howard Robles Guillermo Arturo | GuillermoPromac | C | C | C | C | C | C | L |
| Acosta Elera Abraham Bernabe | abraam16 | L | C | C | C | C | C | C |
| Vivar Cesar David Ignacio | DarkBeider20 | C | C | C | C | L | C | C |
| Guillen Giraldo Mike Dylan | FulLHous | C | C | C | L | C | C | C |

5.2.2.3 Sprint Backlog 2

El objetivo principal de este Sprint es desarrollar la interfaz frontend de los dashboards para administradores de restaurantes y proveedores, enfocándose en una estructura clara, navegación eficiente y visualización adecuada de datos críticos.

![][image3]

Trello: [https://trello.com/invite/b/68ffe2b4ec71fc75648c1f28/ATTIdf711a197aade6d0da1e65a2032e1c37292FD061/sprint-backlog-2](https://trello.com/invite/b/68ffe2b4ec71fc75648c1f28/ATTIdf711a197aade6d0da1e65a2032e1c37292FD061/sprint-backlog-2)

5.2.2.4 Development Evidence for Sprint Review

En esta sección se presentan los avances realizados durante el Sprint 2, centrado en el desarrollo de los módulos principales de la aplicación web interna de GlassGo.

El objetivo principal fue implementar funcionalidades claves para la gestión de productos, pedidos, inventario y compras, con el fin de mejorar la eficiencia operativa y la trazabilidad de los recursos dentro de los restaurantes.

Durante este sprint se avanzó en la autenticación de usuarios, el diseño del panel principal y la implementación inicial de tres módulos funcionales clave.

1\. Web Application (Frontend): La siguiente tabla resume los commits realizados en el repositorio UI-Topic-Frontend, que incluyen la implementación de la gestión de productos, inventario y resumen, con el fin de mejorar la eficiencia operativa y la trazabilidad de los recursos dentro de los administradores de restaurantes y proveedores.

|  |  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- | :---- |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |
|  |  |  |  |  |  |

5.2.2.5 Execution Evidence for Sprint Review

A continuación, se presenta el video del frontend de la aplicación web interna. Este demuestra la interacción de los usuarios autenticados con los módulos principales del sistema, incluyendo la navegación por el sidebar, la gestión de productos, el seguimiento de alertas y el control de inventario.

5.2.2.6 Services Documentation Evidence for Sprint Review

Durante este Sprint se avanzó en el desarrollo del frontend interno de GlassGo, habilitando múltiples rutas navegables para los usuarios autenticados (administradores de restaurante y proveedores), en una estructura basada en Vue Router, Domain-Driven Design y componentes cargados dinámicamente. Aunque aún no se han documentado endpoints REST con OpenAPI, se despliegan a continuación los recursos navegables disponibles, que forman parte del ecosistema de consumo de servicios web del sistema.

Descripción del Logro:

Finalización del Landing Page e implementación multilenguaje.  
Desarrollo modular del frontend con rutas específicas por rol (restaurante y proveedor).  
Estructura basada en Vue Router, DDD y carga lazy de componentes.  
Integración visual con PrimeVue y buenas prácticas de separación por contextos.  
Rutas accesibles del sistema (Frontend)

|  |  |  |  |  |
| :---- | :---- | :---- | :---- | :---- |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |
|  |  |  |  |  |

5.2.2.7 Software Deployment Evidence for Sprint Review

5.2.2.8 Team Collaboration Insights during Sprint.

Durante el sprint, se adoptaron estrategias de colaboración efectivas que permitieron un desarrollo fluido y bien organizado del proyecto. A continuación se detallan las prácticas aplicadas:

Se crearon ramas específicas por funcionalidad o sección, siguiendo la convención feature/\[nombre-de-seccion\]. Esto facilitó un trabajo paralelo sin conflictos y mantuvo el repositorio estructurado.  
Cada integrante fue responsable del desarrollo de una o más secciones del frontend, distribuyéndose el trabajo de forma equitativa.  
Se realizaron commits frecuentes y atómicos, lo que permitió un seguimiento detallado del progreso y facilitó la revisión del código.  
Todas las funcionalidades fueron integradas a través de pull requests hacia la rama develop, garantizando control de calidad mediante revisiones cruzadas.  
La comunicación entre los miembros del equipo fue constante, utilizando la plataforma Discord como canal principal para coordinación diaria, resolución de dudas y toma de decisiones técnicas.  
Se aplicaron buenas prácticas de control de versiones con Git, como descripciones claras en los commits, ramas temáticas, y revisión colaborativa mediante PRs.  
El equipo también se enfocó en la calidad del código, utilizando estructuras consistentes, siguiendo estándares de codificación, y asegurando coherencia en estilos y convenciones.

5.2.3.1. Sprint Planning 3

| Sprint \# | Sprint 3 |
| ----- | ----- |
| Sprint Planning Background |  |
| Date | 2025-11-12 |
| Time | 08:00 pm (GMT-5) |
| Location | Modalidad remota mediante la plataforma Discord |
| Prepared By | Howard Robles Guillermo Arturo |
| Attendees (to planning meeting) |  |
| Sprint 2 Review Summary | Durante el Sprint 2 se logró una mejora significativa en la experiencia de inicio para nuevos usuarios, al rediseñar e integrar la landing page con el frontend principal de la aplicación web GlassGo. Se avanzó considerablemente en el desarrollo del módulo frontend, incorporando funcionalidades clave como la gestión de inventario, notificaciones, analíticas y suscripciones para los perfiles de administradores y proveedores. El equipo demostró una sólida coordinación y colaboración en la implementación de estos componentes, respetando los lineamientos definidos en la planificación. Como oportunidad de mejora, se identificó la necesidad de fortalecer aún más la alineación del equipo con los objetivos priorizados del sprint, para asegurar una entrega aún más consistente en próximos ciclos. |
| Sprint 2 Retrospective Summary | Durante el Sprint 2, el equipo mantuvo una comunicación fluida y una coordinación efectiva, lo cual permitió avanzar de forma sólida en varios módulos clave del frontend. La integración continua, las revisiones cruzadas de código y la claridad en las responsabilidades asignadas fueron aspectos destacados que facilitaron un buen ritmo de trabajo. Como oportunidad de mejora, se identificó la necesidad de reforzar el seguimiento y cumplimiento de los objetivos priorizados, así como de mejorar la estimación de tiempos en algunos flujos más complejos. También se mencionó la importancia de alinear aún más los esfuerzos individuales con los objetivos de entrega colectivos. |
| Sprint Goal & User Stories |  |
| Sprint 3 Goal | Nuestro enfoque está en presentar de forma efectiva nuestra propuesta de valor a los nuevos visitantes. También, habilitar la gestión de recetas y pedidos, así como mejorar la sección de ventas, para los administradores de restaurantes; incorporar la gestión de órdenes para los proveedores; y, en general, permitir a ambos segmentos realizar el pago de su suscripción. Asimismo, proporcionar, mediante el API de la plataforma, puntos de accesos a los desarrolladores frontend para que implementen funcionalidades relacionadas con gestión de pedidos, ventas, recetas, inventario, perfil y comentarios. Creemos que esto ofrece a los visitantes mayor confianza hacia el equipo de trabajo y les permite conocer mejor la propuesta de valor. Del mismo modo, mejora los flujos de usuario, al permitir la realización de pagos de suscripción; agiliza las operaciones para los administradores de restaurantes, al facilitar la creación y gestión de ventas, la configuración de recetas y la gestión de pedidos; optimiza el tiempo operativo para los proveedores, al permitir el seguimiento de pedidos. Además, permite a los desarrolladores frontend implementar funcionalidades esenciales de forma más eficiente, incluyendo pedidos, ventas, recetas, inventario, perfil y comentarios. |
| Sprint 3 Velocity | 38 |
| Sum of Story Points | 35 |

5.2.3.2. Aspect Leaders and Collaborators.

Durante el Sprint 3, se ha definido el desarrollo e integración de los módulos principales del frontend de la aplicación web interna GlassGo y del backend, abarcando funcionalidades clave como la gestión de productos, pedidos, inventario y compras. Estas implementaciones buscan optimizar los procesos internos y mejorar la trazabilidad del inventario, brindando mayor eficiencia a los administradores de restaurantes y su personal.

Con el fin de mantener una coordinación efectiva y una comunicación fluida entre los integrantes del equipo, se estructuró la matriz de liderazgo y colaboración (LACX), donde se asignó un líder (L) encargado de cada funcionalidad y colaboradores (C) que brindan apoyo en su implementación.

| Team Member (Last Name, First Name) | GitHub Username | Profile & References  | Paymets & Subscriptions  | Loyalty & Engagerment  | Service Planning  | System Administration  |
| ----- | ----- | :---- | :---- | :---- | :---- | :---- |
| Carlos Lavado Ever Giusephi | sephi-dev05 | C | L | L | C | C |
| Palacín Lazo Gerardo Valentín  | GeraldP03 | C | C | C | C | C |
| Howard Robles Guillermo Arturo | GuillermoPromac | C | C | C | C | C |
| Acosta Elera Abraham Bernabe | abraam16 | L | C | C | C | C |
| Vivar Cesar David Ignacio | DarkBeider20 | C | C | C | C | L |
| Guillen Giraldo Mike Dylan | FulLHous | C | C | C | L | C |

5.2.3.3 Sprint Backlog 3  
El objetivo principal de este Sprint es consolidar una experiencia funcional completa para los distintos perfiles de usuario dentro de la plataforma GlassGo. Se prioriza la mejora de la landing page para comunicar eficazmente la propuesta de valor a nuevos visitantes, así como la habilitación de módulos clave como la gestión de ventas, recetas y pedidos para los administradores de restaurantes, y la gestión de órdenes para los proveedores.

Asimismo, se trabajará en la integración del flujo de pagos por suscripción y en la provisión de APIs REST documentadas, permitiendo al equipo frontend consumir endpoints de forma eficiente para construir las vistas requeridas. Este enfoque integral busca mejorar la usabilidad, operatividad y cohesión entre el frontend y backend, facilitando la validación funcional de la plataforma y avanzando hacia su adopción por parte de los usuarios finales.

![][image4]

Trello: [https://trello.com/invite/b/68ffe30942dcb480aedf84d2/ATTI14ff021bc259e9ac94812c42ae4680e22318D9BD/sprint-backlog-3](https://trello.com/invite/b/68ffe30942dcb480aedf84d2/ATTI14ff021bc259e9ac94812c42ae4680e22318D9BD/sprint-backlog-3)

5.2.3.4 Development Evidence for Sprint Review

Web Services (Backend):

En el backend de la plataforma se realizaron importantes avances enfocados en la gestión de recetas, suministros y lotes. Se implementaron las operaciones CRUD para recetas y el manejo detallado de sus insumos, además de validar y reforzar la integridad de datos mediante objetos de valor específicos. También se añadieron configuraciones para ambientes de desarrollo y producción, y se mejoraron las definiciones de columnas en la base de datos para optimizar el manejo de fechas, precios y cantidades. Se desarrollaron servicios y controladores que facilitan la interacción con los recursos, permitiendo una gestión eficiente y segura de los datos relacionados con el inventario y las operaciones del sistema.

5.2.3.5. Execution Evidence for Sprint Review  
A continuación, se muestra un video con los avances realizados durante el Sprint 3, en el cual se trabajó en la landing page, así como en el desarrollo del frontend y backend.

5.2.3.6. Services Documentation Evidence for Sprint Review.

Durante este sprint se completó al 100% el desarrollo del Landing Page del sistema, consolidando su estructura visual, diseño responsivo, traducción multilenguaje y funcionalidades de navegación. Asimismo, se avanzó de forma significativa en la construcción del frontend del sistema, incluyendo componentes claves como el menú lateral, el dashboard inicial, el módulo de gestión de insumos y la arquitectura modular en Angular bajo DDD (Domain-Driven Design).

Aunque no se desplegaron endpoints REST aún, se documentan a continuación los recursos y avances relevantes del sprint, junto con evidencia de despliegue y repositorio de código.

Descripción del Logro:

Finalización del Landing Page (100%).  
Implementación completa de diseño responsivo, i18n, y redirecciones funcionales.  
Estructura de frontend modular iniciada (menu sidebar, dashboard y componentes base).  
Aplicación de buenas prácticas de organización por bounded contexts en Angular.  
Integración visual basada en Vue con VuePrime y Primeflex.

5.2.3.7. Software Deployment Evidence for Sprint Review

Durante este sprint, se realizaron actividades de despliegue y pruebas de los servicios desarrollados, asegurando que las funcionalidades del sistema estén operativas y accesibles para los usuarios finales. A continuación, se detallan los pasos realizados:

5.2.3.8. Team Collaboration Insights during Sprint

Seguimos usando ramas específicas para cada sección o funcionalidad (feature/\[nombre-de-seccion\]), permitiendo un trabajo paralelo organizado.

Cada miembro del equipo asumió la responsabilidad de desarrollar una o más boundeds del Backend. Se realizaron commits frecuentes, registrando avances de manera continua y detallada. Las funcionalidades desarrolladas se integraron mediante Pull Requests hacia la rama develop. Se mantuvo una comunicación constante mediante la plataforma Discord para coordinar avances y resolver dudas en tiempo real. Se aplicaron buenas prácticas de programación, control de versiones y colaboración en equipo.
