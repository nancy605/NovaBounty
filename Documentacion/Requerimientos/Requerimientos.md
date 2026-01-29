## Técnicas seleccionadas para la recolección de requerimientos
### 1. Descomposición funcional

#### Justificación
Se seleccionó la técnica de descomposición funcional debido a que el proyecto NovaBounty: Eclipse Protocol integra múltiples sistemas interconectados, como combate aéreo y terrestre en Realidad Aumentada, progresión por rangos, misiones y economía virtual. Esta técnica permite dividir el sistema en funciones más pequeñas y comprensibles, facilitando la identificación clara de los requerimientos funcionales.
#### Elaboración
El videojuego fue descompuesto jerárquicamente, partiendo del sistema principal hacia sus subsistemas y subfunciones. Se identificaron los módulos principales: sistema de progresión, sistema de misiones, sistema de combate, sistema de economía y sistema de equipamiento. Cada módulo fue analizado para definir sus funciones específicas y su relación con otros sistemas.
A partir de esta descomposición se establecieron requerimientos como:
Progresión del jugador mediante un sistema de rangos.
Desbloqueo de zonas según el nivel alcanzado.
Alternancia entre combate aéreo y combate en tierra.
Administración de una moneda virtual para mejoras de equipamiento.


### Evidencia
- Diagrama jerárquico de descomposición funcional.
- Lista de módulos y subfunciones identificadas.
- Requerimientos funcionales derivados de cada módulo.
  
Documentacion/Requerimientos/descomposicion_funcional.png




#### 2. Benchmarking
#### Justificación
Se utilizó la técnica de benchmarking con el objetivo de analizar videojuegos del mismo género para identificar buenas prácticas en sistemas de combate, progresión y recompensas. Esta técnica permitió comparar características similares y tomar decisiones fundamentadas para el diseño del proyecto, evitando errores comunes y fortaleciendo la experiencia del jugador.
#### Elaboración
Se realizó un análisis comparativo de videojuegos de acción y ciencia ficción que incorporan:
Sistemas de rangos y progresión.
Combate aéreo y combate cuerpo a cuerpo.
Recompensas y mejora de equipamiento.
Del análisis se obtuvieron lineamientos para definir:
Escalado progresivo de dificultad.
Economía basada en una moneda virtual.
Sistema de obtención y fusión de piezas como mecánica de mejora continua.
#### Evidencia
- Tabla comparativa de los videojuegos analizados.
- Identificación de fortalezas y debilidades detectadas.
- Decisiones de diseño tomadas a partir del análisis comparativo.
  
Documentacion/Requerimientos/benchmarking_tabla.png


