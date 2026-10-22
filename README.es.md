# HydroMark — Complemento de Markdown para OneNote con asistente de IA

[English](README.md) · [简体中文](README.zh.md) · [日本語](README.ja.md) · [한국어](README.ko.md) · **Español** · [Русский](README.ru.md) · [Deutsch](README.de.md) · [Français](README.fr.md) · [Soporte](SUPPORT.es.md)

**HydroMark es un complemento (add-in) de Markdown WYSIWYG para Microsoft OneNote en Windows.** Escribe Markdown en una página de OneNote, pulsa Enter y se renderiza al instante como contenido nativo de OneNote: títulos, listas, tablas, listas de tareas, bloques de código, fórmulas LaTeX y diagramas Mermaid. Sin exportaciones, sin capturas de pantalla, sin cambiar de aplicación. Desde la **v1.1.0**, un **asistente de IA** integrado escribe artículos renderizados, tablas y operaciones de página directamente en tus notas.

> ⚠️ **Este repositorio NO es de código abierto.** Existe únicamente para la documentación del producto, anuncios y comentarios de la comunidad (Issues y Discussions). El código fuente de HydroMark es propietario y **no** se publica aquí. Consulta [Licencia y código fuente](#licencia-y-código-fuente) más abajo.

---

## ¿Qué es HydroMark?

HydroMark es un **complemento de Markdown para OneNote**: un complemento de Windows que integra un verdadero editor de Markdown dentro de Microsoft OneNote. Sigues escribiendo en los cuadernos, el lienzo y la sincronización en la nube de OneNote, pero obtienes el flujo de trabajo de Markdown que realmente quieres: escribe `## Heading`, pulsa Enter y la página muestra un título renderizado en lugar de la sintaxis sin procesar.

Todo se renderiza con **elementos nativos propios de OneNote, no con imágenes**, así que tus notas de Markdown siguen siendo editables, se pueden buscar dentro de OneNote, están disponibles sin conexión y se sincronizan con OneNote en el teléfono, la tableta y la web. Pulsa `F8` para exportar una página de vuelta a `.md`.

Desde la **v1.1.0**, el complemento también incluye un **asistente de IA**. A diferencia de las barras laterales de IA que te entregan texto para copiar y pegar, la IA de HydroMark escribe en la página: inserta artículos totalmente renderizados, crea tablas y ejecuta acciones del complemento como renderizar, exportar, tabla de contenido y ancho de página, con los resultados devueltos al modelo para que pueda confirmar o corregirse a sí mismo.

**Para quién es:** desarrolladores y equipos técnicos, estudiantes e investigadores, personas de producto y operaciones: cualquiera que escriba Markdown pero guarde sus notas en OneNote.

## Datos rápidos

| Elemento              | Detalle                                                              |
| --------------------- | ------------------------------------------------------------------- |
| **Producto**          | HydroMark — complemento de Markdown para OneNote (add-in) con asistente de IA |
| **Categoría**         | Complemento de OneNote / extensión de OneNote / complemento COM de Office |
| **Plataforma**        | Windows 7 y posteriores                                             |
| **Aplicación host**   | OneNote **de escritorio** 2013+ (2016 / 2019 / 2021 / Microsoft 365) |
| **Entorno de ejecución** | .NET Framework 4.8+                                              |
| **No compatible**     | OneNote para Windows 10 (UWP / Microsoft Store), macOS, móvil       |
| **Prueba**            | Prueba completa de 14 días, sin tarjeta de crédito                  |
| **IA**                | Integrada — 15 proveedores, usa tu propia clave de API              |
| **Idiomas**           | 简体中文 · English · 日本語 · 한국어 · Deutsch · Français · Español · Русский |

## ✨ Funciones

### 🤖 Asistente de IA — la función estrella (novedad en 1.1.0)

La mayoría de las barras laterales de IA te entregan un muro de texto para copiar y pegar. El asistente de HydroMark **escribe en tus notas**:

- **Ejecuta acciones del complemento, no solo chat** — inserta un artículo totalmente renderizado, crea tablas, ejecuta operaciones de página (renderizar, exportar, TOC, ancho de página); los resultados de las acciones se devuelven a la conversación para que el modelo pueda confirmar o corregirse a sí mismo.
- **Tablas bajo demanda, con el ancho que pidas** — `insert_table` admite diseños de ancho de página completo y **ajustados al contenido**; la ruta de IA comparte el mismo motor de tablas que el conmutador de ancho `Alt+W`.
- **Usa tu propio modelo** — 15 proveedores integrados (OpenAI, DeepSeek, Kimi, Zhipu, Qwen…), Base URL personalizada para cualquier otro. Tu clave de API permanece en tu equipo; sin servidor intermediario.
- **Multimodal** — pega una captura de pantalla en el chat y referénciala con modelos multimodales.
- **Sigue el idioma** — pregunta en chino, obtén chino; pregunta en inglés, obtén inglés.
- **Incluido en todas las licencias** — la prueba gratuita de 14 días y todos los planes de pago. Ábrelo con `Alt+A` o desde el grupo **AI** de la cinta de opciones.

### 📝 Renderizado de Markdown

- **Renderizado de Markdown en tiempo real** — escribe Markdown, pulsa Enter y ve el formato al instante (WYSIWYG).
- **Vista dual fuente / renderizado** — alterna entre el Markdown sin procesar y la salida renderizada en cualquier momento, por página o por párrafo.
- **Pega Markdown desde cualquier lugar** — `Ctrl+Shift+V` convierte un bloque de Markdown copiado de una página web, un documento o una respuesta de IA en una nota terminada.
- **Resaltado de código** — resaltado de sintaxis para más de 200 lenguajes, más de 100 temas, copia con un clic.
- **Matemáticas LaTeX** — fórmulas en línea y en bloque renderizadas como ecuaciones nativas de OneNote.
- **Diagramas Mermaid / ZenUML** — más de 26 tipos de diagramas: diagrama de flujo, secuencia, clases, estados, Gantt, mapa mental, UML y más.
- **Tablas con conmutador ancho completo ↔ ajustado al contenido** — `Alt+W` cambia cualquier tabla en ambos sentidos; el estado ajustado al contenido persiste.
- **Listas de tareas** — las casillas siguen siendo clicables y se exportan de vuelta como `- [x]` / `- [ ]`.
- **Comandos de barra** — pulsa `/` para abrir una paleta de comandos e insertar bloques de forma rápida.
- **Bloques de resaltado** — destaca visualmente las notas importantes.
- **TOC de página y ancho de página** — genera o oculta automáticamente una tabla de contenido; ancho de página manual o automático.
- **Adaptación completa al modo oscuro** — el contenido renderizado, los diálogos y la barra lateral de IA siguen el tema de OneNote.
- **Importación / exportación fluida** — entran archivos Markdown, salen archivos Markdown (imágenes opcionales).

## Preguntas frecuentes

**¿Existe un complemento de Markdown para OneNote?**
Sí: HydroMark es un complemento de Markdown (add-in) creado específicamente para Microsoft OneNote de escritorio en Windows.

**¿Puedo usar IA para escribir notas en OneNote?**
Sí. HydroMark incluye un asistente de IA que inserta artículos y tablas de Markdown renderizados directamente en la página actual de OneNote, y puede activar acciones del complemento como renderizar, exportar o la tabla de contenido.

**¿Funciona HydroMark con OneNote para Windows 10, Mac o móvil?**
No. HydroMark es compatible con OneNote **de escritorio** 2013 y posteriores (2016 / 2019 / 2021 / Microsoft 365) en Windows 7+. La versión UWP / Microsoft Store de OneNote, macOS y móvil **no** son compatibles.

**¿HydroMark es un complemento de OneNote o una aplicación independiente?**
Es un complemento de OneNote, no una aplicación de notas independiente. Se instala en OneNote y añade una pestaña **HydroMark** a la cinta de opciones; tus notas permanecen en tus cuadernos existentes.

**¿El contenido de Markdown se mantiene nativo en OneNote?**
Sí. El renderizado usa elementos nativos de OneNote en lugar de imágenes, así que las notas siguen siendo editables, se pueden buscar y sincronizar entre clientes de OneNote. Las páginas todavía se pueden exportar a `.md`.

**¿Cómo lo instalo?**
Descarga el instalador multilingüe único desde el sitio web, ejecútalo y abre OneNote: aparecerá una pestaña **HydroMark** en la cinta de opciones. El instalador se adapta automáticamente a OneNote de 32 y 64 bits.

**¿Es gratis?**
Hay una prueba completa de 14 días. Después, las licencias son por dispositivo (correo electrónico + clave): planes Individual y Family, Basic y Pro, de por vida o anuales.

## 🌐 Enlaces oficiales

- Sitio web (inglés): https://hydromark.hydrolinx.top
- Sitio web (中文): https://hydromark.hydrolinx.cn
- Documentación: https://hydromark.hydrolinx.top/documentation
- Precios: https://hydromark.hydrolinx.top/pricing
- Registro de cambios: https://hydromark.hydrolinx.top/changelog

## 💬 Comentarios y soporte

Este es el mejor lugar para contactarnos:

- 🐛 **Informes de errores y solicitudes de funciones** → abre un [Issue](../../issues)
- 💡 **Ideas y debate general** → usa [Discussions](../../discussions)
- 📧 **Correo electrónico** → support@hydrolinx.top
- 📖 **Guía de soporte** → [SUPPORT.es.md](SUPPORT.es.md)

Antes de abrir un issue, busca los existentes para evitar duplicados e incluye tu versión de Windows / OneNote y los pasos para reproducirlo.

## 🗺️ Hoja de ruta

Estamos mejorando HydroMark activamente. A corto plazo:

- Acciones de IA más inteligentes — resúmenes inteligentes, etiquetado automático y más operaciones del complemento que el asistente puede ejecutar
- Más tipos de diagramas y plantillas de bloques
- Una integración más amplia con OneNote

Consulta la página de [Releases](../../releases) para las notas de actualización.

## Licencia y código fuente

HydroMark es **software propietario**. El código fuente **no es de código abierto** y no se distribuye a través de este repositorio. Todos los derechos reservados.

Te damos la bienvenida a:

- Leer la documentación y los anuncios de este repositorio
- Abrir issues y unirte a los debates para ayudarnos a mejorar

**No** puedes, sin permiso escrito explícito:

- Copiar, modificar o redistribuir el código fuente de HydroMark
- Usar el nombre / la marca HydroMark en productos derivados

© HydroLinx. Todos los derechos reservados.

---

*HydroMark — Markdown, tal como OneNote debería haberlo tenido. Ahora con un asistente de IA que hace el trabajo de escribir.*
