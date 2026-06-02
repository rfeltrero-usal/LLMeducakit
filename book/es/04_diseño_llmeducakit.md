# 4. Diseño de LLMeducakit: Arquitectura y Personalización

```{figure} _static/logo.svg
:alt: LLMeducakit logo
:width: 18%
:align: right
---
```

## Empoderamiento de Docentes mediante Modelos Personalizados

La irrupción de los modelos de lenguaje de gran escala (LLM) ha transformado profundamente el panorama educativo, permitiendo nuevas formas de interacción, personalización y acceso al conocimiento. Sin embargo, la mayoría de las soluciones comerciales presentan barreras significativas para su adopción, especialmente en contextos donde la accesibilidad y la autonomía docente son prioritarias.

LLMeducakit es una herramienta de IA de código abierto orientada a **empoderar a los profesores** de todas las especialidades mediante las posibilidades pedagógicas de la personalización de modelos de lenguaje. A través de esta plataforma, docentes e investigadores pueden crear innumerables estrategias educativas innovadoras.

### 1. Estrategias de Personalización

Los docentes pueden personalizar el comportamiento de los modelos LLM mediante distintos enfoques, desde funciones simples hasta estrategias avanzadas:

**a) Prompt Engineering**: Técnicas como el fewshot prompting y los prompts dialógicos permiten ajustar el estilo, tono y tipo de respuesta sin modificar el modelo base, siendo especialmente adecuado para docentes que buscan una personalización rápida y de bajo coste.

**b) Retrieval-Augmented Generation (RAG)**: Una transformación más sustancial que permite integrar bases de conocimiento externas. El RAG es probablemente la más apropiada para el trabajo educativo porque permite "anclar" las respuestas en documentos seleccionados por el equipo docente (currículos, normativas, textos teóricos, materiales de aula).

Esto incrementa la precisión, la alineación con el proyecto educativo, la trazabilidad de las fuentes, eliminando errores y facilitando el control máximo sobre el comportamiento del modelo.

**c) Fine-tuning**: La modificación de parámetros internos del modelo para construir un modelo nuevo que se comporte diferentemente. Exige mayores recursos computacionales pero ofrece personalización profunda.

### 2. Arquitectura Modular de LLMeducakit

LLMeducakit ha sido diseñado como una plataforma **modular y extensible** orientada a la personalización educativa, a la experimentación docente y a la creación de comunidades de innovación. Su arquitectura se basa en varios principios clave:

#### Pluralidad de Modelos
Permite la integración de múltiples modelos de lenguaje de código abierto (LLaMA 2, StableLM, Mistral, Deepseek, etc.), favoreciendo la actualización continua.

#### Interfaz Accesible
Ofrece una experiencia de usuario intuitiva que permite a los docentes interactuar sin necesidad de conocimientos avanzados de programación.

#### Modularidad y Gestión de Recursos
Estructura modular que facilita el manejo de modelos, bases de conocimiento, esquemas de prompts y otros recursos, con ejecución de modelos en un módulo externo de Ollama.

#### Procesamiento Local
Todas las operaciones se realizan de manera local, en servidores propios o en equipos personales de docentes, garantizando privacidad y control de datos.

#### Integración RAG Simplificada
Integra todas las herramientas para la creación y compartición de modelos LLM basados en la modificación de modelos libres mediante estrategias RAG.

#### Transparencia y Control Tecnológico
Acceso de administración que permite a los profesores ejecutar herramientas avanzadas para gestionar parámetros de comportamiento de los modelos.

### 3. El Proceso RAG: De la Consulta a la Respuesta Fundamentada

El flujo operativo de un sistema RAG en LLMeducakit sigue estos pasos:

1. **Consulta del usuario**: El estudiante o docente formula una pregunta sobre el contenido.

2. **Conversión a embeddings**: La consulta se transforma en vectores numéricos, el "lenguaje" de los LLM.

3. **Búsqueda semántica**: El LLM ejecuta una búsqueda semántica buscando fragmentos de texto relevantes en la base de datos vectorial construida con la base de conocimiento.

4. **Recuperación de contexto**: Se seleccionan los fragmentos más relevantes del corpus validado.

5. **Generación de respuesta**: El LLM combina el contexto recuperado con sus capacidades de composición de textos, generando una respuesta precisa y alineada con el corpus.

Este enfoque garantiza que las respuestas sean coherentes, contextualmente relevantes y verificables, **minimizando las "alucinaciones"** típicas de modelos no conectados a bases de datos externas.

### 4. Estrategias Educativas Innovadoras

La implementación del sistema RAG en LLMeducakit permite operacionalizar dos estrategias educativas centrales:

#### Tutores Adaptativos por Competencias
Un sistema que evalúa el trabajo del estudiante en tiempo real, propone itinerarios de mejora y personaliza la retroalimentación según competencias específicas. La base de conocimiento contiene rúbricas, descriptores detallados y ejemplos progresivos.

#### Detectores de Sesgos Implícitos
Una herramienta para auditar ética de materiales didácticos, identificando prejuicios culturales, de género o eurocéntricos sin evidentes. Transforma la IA en un dispositivo de auditoría ética de la cultura digital.

### 5. Principios Fundamentales

El conocimiento más importante para manejar y personalizar estas herramientas de IA no es el conocimiento tecnológico. Es el conocimiento académico que dominan los profesores:

- **Selección cuidada de bibliografía** (la base de conocimiento RAG)
- **Instrucciones depuradas** (prompts generales del RAG)
- **Concepción de estrategias educativas innovadoras** (cómo usar estas herramientas significativamente)

LLMeducakit no solo facilita funciones simples de personalización, sino que habilita la exploración de estrategias educativas avanzadas mediante la personalización de comportamiento de modelos, alineando infraestructura técnica con objetivos pedagógicos y éticos.
