-----

## RFC-AI 0002: Taxonomía de Agentes y Sistemas Multi-Agente

Internet-Draft Grupo Promotor de la Iniciativa RFC-AI
Estado Previsto: Informativo 9 de Julio de 2025
Expira: 9 de Enero de 2026

### Abstract

Este documento establece una **taxonomía fundamental** para clasificar y describir los diferentes tipos de **agentes** y **sistemas multi-agente (MAS)** en el contexto de la Inteligencia Artificial. Con el rápido avance de las tecnologías de IA, especialmente los Modelos de Lenguaje Grandes (LLMs) y su integración en arquitecturas de agentes autónomos, surge la necesidad crítica de un marco de referencia común para la terminología y la comprensión de estos sistemas complejos. Este RFC-AI tiene como objetivo proporcionar definiciones claras y consensuadas de las categorías de agentes y las estructuras de los MAS, facilitando la comunicación, el diseño, el desarrollo, la evaluación y la estandarización futura en este ámbito. Sirve como documento *informativo*, complementando el RFC-AI 0001 (Glosario Fundamental).

### Estado de este Memo

Este Internet-Draft es un trabajo en progreso y no representa el estándar de ninguna organización. Está siendo distribuido para su revisión y consideración por parte de la comunidad interesada en la estandarización de tecnologías de Inteligencia Artificial y Agentes. Los comentarios sobre este borrador deben enviarse a la lista de correo de la Iniciativa RFC-AI (dirección\_lista@ejemplo.com) o al Grupo Promotor.

Los documentos de borrador de Internet son documentos de trabajo del Grupo de Trabajo de Ingeniería de Internet (IETF), sus áreas y sus grupos de trabajo. Tenga en cuenta que otros grupos también pueden distribuir documentos de trabajo como Internet-Drafts. Los Internet-Drafts son documentos de borrador válidos por un máximo de seis meses y pueden ser actualizados, reemplazados u obsoletos por otros documentos en cualquier momento. No es apropiado utilizar los Internet-Drafts como material de referencia o citarlos de otra forma que no sea como "trabajo en progreso" ("work in progress").

### Tabla de Contenidos

1.  Introducción
2.  Definición de Agente (Revisión y Expansión)
3.  Clasificación de Agentes por Arquitectura y Comportamiento
    3.1. Agentes Reactivos Simples
    3.2. Agentes Reactivos Basados en Modelos
    3.3. Agentes Basados en Objetivos
    3.4. Agentes Basados en Utilidad
    3.5. Agentes de Aprendizaje (Learning Agents)
    3.6. Agentes Híbridos
    3.7. Agentes LLM-based
4.  Clasificación de Sistemas Multi-Agente (MAS)
    4.1. MAS Cooperativos
    4.2. MAS Competitivos
    4.3. MAS Híbridos/Coexistentes
    4.4. MAS Jerárquicos
    4.5. MAS Distribuidos
5.  Interacciones y Comunicación entre Agentes (Mención)
6.  Consideraciones de Seguridad
7.  Consideraciones de Privacidad
8.  Consideraciones Específicas de IA
9.  Referencias
10. Dirección del Autor

-----

### 1\. Introducción

El concepto de "agente" ha sido fundamental en la Inteligencia Artificial desde sus inicios, proporcionando un marco conceptual para diseñar sistemas autónomos capaces de percibir, razonar y actuar en entornos complejos. Con la aparición de Modelos de Lenguaje Grandes (LLMs) y su creciente integración como componentes centrales de agentes (los "Agentes LLM-based"), así como el interés en orquestar múltiples de estos agentes en **sistemas multi-agente (MAS)** para resolver problemas complejos, la diversidad de arquitecturas y comportamientos de agentes ha proliferado.

Esta diversidad, si bien es un motor de innovación, también introduce desafíos en la comunicación y la estandarización. La falta de una taxonomía clara y consensuada puede llevar a ambigüedades, dificultar la comparación de sistemas y obstaculizar los esfuerzos de colaboración.

El objetivo de este RFC-AI 0002 es proporcionar un marco clasificatorio para los agentes y los sistemas multi-agente, basándose en conceptos fundamentales de la teoría de agentes y extendiéndolos para incluir las nuevas arquitecturas emergentes. Este documento es **informativo** y busca ofrecer un lenguaje común para describir estos sistemas, lo que es esencial para futuros RFC-AIs que abordarán aspectos más técnicos de interoperabilidad, seguridad y evaluación. Complementa el RFC-AI 0001 [RFC-AI.0001], que define el glosario fundamental.

-----

### 2\. Definición de Agente (Revisión y Expansión)

En el contexto de este documento y de la Iniciativa RFC-AI, un **Agente** se define como:

Una entidad autónoma que percibe su **entorno** a través de **sensores** y actúa sobre ese entorno a través de **actuadores**, a lo largo del tiempo, para lograr **objetivos** o **tareas** específicas, exhibiendo cierto grado de **autonomía** y, en muchos casos, **inteligencia**.

**Componentes Clave de un Agente:**

  * **Sensores:** Mecanismos a través de los cuales el agente recibe información de su entorno (ej., cámaras, micrófonos, APIs, flujos de datos).
  * **Actuadores:** Mecanismos a través de los cuales el agente realiza acciones en su entorno (ej., motores, interfaces de usuario, llamadas a funciones, ejecución de código).
  * **Entorno:** El contexto o espacio en el que el agente opera y con el que interactúa. Puede ser físico (un robot en una habitación) o digital (un agente de software en una red, un LLM interactuando con una base de datos).
  * **Autonomía:** La capacidad de un agente para operar sin intervención humana constante, tomando decisiones y ejecutando acciones de forma independiente dentro de un marco o reglas predefinidas.
  * **Objetivos/Tareas:** Los resultados deseados o las acciones que el agente está programado para lograr o realizar.

Esta definición es amplia para abarcar una variedad de implementaciones, desde agentes robóticos hasta agentes de software basados en LLMs.

-----

### 3\. Clasificación de Agentes por Arquitectura y Comportamiento

Los agentes pueden clasificarse según su complejidad interna, su capacidad de razonamiento y cómo toman decisiones.

#### 3.1. Agentes Reactivos Simples (Simple Reflex Agents)

  * **Descripción:** Agentes que toman decisiones puramente basadas en la percepción actual del entorno, siguiendo un conjunto de reglas de condición-acción predefinidas. No tienen memoria interna del historial de percepciones ni de los efectos de sus acciones.
  * **Características:** Comportamiento determinista, rápido, sin estado, adecuado para entornos completamente observables y reglas claras.
  * **Ejemplos:** Termostato, agente de aspiradora básico (gira si choca con algo), sistema de alerta simple.

#### 3.2. Agentes Reactivos Basados en Modelos (Model-based Reflex Agents)

  * **Descripción:** Extienden los agentes reactivos simples al mantener un estado interno (un "modelo" del mundo) que les permite rastrear partes no observables del entorno o recordar percepciones pasadas. Utilizan tanto la percepción actual como este estado interno para tomar decisiones.
  * **Características:** Tienen memoria, pueden operar en entornos parcialmente observables, pero aún se basan en reglas de condición-acción.
  * **Ejemplos:** Agente de navegación que recuerda el mapa de un área, sistema de control de tráfico que rastrea el flujo de vehículos.

#### 3.3. Agentes Basados en Objetivos (Goal-based Agents)

  * **Descripción:** Además de mantener un modelo del mundo, estos agentes tienen **objetivos** a los que intentan llegar. Utilizan este modelo y sus objetivos para planificar secuencias de acciones que los lleven del estado actual a un estado objetivo. Requieren una capacidad de búsqueda o planificación.
  * **Características:** Comportamiento dirigido a objetivos, capacidad de planificación, pueden explorar diferentes secuencias de acciones.
  * **Ejemplos:** Agente de planificación de rutas, agente de juego de ajedrez que busca el jaque mate, sistema de automatización industrial que busca completar una tarea de ensamblaje.

#### 3.4. Agentes Basados en Utilidad (Utility-based Agents)

  * **Descripción:** Similares a los agentes basados en objetivos, pero añaden una función de **utilidad** que asigna un valor numérico a diferentes estados del mundo o secuencias de acciones. El agente busca maximizar esta utilidad, lo que le permite elegir entre múltiples formas de alcanzar un objetivo o ponderar objetivos conflictivos. Es útil en entornos inciertos o con múltiples resultados deseables/indeseables.
  * **Características:** Racionalidad basada en la optimización de utilidad, toma de decisiones en entornos inciertos, manejo de compensaciones.
  * **Ejemplos:** Agente de inversión financiera, agente de diagnóstico médico que pondera riesgos y beneficios, sistema de control de robots con gestión de recursos limitados.

#### 3.5. Agentes de Aprendizaje (Learning Agents)

  * **Descripción:** Cualquier agente que mejora su rendimiento con la experiencia. Contienen un **elemento de aprendizaje** (que realiza mejoras), un **elemento de rendimiento** (que selecciona acciones externas), un **crítico** (que retroalimenta al elemento de aprendizaje sobre el rendimiento) y un **generador de problemas** (que sugiere nuevas acciones para explorar y aprender).
  * **Características:** Adaptativos, capaces de mejorar con el tiempo, pueden descubrir nuevas reglas o estrategias.
  * **Ejemplos:** Agente de juego que mejora su estrategia, sistemas de recomendación, vehículos autónomos que aprenden a navegar. Pueden combinarse con cualquier arquitectura anterior (reactivo con aprendizaje, basado en objetivos con aprendizaje, etc.).

#### 3.6. Agentes Híbridos

  * **Descripción:** Agentes que combinan dos o más de las arquitecturas anteriores para aprovechar sus fortalezas. Por ejemplo, un agente que usa un componente reactivo para acciones rápidas y un componente basado en objetivos para planificación a largo plazo.
  * **Características:** Flexibles, robustos, optimizados para diferentes niveles de abstracción.
  * **Ejemplos:** Un robot que usa reglas reactivas para evitar obstáculos inmediatos pero planifica su ruta con un objetivo global, un asistente virtual que combina NLU reactivo con planificación de tareas complejas.

#### 3.7. Agentes LLM-based (Agentes Basados en Modelos de Lenguaje Grandes)

  * **Descripción:** Agentes que utilizan uno o más Modelos de Lenguaje Grandes (LLMs) como su componente central de razonamiento o "cerebro". El LLM puede ser responsable de la planificación, la interpretación de percepciones, la toma de decisiones, la generación de acciones o la interacción con el entorno. A menudo, estos agentes combinan el LLM con otras herramientas (APIs, bases de datos, búsqueda en la web) para extender sus capacidades más allá del puro procesamiento de texto.
  * **Características:** Capacidad de razonamiento lingüístico avanzado, flexibilidad en la comprensión de tareas, adaptabilidad a nuevas instrucciones, a menudo requieren mecanismos para evitar alucinaciones y gestionar el contexto. Pueden exhibir características de agentes basados en objetivos, utilidad o aprendizaje, dependiendo de cómo se utilice el LLM y las herramientas auxiliares.
  * **Ejemplos:** Agentes de automatización de tareas con LLM, agentes de investigación autónomos, asistentes virtuales conversacionales avanzados que pueden usar herramientas.

-----

### 4\. Clasificación de Sistemas Multi-Agente (MAS)

Un **Sistema Multi-Agente (MAS)** se define como un sistema que consiste en múltiples **agentes** que interactúan entre sí (y a veces con entidades no-agente) en un **entorno** compartido para lograr objetivos, que pueden ser individuales, colectivos o una combinación.

Los MAS pueden clasificarse según la naturaleza de la interacción y la organización de los agentes.

#### 4.1. MAS Cooperativos

  * **Descripción:** Los agentes en estos sistemas tienen un objetivo común y trabajan juntos para lograrlo. Comparten información, coordinan acciones y pueden depender unos de otros.
  * **Características:** Objetivo común, coordinación explícita o implícita, alta comunicación y colaboración.
  * **Ejemplos:** Enjambres de drones para mapeo, robots colaborativos en una línea de montaje, agentes de software que resuelven un problema de optimización distribuida.

#### 4.2. MAS Competitivos

  * **Descripción:** Los agentes en estos sistemas tienen objetivos individuales que están en conflicto o son mutuamente excluyentes. Compiten por recursos, información o para alcanzar sus propios objetivos antes que otros. A menudo se estudian con herramientas de teoría de juegos.
  * **Características:** Objetivos divergentes, competencia por recursos, interacciones estratégicas.
  * **Ejemplos:** Agentes de trading en mercados financieros, agentes de juego de estrategia (ej. ajedrez contra otro agente), simulaciones de ecología con agentes depredadores/presas.

#### 4.3. MAS Híbridos/Coexistentes

  * **Descripción:** Sistemas donde algunos agentes pueden cooperar para ciertos sub-objetivos, mientras que otros compiten, o donde los agentes simplemente coexisten y persiguen sus propios objetivos con una interacción mínima o indirecta.
  * **Características:** Mezcla de cooperación y competición, o independencia relativa.
  * **Ejemplos:** Simulación de una economía de mercado, sistemas de gestión de tráfico con vehículos autónomos y humanos, simulaciones sociales.

#### 4.4. MAS Jerárquicos

  * **Descripción:** La interacción y el control dentro del MAS se estructuran en niveles. Hay agentes "líderes" o "superiores" que dirigen o asignan tareas a agentes "subordinados", que a su vez pueden tener sus propios subordinados.
  * **Características:** Estructura de árbol o jerárquica, control centralizado o semi-centralizado, roles bien definidos.
  * **Ejemplos:** Sistema de control de flota de vehículos donde un agente central asigna rutas a agentes de vehículos individuales, un sistema de gestión de fábrica con un agente coordinador principal.

#### 4.5. MAS Distribuidos

  * **Descripción:** Los agentes operan de forma más independiente, sin un control centralizado fuerte. Las decisiones y el procesamiento se distribuyen entre los agentes, que interactúan principalmente de forma peer-to-peer o a través de un entorno compartido.
  * **Características:** Sin punto único de fallo, robustez, escalabilidad, coordinación emergente o basada en normas locales.
  * **Ejemplos:** Redes de sensores distribuidas, sistemas de computación grid/cloud con asignación autónoma de tareas, enjambres de robots sin líder central.

-----

### 5\. Interacciones y Comunicación entre Agentes (Mención)

Mientras que este documento se centra en la taxonomía, es importante destacar que la comunicación y la interacción son pilares de los sistemas multi-agente. Futuros RFC-AIs profundizarán en:

  * **Lenguajes de Comunicación de Agentes (ACLs - Agent Communication Languages):** Formatos y protocolos estandarizados para que los agentes intercambien mensajes (ej., FIPA ACL, KQML).
  * **Mecanismos de Coordinación:** Métodos y algoritmos que los agentes utilizan para coordinar sus acciones y resolver conflictos.
  * **Negociación y Acuerdos:** Procesos por los cuales los agentes llegan a pactos o contratos sobre tareas o recursos.

Estos temas serán cubiertos en detalle en RFC-AIs específicos dentro de la categoría de "Estándares de Interoperabilidad".

-----

### 6\. Consideraciones de Seguridad

Una taxonomía clara es esencial para la seguridad de los sistemas de agentes y multi-agente. Entender el tipo de agente o MAS (reactivo vs. basado en objetivos, cooperativo vs. competitivo) es crucial para identificar sus vulnerabilidades específicas. Por ejemplo, los agentes basados en LLMs pueden ser susceptibles a "prompt injection" (RFC-AI 0008), mientras que los MAS cooperativos pueden ser vulnerables a agentes maliciosos que subviertan la coordinación. Los futuros RFC-AIs sobre seguridad harán referencia a esta taxonomía para contextualizar las amenazas y las contramedidas. La claridad terminológica también reduce el riesgo de errores de diseño que podrían introducir vulnerabilidades.

-----

### 7\. Consideraciones de Privacidad

La taxonomía impacta la privacidad principalmente en la forma en que los agentes perciben, procesan y comparten información. Los agentes con memoria (reactivos basados en modelos, basados en objetivos, etc.) pueden retener datos sensibles, requiriendo consideraciones de privacidad en su diseño y ciclo de vida. En los MAS, la forma en que los agentes cooperativos comparten información podría crear riesgos de privacidad si no se gestiona adecuadamente. La identificación del tipo de agente y MAS facilitará la aplicación de estándares de privacidad (ej., RFC-AI 0010, RFC-AI 0012) para proteger los datos manejados por estos sistemas.

-----

### 8\. Consideraciones Específicas de IA

Esta taxonomía es fundamental para abordar aspectos específicos de IA como la **confiabilidad**, la **auditabilidad** y la **explicabilidad** en agentes y MAS. Los diferentes tipos de agentes tienen distintos grados de complejidad en su toma de decisiones, lo que afecta su explicabilidad. Un agente reactivo simple es más fácil de auditar que un agente basado en LLM que razona de forma compleja. Esta clasificación ayuda a establecer expectativas realistas para la transparencia y la responsabilidad. Además, comprender el tipo de interacción en un MAS es vital para asegurar que la emergencia de comportamientos colectivos sea predecible y controlable.

-----

### 9\. Referencias

  * [1] Russell, S. J., & Norvig, P. (2020). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson. (Referencia fundamental para las arquitecturas de agentes tradicionales).
  * [2] Wooldridge, M. (2009). *An Introduction to MultiAgent Systems* (2nd ed.). John Wiley & Sons. (Referencia clave para los MAS).
  * [3] RFC-AI 0000: Declaración de Propósito e Introducción a la Iniciativa de Estandarización RFC-AI.
  * [4] RFC-AI 0001: Glosario Fundamental de IA/ML/LLM/Agentes.
  * [5] RFC-AI 0008: Definición y Clasificación de Vulnerabilidades en LLMs y Agentes.
  * [6] RFC-AI 0010: Guía Técnica para la Documentación de Datos de Entrenamiento.
  * [7] RFC-AI 0012: Formatos Básicos para Reportar Incertidumbre o Confianza de un Modelo.
  * [8] Example Mailing List / Website (Hipótesis). [http://www.ejemplo.com/iniciativa\_rfc-ai](https://www.google.com/search?q=http://www.ejemplo.com/iniciativa_rfc-ai)

-----

### 10\. Dirección del Autor

Grupo Promotor de la Iniciativa RFC-AI
Dirección de Correo: dirección\_lista@ejemplo.com
URI: [http://www.ejemplo.com/iniciativa\_rfc-ai](https://www.google.com/search?q=http://www.ejemplo.com/iniciativa_rfc-ai)

-----
