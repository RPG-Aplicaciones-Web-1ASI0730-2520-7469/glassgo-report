# **Chapter IV: Product Design**
## **4.1. Style Guidelines**

  <p style="text-align: justify;">
    A style guidelines is a set of rules and standards that define how documents, web content, and software should be written, designed, and presented. Below are the specifications of the parameters implemented in the project structure.
  </p>

### **4.1.1. General Style Guidelines**

- **Branding History**
  <p style="text-align: justify;">
    For the creation of our GlassGo product logo, we opted for a modern and minimalist design that reflects the application's intentions. The logo consists of elegant and simple typography, accompanied by an icon that symbolizes rapid efficiency and product durability during shipping, along with an honest and encouraging phrase. Displaying colors that demonstrate security, speed, and balance such as white, gray, green, orange, and blue.
  </p>

  <p align="center">
    <img src="../src/images/general/Logos_type.png" width="50%">
  </p>

- **Typography**
  <p style="text-align: justify;">
    For our GlassGo product typography, we chose modern and minimalist fonts that reflect the application's intentions. The typography consists of elegant and simple fonts, complementing the icon that symbolizes rapid efficiency and product durability during shipping, along with an honest and encouraging message. The typography uses colors that demonstrate security, speed, and balance including white, gray, green, orange, and blue.
  </p>

  <p align="center">
      <img src="../src/images/general/Letter.png" width="25%">
      <img src="../src/images/general/Letter2.png" width="25%">
  </p>


- **Colors**
  <p style="text-align: justify;">
    GlassGo's color palette consists of tones that convey trust, speed, and professionalism - essential values for a brand focused on secure product delivery. The primary blue reflects stability and security, while orange adds dynamism and movement, reinforcing the idea of immediacy. The neutral gray balances and adds sobriety, ensuring clear and professional communication.
  </p>
  
  - Blue → *#002140*
  - Medium Gray → *#6B6B6B*
  - White → *#FFFFFF*
  - Black → *#000000*

  <p align="center">
    <img src="../src/images/general/Blue.png" width="24%">
    <img src="../src/images/general/Gris.png" width="24%">
    <img src="../src/images/general/White.png" width="24%">
    <img src="../src/images/general/Black.png" width="24%">
  </p>

- **Spacing**

  <p style="text-align: justify;">
    GlassGo's color palette consists of tones that convey trust, speed, and professionalism - essential values for a brand focused on secure product delivery. The primary blue reflects stability and security, while orange adds dynamism and movement, reinforcing the idea of immediacy. The neutral gray balances and adds sobriety, ensuring clear and professional communication.
  </p>

  <p align="center">
    <img src="../src/images/general/(image).png" width="25%">
  </p>

### **4.1.2. Web Style Guidelines**

<p style="text-align: justify;">
  For GlassGo, we are planning to develop a web platform. Therefore, we will implement a responsive design (known as Web Responsive Design) with the goal of optimizing information presentation on any device. This will ensure that the content remains intact and ultimately enhance the user experience.
</p>

<p style="text-align: justify;">
  As a team, we have chosen to incorporate the F-pattern design in our website. This pattern is especially suitable for GlassGo, as users tend to explore content quickly and prioritize information at the top and left of the screen. This helps highlight relevant data from the start and facilitates reading of key sections.
</p>

## **4.2. Information Architecture**
### **4.2.1. Organization Systems**

- **Main Menu**

  | **Topic** | **Definition** |
  | :---: | ----- |
  | Home page | The homepage can display an overview of the service and highlight key features. |
  | Log in | The page where users can log into their session. If they don't have an account, there's a section to register for free in the web service. |
  | Technical support | The page provides a space for users to share their questions, technical assistance, or complaints about the system. |

- **Subscription Page**

  | **Topic** | **Definition** |
  | :---: | ----- |
  | Transport Company Plan | Plan for companies seeking a partnership with a distributor. Benefits include: preferential rates, advanced reports, and priority support. |
  | Finished Goods Distributor Plan | Plan for distributors seeking a logistics solution to properly manage their resources. |
  | Market Plan | Individual plan for common businesses such as restaurants, bars, and liquor stores. |

- **Login Page**

  | **Topic** | **Definition** |
  | :---: | ----- |
  | Registration and Authentication | Plan for companies seeking a partnership with a distributor. Benefits include: preferential rates, advanced reports, and priority support. |

- **Other Pages and Functions**

  | **Topic** | **Definition** |
  | :---: | ----- |
  | User Profile | The homepage can display an overview of the service and highlight key features. |
  | Settings | The page where users can log into their session. If they don't have an account, there's a section to register for free. |
  | About Us | The page provides a space for users to share their questions, technical assistance, or complaints. |
  | Navigation Bar | A clear and consistent navigation bar at the top of each page facilitates navigation between main sections. |
  | Responsive Design | The application must be easy to use on both desktop and mobile devices, adapting the user interface to screen size. |

### **4.2.2. Labeling Systems**

<p style="text-align: justify;">
  For labeling systems, we have chosen to organize content through headers that group sections users can access. This way, users know where to click to access the corresponding sections.
</p>

| **Topic** | **Definition** |
| :---: | ----- |
| Home page | Main section users will reach when entering the web application link. |
| Subscription | In this section, users can view available plans and rates. |
| Technical support | This section provides users with all channels through which they can contact us. |

### **4.2.3. SEO Tags and Meta Tags**

- **Landing Page**

  - **Charset:**

    <p style="text-align: justify;">
      Tells the browser how to interpret text characters. By specifying UTF-8, it ensures GlassGo's landing page correctly displays accents, special characters, and symbols, ensuring proper visualization in any language.
    </p>

    ```html
    <meta charset="utf-8">
    ```

  - **Viewport *(responsive)*:**

    <p style="text-align: justify;">
      Allows the page to adapt to different devices (mobile, tablet, PC), ensuring GlassGo's presentation is legible and optimal on any screen.
    </p>

    ```html
    <meta name="viewport" content="width=device-width, initial-scale=1">
    ```

  - **Title *(SEO)*:**

    <p style="text-align: justify;">
      Defines the title that will appear in the browser tab and search results. Its function is to provide a clear and concise description of GlassGo's main service.
    </p>

    ```html
    <title> GlassGo | Secure Transport and Glass Shipment Traceability </title>
    ```

  - **Meta description:**

    <p style="text-align: justify;">
      Provides a brief summary that will appear in search results. Its goal is to attract users interested in sustainable logistics and secure transport solutions.
    </p>

    ```html
    <meta name="description" content="GlassGo provides secure transport and glass shipment traceability. Reduces losses, ensures product integrity, and improves logistics efficiency.">
    ```

  - **Meta keywords *(SEO, deprecated for Google)*:**
    
    <p style="text-align: justify;">
      Identifies keywords related to GlassGo's service. Although its impact is currently limited, it remains useful for basic indexing systems.
    </p>
    
    ```html
    <meta name="keywords" content="glass transport, sustainable logistics, traceability, secure distribution, fast shipping, GlassGo">
    ```

  - **Meta Authors:**

    <p style="text-align: justify;">
      Attributes landing page content authorship to the GlassGo project team.
    </p>

    ```html
    <meta name="author" content="GlassGo Team">
    ```

  - **Meta robots:**
    
    <p style="text-align: justify;">
      Allows search engines to index GlassGo's page and follow its links, ensuring greater visibility.
    </p>
    
    ```html
    <meta name="robots" content="index, follow">
    ```

  - **Meta Language:**

    <p style="text-align: justify;">
      Indicates the landing's content is in English, optimizing its indexation and browser compatibility.
    </p>

    ```html
    <meta name="language" content="en">
    ```

  - **Meta copyright:**

    <p style="text-align: justify;">
      Indicates copyright ownership of the landing's content and design.
    </p>

    ```html
    <meta name="copyright" content="GlassGo 2025">
    ```

### **4.2.4. Searching Systems**

<p style="text-align: justify;">
  The search engine is fundamental for users to quickly find specific details.
</p>

- **Key Features:**

  <p style="text-align: justify;">
    The objective-based searches will allow business owners, carriers, and distributors to:
  </p>

  - Identify impacts on cargo in the last 24 hours
  - Anticipate routes with high incident rates during transit, saving this information so other carriers can handle with caution
  - Generate evidence if a claim is made by the customer or supplier
  - Verify cargo status before acceptance
  - Tag high-priority inventory during peak seasons
  - Consult transport history to prevent possible cargo breakage

### **4.2.5. Navigation Systems**

<p style="text-align: justify;">
  The Navigation System is the structure that allows users to efficiently move between different sections and pages of the application.
</p>

- **Navigation Structure:**
  - Logo - link to Homepage
  - Homepage - summary / landing with benefits and CTA
  - Solutions - pages by segment
    - Carriers
    - Distributors
    - Businesses *(Business Owners*)
  - Subscriptions — plan and price comparison
  - Support — Help Center, FAQ, contact
  - Contact — contact/sales form
  - Search — global search field
  - Log In / Sign Up button *(right)*

## **4.3. Landing Page UI Design**
### **4.3.1. Landing Page Wireframe**

- **Wireframe 1: Landing page overview**

  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/wireframes/wireframe-1.png" width="60%">
  </p>

- **Wireframe 2: Header and main menu**

  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/wireframes/wireframe-2.png" width="60%">
  </p>

- **Wireframe 3: Benefits and features section**

  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/wireframes/wireframe-3.png" width="60%">
  </p>

- **Wireframe 4: Services details**

  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/wireframes/wireframe-4.png" width="60%">
  </p>

- **Wireframe 5: Registration and subscription process**

  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/wireframes/wireframe-5.png" width="60%">
  </p>

- **Wireframe 6: Testimonials and success stories**

  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/wireframes/wireframe-6.png" width="60%">
  </p>

- **Wireframe 7: FAQ and support**

  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/wireframes/wireframe-7.png" width="60%">
  </p>

- **Wireframe 8: Footer and contact links**

  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/wireframes/wireframe-8.png" width="60%">
  </p>

### **4.3.2. Landing Page Mock-up**

- **Mockup 1: Landing page main view**

  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/mockups/mockup-1.png" width="60%">
  </p>

- **Mockup 2: Header with navigation menu**
  
  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/mockups/mockup-2.png" width="60%">
  </p>

- **Mockup 3: Benefits and value proposition section**
  
  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/mockups/mockup-3.png" width="60%">
  </p>

- **Mockup 4: Services and features details**
  
  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/mockups/mockup-4.png" width="60%">
  </p>

- **Mockup 5: Registration and subscription process**
  
  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/mockups/mockup-5.png" width="60%">
  </p>

- **Mockup 6: Testimonials and success stories**

  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/mockups/mockup-6.png" width="60%">
  </p>

- **Mockup 7: FAQ and support**

  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/mockups/mockup-7.png" width="60%">
  </p>

- **Mockup 8: Footer with contact links**

  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/mockups/mockup-8.png" width="60%">
  </p>

- **Mockup 9: Responsive view on mobile devices**

  <p align="center">
    <img src="../src/images/chapter4/landing-page-ui/mockups/mockup-9.png" width="60%">
  </p>

## **4.4. Web Applications UX/UI Design**

<p style="text-align: justify;">
  The user experience (UX) and user interface (UI) design of our landing page aims to offer clear, attractive, and simple digital interaction for visitors. UX focuses on understanding what users seek and expect, organizing information and navigation flows to make the journey comfortable and efficient. UI, on the other hand, deals with the visual aspect, such as the layout of elements, buttons, menus, and content presentation. By combining both approaches, we will achieve a design that is not only aesthetically pleasing but also functional and easy to use, generating a positive experience that motivates users to become interested in our product.
</p>

### **4.4.1. Web Applications Wireframes**

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/sign-in.png" width="60%">
  </p>
  
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/sign-in-google.png" width="60%">
  </p>
  
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/sign-up.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/sign-up-loading.png" width="60%">
  </p>
     
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/recover-password.png" width="60%">
  </p>
  
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/select-user-role.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/register-complete.png" width="60%">
  </p>

- **Segment 1: Truck Transport Companies**
  
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s1-order-requests.png" width="60%">
  </p>
  
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s1-clients.png" width="60%">
  </p>
    
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s1-tracking.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s1-stock-management.png" width="60%">
  </p>
    
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s1-calendar.png" width="60%">
  </p>
    
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s1-reports.png" width="60%">
  </p>
    
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s1-shipping-history.png" width="60%">
  </p>
    
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s1-claims-log.png" width="60%">
  </p>
    
- **Segment 2&3: Liquor Distributors and Business Owners**

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s2,3-home.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s2,3-create-order.png" width="60%">
  </p>


  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s2,3-tracking.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s2,3-inventory.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s2,3-calendar.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s2,3-reports.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s2,3-history.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireframes/s2,3-claims.png" width="60%">
  </p>

### **4.4.2. Web Applications Wireflow Diagrams**

  <p style="text-align: justify;">
    Wireflow diagrams are graphical representations that combine wireframe structure with flowchart logic, showing how users interact and move within a web application. These diagrams allow visualization of the navigation experience, detect potential usability frictions, and design more fluid and efficient user journeys.
  </p>

  <p style="text-align: justify;">
    The diagrams encompass inventory management, shipment tracking, delivery calendar usage, report generation, and claims management. This way, the diagram provides a comprehensive view of the platform, ensuring a clear, organized experience aligned with each user's needs.
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/wireflow-diagrams/wireflow-diagram.png" width="60%">
  </p>
  
  > [Wireflow - GlassGo](https://lucid.app/lucidchart/1d76ffac-1618-4b03-a28f-a5a840f67ac7/edit?viewport_loc=-12591%2C-6613%2C22617%2C11070%2C0_0&invitationId=inv_592714f1-7efd-4777-8053-5ed7aae18f41)

### **4.4.3. Web Applications Mock-ups**

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/sign-in.png" width="60%">
  </p>
  
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/sign-in-google.png" width="60%">
  </p>
  
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/sign-up.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/sign-up-loading.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/recover-password.png" width="60%">
  </p>
  
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/select-user-role.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/register-complete.png" width="60%">
  </p>

- **Segment 1: Truck Transport Companies**
  
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s1-order-requests.png" width="60%">
  </p>
  
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s1-clients.png" width="60%">
  </p>
    
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s1-tracking.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s1-stock-management.png" width="60%">
  </p>
    
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s1-calendar.png" width="60%">
  </p>
    
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s1-reports.png" width="60%">
  </p>
    
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s1-shipping-history.png" width="60%">
  </p>
    
  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s1-claims-log.png" width="60%">
  </p>
    
- **Segment 2&3: Liquor Distributors and Business Owners**

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s2,3-home.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s2,3-create-order.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s2,3-tracking.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s2,3-tracking-complete.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s2,3-inventory.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s2,3-calendar.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s2,3-reports.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s2,3-history.png" width="60%">
  </p>

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/mockups/s2,3-claims.png" width="60%">
  </p>

### **4.4.4. Web Applications User Flow Diagrams**

- **Diagram 1: Platform user flow start**

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/userflow-diagrams/userflow-1.png" width="60%">
  </p>

- **Diagram 2: Authentication and access process**

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/userflow-diagrams/userflow-2.png" width="60%">
  </p>

- **Diagram 3: Main panel navigation**

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/userflow-diagrams/userflow-3.png" width="60%">
  </p>

- **Diagram 4: Order management and visualization**

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/userflow-diagrams/userflow-4.png" width="60%">
  </p>

- **Diagram 5: Shipment and route tracking**

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/userflow-diagrams/userflow-5.png" width="60%">
  </p>

- **Diagram 6: Incident registration and management**

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/userflow-diagrams/userflow-6.png" width="60%">
  </p>

- **Diagram 7: Process completion and logout**

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/userflow-diagrams/userflow-7.png" width="60%">
  </p>

- **General diagram: Complete platform user flow view**

  <p align="center">
    <img src="../src/images/chapter4/web-applications-ui/userflow-diagrams/userflow-diagram.png" width="60%">
  </p>

## 4.5. Web Applications Prototyping

  > [Prototyping - GlassGo](https://www.figma.com/design/nV0UrH5YsFXu9run93EmRm/GlassGo?node-id=0-1&t=2SDCRONXUcQzrQsj-1)

## 4.6. Domain-Driven Software Architecture

Domain-Driven Design (DDD) focuses on modeling the system based on key business processes: secure transport of liquor in glass containers, shipment traceability, and transport condition monitoring. This approach allows each part of the software to faithfully reflect business logic, facilitating scalability and maintenance of GlassGo, RPG startup's main product.

### 4.6.1. Design-Level EventStorming
* global vision

  ![event_storming_global](../src/images/chapter4/information-architecture/GlassGo%20-%20EventStorming%20(1).jpg)

* Specific Views by Bounded Context:
  * **Identity Access**

  ![identity_&_access_management](../src/diagrams/eventstorming/design-level/Identity_Access_Management.png)

  * **Profiles Preferences**

  ![profile_&_preferences](../src/diagrams/eventstorming/design-level/Profile_Preferences.png)

  * **Payments Subscriptions**

  ![payments_&_subscriptions](../src/diagrams/eventstorming/design-level/Payments_Subscriptions.png)

  * **Service Planning**

  ![service_planning](../src/diagrams/eventstorming/design-level/Service_Planning.png)

  * **Service Execution**

  ![service_execution_&_monitoring](../src/diagrams/eventstorming/design-level/Service_Execution_Monitoring.png)

  * **Dashboard Analytics**

  ![dashboard_&_analytics](../src/diagrams/eventstorming/design-level/Dashboard_Analytics.png)

  * **Loyalty Engagement**

  ![loyalty_&_engagement](../src/diagrams/eventstorming/design-level/Loyalty_Engagement.png)

  * **System Administration**

  ![system_administration](../src/diagrams/eventstorming/design-level/System_Administration.png)

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
