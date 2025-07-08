  # Capítulo III: Requirements Specification

## 3.1. To-Be Scenario Mapping.

Segmento 1: Pacientes

<img src="../assets/TBSM-paciente.jpg" alt="TBSM paciente" height="500" />

Segmento 2: Médicos 

<img src="../assets/TBSM-medico.jpg" alt="TBSM medico" height="500" />


## 3.2. User Stories.
| Epic/Story ID | Titulo | Descripción | Criterios de Aceptación | Relacionado con (Epic ID)|
|-------|-----------------|----------------------------|----------------------------------------|---------|
| US01 | Registrar usuario | Como visitante del segmento médico/paciente, quiero registrarme en la aplicación proporcionando mis datos personales, para crear una cuenta y poder utilizar sus funcionalidades. | Escenario 1: Registro exitoso. <br> Dado que soy un visitante del segmento objetivo médico/paciente <br> Cuando ingreso una dirección de correo válida, una contraseña que cumpla los requisitos de seguridad y acepto los términos y condiciones <br> Entonces se debe crear mi cuenta y mostrarse un mensaje de confirmación. <br><br> Escenario 2: Registro fallido. <br> Dado que soy un visitante <br> Cuando ingreso un correo que ya está registrado o una contraseña inválida <br> Entonces debe mostrarse un mensaje de error indicando el problema. | EP01 |
| US02 | Iniciar sesión | Como usuario registrado (médico o paciente), quiero iniciar sesión con mis credenciales, para acceder a mi cuenta. | Escenario 1: Inicio de sesión exitoso. <br> Dado que soy un usuario registrado <br> Cuando ingreso correctamente mi correo electrónico y contraseña <br> Entonces debo acceder a mi cuenta. <br><br> Escenario 2: Inicio fallido. <br> Dado que soy un usuario registrado <br> Cuando ingreso credenciales incorrectas <br> Entonces debe mostrarse un mensaje: “Usuario o contraseña incorrectos”. | EP01 |
| US03 | Recuperar contraseña | Como usuario registrado, quiero restablecer mi contraseña si la olvido, para poder volver a acceder a mi cuenta. | Escenario 1: Solicitud exitosa. <br> Dado que he olvidado mi contraseña <br> Cuando ingreso un correo registrado en el formulario de recuperación <br> Entonces debo recibir un enlace para crear una nueva contraseña. <br><br> Escenario 2: Solicitud fallida. <br> Dado que he olvidado mi contraseña <br> Cuando ingreso un correo no registrado o inválido <br> Entonces debe mostrarse el mensaje: “Correo inválido”. | EP01 |
| US04 | Consultar historial clínico | Como médico autenticado, quiero consultar el historial clínico de un paciente registrado, para conocer antecedentes y brindar una mejor atención. | Escenario 1: Historial disponible. <br> Dado que estoy autenticado como médico <br> Cuando accedo al perfil de un paciente con historial <br> Entonces debe mostrarse una lista con diagnósticos, citas y tratamientos anteriores. <br><br> Escenario 2: Sin historial. <br> Dado que soy un médico autenticado <br> Cuando accedo al perfil de un paciente sin historial <br> Entonces debe mostrarse el mensaje: “Este paciente aún no tiene historial clínico registrado”. | EP02 |
| US05 | Cancelar cita | Como médico Quiero cancelar una cita médica Para gestionar mi agenda y evitar conflictos con otros compromisos | Escenario : Cancelación exitosa <br> Dado que soy un médico autenticado Cuando selecciono una cita y elijo la opción “Cancelar” Entonces la cita debe marcarse como cancelada y el paciente debe recibir una notificación. | EP02 |
| US06 | Ver citas médicas | Como médico Quiero ver la lista de mis citas programadas del día Para organizar mi agenda y prepararme para las consultas | Escenario : Visualización exitosa <br> Dado que soy un médico autenticado Cuando ingreso a la sección “Mis citas” Entonces debe mostrarse una lista con las citas del día, ordenadas por hora. | EP02 |
| US07 | Enviar recordatorio de cita | Como médico Quiero enviar una notificación al paciente sobre su próxima cita Para recordarle y evitar inasistencias | Escenario : Recordatorio enviado <br> Dado que soy un médico autenticado Cuando selecciono una cita próxima y elijo “Enviar recordatorio” Entonces el paciente debe recibir un mensaje con fecha, hora y nombre del médico. | EP02 |
| US08 | Ver disponibilidad médica | Como paciente autenticado Quiero consultar los horarios disponibles de un médico Para agendar una cita en un horario conveniente | Escenario : Visualización de disponibilidad <br> Dado que soy un paciente autenticado Cuando selecciono un médico en la plataforma Entonces debe mostrarse un calendario con fechas y horarios disponibles. | EP03 |
| US09 | Buscar médico por especialidad | Como paciente Quiero filtrar la búsqueda de médicos por especialidad Para encontrar al profesional adecuado para mi caso | Escenario : Filtro exitoso <br> Dado que soy un paciente Cuando aplico filtros de especialidad en el buscador Entonces debe mostrarse una lista de médicos que cumplan con los criterios seleccionados. | EP03 |
| US10 | Ver detalles de cita | Como paciente autenticado Quiero ver los detalles completos de una cita médica Para confirmar lugar, fecha y médico asignado | Escenario : Visualización exitosa <br> Dado que soy un paciente autenticado Cuando selecciono una cita en mi historial o próximas citas Entonces deben mostrarse todos los detalles: médico, especialidad, fecha, hora y lugar de atención. | EP03 |
| US11 | Pagar cita médica | Como paciente Quiero pagar mi cita desde la aplicación Para confirmar la reserva de manera rápida y segura | Escenario : Pago exitoso <br> Dado que soy un paciente Cuando selecciono una cita pendiente de pago y elijo un método de pago válido Entonces debe procesarse el pago y marcar la cita como “pagada”, mostrando una confirmación. | EP03 |
| US12 | Calificar médico | Como paciente Quiero calificar al médico después de una consulta Para compartir mi experiencia con otros | Escenario 1 : Calificación válida <br> Dado que ya asistí a una cita Cuando selecciono “Calificar médico” en mi historial Entonces debo poder elegir una puntuación del 1 al 5. <br><br> Escenario 2 : Cita pendiente <br> Dado que tengo una cita pendiente Cuando intento calificar al médico Entonces debe mostrarse el mensaje: “Solo puedes calificar después de tu cita”. | EP04 |
| US13 | Comentar sobre atención médica | Como paciente Quiero dejar un comentario sobre la atención recibida Para expresar mi opinión y sugerencias | Escenario : Comentario enviado <br> Dado que soy un paciente autenticado y asistí a una cita Cuando escribo un comentario y lo envío Entonces debe guardarse y mostrarse junto a la calificación. | EP04 |
| US14 | Ver calificaciones de médicos | Como paciente Quiero ver las calificaciones y comentarios de otros pacientes Para tomar una mejor decisión antes de reservar una cita | Escenario : Visualización de calificaciones <br> Dado que soy un paciente Cuando consulto el perfil de un médico Entonces debo ver su calificación promedio, número de evaluaciones y comentarios recientes. | EP04 |
| US15 | Editar perfil | Como usuario médico o paciente Quiero editar mis datos personales Para mantener mi información actualizada | Escenario : Edición exitosa <br> Dado que soy un usuario autenticado Cuando modifico mis datos en “Mi perfil” y guardo Entonces los cambios deben actualizarse correctamente. | EP05 |
| US16 | Ver perfil | Como usuario médico o paciente Quiero ver mi información registrada Para verificar que esté correcta | Escenario : Visualización de perfil <br> Dado que soy un usuario autenticado Cuando accedo a “Mi perfil” Entonces debe mostrarse mi nombre, correo, número y demás datos personales. | EP05 |
| US17 | Cambiar idioma | Como usuario médico o paciente Quiero cambiar el idioma de la plataforma Para usarla en el idioma de mi preferencia | Escenario : Cambio de idioma exitoso <br> Dado que soy un usuario Cuando selecciono otro idioma en la configuración Entonces toda la interfaz debe actualizarse al idioma elegido. | EP05 |
| US18 | Actualizar correo electrónico | Como usuario médico o paciente Quiero actualizar mi correo electrónico Para recibir notificaciones correctamente | Escenario : Actualización exitosa <br> Dado que soy un usuario autenticado Cuando ingreso un nuevo correo válido y lo guardo Entonces el sistema debe actualizar el correo y enviarme una confirmación. | EP05 |
| US19 | Navegar por Landing Page | Como visitante Quiero explorar la landing page del software Para conocer sus beneficios y funcionalidades | Escenario 1 : Navegación exitosa <br> Dado que soy un visitante en la landing page Cuando navego por las secciones Entonces debo encontrar información clara sobre el producto. <br><br> Escenario 2 : Fallo en la página <br> Dado que estoy en la landing page Cuando hay un error del sistema Entonces debe mostrarse un mensaje de error general. | EP06 |
| TS20 | Traducir idioma en Landing Page | Como desarrollador Quiero implementar el cambio de idioma en la landing page Para que los visitantes puedan usarla en su idioma preferido | Escenario : Traducción funcional <br> Dado que la página tiene opción de cambio de idioma Cuando selecciono un idioma Entonces todo el contenido debe actualizarse al idioma elegido. | EP06 |
| TS21 | Contacto con soporte | Como desarrollador Quiero permitir que los visitantes contacten al equipo de soporte desde la landing page Para resolver dudas o problemas | Escenario : Contacto exitoso <br> Dado que estoy en la landing page Cuando selecciono “Contacto” y envío un mensaje Entonces el mensaje debe llegar al equipo de soporte. | EP06 |
| TS22 | Corregir errores del sistema | Como desarrollador Quiero corregir los errores reportados Para asegurar el correcto funcionamiento del sistema | Escenario : Corrección validada <br> Dado que recibo un reporte de error Cuando soluciono el problema Entonces debe verificarse que el error esté resuelto y no vuelva a aparecer. | EP06 |

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

Segmento 1: Pacientes adultas que necesitan atención médica

<img src="../assets/Paciente 1.png" alt="IMpaciente" height="650"  />

Segmento 2: Médicos y especialistas con experiencia

<img src="../assets/Impact map-médico.png" alt="IMmedico" height="650"  />

## 3.4. Product Backlog.

| # Orden | User Story Id | Título                                   | Descripción                                                                                                         | Story Points (1 / 2 / 3 / 5 / 8) |
|---------|---------------|------------------------------------------|---------------------------------------------------------------------------------------------------------------------|----------------------------------|
| 1       | US19          | Navegación por el Landing Page          | Como visitante Quiero navegar por la landing page del software Para obtener la información que deseo del producto.    | 2                                |
| 2       | TS20          | Cambiar el Idioma de la Landing Page    | Como desarrollador Quiero implementar un sistema de cambio de idioma en la landing page Para que los usuarios puedan cambiar el idioma de la página. | 3                                |
| 3       | TS21          | Contactar al Equipo de Soporte          | Como visitante Quiero contactar al equipo de soporte Para obtener ayuda o resolver dudas sobre la landing page.      | 3                                |
| 4       | US01          | Registrar Usuario         | Como visitante Quiero contactar al equipo de soporte Para obtener ayuda o resolver dudas sobre la landing page.      | 3                                |
| 5       | US02          | Iniciar Sesión          | Como visitante Quiero contactar al equipo de soporte Para obtener ayuda o resolver dudas sobre la landing page.      | 3                                |
| 6       | US03          | Olvidar contraseña          | Como visitante Quiero contactar al equipo de soporte Para obtener ayuda o resolver dudas sobre la landing page.      | 3                                |
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

