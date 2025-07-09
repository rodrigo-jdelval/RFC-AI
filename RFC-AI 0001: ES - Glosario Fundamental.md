-----

## RFC-AI 0001: Glosario Fundamental de IA/ML/LLM/Agentes

Internet-Draft Grupo Promotor de la Iniciativa RFC-AI
Estado Previsto: Informativo 3 de Mayo de 2025
Expira: 3 de Noviembre de 2025

### Abstract

Este documento establece un **glosario fundamental de términos clave** relacionados con la Inteligencia Artificial (IA), el Machine Learning (ML), los Modelos de Lenguaje Grandes (LLM) y los Sistemas Multi-Agente (MCPs). El objetivo principal es proporcionar definiciones claras, concisas y consensuadas para facilitar una comunicación precisa y reducir la ambigüedad en el desarrollo, despliegue y estandarización de estas tecnologías. Este glosario sirve como un documento informativo que sienta las bases para futuros RFC-AIs, asegurando que todos los participantes en la Iniciativa RFC-AI y la comunidad en general utilicen un lenguaje común y entendido.

### Estado de este Memo

Este Internet-Draft es un trabajo en progreso y no representa el estándar de ninguna organización. Está siendo distribuido para su revisión y consideración por parte de la comunidad interesada en la estandarización de tecnologías de Inteligencia Artificial, LLM y Agentes. Los comentarios sobre este borrador deben enviarse a la lista de correo de la Iniciativa RFC-AI (dirección\_lista@ejemplo.com) o al Grupo Promotor.

Los documentos de borrador de Internet son documentos de trabajo del Grupo de Trabajo de Ingeniería de Internet (IETF), sus áreas y sus grupos de trabajo. Tenga en cuenta que otros grupos también pueden distribuir documentos de trabajo como Internet-Drafts. Los Internet-Drafts son documentos de borrador válidos por un máximo de seis meses y pueden ser actualizados, reemplazados u obsoletos por otros documentos en cualquier momento. No es apropiado utilizar los Internet-Drafts como material de referencia o citarlos de otra forma que no sea como "trabajo en progreso" ("work in progress").

### Tabla de Contenidos

1.  Introducción
2.  Términos Generales de IA
3.  Términos de Machine Learning (ML)
4.  Términos de Modelos de Lenguaje Grandes (LLM)
5.  Términos de Agentes y Sistemas Multi-Agente
6.  Términos de Seguridad y Responsabilidad en IA
7.  Consideraciones de Seguridad
8.  Consideraciones de Privacidad
9.  Consideraciones Específicas de IA
10. Referencias
11. Dirección del Autor

-----

### 1\. Introducción

El campo de la Inteligencia Artificial y sus subcampos, como el Machine Learning y los Modelos de Lenguaje Grandes, evolucionan a un ritmo vertiginoso. Esta rápida evolución ha llevado a una proliferación de terminología, a menudo utilizada de manera inconsistente o ambigua entre diferentes investigadores, desarrolladores, reguladores y el público en general. Esta falta de un lenguaje común obstaculiza la comunicación efectiva, dificulta la interoperabilidad y crea barreras para la comprensión y la estandarización.

El propósito de este RFC-AI 0001 es establecer un **glosario fundamental** de términos clave, proporcionando definiciones claras, concisas y consensuadas. Este documento es de naturaleza *informativa* y busca ser una referencia básica para todos los documentos subsiguientes de la Iniciativa RFC-AI, así como para cualquier persona que trabaje o se interese en el campo. Al acordar una terminología estándar, podemos construir una base sólida para futuros esfuerzos de estandarización en áreas como la interoperabilidad, la seguridad, la responsabilidad y la evaluación de la IA.

Las definiciones aquí presentadas buscan ser neutrales tecnológicamente cuando sea posible, centrándose en el concepto más que en una implementación específica, y están sujetas a revisión a medida que el campo evolucione.

-----

### 2\. Términos Generales de IA

  * **Inteligencia Artificial (IA):** Campo de la informática dedicado a crear sistemas o máquinas que pueden realizar tareas que normalmente requieren inteligencia humana, como el aprendizaje, la resolución de problemas, la percepción, la comprensión del lenguaje y la toma de decisiones.
  * **Algoritmo de IA:** Conjunto de reglas o instrucciones computacionales diseñadas para realizar una tarea específica dentro de un sistema de IA, a menudo aprendiendo de datos.
  * **Modelo de IA:** La representación de conocimiento o patrón aprendido por un algoritmo de IA a partir de datos. Es el resultado del proceso de entrenamiento y se utiliza para hacer predicciones o tomar decisiones.
  * **Sistema de IA:** Un sistema que comprende un modelo de IA, los datos que lo alimentan (entrada), la infraestructura que lo soporta y los mecanismos para su despliegue y operación, que interactúa con un entorno para lograr objetivos.
  * **Agente (en IA):** Entidad autónoma que percibe su entorno a través de sensores y actúa sobre ese entorno a través de actuadores, para lograr objetivos o tareas específicas.
  * **Agente Autónomo:** Un agente que opera sin intervención humana continua, tomando decisiones y ejecutando acciones de forma independiente dentro de un marco o reglas predefinidas.
  * **Inferencia (en IA):** Proceso de utilizar un modelo de IA ya entrenado para hacer predicciones, tomar decisiones o generar resultados a partir de nuevos datos de entrada.
  * **Entrenamiento (en IA):** Proceso de alimentar un algoritmo de IA con datos para ajustar los parámetros internos de un modelo, permitiéndole aprender patrones, hacer predicciones o realizar una tarea específica.
  * **Prompt Engineering:** El proceso de diseñar y refinar entradas de texto (prompts) para sistemas de IA, especialmente LLMs, con el fin de guiar su comportamiento y obtener resultados deseados.
  * **Sesgo (en modelos de IA):** Una tendencia sistemática y reproducible en un modelo de IA que lleva a resultados injustos, inexactos o discriminatorios para ciertos grupos o casos, a menudo debido a sesgos en los datos de entrenamiento o en el diseño del algoritmo.
  * **Explicabilidad (XAI - Explainable AI):** La capacidad de un sistema de IA para explicar su comportamiento, decisiones o predicciones de una manera comprensible para los humanos.

-----

### 3\. Términos de Machine Learning (ML)

  * **Machine Learning (ML):** Un subcampo de la IA que se centra en el desarrollo de algoritmos que permiten a los sistemas aprender de los datos, identificar patrones y tomar decisiones con una intervención humana mínima.
  * **Dataset (Conjunto de Datos):** Colección estructurada de datos utilizada para entrenar, validar o probar modelos de Machine Learning.
  * **Aprendizaje Supervisado:** Tipo de ML donde el modelo aprende de datos de entrada que están emparejados con resultados o etiquetas de salida correctos.
  * **Aprendizaje No Supervisado:** Tipo de ML donde el modelo busca patrones o estructuras ocultas en datos de entrada sin etiquetas predefinidas.
  * **Aprendizaje por Refuerzo:** Tipo de ML donde un agente aprende a tomar decisiones interactuando con un entorno, recibiendo recompensas o penalizaciones por sus acciones.
  * **Validación Cruzada:** Técnica para evaluar el rendimiento de un modelo de ML dividiendo el dataset en múltiples subconjuntos para entrenamiento y prueba de manera iterativa.
  * **Sobreajuste (Overfitting):** Fenómeno donde un modelo de ML aprende los datos de entrenamiento de manera demasiado específica, incluyendo el ruido, lo que resulta en un mal rendimiento con datos nuevos e invisibles.
  * **Subajuste (Underfitting):** Fenómeno donde un modelo de ML es demasiado simple para capturar los patrones subyacentes en los datos, lo que lleva a un bajo rendimiento tanto en los datos de entrenamiento como en los datos nuevos.

-----

### 4\. Términos de Modelos de Lenguaje Grandes (LLM)

  * **Modelo de Lenguaje Grande (LLM - Large Language Model):** Un tipo de modelo de IA basado en redes neuronales profundas (a menudo arquitecturas Transformer) entrenado en vastas cantidades de datos de texto y código, capaz de comprender, generar y manipular lenguaje humano.
  * **Token:** La unidad básica de texto que un LLM procesa. Puede ser una palabra completa, parte de una palabra o incluso un carácter, dependiendo del tokenizador.
  * **Alucinación (en LLMs):** Fenómeno por el cual un LLM genera información que parece plausible pero es incorrecta, inventada o no está respaldada por los datos de su entrenamiento o por el contexto proporcionado.
  * **Contexto (en LLMs):** La información de entrada previa (prompts, historial de conversación) que un LLM utiliza para generar su respuesta. La longitud del contexto suele estar limitada por la ventana de contexto del modelo.
  * **Ventana de Contexto:** El número máximo de tokens (entrada y/o salida) que un LLM puede procesar o considerar en una sola interacción o "turno" de conversación.
  * **Fine-tuning (Ajuste Fino):** El proceso de entrenar un LLM pre-entrenado en un dataset más pequeño y específico para adaptar sus capacidades a una tarea o dominio particular.
  * **Generación de Lenguaje Natural (NLG - Natural Language Generation):** La capacidad de un sistema de IA para producir texto coherente y lingüísticamente correcto a partir de datos estructurados o un contexto dado.
  * **Comprensión del Lenguaje Natural (NLU - Natural Language Understanding):** La capacidad de un sistema de IA para interpretar y derivar significado del lenguaje humano.

-----

### 5\. Términos de Agentes y Sistemas Multi-Agente

  * **Sistema Multi-Agente (MAS - Multi-Agent System):** Un sistema compuesto por múltiples agentes autónomos que interactúan entre sí y con su entorno para lograr objetivos individuales o colectivos.
  * **Coordinación de Agentes:** El proceso por el cual múltiples agentes trabajan juntos, gestionando sus interacciones para lograr un objetivo compartido o evitar conflictos.
  * **Negociación de Agentes:** Un proceso de comunicación entre agentes para llegar a un acuerdo sobre un plan de acción o la distribución de recursos.
  * **Entorno (de Agente):** El espacio o contexto en el que opera un agente, con el que interactúa a través de percepciones y acciones. Puede ser físico o digital.
  * **Percepción (de Agente):** La información que un agente recibe de su entorno a través de sus sensores.
  * **Acción (de Agente):** Una operación que un agente puede realizar en su entorno a través de sus actuadores.

-----

### 6\. Términos de Seguridad y Responsabilidad en IA

  * **Ataque Adversario (Adversarial Attack):** Un intento deliberado de engañar un modelo de IA mediante la introducción de pequeñas e imperceptibles perturbaciones en los datos de entrada, que provocan que el modelo genere una salida incorrecta.
  * **Inyección de Prompts (Prompt Injection):** Un tipo de ataque adversario en LLMs donde entradas maliciosas en el prompt manipulan el modelo para ignorar instrucciones previas o realizar acciones no deseadas.
  * **Jailbreaking (en LLMs):** Técnicas utilizadas para eludir las salvaguardas o filtros de seguridad de un LLM, induciéndolo a generar contenido que normalmente rechazaría (ej. información dañina, sesgada o peligrosa).
  * **Privacidad Diferencial:** Un marco y un conjunto de técnicas para compartir información sobre un dataset mientras se protege la privacidad de los individuos en ese dataset.
  * **Robo de Modelo (Model Stealing/Extraction):** Un ataque donde un adversario infiere o reconstruye un modelo de IA, o sus propiedades, consultando el modelo objetivo a través de una API.
  * **Envenenamiento de Datos (Data Poisoning):** Un ataque donde se inyectan datos maliciosos en el conjunto de entrenamiento de un modelo de IA para degradar su rendimiento o inducir comportamientos específicos no deseados.
  * **Responsabilidad (Accountability - en IA):** La capacidad de atribuir y responsabilizar a individuos u organizaciones por los resultados y el impacto de los sistemas de IA, incluyendo la capacidad de auditar y rastrear las decisiones del sistema.
  * **Auditoría de IA:** El proceso sistemático de evaluar un sistema de IA para verificar su cumplimiento con ciertos estándares, políticas o principios, incluyendo equidad, transparencia y rendimiento.

-----

### 7\. Consideraciones de Seguridad

Este documento, al ser un glosario, no introduce nuevas vulnerabilidades de seguridad directamente. Sin embargo, una **terminología clara** es fundamental para discutir y abordar las preocupaciones de seguridad en la IA. La ambigüedad en los términos puede llevar a malentendidos en la identificación y mitigación de riesgos. La Iniciativa RFC-AI considerará la seguridad como un principio transversal en todos los futuros documentos que definan protocolos o arquitecturas.

-----

### 8\. Consideraciones de Privacidad

Similar a la seguridad, este glosario no tiene implicaciones directas en la privacidad. No obstante, la **privacidad** es una preocupación primordial en la IA, especialmente al tratar con datos personales. La definición precisa de términos como "datos de entrenamiento", "datos sensibles" o "privacidad diferencial" es crucial para desarrollar estándares que protejan adecuadamente la información privada.

-----

### 9\. Consideraciones Específicas de IA

Este glosario aborda directamente muchas de las consideraciones clave específicas de la IA, como el **sesgo/equidad**, la **explicabilidad** y la **robustez**, al proporcionar definiciones estandarizadas para estos conceptos. Una comprensión común de estos términos es esencial para el desarrollo de sistemas de IA responsables y fiables. Futuros RFC-AIs profundizarán en los aspectos técnicos de cómo medir, mitigar o implementar soluciones relacionadas con estos conceptos.

-----

### 10\. Referencias

  * [1] ISO/IEC JTC 1/SC 42 Artificial intelligence. [https://www.iso.org/committee/6794461.html](https://www.google.com/search?q=https://www.iso.org/committee/6794461.html)
  * [2] IEEE Standards Association. [https://standards.ieee.org/](https://standards.ieee.org/)
  * [3] National Institute of Standards and Technology (NIST) Artificial Intelligence. [https://www.nist.gov/artificial-intelligence](https://www.nist.gov/artificial-intelligence)
  * [4] RFC-AI 0000: Declaración de Propósito e Introducción a la Iniciativa de Estandarización RFC-AI. (Ver enlace en el README del repositorio).
  * [5] Example Mailing List / Website (Hipótesis). [http://www.ejemplo.com/iniciativa\_rfc-ai](https://www.google.com/search?q=http://www.ejemplo.com/iniciativa_rfc-ai)

-----

### 11\. Dirección del Autor

Grupo Promotor de la Iniciativa RFC-AI
Dirección de Correo: dirección\_lista@ejemplo.com
URI: [http://www.ejemplo.com/iniciativa\_rfc-ai](https://www.google.com/search?q=http://www.ejemplo.com/iniciativa_rfc-ai)

-----
