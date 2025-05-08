# Final-Report

# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management.

En la siguiente sección, detallaremos las herramientas, convenciones, referencias y configuraciones empleadas a lo largo del desarrollo del proyecto, que contribuyeron a mantener la consistencia en el trabajo realizado.

### 5.1.1. Software Development Environment Configuration.

En este apartado, se van a mencionar los distintos productos de software empleados por el equipo de desarrollo, para llevar acabo las actividades relacionadas con la elaboración del proyecto.

**Project Management:**

1. **Discord: https://discord.com/** Aunque originalmente su uso es mas para la comunidad de gamers para comunicarse entre ellos, Discord también se puede utilizar para mejorar la experiencia del usuario a travez de diferentes lugares de comunicación, fijar mensajes, diferentes canales de texto y actividad de los integrantes del grupo.

2. **WhatsApp: https://web.whatsapp.com/** WhatsApp es una aplicación de mensajería instantánea que se utiliza para la comunicación en tiempo real. Aunque no es una herramienta de gestión de proyectos, se puede utilizar para mantener en contacto con los miembros del equipo. 

**Requirements Managemnts:**

1. **Trello: https://trello.com/** Es un software de gestión de proyectos, que facilita asignar y organizar las tareas a realizar. 


**Product UX/UI Design**

1. **Figma: https://www.figma.com/** Figma es una herramienta de edición gráfica, en donde se puede diseñar y prototipar páginas web. Se utilizó para crear los wireframes, mock-ups del proyecto

2. **UXPressia: https://uxpressia.com/** Es una herramienta en línea que permite a los equipos de trabajo identificar y comprender los problemas, necesidades y comportamiento del usuario, lo utilizamos para realizar el Empathy Map, Journey Map, Impact Map

3. **Miro: https://miro.com/es/** Es una plataforma colaborativa el cual permite crear y usar pizarras digitales personalizadas en tiempo real. Lo utilizamos para la creación del As-is y To-Be scenario map.

**Software Development:**

1. **Landing Page:** Para la creación de la landing page, se utilizaron las tecnologias base del desarrollo web: HTML5, CSS3 y JavaScript, Tambien se usó ReactJs y el framework Tailwindcss para facilitar el desarrollo del proyecto.

**Software Documentation:**

1. **GitHub: https://github.com/** GitHub es una plataforma de desarrollo colaborativo que utiliza el sistema de control de versiones Git. Se utiliza para alojar, revisar y colaborar en proyectos de desarrollo de software, lo que facilita la colaboración entre desarrolladores.

2. **LucidChart: https://lucid.app/** LucidChart es una plataforma que cuenta con opciones para la creación de diagramas, mapas mentales, flujos y más, con el uso de plantillas y tableros con edición en tiempo real. Fue utilizado en el desarrollo del diagrama de clases UML

3. **Structurizr: https://www.structurizr.com/** Es una plataforma que permite modelado de diagramas de arquitectura de software por medio de código. Structurizr fue utilizado para crear el modelo C4 de nuestro proyecto.


### 5.1.2. Source Code Management.

El manejo y organización del trabajo se llevaron a cabo mediante una organización en Github Organización: https://github.com/SI730-SW53-OpenSource-Grupo5 Landing Page Repository: https://github.com/SI730-SW53-OpenSource-Grupo5/LandingPage-ConnectionLink.git 

Asimismo, para llevar a cabo un mejor control de cómo crear ramas y realizar cambios en el código fuente, se procedió a utilizar GitFlow.

De este modo, se tenían 2 ramas principales: main y development.

* main: En esta rama almacenaremos las versiones oficiales de nuestro repositorio que ya deben pasar a producción.
* development: Esta rama se utilizará como rama de integración para las “feature” branches. Una vez alcance un estado estable y el equipo lo considere listo para ser lanzado, se unirá a la rama main.
  
**Commit Conventions:**    
El formato de nuestros commits sigue la estructura de los “Conventional Commits” en su versión 1.0.0 (https://www.conventionalcommits.org/en/v1.0.0/) con el objetivo de proporcionar una lectura sencilla de los mismos. Por ello seguimos el siguiente formato: "< type>[optional scope]: < description>" Donde:

* type: Especifica el tipo de cambio realizado, únicamente puede ser feat, fix, update, etc.
* scope: Es el alcance que tiene nuestro commit.
* description: Es un breve resumen de los cambios de código.

### 5.1.3. Source Code Style Guide & Conventions.
En el proyecto hemos hecho uso de algunas convenciones y guia de estilos para el desarrollo del Landing Page.

**React:**

   + Componentes: Se fomenta la creación de componentes para mantener un código limpio y modularizado.
   + Nomenclatura Descriptiva: Utilizamos nombres descriptivos para que se pueda entender cual es su función dentro de la página.
   + Estado y Props: Hacemos uso de los estados y props para pasar datos entre componentes y tener una página reactiva.

**Tailwind CSS:**
   + Clases Utilitarias: Usamos las clases proporcionadas por Tailwind para darle estilos a los elementos de forma eficiente.

**General:**
   + Estructura de Carpetas Organizadas: Mantenemos una estructura de carpetas organizadas para los archivos de React, facilitando así la navegación y entendimiento del proyecto. 

**Git:**
   + Ramas Descriptivas: Utilizamos  nombres de ramas descriptivas para una gestión eficiente del código y las versiones.
   + Flujo de Trabajo Colaborativo: Hacemos uso de ramas para el desarrollo colaborativo.


### 5.1.4. Software Deployment Configuration.

En esta entrega, hemos finalizado nuestra Landing Page y configurado su despliegue de la siguiente manera:

Repositorio GitHub: El código de la Landing Page está alojado en un repositorio específico dentro de nuestra comunidad pública en GitHub.

Vercel: Utilizamos la aplicación Vercel para desplegar la página. Esto nos permite una visualización clara y accesible para los usuarios.

Esta configuración nos brinda un método eficiente y transparente para el despliegue de nuestro proyecto, asegurando una experiencia óptima para nuestros usuarios.

## 5.2. Landing Page, Services & Applications Implementation.

### 5.2.1. Sprint 1

El primer sprint es una etapa importante en nuestro marco de gestión de proyectos de metodología ágil Scrum. En este periodo, agendamos reuniones con el objetivo de conocer mejor las características de cada integrante, y delegamos tareas para materializar el diseño y funcionalidades ya establecidas, para transformarlos en un landing page funcional y que cumple las heurísticas.

#### 5.2.1.1. Sprint Planning 1.

| Sprint 1                   | Implementación de funcionalidades y diseño de la aplicación.                                                                                                                                           |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sprint Planning Background |                                                                                                                                                                                                        |
| Date                       | 10/04/2025                                                                                                                                                                                             |
| Time                       | 20:00                                                                                                                                                                                                  |
| Location                   | Reunión realizada en Discord                                                                                                                                         |
| Prepared By                |                                                                                                  Eddo Su Caletti                                              |
| Attendees                  |  Alexander Paolo Justo Yauricasa, Carlos De La Cruz Villarreal, Miguel Angel Vidal Castro, Fabian Alonso Reyes Trujillano, Ariana Ramirez Carrasco |
| Sprint Goal & User Stories |                                                                                                                                                                                                        |
  | Sprint 1 Goal              | Implementar y desplegar la landing page implica desarrollar una versión funcional basada en los diseños aprobados, integrando elementos clave como formularios, llamados a acción y seguimiento analítico.                                                                                                                                                                |
| Sprint 1 Velocity          |                                                 35               |
| Sum of Story Points        |                                                       30            |

#### 5.2.1.2. Sprint Backlog 1.

| Id   | Title            | Id   | Title                           | Description                                                                           | Estimations (Hours) | Assigned To                       | Status |
|------|------------------|------|---------------------------------|---------------------------------------------------------------------------------------|---------------------|-----------------------------------|--------|
| CC01 | Toolbar     | C01  | Barra de ayuda | Desarrollo de la barra superior para ayudar al usuario a encontrar secciones. | 3                   |      | Done   |
| CC02 | Button component | C02  | Button Design responsive        | Desarrollo e implementación de los estilos que corresponden al Button                 | 2                   |  | Done   |
| CC03 | Navbar component | C03  | Sección Navbar responsive       | Desarrollo e implementación de los estilos que corresponden a la sección Navbar       | 3                   |  | Done   |
| CC04 | Contact          | C04  | Sección Contact responsive      | Desarrollo e implementación de los estilos que corresponden a la sección Contact      | 3                   |   | Done   |
| CC05 | Footer           | C05  | Sección Footer responsive       | Desarrollo e implementación de los estilos que corresponden a la sección Footer       | 2                   |   | Done   |
| CC06 | Service          | C06  | Sección Service responsive      | Desarrollo e implementación de los estilos que corresponden a la sección Service      | 2                   |              | Done   |
| CC07 | Prices           | C07 | Sección Prices responsive       | Desarrollo e implementación de los estilos que corresponden a la sección Prices       | 2                   |        | Done   |
| CC08 | Register           | C08 | Sección Register       | Desarrollo e implementación los estilos que corresponden a la seccion Register       | 2                   |        | Done   |
| CC09 |  Button translator	          | C09 | Sección Button translator       | Desarrollo e implementación los estilos que corresponden a la seccion Button translator       | 4                   |        | Done   |

<img src="./assets/Trello.png" alt="Captura Sprint 1 en Trello" width="80%">
   
Link del trello: https://trello.com/b/E7ZyFdYk/vitameet

#### 5.2.1.3. Development Evidence for Sprint Review.

| Repository                 | Branch                   | Commit ID | Commit Message                                                                      | Commit Message Body | Commited On(Date) |
|----------------------------|--------------------------|-----------|-------------------------------------------------------------------------------------|---------------------|-------------------|
| Landing-Page | feature/start           |  6e1825098a9bb126828c89d3b7cd97a21aa0c9db  | feat: add files                                                                   | -                   | 27/04/2025        |
| Landing-Page | feature/animation          |  dbbde2c86106f3706e411b2abe7d1aa9cd727370  | feat(animation): group commit, added animations                                                                  | -                   | 27/04/2025        |
| Landing-Page | feature/colors           |  6caee6df6b32fe8659ac33c75f0c31341ff4e19a  | Add files via upload                                                                | -                   | 27/04/2025        |
| Landing-Page | feature/landing |  c31a8045ab6c04ce81b33465eb0802358323cda2  | feat: add landing                | -                   | 27/04/2025        |
| Landing-Page | feature/login    |  e09522ac580d84b9f1be39fbdb172e1b33a1ebc5  | feat:add login landing page Styles  <br> Add images login| -                   | 27/04/2025        |
| Landing-Page | feature/     |    |  | -                   | 27/04/2025        |


#### 5.2.1.4. Testing Suite Evidence for Sprint Review.



| Repository          | Branch | Commit ID                                | Commit Message                     | Commit Message (Body) | Committed on (Date) |
|---------------------|--------|------------------------------------------|------------------------------------|-----------------------|---------------------|
| Acceptance-Test     | main   | c31a8045ab6c04ce81b33465eb0802358323cda2 | Initial commit                     | -                     | 13/04/2025          |
| Acceptance-Test     | main   | 6e1825098a9bb126828c89d3b7cd97a21aa0c9db | feat: Added us-16 acceptance test  | -                     | 27/04/2025          |
| Acceptance-Test     | main   | dbbde2c86106f3706e411b2abe7d1aa9cd727370 | feat: Added us-17 acceptance test  | -                     | 27/04/2025          |
| Acceptance-Test     | main   | 6caee6df6b32fe8659ac33c75f0c31341ff4e19a | feat: Added us-18 acceptance test  | -                     | 27/04/2025          |
| Acceptance-Test     | main   | e09522ac580d84b9f1be39fbdb172e1b33a1ebc5 | feat: Added us-19 acceptance test  | -                     | 27/04/2025          |
| Acceptance-Test     | main   | cd8cc231ff1973cbffd9adec1839191a5d98ea62 | feat: Added us-20 acceptance test  | -                     | 27/04/2025          |

#### 5.2.1.5. Execution Evidence for Sprint Review.

<img src="./assets/landing.png" alt="Captura landingPage" width="100%"><br/>

**Enlace a la página:** 

#### 5.2.1.6. Services Documentation Evidence for Sprint Review.

En este sprint 1, los miembros del equipo lograron completar satisfactoriamente todas las tareas propuestas. Este sprint estuvo enfocado principalmente en el desarrollo del landing pague. A lo largo del desarrollo, se realizaron múltiples correcciones a errores presentes en el código, lo que permitió mejorar.
- En el mundo de la programación una landing page es esencial para convertir visitantes en clientes, ya que está diseñada estratégicamente para guiar al usuario hacia una acción específica (como comprar, registrarse o descargar). A diferencia de un sitio web general, enfoca todo el contenido en un único objetivo, eliminando distracciones y optimizando la experiencia del usuario. Con elementos clave como un titular persuasivo, beneficios claros, testimonios y un llamado a la acción (CTA) destacado, aumenta significativamente las tasas de conversión y el retorno de inversión (ROI) de campañas de marketing.

#### 5.2.1.7. Software Deployment Evidence for Sprint Review.

Para este sprint presentado de la landing page se optó por varias herramientas para su desarrollo y despliegue en la web de manera pública.

* Git: Se utilizó para el control de versiones del código fuente.
* GitHub: Se utilizó para crear el repositorio de la landing page, donde se subió el código fuente.


#### 5.2.1.8. Team Collaboration Insights during Sprint.

Para documentar los avances de este Sprint, utilizamos GitHub. Uno de los integrantes del equipo configuró el repositorio inicial, generando múltiples ramas que permitieron trabajar en paralelo sin afectar el progreso de los demás. Clonamos el repositorio localmente con Git, implementamos los cambios necesarios y los subimos a GitHub. Al finalizar, registramos todas las modificaciones, las cuales quedarán disponibles en el repositorio para su revisión.

<br/><img src="./assets/IssuesGithub.png" alt="Imagen" width="100%"><br/>

<img src="./assets/Network.png" alt="Imagen" width="100%"><br/>

