# Capítulo III: Requirements Specification

## 3.1. To-Be Scenario Mapping.

Segmento 1: Personas adultas que necesitan atención médica

<img src="../assets/TBSM-paciente.jpg" alt="TBSM paciente" height="500" />

Segmento 2: Médicos generales y especialistas con experiencia

<img src="../assets/TBSM-medico.jpg" alt="TBSM medico" height="500" />


## 3.2. User Stories.
| Epic/Story ID | Titulo | Descripción | Criterios de Aceptación | Relacionado con (Epic ID)|
|-------|-----------------|----------------------------|----------------------------------------|---------|
| US01 | Registrar usuario | Como visitante Quiero registrar mi cuenta Para hacer uso de la aplicación. | Escenario 1: Usuario ingresa credenciales válidas. <br> Dado que el visitante desee crear una cuenta personal en la aplicación Cuando ingrese las credenciales de una cuenta inexistente en la base de datos y una contraseña que cumple con todos los requisitos de seguridad, y acepte los términos y condiciones de uso Entonces se creará la cuenta del médico. <br> Escenario 2: Visitante ingresa credenciales incorrectas. <br> Dado que el visitante ingresa credenciales de una cuenta ya existe  Cuando ingrese una dirección de correo electrónico o contraseña que no cumplen con los requisitos especificados Entonces se le denegará la operación | EP01 |
| US02 | Confirmación de registro de cuenta | Como usuario Quiero recibir una confirmación al registrar mi cuenta Para saber que el proceso se completó correctamente. | Escenario 1: Confirmar registro de cuenta <br> Dado que el usuario ha completado el formulario de registro Cuando envío mis datos Entonces debería recibir un correo de confirmación para activar mi cuenta. <br> Escenario 2: Error en la confirmación de cuenta <br>  Dado que el usuario no he completado el formulario de registro correctamente Cuando envío mis datos Entonces debería recibir un mensaje diciendo "Error en la confirmación". | EP01 |
| US03 | Iniciar sesión | Como usuario registrado Quiero iniciar sesión Para acceder a mi cuenta. | Escenario 1: Inicio de sesión exitoso <br> Dado que soy un usuario registrado Cuando ingreso mi nombre de usuario y contraseña Entonces debería acceder a mi cuenta. <br> Escenario 2: Inicio de sesión erróneo <br> Dado que soy un usuario registrado Cuando ingreso mi nombre de usuario o contraseña incorrecto Entonces saldrá en pantalla una mensaje "Usuario o contraseña incorrecto" | EP01 | 
| US04 | Restablecer contraseña | Como usuario Quiero restablecer mi contraseña si la olvido Para poder acceder a mi cuenta. | Escenario 1: Restablecer contraseña exitoso <br> Dado que el usuario ha olvidado mi contraseña Cuando ingreso mi correo para restablecerla Entonces debería recibir un enlace para crear una nueva contraseña. <br> Escenario 2:  Error de restablecer contraseña <br> Dado que el usuario he olvidado mi contraseña Cuando ingreso un correo inválido para restablecerla Entonces aparecera un mensaje "Correo inválido" | EP01 |
| US05 | Cerrar sesión | Como usuario Quiero cerrar sesión Para proteger mi cuenta cuando termine de usar la aplicación. | Escenario : Cierre de sesión exitoso <br> Dado que soy un usuario de la aplicación Cuando hago clic en el botón "Cerrar sesión" Entonces debería ser desconectado de mi cuenta y redirigido a la página de inicio. | EP01 | 
| US06 | Editar datos del usuario | Como usuario registrado Quiero editar mis datos personales Para mantener mi información actualizada. | Escenario : Editar datos del usuario <br> Dado que soy un usuario Cuando edito mis datos personales y hago clic en "Guardar cambios" Entonces mis datos se actualizan correctamente en la plataforma.| EP01 | 
| US07 | Eliminar cuenta | Como usuario Quiero eliminar mi cuenta Para dejar de utilizar la plataforma. | Escenario : Cuenta eliminada <br> Dado que soy un usuario Cuando solicito eliminar mi cuenta Entonces se me solicita una confirmación y mi cuenta se elimina de la plataforma tras confirmar. | EP01 |
| US08 | Filtrar búsqueda de médicos | Como paciente Quiero filtrar la búsqueda de médicos por disponibilidad Para facilitar la elección. | Escenario : Filtrar médicos por disponibilidad <br> Dado que soy un paciente Cuando selecciono un horario en el filtro Entonces los resultados deben ajustarse a esa disponibilidad. | EP02 |
| US09 | Ver información del médico | Como paciente Quiero ver los detalles de un médico Para tomar una decisión informada. | Escenario : Ver detalles del médico <br> Dado que estoy en la lista de médicos Cuando hago clic en un perfil de médico Entonces debo ver su especialidad, horarios disponibles, y experiencia. | EP02 | 
| US10 | Pagar la cita | Como paciente Quiero pagar mi cita médica Para confirmar mi asistencia. | Escenario 1: Pago exitoso <br> Dado que tengo una cita programada Cuando elijo el método de pago y completo la transacción Entonces debo recibir un comprobante de pago y la cita debe ser confirmada. <br> Escenario 2: Error en el pago <br> Dado que tengo una cita programada Cuando intento completar el pago con una tarjeta inválida Entonces debo recibir un mensaje indicando "El pago no pudo ser procesado. Verifique los datos de pago." | EP02 | 
| US11 | Cancelar cita médica | Como paciente Quiero poder cancelar una cita médica si no puedo asistir para liberar el espacio para otro paciente. | Escenario: Cancelación exitosa. <br> Dado que soy un paciente Cuando selecciono una cita y elijo "Cancelar" Entonces la cita se cancela y se me notifica. | EP02 |
|US12 |  Agendar Cita Médica | Como paciente Quiero poder separar o agendar una cita con un médico cuando elijo una fecha y hora disponibles Para asegurarme de que mi consulta esté confirmada. | Escenario: Separar cita exitosa. <br> Dado que soy un paciente y estoy navegando por el perfil de un médico Cuando selecciono una fecha y hora disponible para la cita Entonces la cita se agenda automáticamente en el sistema| EP02 |
| US13 | Ver historial de pacientes atendidos | Como médico Quiero ver el historial de los pacientes atendidos Para un mejor seguimiento de su tratamiento. | Escenario : Ver historial de pacientes <br> Dado que soy un médico Cuando accedo al perfil de un paciente Entonces debo poder ver su historial médico con las visitas anteriores. | EP03 |
| US14 | Acceder al historial médico del paciente | Como médico Quiero acceder al historial médico de mis pacientes Para ofrecer una atención más adecuada. | Escenario : Acceder al historial médico del paciente <br> Dado que soy un médico Cuando accedo al perfil de un paciente Entonces debo poder ver su historial médico completo. | EP03 | 
| US15 | Dejar una reseña sobre un médico | Como paciente Quiero poder dejar una reseña sobre un médico después de una cita Para compartir mi experiencia con otros usuarios. | Escenario : Reseña publicada. <br> Dado que soy un paciente Cuando termino mi cita con un médico Entonces puedo dejar una reseña con mi calificación o comentarios | EP03 |
| US16 | Navegación por el Landing Page | Como visitante Quiero navegar por la landing page del software Para obtener la información que deseo del producto. | Escenario 1: Visualizar información en la landing page <br>  Dado que el visitante está en la landing page Cuando navega por las secciones y reseñas Entonces debe encontrar información clara y relevante sobre las funcionalidades y beneficios del software. <br> Escenario 2: Error en el sistema <br> Dado que el visitante se encuentre dentro de la landing page Cuando ocurra algún problema con el sistema Entonces no se muestra ninguna sección o reseña y se muestra un mensaje de error. | EP04 | 
| US17 | Acceder a la aplicación desde la landing page | Como visitante de la página Quiero poder acceder a la aplicación desde la landing page Para empezar a usarla. | Escenario : Acceder a la aplicación <br> Dado que soy un visitante Cuando hago clic en "Comienza ya" Entonces debería ser redirigido a la página de inicio de sesión de la aplicación. | EP04 |
| TS18 | Cambiar el Idioma de la Landing Page | Como visitante Quiero cambiar el idioma de la landing page Para poder entender mejor la información presentada. | Escenario : Cambio de idioma exitoso. <br>Dado que el visitante está en la landing page Cuando selecciona un idioma diferente en el menú de idiomas Entonces la página debe cambiar al idioma seleccionado.| EP04 |
| TS19 | Contactar al Equipo de Soporte | Como visitante Quiero contactar al equipo de soporte Para obtener ayuda o resolver dudas sobre la plataforma. | Escenario: Contacto exitoso. <br> Dado que el visitante está en la landing page Cuando selecciona la opción de contacto Entonces debe poder enviar un mensaje al equipo de soporte con su consulta o solicitud.| EP04 |
| TS20 | Solucionar Errores Reportados | Como desarrollador Quiero corregir los errores del software notificados por el equipo de QA Para mejorar la calidad del producto. | Escenario: Errores corregidos. <br> Dado que  el desarrollador recibe un reporte de error Cuando identifica y soluciona el problema Entonces debe confirmar la corrección con el equipo de QA.| EP04 |

**Epic 01: Gestión de cuentas de usuario**

| **Story ID** | **Título**                         |
|--------------|------------------------------------|
| US-01        | Registrar Usuario                  |
| US-02        | Confirmación de Registro de cuenta |
| US-03        | Iniciar sesión                     |
| US-04        | Restablecer contraseña             |
| US-05        | Cerrar sesión                      |
| US-06        | Editar datos del usuario           |
| US-07        | Eliminar cuenta                    |

## 3.3. Impact Mapping.

Segmento 1: Personas adultas que necesitan atención médica

<img src="../assets/Impact map-paciente.png" alt="IMpaciente" height="650"  />

Segmento 2: Médicos generales y especialistas con experiencia

<img src="../assets/Impact map-médico.png" alt="IMmedico" height="650"  />

## 3.4. Product Backlog.

| # Orden | User Story Id | Título | Descripción | Story Points (1 / 2 / 3 / 5 / 8) |
|---------|---------------|--------|-------------|----------------------------------|
| 1       | US08          | Acceder a la aplicación desde la landing page | Como usuario de la página Quiero poder acceder a la aplicación desde la landing page Para empezar a usarla. | 1 |
| 2       | US11          | Confirmación de registro de cuenta | Como usuario Quiero recibir una confirmación al registrar mi cuenta Para saber que el proceso se completó correctamente. | 1 |
| 3       | US16          | Cerrar sesión | Como usuario Quiero cerrar sesión Para proteger mi cuenta cuando termine de usar la aplicación. | 1 |
| 4       | US22          | Ver información del médico | Como paciente Quiero ver los detalles de un médico Para tomar una decisión informada. | 1 |
| 5       | US30          | Visualizar citas médicas programadas | Como paciente Quiero ver las citas médicas que tengo programadas Para estar al tanto de mi agenda. | 1 |
| 6       | US12          | Iniciar sesión | Como usuario registrado Quiero iniciar sesión Para acceder a mi cuenta. | 2 |
| 7       | US17          | Editar datos del médico | Como médico registrado Quiero editar mis datos personales Para mantener mi información actualizada. | 2 |
| 8       | US18          | Editar datos del paciente | Como paciente registrado Quiero editar mis datos personales Para mantener mi información actualizada. | 2 |
| 9       | US13          | Restablecer contraseña | Como usuario Quiero restablecer mi contraseña si la olvido Para poder acceder a mi cuenta. | 2 |
| 10      | US23          | Revisar valoraciones y reseñas sobre el médico | Como paciente Quiero ver las valoraciones y reseñas de un médico Para tomar una mejor decisión al elegirlo. | 2 | 
| 11      | US20          | Buscar médico especializado | Como paciente Quiero buscar médicos según especialidad Para encontrar el adecuado para mis necesidades. | 3 |
| 12      | US21          | Filtrar búsqueda de médicos | Como paciente Quiero filtrar la búsqueda de médicos por disponibilidad Para facilitar la elección. | 3 |
| 13      | US24          | Generar valoraciones y reseñas sobre el médico | Como paciente Quiero poder valorar y dejar una reseña sobre un médico Para compartir mi experiencia con otros usuarios. | 3 |
| 14      | US26          | Pagar la cita | Como paciente Quiero pagar mi cita médica Para confirmar mi asistencia. | 3 |
| 15      | US27          | Generar comprobante electrónico | Como paciente Quiero recibir un comprobante electrónico del pago de mi cita Para tener un registro. | 3 |
| 16      | US01          | Implementación de la sección “Home” en la Landing Page | Como usuario de la plataforma web Quiero poder visualizar la sección "Home" de la landing page para tener una primera vista del producto. | 3 |
| 17      | US02          | Implementación de la sección “About us” en la Landing Page | Como usuario de la plataforma Quiero visualizar la sección "About us" de la landing page Para tener información de la startup. | 3 |
| 18      | US03          | Implementación de la sección "Services" en la Landing Page | Como usuario de la plataforma Quiero visualizar la sección "Services" en la landing page Para tener información de los servicios ofrecidos por la aplicación | 3 |
| 19      | US04          | Implementación de la sección "Plans" en la Landing Page | Como usuario de la plataforma Quiero visualizar los planes de suscripción Para tener información de las membresías | 3 |
| 20      | US05          | Implementación de la sección "About the Team" en la Landing Page. | Como usuario Quiero conocer al equipo detrás de la startup Para entender la experiencia y misión de la plataforma. | 3 |
| 21     | US06          | Implementación de las reseñas de la landing page. | Como usuario Quiero conocer las reseñas de otras personas usando la plataforma Para saber si me conviene usarlo | 3 |
| 22      | US10          | Registrar paciente | Como paciente Quiero poder registrar mi cuenta Para hacer uso de la aplicación | 5 |
| 23      | US14          | Autenticar la cuenta del médico | Como médico Quiero autenticar mi cuenta Para poder verificar mi identidad. | 5 |
| 24      | US15          | Autenticar la cuenta del paciente |Como paciente Quiero autenticar mi cuenta Para verificar mi identidad | 5 |
| 25      | US19          | Eliminar cuenta | Como usuario Quiero eliminar mi cuenta Para dejar de utilizar la plataforma. | 5 |
| 26      | US07          | Landing Page Responsive a diferentes tamaños de pantalla. | Como usuario de la página Quiero que la landing page sea responsive Para que se vea bien en dispositivos móviles y escritorios. | 5 |
| 27      | US28          | Ver historial de pacientes atendidos | Como médico Quiero ver el historial de los pacientes atendidos Para un mejor seguimiento de su tratamiento. | 5 |
| 28      | US29          | Ver métricas de servicio del médico | Como médico Quiero ver las métricas de mis servicios Para evaluar mi desempeño y mejorar la atención. | 5 |
| 29      | US30          | Visualizar citas médicas programadas | Como paciente Quiero ver las citas médicas que tengo programadas Para estar al tanto de mi agenda. | 5 |
| 30      | US25          | Separar cita con el médico | Como paciente Quiero separar una cita con el médico Para agendar una consulta. | 8 |
| 31      | US09          | Registrar médico | Como médico Quiero registrar mi cuenta Para hacer uso de la aplicación. | 8 |