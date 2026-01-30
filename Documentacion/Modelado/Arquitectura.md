**2. SELECCIÓN DEL DISEÑO ARQUITECTÓNICO**

**Arquitectura seleccionada**  
Arquitectura en capas basada en Domain-Driven Design (DDD)

**Descripción de la arquitectura**  
La arquitectura en capas basada en Domain-Driven Design organiza el sistema colocando el dominio del problema como el núcleo principal del software. En esta arquitectura, las reglas de negocio y la lógica central del videojuego se mantienen independientes de la interfaz de usuario y de los aspectos técnicos, como la persistencia de datos o los servicios externos.  
El sistema se divide en capas bien definidas, lo que permite una mejor organización, mantenimiento y escalabilidad del proyecto.

**Justificación de la arquitectura seleccionada**  
Se seleccionó esta arquitectura debido a que el proyecto NovaBounty: Eclipse Protocol presenta múltiples reglas de negocio complejas e interconectadas, tales como:

- Sistema de progresión por rangos y desbloqueo de zonas.
- Sistema de misiones de cazarrecompensas.
- Combate aéreo y combate en tierra en Realidad Aumentada.
- Economía virtual basada en Novacoins.
- Sistema de obtención y fusión de piezas para armas y naves.

Una arquitectura centrada en el dominio permite que estos sistemas se mantengan desacoplados de la interfaz AR, facilitando modificaciones, ampliaciones y mantenimiento sin afectar el funcionamiento general del videojuego.


**ESTRUCTURA DE LA ARQUITECTURA APLICADA AL PROYECTO**

**Capa de Dominio**  
Contiene las reglas de negocio principales del juego:

- Lógica de combate.
- Sistema de rangos.
- Economía del juego.
- Reglas de recompensas y mejoras.

**Capa de Aplicación**  
Gestiona los casos de uso del sistema:

- Gestión de misiones.
- Flujo de progresión del jugador.
- Coordinación entre sistemas.

**Capa de Presentación**  
Encargada de la interacción con el usuario:

- Interfaces de Realidad Aumentada.
- HUD y controles del jugador.
- Retroalimentación visual y auditiva.

**Capa de Infraestructura**  
Maneja los aspectos técnicos:

- Almacenamiento de datos.
- Persistencia del progreso.
- Gestión de recursos del sistema.


**BENEFICIOS DE LA ARQUITECTURA PARA EL PROYECTO**

- Facilita la comprensión del sistema.
- Permite escalar nuevas mecánicas de juego.
- Aísla la lógica del negocio de la interfaz.
- Mejora la mantenibilidad y organización del código.


**3. DISEÑO DETALLADO**

Para el diseño detallado del proyecto NovaBounty: Eclipse Protocol se seleccionaron patrones de diseño que permiten organizar la lógica del sistema, mejorar la mantenibilidad del código y facilitar la evolución del videojuego. Los patrones fueron elegidos de acuerdo con las necesidades del proyecto, el tipo de arquitectura centrada en el dominio y las mecánicas del juego.


**3.1 PATRONES DE DISEÑO CREACIONALES**

**Factory Method (Método de fábrica)**

**Aplicación en el proyecto**  
Se utiliza para la creación de enemigos, armas y piezas tanto en el combate aéreo como en el combate en tierra

**Justificación**  
El videojuego maneja distintos tipos de enemigos y equipamiento que varían según el rango, la zona y la dificultad. El patrón Factory Method permite crear estas instancias sin acoplar el sistema a clases concretas, facilitando la expansión del contenido del juego.

**Ejemplo de uso**

- Creación de enemigos según el rango del jugador.
- Generación de piezas con diferente rareza.

**Singleton**

**Aplicación en el proyecto**  
Se aplica en sistemas globales del juego, como:

- Gestor de economía (Novacoin).
- Gestor de progreso del jugador.
- Controlador del estado general de la partida.

**Justificación**  
Estos sistemas deben tener una única instancia durante la ejecución del juego para evitar inconsistencias en los datos del jugador y la economía.


**3.2 PATRONES DE DISEÑO ESTRUCTURALES**

**Facade (Fachada)**

**Aplicación en el proyecto**  
Se utiliza para simplificar la interacción entre la capa de presentación (AR) y los subsistemas internos del juego.

**Justificación**  
El combate, la economía, las misiones y la progresión son sistemas complejos. El patrón Fachada permite exponer una interfaz sencilla para que la capa de presentación no dependa directamente de la lógica interna del dominio.

**Ejemplo de uso**

- Iniciar una misión.
- Finalizar un combate y otorgar recompensas.

**Decorator (Decorador)**

**Aplicación en el proyecto**  
Se emplea para mejorar dinámicamente armas y naves mediante el sistema de fusión de piezas.

**Justificación**  
El patrón Decorator permite añadir mejoras como daño extra, mayor resistencia o habilidades especiales sin modificar la clase base del arma o nave, apoyando la progresión continua del jugador.


**3.3 PATRONES DE DISEÑO DE COMPORTAMIENTO**

**Strategy (Estrategia)**

**Aplicación en el proyecto**  
Se utiliza para definir distintos comportamientos de combate de los enemigos.

**Justificación**  
Los enemigos presentan comportamientos variables como ataques normales, ataques falsos, habilidades especiales o defensas prolongadas. El patrón Estrategia permite cambiar el comportamiento sin alterar la estructura principal del enemigo.

**Ejemplo de uso**

- Enemigos agresivos.
- Enemigos defensivos.
- Enemigos con habilidades especiales.

**State (Estado)**

**Aplicación en el proyecto**  
Se aplica al sistema de combate en tierra para gestionar los estados del enemigo.

**Justificación**  
El comportamiento del rival cambia según su estado (defendiendo, atacando, cansado). El patrón Estado permite modificar su comportamiento dinámicamente sin condicionales complejos.

**Estados identificados**

- Estado de defensa.
- Estado de ataque.
- Estado de cansancio.

**Observer (Observador)**

**Aplicación en el proyecto**  
Se utiliza para actualizar la interfaz del usuario cuando ocurren cambios en el estado del juego.

**Justificación**  
El HUD del juego debe reaccionar automáticamente a eventos como:

- Daño recibido.
- Cambio de escudos.
- Obtención de recompensas.

El patrón Observador permite notificar estos cambios sin acoplar la lógica del dominio a la interfaz AR.


**3.4 BENEFICIOS DEL DISEÑO DETALLADO**

- Mejora la organización y legibilidad del código.
- Facilita la reutilización de componentes.
- Permite escalar el sistema con nuevas mecánicas.
- Reduce el acoplamiento entre sistemas.
- Refuerza la arquitectura centrada en el dominio.
