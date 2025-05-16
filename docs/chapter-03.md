# Capítulo III: Requirements Specification

## 3.1. To-Be Scenario Mapping.

Segmento 1: Personas adultas que necesitan atención médica

<img src="../assets/TBSM-paciente.jpg" alt="TBSM paciente" height="500" />

Segmento 2: Médicos generales y especialistas con experiencia

<img src="../assets/TBSM-medico.jpg" alt="TBSM medico" height="500" />


## 3.2. User Stories.
| Epic/Story ID | Titulo | Descripción | Criterios de Aceptación | Relacionado con (Epic ID)|
|-------|-----------------|----------------------------|----------------------------------------|---------|
| US01 | Registrar usuario | Como visitante del segmento objetivo médico/paciente Quiero registrar mi cuenta Para hacer uso de la aplicación. | Escenario 1: Visitante del segmento objetivo médico/paciente ingresa credenciales válidas. <br> Dado que el visitante del segmento objetivo médico/paciente desee crear una cuenta personal en la aplicación Cuando ingrese las credenciales de una cuenta inexistente en la base de datos y una contraseña que cumple con todos los requisitos de seguridad, y acepte los términos y condiciones de uso Entonces se creará la cuenta del médico. <br> Escenario 2: Visitante ingresa credenciales incorrectas. <br> Dado que el visitante del segmento objetivo médico/paciente ingresa credenciales de una cuenta ya existe  Cuando ingrese una dirección de correo electrónico o contraseña que no cumplen con los requisitos especificados Entonces se le denegará la operación | EP01 |
| US02 | Iniciar sesión | Como usuario del segmento objetivo médico/paciente registrado Quiero iniciar sesión Para acceder a mi cuenta. | Escenario 1: Inicio de sesión exitoso <br> Dado que soy un médico/paciente registrado Cuando ingreso mi nombre de usuario y contraseña Entonces debería acceder a mi cuenta. <br> Escenario 2: Inicio de sesión erróneo <br> Dado que soy un médico/paciente registrado Cuando ingreso mi nombre de usuario o contraseña incorrecto Entonces saldrá en pantalla una mensaje "Usuario o contraseña incorrecto" | EP01 | 
| US03 | Olvidar contraseña | Como usuario del segmento objetivo médico/paciente Quiero restablecer mi contraseña si la olvido Para poder acceder a mi cuenta. | Escenario 1:  Restablecimiento exitoso <br> Dado que el médico/paciente ha olvidado su contraseña Cuando ingreso un correo válido en el formulario de recuperación para restablecerla Entonces debería recibir un enlace para crear una nueva contraseña. <br> Escenario 2:  Error por correo inválido <br> Dado que el médico/paciente he olvidado su contraseña Cuando ingrese un correo inválido para restablecerla Entonces aparecera un mensaje "Correo inválido" | EP01 |
| US04 | Historial del paciente | Como médico  Quiero consultar el historial clínico de un paciente registrado Para conocer antecedentes y brindar mejor atención | Escenario 1: Visualización exitosa del historial <br> Dado que soy un médico autenticado en la aplicación Cuando accedo al perfil de un paciente y selecciono “Ver historial” Entonces debería mostrarse una lista de diagnósticos, citas o tratamientos anteriores.<br> Escenario 2: Paciente sin historial registrado<br>Dado que soy un médico autenticado Cuando accedo al perfil de un paciente sin historial Entonces debería mostrarse un mensaje que indique “Este paciente aún no tiene historial clínico registrado”.  | EP02 | 
| US05 | Cancelar  una cita | Como médico Quiero poder cancelar  una cita médica Para gestionar mi agenda y evitar conflictos con otros compromisos | Escenario 1: Cancelación exitosa de cita <br> Dado que soy un médico Cuando selecciono una cita y elijo la opción “Cancelar” Entonces la cita debería marcarse como cancelada y el paciente recibir una notificación.| EP02 | 
| US06 | Ver citas médicas | Como médico Quiero visualizar la lista de mis citas médicas programadas durante el día Para organizar mi agenda y prepararme para atender a los pacientes | Escenario : visualización exitosa <br> Dado que soy un médico en la plataforma Cuando ingreso a la sección “Mis citas” Entonces debería mostrarse un listado con las citas del día ordenadas por hora.| EP02 |
| US07 | Notificar a los pacientes | Como médico Quiero enviar una notificación al paciente sobre su cita programada Para ayudarle a recordar y evitar que falte a la consulta médica | Escenario :  Envío de notificación exitoso <br> Dado que soy un médico  Cuando selecciono una cita próxima y elijo “Enviar recordatorio” Entonces el paciente debería recibir un mensaje con la fecha, hora y nombre del médico.| EP02 |
| US08 | Consultar horario | Como paciente Quiero consultar los horarios disponibles de un médico Para elegir una fecha y hora conveniente para agendar mi cita médica | Escenario : Visualización de disponibilidad <br> Dado que soy un paciente autenticado Cuando selecciono un médico en la plataforma Entonces debería mostrarse un calendario con los días y horarios disponibles para citas. | EP03 |
| US09 | Filtrar búsqueda de médicos | Como paciente Quiero filtrar médicos por especialidad Para encontrar fácilmente al profesional adecuado para agendar mi cita | Escenario: Filtro exitoso de médicos <br> Dado que soy un paciente Cuando accedo a la opción de agendar una cita y aplico filtros Entonces debería mostrarse una lista de médicos que coincidan con los criterios seleccionados . | EP03 | 
| US10 | Detalles de la cita | Como paciente Quiero ver los detalles completos de una cita médica agendada Para saber las características y detalles de la cita| Escenario : Visualización de detalle exitosa <br> Dado que soy un paciente autenticado Cuando selecciono una cita de mi historial o lista de próximas citas Entonces debería mostrarse el nombre del médico, la especialidad, la fecha y hora de la cita, el lugar de atención. | EP03 | 
| US11 | Pagar la cita | Como paciente Quiero poder pagar mi cita médica desde la aplicación Para confirmar la reserva de manera rápida y segura | Escenario: Pago exitoso <br> Dado que soy un paciente Cuando selecciono una cita pendiente de pago y elijo un método de pago Entonces debería procesarse el pago y marcar la cita como “pagada”, mostrando un mensaje de confirmación.  | EP03 |
| US12 |  Calificar médico | Como paciente Quiero poder calificar al médico después de mi cita Para compartir mi experiencia y ayudar a otros pacientes | Escenario 1: Calificación exitosa <br>Dado que soy un paciente autenticado que ya tuvo una cita Cuando selecciono la opción “Calificar médico” desde el historial de citas Entonces eliges la puntuación. <br> Escenario 2: Cita aún no atendida <br> Dado que soy un paciente con una cita pendiente Cuando intento calificar al médico Entonces debería aparecer un mensaje que diga: “Solo puedes calificar después de haber asistido a tu cita.” | EP04 |
| US13 | Dejar comentario sobre atención médica | Como paciente Quiero dejar un comentario breve sobre la atención Para expresar mi opinión y sugerir mejoras | Escenario : Comentario enviado correctamente <br> Dado que soy un paciente autenticado Cuando accedo al historial de citas atendidas y escribo un comentario en el campo correspondiente Entonces el comentario se guarda y aparece junto a la calificación.| EP04 |
| US14 | Ver calificaciones de médicos | Como paciente Quiero ver las calificaciones y comentarios de otros pacientes Para tomar una mejor decisión antes de agendar una cita médica | Escenario : Visualización de valoraciones <br> Dado que soy un paciente  Cuando consulto el perfil de un médico Entonces debería ver la calificación promedio, número de evaluaciones y algunos comentarios recientes. | EP04 |
| US15 | Editar perfil | Como usuario de los segmentos objetivo médico y paciente Quiero poder editar mis datos personales Para mantener mi información actualizada en la plataforma | Escenario : Edición exitosa <br> Dado que soy un usuario de los segmentos objetivo médico o paciente Cuando modifico mis datos personales en la sección “Mi perfil” Entonces estos cambios deben guardarse correctamente. | EP05 | 
| US16 | Ver mi perfil | Como usuario de los segmentos objetivos médico y paciente Quiero poder visualizar mi información personal registrada Para verificar que mis datos estén correctos | Escenario : Visualización de perfil <br> Dado que soy un usuario autenticado Cuando accedo a la opción “Mi perfil” Entonces debería mostrarse mi nombre, correo, número, y otros datos personales. | EP05 |
| US17 | Traducir idioma | Como usuario de los segmento objetivo médico y pacienteQuiero poder seleccionar el idioma de mi preferencia Para usar la plataforma en el idioma que me resulte más cómodo | Escenario : Cambio de idioma exitoso <br> Dado que soy un usuario del segmento objetivo médico y paciente Cuando de click en el botón para cambiar idioma  Entonces toda la interfaz debería actualizarse al idioma seleccionado. | EP05 |
| US18 | Actualizar correo electrónico | Como usuario de los segmento objetivo médico y paciente Quiero actualizar mi dirección de correo electrónico en mi perfil Para recibir notificaciones y comunicaciones importantes | Escenario : Correo actualizado correctamente <br> Dado que soy un usuario autenticado Cuando ingreso una nueva dirección de correo válida y la guardo Entonces el sistema debe actualizar mi correo y enviarme un correo de confirmación. | EP05 |
| US19 | Navegación por el Landing Page | Como visitante del segmento objetivo médico/paciente Quiero navegar por la landing page del software Para obtener la información que deseo del producto. | Escenario 1: Visualizar información en la landing page <br>  Dado que el visitante del segmento objetivo médico/paciente está en la landing page Cuando navega por las secciones y reseñas Entonces debe encontrar información clara y relevante sobre las funcionalidades y beneficios del software. <br> Escenario 2: Error en el sistema <br> Dado que el visitante del segmento objetivo médico/paciente  se encuentre dentro de la landing page Cuando ocurra algún problema con el sistema Entonces no se muestra ninguna sección o reseña y se muestra un mensaje de error. | EP06 | 
| TS20 | Cambiar el Idioma de la Landing Page |  Como desarrollador Quiero implementar un sistema de cambio de idioma en la landing page Para que los usuarios puedan cambiar el idioma de la página. | Escenario : Implementación del cambio de idioma exitoso. <br> Dado que la aplicación tiene la opción de cambiar de idioma  Cuando el visitante del segmento objetivo médico/paciente selecciona un idioma diferente Entonces la página debe reflejar el idioma seleccionado en todo el contenido.| EP06 |
| TS21 | Contactar al Equipo de Soporte | Como desarrollador Quiero implementar un sistema de contacto con el equipo de soporte Para que los usuarios puedan enviar consultas sobre el landing page | Escenario: Contacto exitoso con soporte. <br> Dado que el visitante del segmento objetivo médico/paciente está en la landing page Cuando selecciona la opción de contacto Entonces debe poder enviar un mensaje al equipo de soporte con su consulta o solicitud. | EP06 |
| TS22 | Solucionar Errores Reportados | Como desarrollador Quiero corregir los errores reportados por el equipo de QA Para garantizar que el software funcione correctamente y cumplir con los estándares de calidad. | Escenario: Errores corregidos. <br> Dado que el desarrollador recibe un reporte de error Cuando analiza y soluciona el problema Entonces debe confirmar la corrección con el equipo de QA y verificar que el error no se repita en el sistema.| EP06 |

**Epic 01: Gestión de cuentas de usuario**

| **Story ID** | **Título**                         |
|--------------|------------------------------------|
| US-01        | Registrar Usuario                  |
| US-02        | Iniciar Sesión                     |
| US-03        | Olvidar contraseña                 |


**Epic 02: Gestión de agenda y atención médica** 

| **Story ID** | **Título**                          |
|--------------|-------------------------------------|
| US04         | Historial del paciente              |
| US05         | Cancelar una cita                   |
| US06         | Ver citas médicas                   |
| US07         | Notificar a los pacientes           |


**Epic 03: Reserva y Gestión de Citas para Pacientes**
| **Story ID** | **Título**                               |
|--------------|------------------------------------------|
| US08         | Consultar horario                        |
| US09         | Filtrar búsqueda de médicos              |
| US10         | Detalles de la cita                      |
| US11         | Pagar la cita                            |


**Epic 04: Evaluación y Retroalimentación de Servicios**

| **Story ID** | **Título**                                    |
|--------------|-----------------------------------------------|
| US12         | Calificar médico                              |
| TS13         | Dejar comentario sobre atención médica        |
| TS14         | Ver calificaciones de médicos                 |


**Epic 05: Configuración y Administración del Perfil de Usuario**
| **Story ID** | **Título**                                      |
|--------------|-------------------------------------------------|
| US15         | Editar perfil                                   |
| US16         | Ver mi perfil                                   |
| US17         | Traducir idioma                                 |
| US18         | Actualizar correo electrónico                   |

**Epic 06: Landing Page y Soporte Técnico**
| **Story ID** | **Título**                                        |
|--------------|---------------------------------------------------|
| US19         | Navegación por el Landing Page                    |
| US20         | Cambiar el Idioma de la Landing Page              |
| US21         | Contactar al Equipo de Soporte                    |
| US22         | Solucionar Errores Reportados                     |





## 3.3. Impact Mapping.

Segmento 1: Personas adultas que necesitan atención médica

<img src="../assets/Impact map-paciente.png" alt="IMpaciente" height="650"  />

Segmento 2: Médicos generales y especialistas con experiencia

<img src="../assets/Impact map-médico.png" alt="IMmedico" height="650"  />

## 3.4. Product Backlog.

| # Orden | User Story Id | Título                                   | Descripción                                                                                                         | Story Points (1 / 2 / 3 / 5 / 8) |
|---------|---------------|------------------------------------------|---------------------------------------------------------------------------------------------------------------------|----------------------------------|
| 1       | US19          | Navegación por el Landing Page          | Como visitante Quiero navegar por la landing page del software Para obtener la información que deseo del producto.    | 2                                |
| 2       | TS20          | Cambiar el Idioma de la Landing Page    | Como desarrollador Quiero implementar un sistema de cambio de idioma en la landing page Para que los usuarios puedan cambiar el idioma de la página. | 3                                |
| 3       | TS21          | Contactar al Equipo de Soporte          | Como visitante Quiero contactar al equipo de soporte Para obtener ayuda o resolver dudas sobre la landing page.      | 3                                |
| 4       | US01          | Contactar al Equipo de Soporte          | Como visitante Quiero contactar al equipo de soporte Para obtener ayuda o resolver dudas sobre la landing page.      | 3                                |
| 5       | US02          | Contactar al Equipo de Soporte          | Como visitante Quiero contactar al equipo de soporte Para obtener ayuda o resolver dudas sobre la landing page.      | 3                                |
| 6       | US03          | Contactar al Equipo de Soporte          | Como visitante Quiero contactar al equipo de soporte Para obtener ayuda o resolver dudas sobre la landing page.      | 3                                |
| 7       | US04          | Historial del paciente             | Como médico Quiero consultar el historial clínico de un paciente registrado Para conocer antecedentes y brindar mejor atención.                                              | 5                                |
| 8       | US05          | Cancelar una cita                  | Como médico Quiero poder cancelar una cita médica Para gestionar mi agenda y evitar conflictos con otros compromisos.                                                         | 3                                |
| 9       | US06          | Ver citas médicas                  | Como médico Quiero visualizar la lista de mis citas médicas programadas durante el día Para organizar mi agenda y prepararme para atender a los pacientes.                    | 3                                |
| 10       | US07          | Notificar a los pacientes          | Como médico Quiero enviar una notificación al paciente sobre su cita programada Para ayudarle a recordar y evitar que falte a la consulta médica.                             | 3                                |
| 11       | US08          | Consultar horario                  | Como paciente Quiero consultar los horarios disponibles de un médico Para elegir una fecha y hora conveniente para agendar mi cita médica.                                     | 3                                |
| 12       | US09          | Filtrar búsqueda de médicos        | Como paciente Quiero filtrar médicos por especialidad Para encontrar fácilmente al profesional adecuado para agendar mi cita.                                                | 3                                |
| 13      | US10          | Detalles de la cita                | Como paciente Quiero ver los detalles completos de una cita médica agendada Para saber las características y detalles de la cita.                                            | 3                                |
| 14      | US11          | Pagar la cita                     | Como paciente Quiero poder pagar mi cita médica desde la aplicación Para confirmar la reserva de manera rápida y segura.                                                      | 5                                |
| 15      | US12          | Calificar médico                   | Como paciente Quiero poder calificar al médico después de mi cita Para compartir mi experiencia y ayudar a otros pacientes.                                                   | 3                                |
| 16      | US13          | Dejar comentario sobre atención médica | Como paciente Quiero dejar un comentario breve sobre la atención Para expresar mi opinión y sugerir mejoras.                                                                    | 2                                |
| 17      | US14          | Ver calificaciones de médicos      | Como paciente Quiero ver las calificaciones y comentarios de otros pacientes Para tomar una mejor decisión antes de agendar una cita médica.                                  | 3                                |
| 18      | US15          | Editar perfil                     | Como usuario de los segmentos objetivo médico y paciente Quiero poder editar mis datos personales Para mantener mi información actualizada en la plataforma.                 | 3                                |
| 19      | US16          | Ver mi perfil                     | Como usuario de los segmentos objetivos médico y paciente Quiero poder visualizar mi información personal registrada Para verificar que mis datos estén correctos.            | 2                                |
| 20      | US17          | Traducir idioma                   | Como usuario de los segmento objetivo médico y paciente Quiero poder seleccionar el idioma de mi preferencia Para usar la plataforma en el idioma que me resulte más cómodo. | 3                                |
| 21      | US18          | Actualizar correo electrónico     | Como usuario de los segmento objetivo médico y paciente Quiero actualizar mi dirección de correo electrónico en mi perfil Para recibir notificaciones y comunicaciones importantes. | 5                                |
| 22      | TS22          | Solucionar Errores Reportados     | Como desarrollador Quiero corregir los errores reportados por el equipo de QA Para garantizar que el software funcione correctamente y cumplir con los estándares de calidad. | 8                                |

