# Chapter IV: Product Design
## 4.1. Style Guidelines

A style guidelines is a set of rules and standards that define how documents, web content, and software should be written, designed, and presented. Below are the specifications of the parameters implemented in the project structure.

### 4.1.1. General Style Guidelines

* Branding History

  For the creation of our GlassGo product logo, we opted for a modern and minimalist design that reflects the application's intentions. The logo consists of elegant and simple typography, accompanied by an icon that symbolizes rapid efficiency and product durability during shipping, along with an honest and encouraging phrase. Displaying colors that demonstrate security, speed, and balance such as white, gray, green, orange, and blue.

  ![Logos](../src/images/general/Logos_type.png)

* Typography

  For our GlassGo product typography, we chose modern and minimalist fonts that reflect the application's intentions. The typography consists of elegant and simple fonts, complementing the icon that symbolizes rapid efficiency and product durability during shipping, along with an honest and encouraging message. The typography uses colors that demonstrate security, speed, and balance including white, gray, green, orange, and blue.

  ![Letter_type1](../src/images/general/Letter.png)

  ![Letter_type2](../src/images/general/Letter2.png)

* Colors

  GlassGo's color palette consists of tones that convey trust, speed, and professionalism - essential values for a brand focused on secure product delivery. The primary blue reflects stability and security, while orange adds dynamism and movement, reinforcing the idea of immediacy. The neutral gray balances and adds sobriety, ensuring clear and professional communication.

  * Blue → *#002140*

    ![Blue](../src/images/general/Blue.png)

  * Medium Gray → *#6B6B6B*
  * White → *#FFFFFF*
  * Black → *#000000*

    ![Gray](../src/images/general/Gris.png)![White](../src/images/general/White.png)![Black](../src/images/general/black.png)

* Spacing

  GlassGo's color palette consists of tones that convey trust, speed, and professionalism - essential values for a brand focused on secure product delivery. The primary blue reflects stability and security, while orange adds dynamism and movement, reinforcing the idea of immediacy. The neutral gray balances and adds sobriety, ensuring clear and professional communication.

  ![][image8]

### 4.1.2. Web Style Guidelines

  For GlassGo, we are planning to develop a web platform. Therefore, we will implement a responsive design (known as Web Responsive Design) with the goal of optimizing information presentation on any device. This will ensure that the content remains intact and ultimately enhance the user experience.

  As a team, we have chosen to incorporate the F-pattern design in our website. This pattern is especially suitable for GlassGo, as users tend to explore content quickly and prioritize information at the top and left of the screen. This helps highlight relevant data from the start and facilitates reading of key sections.

## 4.2. Information Architecture

### 4.2.1. Organization Systems

* Main Menu

| Topic | Definition |
| :---: | ----- |
| Home page | The homepage can display an overview of the service and highlight key features. |
| Log in | The page where users can log into their session. If they don't have an account, there's a section to register for free in the web service. |
| Technical support | The page provides a space for users to share their questions, technical assistance, or complaints about the system. |

* Subscription Page

| Topic | Definition |
| :---: | ----- |
| Transport Company Plan | Plan for companies seeking a partnership with a distributor. Benefits include: preferential rates, advanced reports, and priority support. |
| Finished Goods Distributor Plan | Plan for distributors seeking a logistics solution to properly manage their resources. |
| Market Plan | Individual plan for common businesses such as restaurants, bars, and liquor stores. |

* Login Page

| Topic | Definition |
| :---: | ----- |
| Registration and Authentication | Plan for companies seeking a partnership with a distributor. Benefits include: preferential rates, advanced reports, and priority support. |

* Other Pages and Functions

| Topic | Definition |
| :---: | ----- |
| User Profile | The homepage can display an overview of the service and highlight key features. |
| Settings | The page where users can log into their session. If they don't have an account, there's a section to register for free. |
| About Us | The page provides a space for users to share their questions, technical assistance, or complaints. |
| Navigation Bar | A clear and consistent navigation bar at the top of each page facilitates navigation between main sections. |
| Responsive Design | The application must be easy to use on both desktop and mobile devices, adapting the user interface to screen size. |

### 4.2.2. Labeling Systems

For labeling systems, we have chosen to organize content through headers that group sections users can access. This way, users know where to click to access the corresponding sections.

| Topic | Definition |
| :---: | ----- |
| Home page | Main section users will reach when entering the web application link. |
| Subscription | In this section, users can view available plans and rates. |
| Technical support | This section provides users with all channels through which they can contact us. |

### 4.2.3. SEO Tags and Meta Tags

* ### Landing Page

  * Charset:
    *\<meta charset="utf-8"\>*

    Tells the browser how to interpret text characters. By specifying UTF-8, it ensures GlassGo's landing page correctly displays accents, special characters, and symbols, ensuring proper visualization in any language.

  * Viewport(responsive):
    *\<meta name="viewport" content="width=device-width, initial-scale=1"\>*

    Allows the page to adapt to different devices (mobile, tablet, PC), ensuring GlassGo's presentation is legible and optimal on any screen.

  * Title(SEO):
    *\<title\>GlassGo | Secure Transport and Glass Shipment Traceability\</title\>*

    Defines the title that will appear in the browser tab and search results. Its function is to provide a clear and concise description of GlassGo's main service.

  * Meta description:
    *\<meta name="description" content="GlassGo provides secure transport and glass shipment traceability. Reduces losses, ensures product integrity, and improves logistics efficiency."\>*

    Provides a brief summary that will appear in search results. Its goal is to attract users interested in sustainable logistics and secure transport solutions.

  * Meta keywords(SEO, deprecated for Google):
    *\<meta name="keywords" content="glass transport, sustainable logistics, traceability, secure distribution, fast shipping, GlassGo"\>*

    Identifies keywords related to GlassGo's service. Although its impact is currently limited, it remains useful for basic indexing systems.

  * Meta Authors:
    *\<meta name="author" content="GlassGo Team"\>*

    Attributes landing page content authorship to the GlassGo project team.

  * Meta robots:
    *\<meta name="robots" content="index, follow"\>*

    Allows search engines to index GlassGo's page and follow its links, ensuring greater visibility.

  * Meta Language:
    *\<meta name="language" content="en"\>*

    Indicates the landing's content is in English, optimizing its indexation and browser compatibility.

  * Meta copyright:
    *\<meta name="copyright" content="GlassGo 2025"\>*

    Indicates copyright ownership of the landing's content and design.

* ### Web Application

  * Charset:
    *\<meta charset="utf-8"\>*

    Ensures all characters and symbols in GlassGo's application interface display correctly.

  * Viewport(responsive):
    *\<meta name="viewport" content="width=device-width, initial-scale=1"\>*

    Ensures the web application (management panel, traceability dashboard) is fully responsive and adapts to different devices.

  * Title(SEO):
    *\<title\>GlassGo App | Traceability and Management Panel\</title\>*

    Defines the title that appears in the browser to identify the web application panel.

  * Meta description:
    *\<meta name="description" content="GlassGo's internal panel for managing shipments, traceability, and subscription plans. Exclusive access for registered users."\>*

    Describes the panel's content, although its SEO relevance is limited as it's an internal space.

  * Meta Authors:
    *\<meta name="author" content="GlassGo Team"\>*

    Attributes control panel development to the brand.

  * Meta robots:
    *\<meta name="robots" content="noindex, nofollow"\>*

    Prevents search engines from indexing private application content (shipping history, metrics, etc.).

  * Meta Language:
    *\<meta name="language" content="en"\>*

    Declares English as GlassGo panel's main language.

  * Meta copyright:
    *\<meta name="copyright" content="GlassGo 2025"\>*

    Legally protects GlassGo software's content and design.

### 4.2.4. Searching Systems

The search engine is fundamental for users to quickly find specific details.
* Key Features

  The objective-based searches will allow business owners, carriers, and distributors to:

  * Identify impacts on cargo in the last 24 hours
  * Anticipate routes with high incident rates during transit, saving this information so other carriers can handle with caution
  * Generate evidence if a claim is made by the customer or supplier
  * Verify cargo status before acceptance
  * Tag high-priority inventory during peak seasons
  * Consult transport history to prevent possible cargo breakage

### 4.2.5. Navigation Systems

The Navigation System is the structure that allows users to efficiently move between different sections and pages of the application.

* Navigation Structure
  * Logo - link to Homepage
  * Homepage — summary / landing with benefits and CTA
  * Solutions — pages by segment
    * Carriers
    * Distributors
    * Businesses (Business Owners)
  * Subscriptions — plan and price comparison
  * Support — Help Center, FAQ, contact
  * Contact — contact/sales form
  * Search — global search field
  * Log In / Sign Up button (right)

## 4.3. Landing Page UI Design

### 4.3.1. Landing Page Wireframe

**Wireframe 1: Landing page overview**
![](../src/images/chapter4/landing-page-ui/wirefram-1.png)

**Wireframe 2: Header and main menu**
![](../src/images/chapter4/landing-page-ui/wireframe-2.png)

**Wireframe 3: Benefits and features section**
![](../src/images/chapter4/landing-page-ui/wireframe-3.png)

**Wireframe 4: Services details**
![](../src/images/chapter4/landing-page-ui/wireframe-4.png)

**Wireframe 5: Registration and subscription process**
![](../src/images/chapter4/landing-page-ui/wirefram-5.png)

**Wireframe 6: Testimonials and success stories**
![](../src/images/chapter4/landing-page-ui/wireframe-6.png)

**Wireframe 7: FAQ and support**
![](../src/images/chapter4/landing-page-ui/wireframe-7.png)

**Wireframe 8: Footer and contact links**
![](../src/images/chapter4/landing-page-ui/wireframe-8.png)

### 4.3.2. Landing Page Mock-up

**Mockup 1: Landing page main view**
![](../src/images/chapter4/landing-page-ui/Mockup-1.png)

**Mockup 2: Header with navigation menu**
![](../src/images/chapter4/landing-page-ui/Mockup-2.png)

**Mockup 3: Benefits and value proposition section**
![](../src/images/chapter4/landing-page-ui/Mockup-3.png)

**Mockup 4: Services and features details**
![](../src/images/chapter4/landing-page-ui/Mockup-4.png)

**Mockup 5: Registration and subscription process**
![](../src/images/chapter4/landing-page-ui/Mockup-5.png)

**Mockup 6: Testimonials and success stories**
![](../src/images/chapter4/landing-page-ui/Mockup-6.png)

**Mockup 7: FAQ and support**
![](../src/images/chapter4/landing-page-ui/Mockup-7.png)

**Mockup 8: Footer with contact links**
![](../src/images/chapter4/landing-page-ui/Mockup-8.png)

**Mockup 9: Responsive view on mobile devices**
![](../src/images/chapter4/landing-page-ui/Mockup-9.png)

## 4.4. Web Applications UX/UI Design

The user experience (UX) and user interface (UI) design of our landing page aims to offer clear, attractive, and simple digital interaction for visitors. UX focuses on understanding what users seek and expect, organizing information and navigation flows to make the journey comfortable and efficient. UI, on the other hand, deals with the visual aspect, such as the layout of elements, buttons, menus, and content presentation. By combining both approaches, we will achieve a design that is not only aesthetically pleasing but also functional and easy to use, generating a positive experience that motivates users to become interested in our product.

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

Wireflow diagrams are graphical representations that combine wireframe structure with flowchart logic, showing how users interact and move within a web application. These diagrams allow visualization of the navigation experience, detect potential usability frictions, and design more fluid and efficient user journeys.

The diagrams encompass inventory management, shipment tracking, delivery calendar usage, report generation, and claims management. This way, the diagram provides a comprehensive view of the platform, ensuring a clear, organized experience aligned with each user's needs.

![Wireflow_diagram](../src/images/chapter4/style-guidelines/Wireflow_diagram.png)

[https://lucid.app/lucidchart/1d76ffac-1618-4b03-a28f-a5a840f67ac7/edit?viewport\_loc=-12591%2C-6613%2C22617%2C11070%2C0\_0\&invitationId=inv\_592714f1-7efd-4777-8053-5ed7aae18f41](https://lucid.app/lucidchart/1d76ffac-1618-4b03-a28f-a5a840f67ac7/edit?viewport_loc=-12591%2C-6613%2C22617%2C11070%2C0_0&invitationId=inv_592714f1-7efd-4777-8053-5ed7aae18f41)

### 4.4.3. Web Applications Mock-ups

* Login - Main access screen that allows login based on user type. Prioritizes simplicity, high contrast, and accessible buttons.

  **![Log in](../src/images/chapter4/prototyping/login-Sign%20in.png)**

* Google Login – Quick Access
Alternative authentication option using Google account to streamline the login process.

  **![Log in - Google](../src/images/chapter4/prototyping/Login-Sign%20in-Google.png)**

* Update forgotten passwords.

  **![Recover - password](../src/images/chapter4/prototyping/recover_password.png)**

* Register an account to access the app.

  **![Sign up](../src/images/chapter4/prototyping/Register-Sign%20up.png)**

* GlassGo Welcome Screen
Presents the system's visual identity before entering the main panel.

   **![Succesful](../src/images/chapter4/prototyping/Register-Loading-Succesful-maybe.png)**

#### Segment 1: Carriers

* Initial view with active trips summary, notifications, and quick access.
  
  **![Home](../src/images/chapter4/prototyping/Home.png)**

* Create and view summary of assigned delivery orders.
  
  **![Customer list](../src/images/chapter4/prototyping/Create_order.png)**

* Shows current route with origin, destination, and defined control points.
  
  **![Tracking](../src/images/chapter4/prototyping/Traking.png)**

* View real-time truck location, showing deviation, impact, or speed excess alerts.
  
  **![Detailed Tracking](../src/images/chapter4/prototyping/Traking_complete.png)**

* Displays transported products and their status. Allows reporting incidents or confirming reception.
  
  **![Inventory](../src/images/chapter4/prototyping/Inventary.png)**

* Shows scheduled dates and estimated arrival times (ETA) for route planning.
  
  **![Calendar](../src/images/chapter4/prototyping/Calendar.png)**

* Form to register events such as delays, damages, or alerts during the trip.
  
  **![Report](../src/images/chapter4/prototyping/Report.png)**

* Completed trips log with dates, times, and distances information.
  
  **![History](../src/images/chapter4/prototyping/History.png)**

* Shows claims associated with previous deliveries for reference and tracking.
  
  **![Claim](../src/images/chapter4/prototyping/Claim.png)**

---

#### Segments 2 & 3: Liquor Distributors and Business Owners

* General summary of active orders, deliveries, and performance statistics.
  
  **![Home](../src/images/chapter4/prototyping/Customers/camiones.png)**

* Shows associated businesses and their recent orders.
  
  **![Customer](../src/images/chapter4/prototyping/Clientes/Camiones.png)**

* Displays real-time location of assigned trucks on map.
  
  **![Tracking](../src/images/chapter4/prototyping/Tracking/camiones.png)**

* Views available products with quantity, status, and option to edit records.
  
  **![Stock](../src/images/chapter4/prototyping/Stock%20management.png)**

* Review and organize upcoming deliveries through a visual calendar.
  
  **![Calendar](../src/images/chapter4/prototyping/Calendar/camiones.png)**

* Shows comparative metrics of time, distance, and delivery costs.
  
  **![Report](../src/images/chapter4/prototyping/Report/camiones.png)**

* Previous purchases record with status, date, and amount.
  
  **![History](../src/images/chapter4/prototyping/Shipping%20history.png)**

* Enables direct communication with carriers from the panel.
  
  **![Communication](../src/images/chapter4/prototyping/Claims%20registry.png)**  

### 4.4.4. Web Applications User Flow Diagrams

**Diagram 1: Platform user flow start**
![](../src/images/chapter4/information-architecture/1.png)

**Diagram 2: Authentication and access process**
![](../src/images/chapter4/information-architecture/2.png)

**Diagram 3: Main panel navigation**
![](../src/images/chapter4/information-architecture/3.png)

**Diagram 4: Order management and visualization**
![](../src/images/chapter4/information-architecture/4.png)

**Diagram 5: Shipment and route tracking**
![](../src/images/chapter4/information-architecture/5.png)

**Diagram 6: Incident registration and management**
![](../src/images/chapter4/information-architecture/6.png)

**Diagram 7: Process completion and logout**
![](../src/images/chapter4/information-architecture/7.png)

**General diagram: Complete platform user flow view**
![](../src/images/chapter4/information-architecture/ALL.png)

## 4.5. Web Applications Prototyping

[https://www.figma.com/design/nV0UrH5YsFXu9run93EmRm/GlassGo?node-id=0-1\&t=2SDCRONXUcQzrQsj-1](https://www.figma.com/design/nV0UrH5YsFXu9run93EmRm/GlassGo?node-id=0-1&t=2SDCRONXUcQzrQsj-1)

## 4.6. Domain-Driven Software Architecture

Domain-Driven Design (DDD) focuses on modeling the system based on key business processes: secure transport of liquor in glass containers, shipment traceability, and transport condition monitoring. This approach allows each part of the software to faithfully reflect business logic, facilitating scalability and maintenance of GlassGo, RPG startup's main product.

### 4.6.1. Design-Level EventStorming

![](../src/images/chapter4/information-architecture/GlassGo%20-%20EventStorming%20(1).jpg)

### 4.6.2. Software Architecture Context Diagram

* Person:
  * **Carrier:** Drives the truck and uses mobile app to view routes, record trip start/end, and receive impact alerts.
  * **Distributor:** Supervises shipments from offices. Reviews web dashboard, downloads reports.
  * **Business Owner:** End customer who wants to know if their order will arrive on time and unbroken.
  * **RPG Administrator:** Startup staff for internal management, support, and maintenance.
* Software System:
  * **GlassGo:** Central system offering traceability, route optimization, and monitoring.
  * **Google Maps:** Platform providing a REST API for geo-referential information.
  * **PayPal:** Payment gateway for membership charges.
  * **Twilio:** Notification service for sending SMS, emails, or push notifications.

![context-diagram](../src/images/chapter4/domain-driven-software-arquitecture/context-diagram.png)

### 4.6.3. Software Architecture Container Diagrams

* Container:
  * **Mobile App:** Mobile application
  * **Landing Page:** Landing page
  * **Web App:** Web application
  * **API REST:** REST API for data access and business logic
  * **DB:** Relational database

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

Object-Oriented Design focuses on the logical structure of the GlassGo domain, using UML class diagrams to define entities, services, and their relationships. Each diagram represents how classes interact within a bounded context, encapsulating attributes and methods coherent with their responsibilities.

### 4.7.1. Class Diagrams

**Specific Views by Bounded Context**

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

The database design defines the relational structure used by the GlassGo system to ensure data persistence and integrity across all bounded contexts.

### 4.8.1. Database Diagrams

* **Global View:**
  ![global-view](../src/images/chapter4/database-design/global-view.png)

* **Every Bounded Context's view:**

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
