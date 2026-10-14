# SmartBus

## Miembros del grupo LX-XXX-X (sustituir)

1. Espina Apellaniz, David
1. Apellidos, Nombre
1. Apellidos, Nombre
1. Apellidos, Nombre

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

### 3.2. Usuarios del sistema

## 4. Catálogo de requisitos

### 4.1. Requisitos funcionales

#### R.F.01. Título requisito funcional

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- Se debe aplicar la regla de negocio R.N.XX.
- ...

#### 4.1.1. Requisitos de información

##### R.I.01. Título requisito de información

Como [tipo de usuario]
quiero [servicio]
para [razón]

**Prueba de aceptación**
- Descripción de la primera comprobación a realizar
- Descripción de la segunda comprobación a realizar
- ...

#### 4.1.2. Reglas de negocio

##### R.N.01. Título regla negocio

Descripción de la regla de negocio.

### 4.2. Mapa de historias de usuario (opcional)

### 4.3. Requisitos no funcionales (opcional)

**R.N.F. 01. Título requisito no funcional**
Como [tipo de usuario]
quiero [servicio]
para [razón]

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


