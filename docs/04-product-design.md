# Capítulo IV: Product Design 
## 4.1. Style Guidelines

     
   Un style Guidelines es un conjunto de reglas y normas que definen cómo se debe redactar, diseñar y presentar documentos, contenido web y software. A continuación, se detallan las especificaciones de los parámetros implementados en la estructura del proyecto.

   ### 4.1.1. General Style Guidelines

* Branding history

  Para la creación del logo de nuestro producto GlassGo, se ha optado por un diseño moderno y minimalista que refleje las intenciones de la aplicación. El logotipo se compone de una tipografía elegante y sencilla, acompañada de un icono que simboliza eficiencia rápida y la perdurabilidad del producto durante el envío al igual que una frase honesta y alentadora. Mostrando colores que demuestran seguridad, rapidez y equilibrio como lo son el blanco, gris, verde, naranja y azul.

  ![Logos](../src/images/general/Logos_type.png)

* Typography

  Para la creación del logo de nuestro producto GlassGo, se ha optado por un diseño moderno y minimalista que refleje las intenciones de la aplicación. El logotipo se compone de una tipografía elegante y sencilla, acompañada de un icono que simboliza eficiencia rápida y la perdurabilidad del producto durante el envío al igual que una frase honesta y alentadora. Mostrando colores que demuestran seguridad, rapidez y equilibrio como lo son el blanco, gris, verde, naranja y azul.

  ![Letter_type1](../src/images/general/Letter.png)

   ![Letter_type2](../src/images/general/Letter2.png)


* Colors

  La paleta de colores de GlassGo se compone de tonos que transmiten confianza, rapidez y profesionalismo, valores esenciales para una marca enfocada en la entrega segura de productos. El azul principal refleja estabilidad y seguridad, mientras que el naranja aporta dinamismo y movimiento, reforzando la idea de inmediatez. El gris neutro equilibra y aporta sobriedad, asegurando una comunicación clara y profesional.


  * Azul → *\#002140*

    ![Blue](../src/images/general/Blue.png)

    

  * Gris medio → *\#6B6B6B*  
  * Blanco → *\#FFFFFF*  
  * Negro → *\#000000*

    ![Gray](../src/images/general/Gris.png)![White](../src/images/general/White.png)![Black](../src/images/general/black.png)

    

* Spacing

  La paleta de colores de GlassGo se compone de tonos que transmiten confianza, rapidez y profesionalismo, valores esenciales para una marca enfocada en la entrega segura de productos. El azul principal refleja estabilidad y seguridad, mientras que el naranja aporta dinamismo y movimiento, reforzando la idea de inmediatez. El gris neutro equilibra y aporta sobriedad, asegurando una comunicación clara y profesional.

  ![][image8]

### 4.1.2. Web Style Guidelines

  Para GlassGo, estamos planeando desarrollar una plataforma web.Por lo tanto, implementaremos un diseño adaptable(conocido como Web Responsive Design) con el objetivo de optimizar la presentación de información en cualquier dispositivo.Esto asegurará que el contenido se mantenga intacto y, en última instancia, mejorará la experiencia del usuario.  
       
  Como equipo, hemos optado por incorporar el patrón de diseño en forma de F en nuestro sitio web. Este patrón es especialmente adecuado para GlassGo, ya que los usuarios suelen explorar el contenido de manera rápida y priorizando la información de la parte superior e izquierda de la pantalla. Con ello, se logra resaltar datos relevantes desde el inicio y facilitar la lectura de los apartados clave.

  ## 4.2. Information Architecture

  ### 4.2.1. Organization Systems

* Menú principal


| Tópico | Definición |
| :---: | ----- |
| Home page | La página de inicio puede mostrar una vista general del servicio y destacar las características clave. |
| Log in | La página para que el usuario ingrese a su sesión. En caso de no tener sesión hay una sección para poder registrarse gratis en el servicio web.  |
| Technical support | La página ofrece un espacio para que los usuarios compartan sus dudas, asistencia técnica o quejas que se encuentren con el sistema. |

* Pagina de suscripción

| Tópico | Definición |
| :---: | ----- |
| Plan empresa transportista | Plan para las empresas que busquen una alianza con un distribuidor. Los beneficios son: tarifas preferenciales, reportes avanzados y soporte prioritario. |
| Plan distribuidor de insumos terminados | Plan para los distribuidores que buscan una solución logística para manejar correctamente sus recursos.  |
| Plan Market | Plan individual para los negocios comunes como restaurantes, bares y licorerías. |


* Pagina de log in


| Tópico | Definición |
| :---: | ----- |
| Registro y autenticación | Plan para las empresas que busquen una alianza con un distribuidor. Los beneficios son: tarifas preferenciales, reportes avanzados y soporte prioritario. |


* Otras paginas y funciones


| Tópico | Definición |
| :---: | ----- |
| Perfil de usuarios | La página de inicio puede mostrar una vista general del servicio y destacar las características clave. |
| Configuraciones | La página para que el usuario ingrese a su sesión. En caso de no tener sesión hay una sección para poder registrarse gratis en el servicio web.  |
| Acerca de nosotros | La página ofrece un espacio para que los usuarios compartan sus dudas, asistencia técnica o quejas que se encuentren con el sistema. |
| Barra de navegación | Una barra de navegación clara y consistente en la parte superior de cada página facilita la navegación entre las secciones principales de la aplicación. |
| Responsive design | La aplicación debe ser fácil de usar tanto en dispositivos de escritorio como en dispositivos móviles,adaptando la interfaz de usuario según el tamaño de la pantalla. |

  ### 4.2.2. Labeling Systems

  Para los sistemas de etiquetado, hemos optado por organizar el contenido mediante encabezados que agrupen las seccione las que el usuario puede acceder. De esta manera, el usuario sabe dónde hacer clic para acceder a las secciones correspondientes.  
     

| Tópico | Definición |
| :---: | ----- |
| Home page | Sección principal a la cual llegará el usuario al entrar al link de la aplicación web.  |
| Subscription | En esta sección, se podrán ver los planes y tarifas disponibles con los cuales contamos  |
| Technical support | Esta es la sección en la cual se le brindará al usuario todos los canales por los cuales nos puede contactar. |

  ### 4.2.3. SEO Tags and Meta Tags

* ### Landing Page

  * Charset:

    *\<meta charset="utf-8"\>*

    

    Indica al navegador cómo interpretar los caracteres de texto. Al especificar UTF-8, se garantiza que la landing de GlassGo muestre correctamente tildes, la letra "ñ" y símbolos especiales, asegurando una visualización adecuada en cualquier idioma.

    

  * Viewport(responsive):

    *\<meta name="viewport" content="width=device-width, initial-scale=1"\>*

    

    Permite que la página se adapte a diferentes dispositivos (móvil, tablet, PC), asegurando que la presentación de GlassGo sea legible y óptima en cualquier pantalla.

    

  * Title(SEO):

    *\<title\>GlassGo | Transporte seguro y trazabilidad de envíos en vidrio\</title\>*

    

    Define el título que aparecerá en la pestaña del navegador y en los resultados de búsqueda. Su función es dar una descripción clara y concisa del servicio principal de GlassGo.

    

    

  * Meta description:

    *\<meta name="description" content="GlassGo ofrece transporte seguro y trazabilidad de envíos en vidrio. Reduce pérdidas, asegura la integridad del producto y mejora la eficiencia logística."\>*

    Proporciona un resumen breve que aparecerá en los resultados de búsqueda. Su objetivo es atraer a los usuarios interesados en soluciones de logística sostenible y transporte seguro.

    

    

  * Meta keywords(SEO, en desuso para Google):

    *\<meta name="keywords" content="transporte de vidrio, logística sostenible, trazabilidad, distribución segura, envíos rápidos, GlassGo"\>*

    

    Identifica palabras clave relacionadas con el servicio de GlassGo. Aunque actualmente su impacto es limitado, sigue siendo útil para sistemas de indexación básicos.

    

  * Meta Authors:

    *\<meta name="author" content="Equipo GlassGo"\>*

    

    Atribuye la autoría del contenido del landing al equipo responsable del proyecto GlassGo.

    

  * Meta robots:

    *\<meta name="robots" content="index, follow"\>*

    

    Permite a los motores de búsqueda indexar la página de GlassGo y seguir sus enlaces, asegurando mayor visibilidad.

    

  * Meta Language:

    *\<meta name="language" content="es"\>*

    

    Informa que el contenido de la landing está en español, optimizando su indexación y compatibilidad con navegadores.

    

  * Meta copyright:

    *\<meta name="copyright" content="GlassGo 2025"\>*

    

    Indica la titularidad de los derechos de autor del contenido y diseño de la landing.

    

* ### Web Application

  * Charset:

    *\<meta charset="utf-8"\>*

    

    Asegurar que todos los caracteres y símbolos en la interfaz de la aplicación GlassGo se visualicen correctamente.

    

  * Viewport(responsive):

    *\<meta name="viewport" content="width=device-width, initial-scale=1"\>*

    

    Garantiza que la aplicación web (panel de gestión, dashboard de trazabilidad) sea totalmente responsiva y se adapte a diferentes dispositivos.

    

  * Title(SEO):

    *\<title\>GlassGo App | Panel de trazabilidad y gestión\</title\>*

    

    Define el título que aparece en el navegador para identificar el panel de la aplicación web.

    

  * Meta description:

    *\<meta name="description" content="Panel interno de GlassGo para gestionar envíos, trazabilidad y planes de suscripción. Acceso exclusivo para usuarios registrados."\>*

    

    Describe el contenido del panel, aunque su relevancia en SEO es limitada por ser un espacio interno.

    

  * Meta Authors

    *\<meta name="author" content="Equipo GlassGo"\>*

    

    Atribuye el desarrollo del panel de control a la marca.

    

  * Meta robots:

    *\<meta name="robots" content="noindex, nofollow"\>*

    

    Evita que los motores de búsqueda indexen contenido privado de la aplicación (historial de envíos, métricas, etc.).

    

  * Meta Language:

    *\<meta name="language" content="es"\>*

    

    Declara que el idioma principal del panel de GlassGo es español.

    

  * Meta copyright:

    *\<meta name="copyright" content="GlassGo 2025"\>*

    

    Protege legalmente el contenido y diseño del software de GlassGo.

    

###  

### 4.2.4. Searching Systems

   El motor de búsqueda es fundamental para que los usuarios encuentren rápidamente detalles específicos.  
* Características clave

  Las búsquedas por objetivos le permitirá al usuario como dueño de negocio, transportistas o distribuidores son

  * Identificar impactos en el cargamento en las últimas 24h.  
  * Prever rutas con altos índices de incidencias durante el trayecto, guardar esa información para que más transportistas manejen con cautela.  
  * Generar evidencia si se concreta algún reclamo por parte del cliente o el proveedor.  
  * Verificar el estado de la carga antes de aceptar  
  * Etiquetar inventario de alta importancia durante temporadas altas.  
  * Consultar el historial de transporte para prevenir posibles roturas del cargamento.

    ### 4.2.5. Navigation Systems

       El Sistema de Navegación es la estructura que permite a los usuarios desplazarse eficientemente entre las distintas secciones y páginas de la aplicación.  
         
* Estructura de navegación  
  * Logo \- link to Homepage  
  * Homepage— resumen / landing con beneficios y CTA  
  * Solutions / Servicios — páginas por segmento  
    * Transportistas  
    * Distribuidores  
    * Comercios (Dueños de negocio)  
  * Subscriptions / Planes — comparación de planes y precios  
  * Support / Soporte — Centro de ayuda, FAQ, contacto  
  * Contact — formulario de contacto / ventas  
  * Buscar (Search) — campo de búsqueda global  
  * Botón Log In / Sign Up (derecha)

    

    

  ## 4.3. Landing Page UI Design

  ### 4.3.1. Landing Page Wireframe

**Wireframe 1: Vista general de la landing page**
![](../src/images/chapter4/landing-page-ui/wirefram-1.png)

**Wireframe 2: Encabezado y menú principal**
![](../src/images/chapter4/landing-page-ui/wireframe-2.png)

**Wireframe 3: Sección de beneficios y características**
![](../src/images/chapter4/landing-page-ui/wireframe-3.png)

**Wireframe 4: Detalle de servicios ofrecidos**
![](../src/images/chapter4/landing-page-ui/wireframe-4.png)

**Wireframe 5: Proceso de registro o suscripción**
![](../src/images/chapter4/landing-page-ui/wirefram-5.png)

**Wireframe 6: Testimonios y casos de éxito**
![](../src/images/chapter4/landing-page-ui/wireframe-6.png)

**Wireframe 7: Preguntas frecuentes y soporte**
![](../src/images/chapter4/landing-page-ui/wireframe-7.png)

**Wireframe 8: Pie de página y enlaces de contacto**
![](../src/images/chapter4/landing-page-ui/wireframe-8.png)

  ### 4.3.2. Landing Page Mock-up

**Mockup 1: Vista principal de la landing page**
![](../src/images/chapter4/landing-page-ui/Mockup-1.png)

**Mockup 2: Encabezado con menú de navegación**
![](../src/images/chapter4/landing-page-ui/Mockup-2.png)

**Mockup 3: Sección de beneficios y propuesta de valor**
![](../src/images/chapter4/landing-page-ui/Mockup-3.png)

**Mockup 4: Detalle de servicios y funcionalidades**
![](../src/images/chapter4/landing-page-ui/Mockup-4.png)

**Mockup 5: Proceso de registro y suscripción**
![](../src/images/chapter4/landing-page-ui/Mockup-5.png)

**Mockup 6: Testimonios y casos de éxito**
![](../src/images/chapter4/landing-page-ui/Mockup-6.png)

**Mockup 7: Preguntas frecuentes y soporte**
![](../src/images/chapter4/landing-page-ui/Mockup-7.png)

**Mockup 8: Pie de página con enlaces de contacto**
![](../src/images/chapter4/landing-page-ui/Mockup-8.png)

**Mockup 9: Vista responsiva en dispositivos móviles**
![](../src/images/chapter4/landing-page-ui/Mockup-9.png)


  ## 4.4. Web Applications UX/UI Design

  El diseño de experiencia de usuario (UX) y de interfaz de usuario (UI) en nuestra landing page tiene como objetivo ofrecer una interacción digital clara, atractiva y sencilla para los visitantes. La UX se enfoca en entender lo que buscan y esperan los usuarios, organizando la información y los flujos de navegación de forma que el recorrido sea cómodo y eficiente. La UI, en cambio, se ocupa de la parte visual, como la disposición de los elementos, los botones, los menús y la presentación del contenido. Al combinar ambos enfoques, lograremos un diseño que no solo sea estéticamente agradable, sino también funcional y fácil de usar, generando una experiencia positiva que motive al usuario a interesarse en nuestro producto.

### 4.4.1. Web Applications Wireframes

![](../src/images/chapter4/software-architecture/login-Sign%20in.png)
![](../src/images/chapter4/software-architecture/login-Sign%20in-Google.png)
![](../src/images/chapter4/software-architecture/recover_password.png)
![](../src/images/chapter4/software-architecture/Register-Sign%20up.png)
![](../src/images/chapter4/software-architecture/Register-Loading-Succesful-maybe.png)
![](../src/images/chapter4/software-architecture/Dashboard.png)
![](../src/images/chapter4/software-architecture/Orders.png)
![](../src/images/chapter4/software-architecture/Tracking.png)
![](../src/images/chapter4/software-architecture/Tracking_complete.png)
![](../src/images/chapter4/software-architecture/Inventary.png)
![](../src/images/chapter4/software-architecture/Calendar.png)
![](../src/images/chapter4/software-architecture/Report.png)
![](../src/images/chapter4/software-architecture/History.png)
![](../src/images/chapter4/software-architecture/Claim.png)
![](../src/images/chapter4/software-architecture/Customers.png)
![](../src/images/chapter4/software-architecture/Stock_management.png)
![](../src/images/chapter4/software-architecture/Shipping_history.png)
![](../src/images/chapter4/software-architecture/Claims_registry.png)
  


### 4.4.2. Web Applications Wireflow Diagrams

Los diagramas de wireflow son representaciones gráficas que combinan la estructura de wireframes con la lógica de diagramas de flujo, mostrando cómo los usuarios interactúan y se desplazan dentro de una aplicación web. Estos esquemas permiten visualizar la experiencia de navegación, detectar posibles fricciones en la usabilidad y diseñar recorridos más fluidos y eficientes.  
       
de inventario, el seguimiento de envíos, el uso del calendario de entregas, la generación de reportes y la administración de reclamos. De esta manera, el diagrama proporciona una visión integral de la plataforma, asegurando una experiencia clara, ordenada y alineada a las necesidades de cada usuario.  

![Wireflow_diagram](../src/images/chapter4/style-guidelines/Wireflow_diagram.png)

[https://lucid.app/lucidchart/1d76ffac-1618-4b03-a28f-a5a840f67ac7/edit?viewport\_loc=-12591%2C-6613%2C22617%2C11070%2C0\_0\&invitationId=inv\_592714f1-7efd-4777-8053-5ed7aae18f41](https://lucid.app/lucidchart/1d76ffac-1618-4b03-a28f-a5a840f67ac7/edit?viewport_loc=-12591%2C-6613%2C22617%2C11070%2C0_0&invitationId=inv_592714f1-7efd-4777-8053-5ed7aae18f41)

  ### 4.4.3. Web Applications Mock-ups

* Login - Pantalla de acceso principal que permite iniciar sesión según el tipo de usuario. Se prioriza la simplicidad, contraste alto y botones accesibles. 

  **![Log in](../src/images/chapter4/prototyping/login-Sign%20in.png)**  

* Login con Google – Acceso rápido
Opción de autenticación alternativa mediante cuenta Google para agilizar el proceso de ingreso. 

  **![Log in - Google](../src/images/chapter4/prototyping/Login-Sign%20in-Google.png)**  

* Actualizar las contraseñas si se olvidan.

  **![Recover - password](../src/images/chapter4/prototyping/recover_password.png)**  

* Registrar una cuenta para ingresar al la app. 

  **![Sign up](../src/images/chapter4/prototyping/Register-Sign%20up.png)** 

* Pantalla de bienvenida GlassGo
Presenta la identidad visual del sistema antes de ingresar al panel principal.

   **![Succesful](../src/images/chapter4/prototyping/Register-Loading-Succesful-maybe.png)**  

#### Segmento 1: Transportistas

* Vista inicial con resumen de viajes activos, notificaciones y accesos rápidos.
  
  **![Home](../src/images/chapter4/prototyping/Home.png)**  

* Permite crear y ver el resumen de los pedidos asignados para entrega.
  
  **![Customer list](../src/images/chapter4/prototyping/Create_order.png)**  

* Muestra la ruta actual con origen, destino y puntos de control definidos.
  
  **![Tracking](../src/images/chapter4/prototyping/Traking.png)**  

* Permite ver la ubicación en tiempo real de los camiones, mostrando alertas de desvío, impacto o exceso de velocidad.
  
  **![Tracking detallado](../src/images/chapter4/prototyping/Traking_complete.png)**  

* Visualiza los productos transportados y su estado. Permite reportar incidencias o confirmar recepción.
  
  **![Inventary](../src/images/chapter4/prototyping/Inventary.png)**  

* Muestra fechas programadas y horas estimadas de llegada (ETA) para planificar rutas.
  
  **![Calendar](../src/images/chapter4/prototyping/Calendar.png)** 

* Formulario para registrar eventos como retrasos, daños o alertas durante el viaje.
  
  **![Report](../src/images/chapter4/prototyping/Report.png)**

* Registro de viajes completados con información de fechas, tiempos y distancias.
  
  **![History](../src/images/chapter4/prototyping/History.png)**

* Muestra reclamos asociados a entregas previas para referencia y seguimiento.
  
  **![Claim](../src/images/chapter4/prototyping/Claim.png)**

---

#### Segmentos 2 & 3: Distribuidores de licores y Dueños de negocios

* Resumen general de pedidos activos, entregas y estadísticas de desempeño.
  
  **![Home](../src/images/chapter4/prototyping/Customers/camiones.png)**  

* Muestra los negocios asociados y sus pedidos recientes.
  
  **![Customer](../src/images/chapter4/prototyping/Clientes/Camiones.png)**  

* Presenta en mapa la ubicación en tiempo real de los camiones asignados.
  
  **![Tracking](../src/images/chapter4/prototyping/Tracking/camiones.png)**  

* Visualiza los productos disponibles con cantidad, estado y opción para editar registros.
  
  **![Stock](../src/images/chapter4/prototyping/Stock%20management.png)**  

* Permite revisar y organizar próximas entregas mediante un calendario visual.
  
  **![Calendar](../src/images/chapter4/prototyping/Calendar/camiones.png)**  

* Muestra métricas comparativas de tiempo, distancia y costos de entrega.
  
  **![Report](../src/images/chapter4/prototyping/Report/camiones.png)**  

* Registro de compras anteriores con su estado, fecha y monto.
  
  **![History](../src/images/chapter4/prototyping/Shipping%20history.png)**  

* Permite comunicación directa con transportistas desde el panel.
  
  **![Comunication](../src/images/chapter4/prototyping/Claims%20registry.png)**  

### 4.4.4. Web Applications User Flow Diagrams

**Diagrama 1: Inicio del flujo de usuario en la plataforma**
![](../src/images/chapter4/information-architecture/1.png)

**Diagrama 2: Proceso de autenticación y acceso**
![](../src/images/chapter4/information-architecture/2.png)

**Diagrama 3: Navegación por el panel principal**
![](../src/images/chapter4/information-architecture/3.png)

**Diagrama 4: Gestión y visualización de pedidos**
![](../src/images/chapter4/information-architecture/4.png)

**Diagrama 5: Seguimiento de envíos y rutas**
![](../src/images/chapter4/information-architecture/5.png)

**Diagrama 6: Registro y manejo de incidencias**
![](../src/images/chapter4/information-architecture/6.png)

**Diagrama 7: Finalización del proceso y cierre de sesión**
![](../src/images/chapter4/information-architecture/7.png)

**Diagrama general: Vista completa del flujo de usuario en la plataforma**
![](../src/images/chapter4/information-architecture/ALL.png)


## 4.5. Web Applications Prototyping

  [https://www.figma.com/design/nV0UrH5YsFXu9run93EmRm/GlassGo?node-id=0-1\&t=2SDCRONXUcQzrQsj-1](https://www.figma.com/design/nV0UrH5YsFXu9run93EmRm/GlassGo?node-id=0-1&t=2SDCRONXUcQzrQsj-1) 

## 4.6. Domain-Driven Software Architecture

La arquitectura de software orientada al dominio (DDD) se centra en modelar el sistema a partir de los procesos clave del negocio: transporte seguro de licores en envases de vidrio, trazabilidad de envíos y monitoreo de condiciones de transporte. Este enfoque nos permite que cada parte del software refleje fielmente la lógica del negocio, facilitando la escalabilidad y el mantenimiento de GlassGo, el producto principal de la startup RPG.  
        
### 4.6.1 . Design-Level EventStorming

![](../src/images/chapter4/information-architecture/GlassGo%20-%20EventStorming%20(1).jpg)


### 4.6.2. Software Architecture Context Diagram      

* Person:  
  * **Transportista:** Conduce el camión y usa la app móvil para ver rutas, registrar inicio/fin de viaje y recibir alertas de impacto.  
  * **Distribuidor:** Supervisa los envíos desde oficinas. Revisa dashboard web, descarga reportes.  
  * **Dueño de Negocio:** Cliente final que quiere saber si su pedido llegará a tiempo y sin roturas.  
  * **Administrador RPG:** Personal de la startup para gestión interna, soporte y mantenimiento.  
* Software System:  
  * **GlassGo:** Sistema central que ofrece la trazabilidad, optimización de rutas y monitoreo.  
  * **Google Maps:** Plataforma que ofrece una REST API de información geo referencial.  
  * **PayPal :** Pasarela de pagos para cobrar las membresías.  
  * **Twilio:** Servicio de notificaciones para el envío de SMS, emails o notificaciones push.

  ![context-diagram](../src/images/chapter4/domain-driven-software-arquitecture/context-diagram.png)

### 4.6.3. Software Architecture Container Diagrams

* Container:  
  * **Mobile App:** App móvil  
  * **Landing Page:** Página de aterrizaje  
  * **Web App:** App web  
  * **API REST:** API REST para acceso a datos y lógica de negocio  
  * **DB:** Base de datos relacional

  ![container-diagram](../src/images/chapter4/domain-driven-software-arquitecture/container-diagram.png)


### 4.6.4. Software Architecture Components Diagrams

* **Web Application Component Diagram:**
  ![component-diagram1](../src/images/chapter4/domain-driven-software-arquitecture/component-diagram1.png)

* **Web Application Component Diagram:**
  ![component-diagram2](../src/images/chapter4/domain-driven-software-arquitecture/component-diagram2.png)

* **Profile Preferences Component Diagram:**
  ![component-diagram3](../src/images/chapter4/domain-driven-software-arquitecture/component-diagram3.png)

* **Payments Subscriptions Component Diagram:**
  ![component-diagram4](../src/images/chapter4/domain-driven-software-arquitecture/component-diagram4.png)

* **Service Planning Component Diagram:**
  ![component-diagram5](../src/images/chapter4/domain-driven-software-arquitecture/component-diagram5.png)

* **Service Execution Component Diagram:**
  ![component-diagram6](../src/images/chapter4/domain-driven-software-arquitecture/component-diagram6.png)

* **Dashboard Analytics Component Diagram:**
  ![component-diagram7](../src/images/chapter4/domain-driven-software-arquitecture/component-diagram7.png)

* **Loyalty Engagement Component Diagram:**
  ![component-diagram8](../src/images/chapter4/domain-driven-software-arquitecture/component-diagram8.png)

* **System Administration Component Diagram:**
  ![component-diagram9](../src/images/chapter4/domain-driven-software-arquitecture/component-diagram9.png)

## 4.7. Software Object-Oriented Design

  El Diseño Orientado a Objetos se centra en la estructura lógica del dominio GlassGo, utilizando diagramas de clases UML para definir entidades, servicios y sus relaciones. Cada diagrama representa cómo interactúan las clases dentro de un contexto delimitado, encapsulando atributos y métodos coherentes con sus responsabilidades.

### 4.7.1. Class Diagrams

**Vistas Especificas por Bounded Context**

  * **Identity Access Class Diagram:**
    ![class-diagram1](../src/images/chapter4/software-object-oriented-design/class-diagram1.png)
  
  * **Profile Preferences Class Diagram:**
    ![class-diagram2](../src/images/chapter4/software-object-oriented-design/class-diagram2.png)
  
  * **Payment Subscription Class Diagram:**
    ![class-diagram3](../src/images/chapter4/software-object-oriented-design/class-diagram3.png)

  * **Service Planning Class Diagram:**
    ![class-diagram4](../src/images/chapter4/software-object-oriented-design/class-diagram4.png)
  
  * **Service Execution Monitoring Class Diagram:**
    ![class-diagram5](../src/images/chapter4/software-object-oriented-design/class-diagram5.png)

  * **Dashboard Analytics Class Diagram:**
    ![class-diagram6](../src/images/chapter4/software-object-oriented-design/class-diagram6.png)

  * **Loyalty Engagement Class Diagram:**
    ![class-diagram7](../src/images/chapter4/software-object-oriented-design/class-diagram7.png)

  * **System Administration Class Diagram:**
    ![class-diagram8](../src/images/chapter4/software-object-oriented-design/class-diagram8.png)

## 4.8. Database Design

El diseño de la base de datos define la estructura relacional utilizada por el sistema GlassGo para garantizar la persistencia e integridad de los datos en todos los contextos delimitados.


### 4.8.1. Database Diagrams

* **Global View:**
  ![global-view](../src/images/chapter4/database-design/global-view.png)

* **Vistas Especificas por Bounded Context:**

  * **Identity Access Database Diagram:**

    ![database-diagram1](../src/images/chapter4/database-design/database-diagram1.png)
  
  * **Profile Preferences Database Diagram:**

    ![database-diagram2](../src/images/chapter4/database-design/database-diagram2.png)

  * **Payment Subscriptions Database Diagram:**

    ![database-diagram3](../src/images/chapter4/database-design/database-diagram3.png)
  
  * **Service Planning Database Diagram:**

    ![database-diagram4](../src/images/chapter4/database-design/database-diagram4.png)

  * **Service Execution Monitoring Database Diagram:**

    ![database-diagram5](../src/images/chapter4/database-design/database-diagram5.png)

  * **Dashboard Analytics Database Diagram:**

    ![database-diagram6](../src/images/chapter4/database-design/database-diagram7.png)

  * **Loyalty Engagement Database Diagram:**

    ![database-diagram7](../src/images/chapter4/database-design/database-diagram7.png)

  * **System Administration Database Diagram:**

    ![database-diagram8](../src/images/chapter4/database-design/database-diagram8.png)
