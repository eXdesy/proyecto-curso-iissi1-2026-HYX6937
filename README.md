# SmartBus

## Miembros del grupo L5-01

1. Espina Apellaniz, David
2. Pérez Gómez, Juan
3. Mukhiddinov Dilyorbek
4. Apellidos, Nombre

## 1. Introducción al problema

El transporte público en Sevilla, gestionado por TUSSAM, cuenta con una aplicación móvil que usamos a diario, pero que actualmente presenta varios fallos que complican el día a día de los usuarios. Uno de los problemas más comunes y frustrantes es el desajuste en los tiempos de espera; muchas veces la app marca que quedan "3 minutos" para que llegue un autobús que nunca aparece en el tiempo esperado. Además, la aplicación no da ninguna información sobre la ocupación del vehículo. Esto provoca que te quedes esperando en la parada porque la app te indica que el bus está llegando, pero cuando por fin aparece va al 100% de capacidad y no puedes subirte, haciendo que la espera no haya servido de nada. Por otro lado, el método de pago se ha quedado bastante anticuado. En una época en la que casi todo se paga con el móvil mediante NFC (como Apple Pay o Google Pay), el sistema nos sigue obligando a depender exclusivamente de la tarjeta física del bonobús, impidiendo viajar si te la olvidas en casa.

Para solucionar todos estos problemas, en este proyecto proponemos el desarrollo de un nuevo sistema de información llamado "SmartBus". La idea es que esta plataforma integre el aforo en tiempo real de los vehículos junto con una posición GPS más precisa, avisando desde la app si un autobús ya va completo para que la persona pueda buscar una alternativa. También vamos a diseñar el sistema para virtualizar los títulos de transporte actuales, permitiendo a los usuarios vincular su bonobús al móvil para acceder y pagar el viaje directamente acercando el teléfono, igual que hacemos con las tarjetas bancarias.

## 2. Glosario de términos

- Aforo en tiempo real: Número actual de pasajeros a bordo de un autobús en un momento dado.

- Bonobús virtual: Título de transporte digitalizado y almacenado en el teléfono móvil del usuario.

- NFC: Tecnología inalámbrica de corto alcance que permite validar el viaje acercando el móvil a la máquina.

- Sistema de Ayuda a la Explotación (SAE): Servidor central que controla por GPS la posición, horarios y rutas de toda la flota de autobuses.

- Título de transporte: Soporte físico o digital (billete sencillo, tarjeta mensual, abono) que da derecho a viajar.

- Transbordo: Cambio a otra línea de autobús dentro de un margen de tiempo determinado, aplicando un descuento o coste cero.

- Validación: Acción de registrar el viaje en la máquina al subir, comprobando los permisos y descontando el saldo.

- Validadora: Máquina instalada en el autobús donde el pasajero acerca su tarjeta o móvil para pagar.

## 3. Visión general del sistema

### 3.1. Requisitos generales

#### R.G.01. Mejorar la precisión de la información del transporte

Como usuario del transporte público, quiero consultar información precisa y actualizada sobre la ubicación y el tiempo estimado de llegada de los autobuses, para planificar mejor mis desplazamientos.

#### R.G.02. Consultar la ocupación de los autobuses

Como usuario del transporte público, quiero conocer el nivel de ocupación de los autobuses antes de que lleguen a mi parada, para poder elegir la mejor alternativa de transporte.

#### R.G.03. Digitalizar los títulos de transporte

Como usuario del transporte público, quiero utilizar mi bonobús desde el teléfono móvil, para poder pagar y validar mis viajes sin depender exclusivamente de una tarjeta física.

#### R.G.04. Facilitar la gestión del transporte

Como responsable de la gestión del transporte, quiero disponer de información actualizada sobre la ubicación y la ocupación de los autobuses, para mejorar el seguimiento del servicio y la información proporcionada a los pasajeros.

### 3.2. Usuarios del sistema

- Pasajero: consulta las líneas, las paradas, la ubicación y los tiempos estimados de llegada de los autobuses. También consulta su ocupación, gestiona su bonobús virtual y valida sus viajes mediante NFC.

- Personal de gestión del transporte: supervisa la información de los autobuses y el estado del servicio para facilitar su seguimiento y gestión.

- Administrador del sistema: gestiona los usuarios y los parámetros generales del sistema, así como la configuración necesaria para su correcto funcionamiento.

- Conductor del bus: lleva el bus y notifica de retrasos o incidencias.

## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales
#### R.F.01. Ubicación
-Como usuario quiero que la aplicación me informe de la última parada que haya pasado el bus del autobús para calcular mejor el tiempo de espera en la parada.

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### R.F.02. Capacidad del autobús
-Como usuario quiero que la aplicación me informe de la capacidad del autobús en todo momento para calcular para ver si voy a caber en el bus.

**Prueba de aceptación**

#### R.F.03. Capacidad máxima
-Como usuario quiero que la aplicación me muestre la capacidad máxima del autobús para saber si quepo o no. También quiero saber la capacidad máxima para que no se acepte a un número de pasajero mayor a la capacidad del bus y así disminuir el número de heridos y problemas en caso de accidente.

**Prueba de acceptación**

#### R.F.04. Registro Autobús
-Como usuario quiero que la aplicación me de un registre el número de personas que se encuentran en el bus, sumando las que se suben a él y restando las que se bajan.

**Pruebas de acceptación**

#### R.F.05. Paradas de cada línea
-Como usuario quiero que el sistema me marque las paradas disponibles para esa línea de autobús para saber donde cogerlo.

**Pruebas de aceptación**

#### R.F.06. Paradas
-Como usuario quiero que la aplicación me diga la ubicación de la parada, que líneas pasan por ella y cuanto tiempo le queda a un bus de cada línea en llegar a la parada.

**Pruebas de acceptación**

#### R.F.07. Pagos
-Como usuario quiero poder tener distintas formas de pago como con mi móvil, tarjeta de crédito, efectivo o bonobus, para tener flexibilidad y no quedarme en tierra por no poder pagar el viaje.

**Pruebas de aceptación**

#### R.F.08. Pagos con bonos
-Como personal de gestión quiero que le reste el dinero correspondiente al viaje al bono.

**Pruebas de aceptación**

#### R.F.09. Trasbordo
-Como usuario quiero que se me aplique un descuento si me subo en 2 autobuses consecutivos para poder ahorrar en mis viajes.

**Pruebas de aceptación**

#### R.F.10. Tráfico denso o averías
-Como usuario quiero que la aplicación me notifique en caso de retraso por tráfico o por algún tipo de avería para poder tomar medidas a la hora de llegar a mi destino.

**Pruebas de aceptación**

#### R.F.11. Previsión de llegada
-Como usuario quiero que la aplicación me prevea el tiempo medio que tarda el bus en llegar a la parada que escoja para poder saber mi hora de llegada.

**Pruebas de aceptación**

#### R.F.12. Recarga de bonobús
-Como usuario quiero poder recargar el saldo de mi bonobús virtual directamente desde la app mediante tarjeta de crédito/débito, Apple Pay o Google Pay.

**Pruebas de aceptación**

#### R.F.13. Paradas y líneas favoritas
-Como usuario quiero poder escoger mis paradas y líneas habituales como favoritas para que me sea más rápido acceder a ellas.

**Pruebas de aceptación**

#### R.F.14. Cambio por eventos
-Como administrador quiero poder cambiar las rutas de las líneas de los buses para no tener que cancelar líneas por cortes de carretera.

**Pruebas de aceptación**


#### R.F.15. Historial de velocidad en hora punta

-Como sistema de gestión quiero calcular los tiempos de espera basándome en la velocidad media histórica de ese tramo a ese día y hora exacta.

**Pruebas de aceptación**

#### R.F.16. Parada bajada
-Como usuario quiero indicarle al conductor en qué parada quiero bajar para que el conductor no se equivoque y no se pase la parada.

**Pruebas de aceptación**

#### R.F.17. Aviso retraso
-Como conductor quiero poder avisar si el bus va con retraso o no, notificando la llegada a cada parada, para avisar a los pasajeros de la situación.

**Pruebas de aceptación**

#### R.F.18. Averías
-Como conductor quiero poder notificar de averías a la empresa y los pasajeros, para que estos sepan que el bus no va a continuar el trayecto preestablecido.

**Pruebas de aceptación**

#### 4.1.1. Requisitos de información

##### R.I.01. Consulta de información de la parada

Como pasajero quiero consultar los datos detallados de una parada específica (nombre, ubicación, líneas que la utilizan y tiempos de llegada estimados por línea) para saber cuándo llegará mi autobús y planificar mi tiempo de espera.

**Prueba de aceptación**
- Comprobar que, al introducir el número o nombre de la parada en el buscador, se muestran todas las líneas operativas que pasan por ella.
- Comprobar que para cada línea se muestra el tiempo estimado de llegada de los dos próximos autobuses.
- Se debe aplicar la regla de negocio RN.02 : Verificar que si un autobús en camino tiene su aforo al máximo, no se muestra su tiempo de llegada o se indica visualmente que está "Completo".

#### R.I.02. Información del estado de ocupación del autobús

Como pasajero quiero visualizar el aforo actual del autobús que se dirige a mi parada para decidir si espero a ese vehículo o busco una alternativa si está muy lleno.

**Prueba de aceptación**
- Comprobar que junto al tiempo de llegada de cada autobús en la pantalla de la parada, se muestra un indicador con su ocupación.
- Comprobar que el sistema actualiza este aforo en tiempo real tras cada parada realizada por el vehículo.
- Se debe aplicar la regla de negocio RN.04: Verificar que el número de pasajeros mostrados nunca es menor que cero.

#### R.I.03. Información del Bonobús Virtual

Como pasajero quiero ver los datos de mi título de transporte digital (tipo de abono, saldo disponible y estado) para comprobar si tengo fondos suficientes antes de subir al autobús e intentar validar mi viaje.

**Prueba de aceptación**
- Comprobar que al abrir la sección de pagos o bonobús en la aplicación, se muestra el saldo en euros actualizado, reflejando los pagos anteriores.
- Se debe aplicar la regla de negocio RN.03: Verificar que el sistema no permite que el saldo mostrado supere los 50€.
- Se debe aplicar la regla de negocio RN.05: Comprobar que, si la tarjeta ha sido bloqueada, el estado mostrado es "Bloqueado" y no "Activo".

#### R.I.04. Historial de validaciones y transbordos

Como pasajero quiero visualizar un registro de mis viajes recientes (fecha, hora, línea, importe pagado y si se aplicó descuento por transbordo) para llevar un control personal de mis gastos en transporte.

**Prueba de aceptación**
- Comprobar que tras validar el billete, el nuevo viaje aparece en la lista del historial.
- Se debe aplicar la regla de negocio RN.06 y RN.07: Verificar que si el viaje se realiza en menos de 1 hora respecto al anterior y con el mismo bonobús, el historial muestra correctamente la aplicación del descuento en el importe.

#### 4.1.2. Reglas de negocio

##### RN.01. Saldo suficiente: 
Para que una validación NFC sea exitosa, el saldo del bonobús virtual debe ser igual o superior al coste de la tarifa vigente

##### RN.02. Autobús completo:
Si el número de validaciones menos el número de bajadas iguala la capacidad máxima del autobús, el estado de ocupación pasará automáticamente a "Completo" y se ocultará el tiempo de llegada para los usuarios de la siguiente parada.

##### RN.03. Límite de saldo:
El saldo máximo acumulable en un bonobús virtual recargable no podrá superar los 50€.

##### RN.04. Aforo lógico: 
El número actual de pasajeros a bordo de un autobús nunca puede ser un valor negativo.

##### RN.05. Bloqueo antifraude: 
Si el sistema registra más de cinco validaciones consecutivas del mismo título de transporte en la misma máquina en menos de 2 minutos, el bonobús virtual se bloqueará temporalmente.

##### RN.06. Descuento en el trasbordo:
Para que se efectúe el descuento en el trasbordo tienes que haber utilizado el pago con el mismo bonobus o tarjeta.

##### RN.07. Hora de descuento de trasbordo
Para que se efectue el descuento del trasbordo tiene que pasar menos de 1 hora entre los pagos.





### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales

#### R.N.F.01. Rendimiento de la aplicación

Como usuario del transporte público, quiero que la aplicación responda rápidamente a mis consultas, para consultar la información de los autobuses sin esperas innecesarias.

**Criterio de aceptación**

- Las consultas de ubicación, paradas y ocupación deben responder en menos de 1 segundos en condiciones normales de funcionamiento.
- Las consultas principales deben responder en menos de 2 segundos con hasta 1.000 usuarios concurrentes.

#### R.N.F.02. Actualización de la información

Como usuario del transporte público, quiero que la información sobre la ubicación y la ocupación de los autobuses se actualice periódicamente, para tomar decisiones basadas en datos recientes.

**Criterio de aceptación**

- La aplicación debe mostrar cuándo se actualizaron por última vez los datos de ubicación y ocupación.
- La aplicación debe indicar cuando la información disponible está desactualizada o no se puede obtener.

#### R.N.F.03. Seguridad y privacidad

Como usuario del transporte público, quiero que mis datos personales y la información de mi bonobús estén protegidos, para evitar accesos y operaciones no autorizados.

**Criterio de aceptación**

- Solo los usuarios autorizados pueden acceder a la información privada de su cuenta.
- Las operaciones de consulta y modificación del bonobús deben verificar los permisos correspondientes.

#### R.N.F.04. Disponibilidad del sistema

Como usuario del transporte público, quiero que SmartBus esté disponible cuando necesite consultar información o utilizar mi bonobús virtual, para poder planificar y realizar mis viajes.

**Criterio de aceptación**

- Si el servicio no está disponible, la aplicación debe informar al usuario y no mostrar datos antiguos como si fueran actuales.

#### R.N.F.05. Usabilidad y accesibilidad

Como usuario del transporte público, quiero que la aplicación tenga una interfaz clara y fácil de utilizar, para consultar información y realizar operaciones sin dificultad.

**Criterio de aceptación**

- Los mensajes de error deben explicar el problema y, cuando sea posible, indicar cómo continuar.
- Las funciones principales, como consultar una parada, comprobar la ocupación y acceder al bonobús virtual, deben estar identificadas claramente.

#### R.N.F.06. Precisión de la ubicación

La información GPS debe permitir conocer la posición del autobús con suficiente precisión.

**Criterio de aceptación**

- En condiciones normales, el error de ubicación no debe superar los 20 metros

#### R.N.F.07. Tiempo de validación NFC

La validación del bonobús virtual debe realizarse rápidamente para evitar colas al subir al autobús.

**Criterio de aceptación**

- El resultado de la validación debe mostrarse en menos de 2 segundos en condiciones normales.

#### R.N.F.08. Gestión de la pérdida de conexión

La aplicación debe informar de los problemas de conectividad sin presentar información desactualizada como si fuera actual.

**Criterio de aceptación**

- Si se pierde la conexión, debe mostrarse un aviso y la hora de la última actualización disponible.

#### R.N.F.09. Compatibilidad

La aplicación debe funcionar correctamente en los dispositivos móviles y relojes intelegentes compatibles con el proyecto.

**Criterio de aceptación**

- Mantener las funciones principales en las versiones de Android e iOS que se definan como compatibles.

#### R.N.F.10. Protección de las operaciones de pago

El sistema debe garantizar que las operaciones de validación y descuento de saldo se procesen de forma consistente.

**Criterio de aceptación**

- Una misma operación identificada no debe descontar el saldo más de una vez, aunque se reintente por un fallo de conexión.

-- fin entregable 1 --

## 5. Modelo conceptual

### 5.1. Diagramas de clases UML

- con restricciones.

### 5.2. Escenarios de prueba

- con descripción textual y diagrama de objetos UML.

## 6. Matrices de trazabilidad

- Matriz de trazabilidad entre los elementos del modelo conceptual y los requisitos.

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:------|:-----------|:-----------|:-----------|:-----------|
| RI-1  | X          | X          | X          | X          |
| RI-2  |            | X          |            | X          |
| RF-1  |            | X          |            | X          |
| RF-2  | X          |            | X          | X          |
| RN-1  |            | X          |            |            |
| RN-2  | X          | X          | X          |            |
| ...   |            |            |            |            |

-- fin entregable 2 --

## 7. Modelo relacional en 3FN

- Relaciones obtenidas al aplicar la transformación del modelo conceptual.

### 7.1.  Justificación de la estrategia de transformación de jerarquías

- si se identificaron jerarquías en el MC.


### 8. Matriz de trazabilidad MC/SQL (opcional):

- Restricciones sobre el MC / Elementos del modelo tecnológico (SQL) (Triggers, checks, etc.)
- Incluir Reglas de negocio — Constraints/Triggers en las matrices de trazabilidad para el entregable 3

|       | EntidadX   | AsociaciónX  | RestricciónX  | Entidad2 ...   | 
|:-------|:-------|:-------|:-------|:-------|
| TABLA-1 |        |        |        |        |
| TABLA-2 |        |        |        |        |
| TABLA-3 |        |        |        |        |
| TABLA-4 |        |        |        |        |
| TRIG-1 |        |        |        |        |
| TRIG-2 | X      | X      |        | X      |
| TRIG-3 |        | X      |        | X      |
| TRIG-4 |        |        | X      |        |
| CONST-1 |        |        |        |        |
| CONST-2 | X      | X      |        | X      |
| CONST-3 |        | X      |        | X      |
| CONST-4 |        |        | X      |        |

Se consideran todo tipo de constraints declarativas (aquellas definidas durante el CREATE TABLE).
-- fin entregable 3 --

## Referencias


