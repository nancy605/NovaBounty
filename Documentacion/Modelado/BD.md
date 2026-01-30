## 4. Diseño de la Base de Datos
El diseño de la base de datos del proyecto **NovaBounty: Eclipse Protocol** tiene como propósito organizar de manera estructurada la información del sistema, garantizando la integridad de los datos, la correcta gestión del progreso del jugador y el soporte a las mecánicas principales del videojuego.



### 4.1 Justificación del Modelo de Datos

Para el sistema se seleccionó un **modelo de datos relacional**.

**Justificación:**

El modelo relacional es adecuado debido a que el videojuego maneja datos estructurados y altamente relacionados, tales como:

* Usuarios
* Personajes
* Misiones
* Recompensas
* Progreso del jugador
* Economía virtual

Este modelo permite:

* Establecer relaciones claras mediante **llaves primarias y foráneas**
* Evitar la duplicidad de información
* Garantizar la **integridad referencial** de los datos

Además, facilita:

* La consulta eficiente del progreso del jugador
* La gestión de misiones y recompensas
* La administración de la moneda virtual (**Novacoin**)

El modelo relacional es compatible con sistemas gestores de bases de datos ampliamente utilizados como **MySQL** y **PostgreSQL**, lo que favorece la **escalabilidad**, el **mantenimiento** y la **estabilidad** del sistema.



### 4.2 Diseño del Diagrama Entidad–Relación (DER)

El **Diagrama Entidad–Relación (DER)** representa gráficamente la estructura lógica de la base de datos, mostrando las entidades principales, sus atributos y las relaciones entre ellas.

#### Entidades Principales

* **Usuario**
* **Personaje**
* **Misión**
* **Progreso**
* **Recompensa**
* **Economía**

#### Relaciones Identificadas

* Un **usuario** puede tener uno o varios **personajes**.
* Un **personaje** puede completar múltiples **misiones**.
* Cada **misión** genera una o varias **recompensas**.
* El **progreso** registra el avance del personaje en cada misión.
* La **economía** se asocia a cada personaje para gestionar la moneda virtual.

El DER permite visualizar de forma clara la organización de los datos y asegura que las relaciones sean coherentes con la lógica interna del videojuego.



### Evidencia

* Diagrama Entidad–Relación donde se muestran:

  * Entidades
  * Atributos
  * Llaves primarias
  * Llaves foráneas




