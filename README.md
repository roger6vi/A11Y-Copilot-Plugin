 █████╗  ██╗ ██╗ ██╗   ██╗         ██████╗  ██████╗  ██████╗ ██╗██╗      ██████╗ ████████╗
██╔══██╗███║███║╚██╗ ██╔╝        ██╔════╝ ██╔═══██╗ ██╔══██╗██║██║     ██╔═══██╗╚══██╔══╝
███████║╚██║╚██║ ╚████╔╝         ██║      ██║   ██║ ██████╔╝██║██║     ██║   ██║   ██║
██╔══██║ ██║ ██║  ╚██╔╝          ██║      ██║   ██║ ██╔═══╝ ██║██║     ██║   ██║   ██║
██║  ██║ ██║ ██║   ██║           ╚██████╗ ╚██████╔╝ ██║     ██║███████╗╚██████╔╝   ██║
╚═╝  ╚═╝ ╚═╝ ╚═╝   ╚═╝            ╚═════╝  ╚═════╝  ╚═╝     ╚═╝╚══════╝ ╚═════╝    ╚═╝
<p align="left">
  <img alt="Version" src="https://img.shields.io/badge/version-1.1-2563eb?style=flat-square">
  <img alt="Figma Plugin" src="https://img.shields.io/badge/Figma-Plugin-A259FF?style=flat-square&logo=figma&logoColor=white&labelColor=3f434b">
</p>

Un plugin de Figma que permite anotar, validar y documentar
la accesibilidad de una pantalla **sin salir de Figma**.
Funciona en modo diseño y en Dev Mode. El mismo plugin,
dos experiencias adaptadas a cada rol.

---

## Instalación

El plugin se distribuye por este repositorio. Sin terminal, sin `npm`, sin compilar nada.

> ⚠️ **Importante**: este repositorio NO contiene código fuente. NO ejecutes `npm install` ni `npm run dev` — no va a funcionar y no hace falta. Solo descarga el ZIP y segue los pasos de abajo.

### Primera vez

1. Descarga el ZIP: **[Descargar última versión](https://github.com/roger6vi/A11Y-Copilot-Plugin/archive/refs/heads/main.zip)**
2. Descomprime el ZIP en una carpeta estable de tu ordenador (por ejemplo `Documentos/A11Y-Copilot-Plugin/`)
3. Abre **Figma Desktop** (el plugin no funciona en Figma web)
4. En el menú superior: `Plugins → Development → Import plugin from manifest…`
5. Selecciona el archivo `plugin/manifest.json` dentro de la carpeta que acabas de descomprimir
6. Listo. A partir de ahora, en cualquier archivo de Figma, abre el plugin desde `Plugins → Development → A11Y Copilot`

### Actualizar a una nueva versión

Cuando salga una versión nueva:

1. Vuelve a descargar el ZIP desde el mismo enlace de arriba
2. Reemplaza la carpeta anterior por la nueva (o descomprime encima pisando los archivos)
3. Figma usará la nueva versión automáticamente. **No hace falta volver a importar el manifest**: Figma recuerda la ruta.

Puedes ver qué ha cambiado en cada versión en el [CHANGELOG](./CHANGELOG.md).

> Nota: los artefactos del plugin viven dentro de la carpeta `plugin/`. La documentación (`README`, `CHANGELOG`, `LICENSE`) se mantiene en la raíz del repositorio.

### Requisitos

- **Figma Desktop** (imprescindible, no funciona en navegador): [figma.com/downloads](https://www.figma.com/downloads/)
- Nada más.

> Si tienes terminal y `git` instalados puedes clonar el repo y hacer `git pull` para actualizar. Pero no es necesario — con el ZIP basta.

### ¿Has encontrado un bug o quieres pedir algo?

Abre un issue en el repositorio de desarrollo: **[A11Y-Copilot issues](https://github.com/roger6vi/A11Y-Copilot/issues)** (necesitarás acceso; si no lo tienes, pídelo al responsable del plugin).

---

## Qué es

A11Y Copilot es un plugin de Figma pensado para cerrar el hueco entre
diseño y desarrollo cuando se trata de accesibilidad. La accesibilidad
se pierde en el handoff: diseño toma decisiones sobre roles, orden de
lectura, textos alternativos y jerarquía de encabezados, pero esa
información viaja entre equipos sin un canal estructurado quedandose
repartida entre documentos paralelos, comentarios de Figma y
conversaciones puntuales, formatos que dificultan que llegue 
la información completa al momento de implementar.

**El resultado**: trabajo de accesibilidad que se duplica o se queda
incompleto en el camino entre diseño y desarrollo, no por falta de
intención de ningún equipo, sino por la falta de un puente común entre
ambas disciplinas.

Este plugin es ese puente. Taggeas cada nodo relevante con su rol
semántico, defines el orden de lectura y foco, añades labels y notas de
producto, y el equipo de desarrollo lo ve todo directamente en Dev Mode,
sin tener que salir de Figma. Mismo archivo, mismo flujo, sin
documentos paralelos.

## Para quién es

| Rol                        | Qué hace con el plugin                                                                                                                                              |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Diseño / Accesibilidad** | Anota cada pantalla con roles semánticos, orden de lectura/foco, etiquetas y textos alternativos. Valida problemas en tiempo real.                                  |
| **Desarrollo**             | Abre el plugin en Dev Mode, inspecciona cualquier nodo y ve directamente los metadatos de accesibilidad que le corresponden, tal como los dejó el equipo de diseño. |

¿Es para ti si eres un diseñador que **nunca ha pensado en
accesibilidad**? Sí. El plugin está diseñado para que puedas empezar
sin conocimientos previos de ARIA, WCAG ni de cómo funciona un lector
de pantalla. Va a proponerte valores por defecto razonables para cada
rol que asignes y te va a avisar cuando falte algo importante (un
label, un texto alternativo, un orden duplicado). No sustituye a una
auditoría formal de accesibilidad, pero sí te da un punto de partida
estructurado sobre el que iterar.

Conocimiento recomendado (no obligatorio): tener claro qué es un
botón, un heading, un campo de formulario y una imagen. A partir de
ahí el plugin te guía.

---

## Primeros pasos

Un recorrido de 60 segundos desde cero hasta taggear tu primer nodo.

**1. Instala el plugin.** Sigue los pasos de la sección
[Instalación](#instalación) al principio de este documento. Es
descargar el ZIP e importarlo desde Figma — un par de minutos como mucho.

**2. Ábrelo en un archivo.** En cualquier archivo de Figma Desktop:
`Plugins → Development → A11Y Copilot`. El plugin se abre como panel
lateral.

**3. Selecciona un frame.** Hasta que no selecciones nada, el panel te
muestra una pantalla vacía con instrucciones breves. Selecciona un
frame, componente, instancia o sección en el canvas y el plugin
escaneará toda su estructura.

**4. Taggea tu primer nodo.** El plugin lista jerárquicamente todos los
nodos que ha encontrado dentro de tu selección. Haz click en el
selector de rol (el badge de la derecha de la fila) y elige, por
ejemplo, `Button`. El plugin propone automáticamente focus + reading
activos y captura el texto visible como label. Ya tienes tu primer
nodo anotado.

**5. Confirma con Marcar.** Todo lo que has editado está en un
borrador local (preview en vivo). Pulsa **Marcar** en el footer para
persistirlo en Figma. A partir de ahí viaja con el nodo.

**6. Observa las specs.** Pulsa el icono de lock en la cabecera para
alternar a la **Vista de specs**, donde verás el resumen estructural.
Desde ahí puedes generar el blueprint nativo que aparecerá en Dev
Mode como annotations nativas de Figma.

Eso es todo. El resto de este documento profundiza en cada pieza.

---

## Anatomía de la interfaz

Un vistazo de arriba abajo al panel, para que sepas qué es cada cosa
antes de entrar en detalle.

```
┌──────────────────────────────────────────────────┐
│ [🔒/🔓]    A11Y Copilot             [⚙]          │  ← Header
├──────────────────────────────────────────────────┤
│                                                  │
│  Frame seleccionado · 12 nodos · 3 tagueados     │  ← Resumen
│                                                  │
│  ╭────────────────────────────────────────────╮  │
│  │ [R1][F1] 🔲 Hero banner        [·][⋯·][▼]  │  │  ← Fila de nodo
│  │  ─ Heading 1 ─                  ·[Enabled] │  │    (Top + bottom)
│  ╰────────────────────────────────────────────╯  │
│                                                  │
│  ╭────────────────────────────────────────────╮  │
│  │ [R2][F2] 🔘 Submit button      [2][⋯][▼]   │  │
│  │  Send form                     [Enabled]   │  │
│  ╰────────────────────────────────────────────╯  │
│                                                  │
│  [+ Add element]                                 │  ← Inline add
│                                                  │
├──────────────────────────────────────────────────┤
│                        [Clear]  [Marcar / Specs] │  ← Footer
└──────────────────────────────────────────────────┘
```

Piezas, de arriba abajo y de izquierda a derecha:

- **Header**: a la izquierda, el botón **lock/unlock** que alterna
  entre Vista de edición y Vista de specs. A la derecha, el icono de
  **⚙ engranaje** que abre Settings como modal.
- **Resumen del frame**: contador de nodos totales, cuántos están
  tagueados y cuántos participan en el focus flow. Si hay issues,
  aparece un contador con el número de problemas detectados.
- **Lista de nodos**: cada fila es un nodo del árbol. La jerarquía se
  respeta visualmente.
- **Flow pills `R` / `F`**: a la izquierda de cada fila, dos badges
  redondos con un número dentro. `R` = Reading order, `F` = Focus
  order. Click sobre el pill incluye o excluye ese nodo del flujo
  correspondiente. El número se asigna automáticamente.
- **Icono de tipo de nodo + nombre**: identifica de qué nodo de Figma
  se trata (frame, component, instance, text, section, group…). El
  nombre es el que tiene el nodo en Figma.
- **Cluster derecho**: pictos pequeños que resumen el estado de
  metadata de ese nodo:
  - **Icono de doc link** — aparece si el nodo tiene dev docs enlazadas.
  - **Icono de notes** — aparece si hay notas de producto.
  - **Menú kebab `⋯`** — abre las opciones extra (dev docs, notas,
    atributos personalizados). Si hay opciones activas, un **badge
    numérico** a la izquierda del kebab resume cuántas.
  - **Badge de rol** (píldora) — dropdown inline para asignar el rol
    semántico (Button, Heading, Image, etc.).
  - **Arrow up / down** — flechas de reordenación manual (solo cuando
    procede).
- **Bottom row**: segunda línea dentro de la misma fila, con el campo
  semántico (label, heading level, text alternative) a la izquierda y
  el selector de **State** (dropdown) a la derecha.
- **Botón de info (ℹ)**: a la derecha del todo, abre el panel de
  metadata expandida del nodo.
- **Add element**: botón para pinar en la lista un nodo que estaría
  fuera del preview normal (por ejemplo, un descendiente textual que
  el plugin no promueve por defecto).
- **Footer**: a la derecha, el botón principal cambia según la vista:
  - Vista de edición → **Marcar** (persiste el borrador) y **Limpiar**
    (borra metadata del nodo seleccionado).
  - Vista de specs → **Generar specs** (crea/actualiza el blueprint
    nativo en Dev Mode).

En Dev Mode este panel es más simple: lock bloqueado en specs, sin
footer de edición, solo consulta.

---

## Modo diseño — Vista de edición

Aquí vive el grueso del trabajo. Cuando seleccionas un frame, el plugin
escanea su árbol entero y construye la lista que vas a editar.

### Seleccionar un frame

El plugin no hace nada hasta que selecciones algo en el canvas. Puedes
seleccionar:

- Un **frame** de pantalla completa.
- Un **componente** o **instancia** individual.
- Una **section** (solo como organizador visual — no aporta semántica,
  pero sus hijos sí se escanean).

Al seleccionar, el plugin escanea toda la descendencia visible y monta
la lista. Si la selección cambia, re-escanea. Si haces click sobre una
fila del preview, el plugin **selecciona ese nodo en el canvas y hace
scroll hasta él**, para que no pierdas el contexto visual de qué
estás taggeando.

En la selección vacía el plugin muestra una pantalla de bienvenida con
los pasos básicos y un par de tips. Es el sitio al que vuelves si
deseleccionas todo.

### Roles semánticos

El selector de rol (la píldora del cluster derecho de cada fila) es la
pieza central. Asignar un rol tiene tres efectos:

1. **Propuesta automática de defaults.** Cada rol tiene sus propios
   valores por defecto para focus y reading. Por ejemplo, al asignar
   `Button` el plugin activa automáticamente focus + reading. Al
   asignar `Image`, activa textAlt pero deja reading/focus en `false`
   hasta que tú decidas. No es un bloqueo: es una propuesta razonable
   que puedes cambiar después.

2. **Captura de label.** Para roles con estrategia `capture-text`
   (Button, Heading, Link, Text, Checkbox, Toggle button, Switch, List
   item, Tab bar, Accordion, Dropdown, Grouped text), el plugin
   intenta capturar el texto visible del nodo como label inicial.
   Para roles con estrategia `editable` (Image, Text field, Password
   field, Search field, Number field, Date field, Text area, Slider),
   el label queda vacío y editable. Para `fixed` (Stepper, Carousel),
   se asume que el patrón define el label de otra forma.

3. **Selector de estado contextual.** Según el rol, el dropdown de
   State muestra solo los valores que tienen sentido. Un Button puede
   estar `Enabled / Disabled / Error / Read only`; un Checkbox puede
   estar `Selected / Not selected / Disabled / Error`; un Heading o un
   Text no expone selector de estado porque no aplica.

El plugin incluye **22 roles**. La tabla completa con su uso
recomendado está en [Referencia de roles semánticos](#referencia-de-roles-semánticos).

### Reading order y focus order

Cada nodo tagueado puede pertenecer a dos flujos:

- **Reading order (`R`)**: el orden en el que un lector de pantalla
  recorre la pantalla. Lo componen los nodos con contenido textual o
  con label accesible (headings, textos, botones, links, inputs,
  imágenes con texto alternativo, etc.).
- **Focus order (`F`)**: el orden en el que el foco de teclado salta
  entre elementos. Lo componen los nodos interactivos.

Los pills `R` y `F` a la izquierda de cada fila son **toggles
directos**. Click sobre `R` incluye o excluye el nodo del reading
flow; click sobre `F` hace lo mismo con el focus flow. El número
dentro del pill indica la posición del nodo en ese flujo.

**El orden se asigna automáticamente** según el orden de la lista
(que por defecto replica el orden de árbol de Figma). No tienes que
escribir números a mano. Si quieres cambiar el orden de un nodo, usa
las flechas **arriba/abajo** del cluster derecho: el plugin
recalcula todos los números afectados en cascada.

> Dato importante: reading es el **master switch** de los slots
> semánticos. Si apagas `R` en un nodo que tenía heading, label o
> textAlt, el plugin apaga también esos campos en cascada. No pueden
> existir sin reading activo.

### Labels y textos alternativos

El campo inline debajo del nombre del nodo es donde vive el **texto
accesible** del nodo. Qué muestra depende del rol:

- **Roles interactivos y textuales con `reading` activo** → campo de
  **label** (accessible name). Para un botón es "Enviar formulario";
  para un link es "Volver al inicio"; para un heading es el texto del
  título.
- **Rol `Image`** → dropdown de **Alternative type** con dos opciones:
  - **Info** — descripción informativa del contenido visual
    (logotipos con significado, ilustraciones que aportan información).
  - **Func** — descripción funcional (una imagen que actúa como botón
    describe lo que hace, no lo que es).
  - Al elegir tipo, aparece el campo de texto alternativo para
    rellenar.
- **Rol `Heading`** → además del label, un selector de nivel: `h1`,
  `h2`, `h3`, `h4`, `h5`, `h6`, `p`. El nivel define cómo se anuncia
  la jerarquía al lector de pantalla.

Para capturar texto desde descendientes del nodo sin tener que
reescribirlo, el plugin expone un **picker de texto interno** (atajo
`Pick inner text`): lista todos los nodos `TEXT` dentro del nodo
tagueado y puedes elegir cuál sirve de label. Útil cuando un botón
tiene varios texts anidados y quieres elegir explícitamente cuál es el
accessible name.

### Contenedores

Los frames que agrupan elementos pueden marcarse como
**contenedores** para aportar estructura semántica. Hay tres tipos:

- **Wrapper** — agrupación genérica, sin significado semántico fuerte.
- **List** — el frame representa una lista; sus hijos son list items.
- **Screen** — el frame es una pantalla completa (landmark `main`).

Un contenedor no expone toggles de reading/focus ni bottom row con
label/state: es estructura pura. El rol de un contenedor se asigna
desde el mismo dropdown (opción `Mark as container` / `Remove
container`), no desde la lista de roles semánticos.

### Menú de opciones extra (⋯)

El kebab del cluster derecho abre tres opciones que no viven en la
fila principal porque no son de uso frecuente. Un **badge numérico**
junto al kebab te indica de un vistazo cuántas están activas en este
nodo.

#### Dev docs

Un enlace a la documentación técnica del componente o patrón. Acepta
tres formatos:

- URL externa (cualquier `http(s)://...`).
- Ruta de Figma (`figma.com/...`, con o sin dominio).
- File ID de Figma (el hash que aparece en la URL de un archivo).

El plugin valida el formato al guardar: si no encaja en ninguno de
los tres, muestra el mensaje "Enter a valid URL, figma.com path or
Figma file ID" y no guarda. Cuando el link es válido, aparece un icono
de link en el cluster derecho del nodo que abre el enlace con
`figma.openExternal()`. En la Vista de specs también se renderiza
copiable.

#### Notas de producto

Campo multilínea con **toolbar markdown completo**. Los botones
disponibles:

- **Bold / Italic / Strikethrough** — formato básico de texto.
- **Inline code / Code block** — para snippets técnicos.
- **Link** — inserta un enlace con placeholder editable.
- **Heading** — insertar encabezado dentro de la nota.
- **Bullet list / Numbered list** — listas con viñetas o numeradas.

Las notas viajan con el nodo y se renderizan:

- En el propio diálogo mientras las editas (preview en vivo del
  markdown).
- En la Vista de specs como bloque expandible.
- En el **blueprint nativo** en Dev Mode, bajo la categoría `Notes`.

Piensa en las notas como un espacio para todo lo que no encaja en los
campos estructurados: comportamiento esperado, casos edge,
referencias cruzadas a otras pantallas, aclaraciones de producto
específicas de ese componente en ese contexto.

#### Atributos personalizados

Pares **clave + valor** de texto libre para cualquier metadato que no
encaje en los campos estándar. Ejemplos reales:

- `aria-describedby` → `"error-hint-1"` (referencias ARIA explícitas)
- `estado-visual` → `"loading"` (estados que no están en la matriz
  estándar)
- `analytics-id` → `"cta-submit"` (metadata para tracking)

Límites validados al guardar:

- Clave: máximo 40 caracteres.
- Valor: máximo 500 caracteres.
- Entradas con clave o valor vacíos no se persisten.

Cuando el nodo hereda atributos de su componente origen, el diálogo
muestra esos valores como parent values. Si los sobrescribes
localmente, aparece un botón **Restaurar** que vuelve a los valores
heredados de un click, sin perder el resto del contexto. Este botón
es el patrón general del plugin: **el override es local, el baseline
persiste**.

#### Badge numérico

El pequeño badge gris a la izquierda del kebab cuenta cuántas de las
tres opciones (dev docs, notes, custom attributes) están activas en
ese nodo. Sirve para identificar de un vistazo qué filas tienen
metadata extra sin tener que abrir una por una.

### Reordenar y pin

Dos mecanismos para organizar la lista:

**Flechas arriba/abajo.** Aparecen en el cluster derecho cuando
procede y mueven el nodo una posición en la lista. La reordenación se
propaga a los números de reading y focus order automáticamente: no
tocas números, mueves filas.

**Pin.** El botón **+ Add element** al final de la lista abre un
selector que te permite pinar en el preview nodos que normalmente no
aparecen (por ejemplo, un descendiente textual que el plugin no
promueve a fila propia por defecto). Los nodos pinados se identifican
con una `X` pequeña a su derecha para desanclar y dejan de aparecer
si quitas el tag. Úsalo cuando un elemento necesita tag pero no está
en la lista por defecto.

### Borrador local y Marcar

Toda la edición vive en un **borrador local** que se refleja en la
vista previa en tiempo real. Los cambios **no se persisten en Figma
hasta que pulsas Marcar**. Eso te permite:

- Iterar rápido sin escribir en pluginData en cada pulsación.
- Ver el efecto inmediato de cambiar un rol o mover un orden.
- Descartar todo cerrando el plugin si has hecho un lío (aunque
  perderás el trabajo no persistido, así que marca frecuentemente).

El botón **Marcar** persiste el borrador en `pluginData` bajo la clave
`a11y` de cada nodo. El botón **Limpiar** elimina los tags del nodo
seleccionado (o de los nodos seleccionados si hay varios), preservando
la baseline heredada del componente origen para que el icono de
refresh pueda restaurarla.

---

## Modo diseño — Vista de specs

Pulsa el icono de **lock** en la cabecera y el panel cambia a la
Vista de specs. Es la misma información, pero en modo consulta: solo
muestra los nodos que tienen metadata de accesibilidad, sin editores
inline.

### Resumen estructural

La lista se filtra a los nodos tagueados y se presenta como **árbol
jerárquico**. Cada fila muestra:

- Nombre del nodo e icono de tipo.
- Rol asignado (píldora de solo lectura).
- Orden de reading y focus (pills informativas).
- Campo semántico con su valor (label, heading level, textAlt).
- State si lo hay.
- Botón de **info** a la derecha que despliega la metadata expandida:
  rol, estado, container, reading order, focus order, label / heading
  level / text alt, dev docs (con botones de abrir y copiar) y notas
  de producto renderizadas en markdown.

Es la vista que un dev puede abrir para ver el handoff completo antes
de empezar a implementar.

### Blueprint nativo

El botón **Generar specs** del footer crea un conjunto de
**annotations nativas de Figma** sobre el frame activo. Estas
annotations quedan **dentro del archivo de Figma** y viven en el
panel de **Inspect de Dev Mode**, agrupadas en tres categorías:

- **Reading order** (color Figma azul): una annotation por nodo del
  flujo de lectura, con el número de orden.
- **Focus order** (color Figma rojo): una annotation por nodo del
  flujo de foco.
- **Notes** (color Figma amarillo): una annotation por cada nodo que
  tiene notas de producto, con el markdown renderizado.

El blueprint se sincroniza con el borrador activo: si editas en la
Vista de edición y cambias a Vista de specs sin haber pulsado
Marcar, **Generar specs** refleja los cambios del borrador. El botón
indica si el blueprint actual está sincronizado con el estado del
handoff, y si no lo está, genera la diferencia.

---

## Dev Mode

Cuando un desarrollador abre el plugin en Dev Mode, la interfaz se
reduce a lo esencial: **Vista de specs** y **Settings**. No hay
edición ni footer de acciones. El contexto es de consulta pura.

Lo que ve exactamente el dev:

- La misma lista jerárquica de nodos tagueados, con su metadata
  completa: rol, orden, label, alt text, state, dev docs y notas de
  producto.
- El **Metadata inspector**: al seleccionar un nodo, un panel dedicado
  muestra todos los campos estructurados de ese nodo con un diseño
  orientado a copiar/pegar. Incluye colapsado de bloques de código
  (útil si las notas tienen snippets largos).
- Los campos de dev docs se exponen con dos acciones: **Open dev
  docs** (abre el enlace con `figma.openExternal()`) y **Copy URL**
  (copia el enlace al portapapeles con feedback visual).

Si el equipo de diseño generó un blueprint, las anotaciones aparecen
además como **tarjetas de anotaciones nativas de Figma** en las categorías **Reading
order**, **Focus order** y **Notes**, directamente en el panel de
Inspect — sin necesidad de abrir el plugin.

```
  Dev Mode → Inspect → Annotations
  ┌─────────────────────────────┐
  │ 🏷  Accessibility           │
  │                             │
  │  Role: Button               │
  │  Label: "Enviar formulario" │
  │  Focus order: 3             │
  │  Reading order: 5           │
  └─────────────────────────────┘
```

En práctica: un dev puede hacer todo el handoff consultando solo el
panel de Inspect nativo. El plugin abierto es útil cuando se quiere
explorar la pantalla entera o navegar entre nodos sin perder la vista
de conjunto.

---

## Herencia y reutilización

Uno de los conceptos clave del plugin. La metadata de accesibilidad no
se "copia y pega": se **hereda** siguiendo las reglas de componentes
de Figma, y esa herencia es resiliente a cambios.

### Component → instance

Cuando una instancia vive en el canvas, el plugin resuelve su
metadata en cadena: `instance → mainComponent → (si variante) variant
de origen`. Si el componente origen ya tiene tags, la instancia los
hereda automáticamente. No tienes que taggear cada instancia a mano:
taggea el componente una vez y propaga.

Los campos que se heredan desde el `sourceOrigin` son:

- Rol, estado y container.
- Reading, focus y sus órdenes.
- Label, heading level, textAlt y su tipo.
- Dev docs y notas de producto.
- Atributos personalizados.

### Override vs inherited

Cualquier campo heredado puede sobrescribirse localmente en la
instancia. El plugin distingue visualmente cuando un valor viene del
parent (inherited) de cuando es local (override). El valor local
siempre gana — eso es lo que te permite, por ejemplo, cambiar el
label de un botón reutilizado en un contexto distinto sin romper el
componente original.

Cuando hay override local, aparece el botón **Restaurar** (en el
diálogo de atributos personalizados; un icono equivalente en otros
campos) que vuelve al valor heredado sin perder el resto del
contexto.

### Cambio de variante

Si una instancia cambia de variante en Figma, el plugin vuelve a
resolver su `mainComponent` en el siguiente escaneo y muestra la
metadata de la **variante actual**, no la anterior. Esto es
importante para componentes con variantes que cambian rol o estado
(un botón que alterna entre primary y disabled, un checkbox que
alterna entre selected y not-selected): cada variante puede tener su
propia metadata y el plugin te muestra la que corresponde.

### Frames copiados o duplicados

Cuando copias o duplicas un frame con tags, el plugin detecta que la
copia **ya no es el frame original**. En el siguiente escaneo
convierte la metadata heredada o relacionada en una **nueva base
local** dentro de la copia. La pantalla duplicada conserva sus tags
actuales, pero puede evolucionar independientemente sin pisar la
original. Útil cuando diseñas variantes de una pantalla (loading,
error, empty state) a partir de un frame base.

### Clear tags — opt-out explícito

El botón **Limpiar** del footer no borra sourceOrigin: lo que hace es
escribir **sentinels de opt-out** (`null`) por cada campo heredado.
El resultado visible es que el nodo queda sin tags, pero la baseline
del componente origen sigue ahí detrás. Un click en el icono de
**refresh** en la UI vuelve a heredar todo en bloque: es un reset
limpio sin perder el componente origen de referencia.

Si el nodo **no tiene sourceOrigin** (es un nodo autónomo, no viene
de ningún componente), Clear borra todo literalmente.

---

## Validaciones en tiempo real

El plugin valida cada frame al escanear y muestra los issues
encontrados en el header del preview. Los issues se recalculan cada
vez que cambias algo en el borrador: no hay que pulsar "validar",
pasa en vivo.

Qué se valida hoy:

| Issue                     | Cuándo se dispara                                                                                             | Mensaje                                                           |
| ------------------------- | ------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| **Missing text alt**      | Un nodo con rol que requiere `textAlt` (hoy solo `Image`) no tiene texto alternativo rellenado.               | `Role "{role}" should provide text alternative content.`          |
| **Duplicate reading order** | Dos o más nodos comparten el mismo número en el flujo de lectura.                                             | `Reading order {order} is duplicated.`                            |
| **Duplicate focus order** | Dos o más nodos comparten el mismo número en el flujo de foco.                                                | `Focus order {order} is duplicated.`                              |

Los duplicados normalmente no deberían aparecer porque el plugin
asigna los números automáticamente, pero pueden ocurrir al combinar
frames heredados con overrides locales, o al importar data antigua.
La solución es usar las flechas de reordenación: mover un nodo una
posición recalcula la cascada entera.

---

## Referencia de roles semánticos

Los 22 roles del plugin, agrupados por familia. Las capacidades
(focus / reading / heading / textAlt) y defaults se aplican
automáticamente al asignar el rol. Los ejemplos de mapping ARIA son
orientativos (la definición final depende del patrón de
implementación del dev).

### Texto y estructura

| Rol              | Label            | Uso recomendado                                                                               | Capacidades               |
| ---------------- | ---------------- | --------------------------------------------------------------------------------------------- | ------------------------- |
| `heading`        | Heading          | Títulos de sección. El nivel (`h1`–`h6` o `p`) se elige en el campo semántico.                | reading, heading          |
| `text`           | Text             | Párrafos, textos descriptivos, cualquier contenido textual plano que debe anunciarse.         | reading                   |
| `groupedText`    | Grouped text     | Conjunto de textos que se anuncian como una unidad (ej. nombre + email en una card).          | reading                   |
| `listItem`       | List item        | Un elemento dentro de una lista (el contenedor debe marcarse como `List`).                    | reading                   |
| `image`          | Image            | Imágenes que requieren texto alternativo. Elige entre `info` (informativa) y `func` (funcional). | reading, textAlt          |

### Interactivos básicos

| Rol              | Label            | Uso recomendado                                                                               | Capacidades               |
| ---------------- | ---------------- | --------------------------------------------------------------------------------------------- | ------------------------- |
| `button`         | Button           | Botón estándar que dispara una acción (submit, abrir modal, cerrar, etc.).                    | focus, reading            |
| `toggleButton`   | Toggle button    | Botón con dos estados que se mantiene pulsado/no pulsado (mute, pin).                         | focus, reading            |
| `link`           | Link             | Enlace a otra pantalla, URL externa o anchor dentro de la misma pantalla.                     | focus, reading            |
| `checkbox`       | Checkbox         | Casilla de selección múltiple (lista de opciones, aceptar términos).                          | focus, reading            |
| `switch`         | Switch           | Toggle binario (on/off) para configuraciones.                                                 | focus, reading            |

### Formularios

| Rol              | Label            | Uso recomendado                                                                               | Capacidades               |
| ---------------- | ---------------- | --------------------------------------------------------------------------------------------- | ------------------------- |
| `textField`      | Text field       | Input de texto de una línea.                                                                  | focus, reading            |
| `passwordField`  | Password field   | Input de contraseña (texto enmascarado).                                                      | focus, reading            |
| `searchField`    | Search field     | Input de búsqueda (con semántica específica de search).                                       | focus, reading            |
| `numberField`    | Number field     | Input numérico con validación/controles específicos.                                          | focus, reading            |
| `dateField`      | Date field       | Input de fecha (calendar picker o similar).                                                   | focus, reading            |
| `textArea`       | Text area        | Input de texto multilínea.                                                                    | focus, reading            |
| `slider`         | Slider           | Control de rango (volumen, zoom, filtro de precio).                                           | focus, reading            |

### Compuestos

| Rol              | Label            | Uso recomendado                                                                               | Capacidades               |
| ---------------- | ---------------- | --------------------------------------------------------------------------------------------- | ------------------------- |
| `tabBar`         | Tab bar          | Barra de pestañas que alterna entre varios paneles de contenido.                              | focus, reading            |
| `stepper`        | Stepper          | Control de incremento/decremento (cantidad en carrito, número de pasajeros).                  | focus, reading            |
| `accordion`      | Accordion        | Panel expandible/colapsable con título y contenido oculto.                                    | focus, reading            |
| `dropdown`       | Dropdown         | Selector que abre un popover con opciones (select, menú contextual, combobox).                | focus, reading            |
| `carousel`       | Carousel         | Carrusel de contenido navegable (banners, galería de imágenes).                               | focus, reading            |

### Estados permitidos por familia

Cada rol expone solo los estados que tienen sentido. La tabla resume
los bloques:

- **Roles sin estado** (`heading`, `text`, `groupedText`, `listItem`,
  `image`) — no exponen selector de State.
- **Actionable** (`button`, `link`, `carousel`, `slider`) —
  `Enabled / Disabled / Error` (`button` añade `Read only`).
- **Selectable** (`toggleButton`, `checkbox`, `tabBar`, `stepper`) —
  `Selected / Not selected / Disabled / Error`. `toggleButton` y
  `checkbox` fuerzan `focus: false` cuando están `disabled`.
- **Switch** (`switch`) — `On / Off / Disabled / Error`. `switch`
  fuerza `focus: false` cuando está `disabled`.
- **Text inputs** (`textField`, `passwordField`, `searchField`,
  `numberField`, `dateField`, `textArea`) — `Enabled / Disabled /
  Error / Filled / Read only`.
- **Expandable** (`accordion`, `dropdown`) — `Expanded / Collapsed /
  Disabled / Error`. `dropdown` propone `focus` y `reading` cuando
  está `expanded`.

---

## Referencia de estados

Los 11 estados del plugin, ordenados por uso:

| Estado         | Label         | Cuándo usarlo                                                                         |
| -------------- | ------------- | ------------------------------------------------------------------------------------- |
| `enabled`      | Enabled       | El elemento está disponible para interactuar (estado por defecto de interactivos).    |
| `disabled`     | Disabled      | El elemento no acepta interacción (visualmente apagado o bloqueado).                  |
| `error`        | Error         | El elemento está en estado de error (campo inválido, acción fallida).                 |
| `read-only`    | Read only     | El elemento muestra información pero no se puede editar (input bloqueado).            |
| `filled`       | Filled        | Un input ya tiene valor introducido.                                                  |
| `on`           | On            | Switch en posición activa.                                                            |
| `off`          | Off           | Switch en posición inactiva.                                                          |
| `selected`     | Selected      | Elemento seleccionable que está actualmente seleccionado (tab, checkbox, toggle).     |
| `not-selected` | Not selected  | Elemento seleccionable que no está seleccionado.                                      |
| `expanded`     | Expanded      | Accordion, dropdown o panel colapsable que está abierto.                              |
| `collapsed`    | Collapsed     | Accordion, dropdown o panel colapsable que está cerrado.                              |

Recuerda: qué estados puedes elegir depende del rol. Un `Heading` no
tiene selector de estado; un `Button` no puede estar `Selected`; un
`Switch` no puede estar `Expanded`. El plugin filtra
automáticamente.

---

## Settings

El icono de **⚙ engranaje** en la cabecera abre Settings como modal.
Mismo modal en los dos modos del plugin.

### Apariencia

Tres ajustes de presentación:

- **Theme** — seis opciones:
  - **System** — sigue el tema del sistema operativo.
  - **Paper** — tema claro cálido.
  - **Graphite** — tema oscuro neutro.
  - **Sky** — tema claro con acentos azules.
  - **Ocean** — tema oscuro con acentos azules.
  - **Leaf** — tema con acentos verdes.
- **Density** — dos niveles:
  - **Compact** — espaciado reducido, más filas visibles por pantalla.
  - **Normal** — espaciado estándar, más aire entre filas.
- **Font size** — rango discreto de 8pt a 24pt (valores disponibles:
  8, 10, 12, 14, 16, 18, 20, 22, 24).

### Idioma

Un selector con cinco idiomas:

- **Català**
- **English**
- **Español**
- **Euskara**
- **Galego**

El cambio es instantáneo — todos los textos del plugin se recargan
en el idioma elegido.

### About

Tres filas:

- **Version** — la versión instalada del plugin (hoy V0.7.8).
- **Changelog** — abre un modal con el CHANGELOG.md del proyecto
  renderizado como markdown.
- **Help** — abre un modal con este propio README renderizado como
  markdown. Si estás leyendo esto dentro del plugin, estás en ese
  modal.

### Zona de peligro

Acciones destructivas que eliminan metadata. Todas pasan por un
diálogo de confirmación con checkbox obligatorio ("I understand this
action cannot be undone"):

- **Clear selected node / Clear selected nodes** — elimina la
  metadata del nodo (o nodos) seleccionados y de todos sus
  descendientes. Solo está habilitado si hay selección y esa selección
  tiene metadata.
- **Clear current page** — elimina toda la metadata de todos los nodos
  de la página actual.
- **Clear entire document** — elimina toda la metadata de todas las
  páginas del archivo.

Tras ejecutar, el plugin muestra un feedback con el contador
`Cleared N key(s) from {scope}.`. No hay undo desde el plugin (sí
desde el undo nativo de Figma con Cmd+Z).

> ⚠️ **Atención**: a diferencia del botón **Limpiar** del footer —
> que preserva la baseline heredada con sentinels `null` — las
> acciones de Danger Zone borran literalmente el pluginData. Úsalas
> con cuidado, especialmente `Clear entire document`.

---

## Tips y mejores prácticas

Consejos de uso que ahorran tiempo y evitan dolor.

**Taggea primero en los componentes del design system.** Las
instancias heredan automáticamente — si taggeas una vez en el
componente origen, todas las instancias que viven en las pantallas
reciben los tags sin trabajo manual. Es el multiplicador más
importante del plugin. Invierte tiempo en el DS, recoge frutos en las
pantallas.

**Usa atributos personalizados para lo que no encaja.** `aria-describedby`,
referencias a live regions, estados visuales que no están en la
matriz estándar, identificadores de analytics: todo eso cabe como par
clave+valor. Pero no abuses: si algo se usa muchas veces, propón un
campo estructurado antes que acumular custom attributes.

**Marca frecuentemente.** El borrador local vive en memoria de UI: si
recargas el plugin (Cmd+Option+P) o cierras y vuelves a abrir sin
marcar, pierdes lo que no hayas persistido. No acumules sesiones
enteras de edición sin confirmar. Marca después de cada componente o
cada sección lógica.

**Genera el blueprint antes del handoff.** Los devs pueden consultar
la Vista de specs con el plugin abierto, pero el **blueprint
nativo** vive en el panel de Inspect sin depender del plugin. Si el
equipo de desarrollo está acostumbrado a inspeccionar en Dev Mode sin
plugins extra, el blueprint es el formato que van a ver por defecto.
Genéralo (o regenéralo) antes de anunciar que la pantalla está
lista.

**Usa las flechas, no números.** Nunca tienes que escribir un orden
de reading o focus a mano. Si el orden no queda como quieres, mueve
las filas con las flechas del cluster derecho: el plugin recalcula
toda la cascada. Los únicos números que vas a ver son los que
aparecen en los pills `R` y `F` (y esos se actualizan solos).

**Recarga rápido con Cmd+Option+P.** En Figma Desktop, el atajo
`Cmd+Option+P` re-ejecuta el último plugin usado. Si estás iterando en
el código del plugin (o en la pantalla), es más rápido que ir al
menú.

**Confía en los defaults.** Cuando asignas un rol, el plugin propone
valores razonables. No los cambies salvo que tengas motivo. Por
ejemplo, un `Button` viene con focus + reading activos por defecto:
eso es correcto en el 95% de los casos. No desactives reading por
costumbre; deja que el plugin guíe.

---

## Idiomas

La interfaz está disponible en **inglés, español, catalán, gallego y
euskera**. Se configura desde Settings dentro del plugin.

## Estado actual

El plugin está en **V1.1** y es funcional para los flujos de Vista
de edición, Vista de specs y Blueprint nativo en Dev Mode, incluyendo
enlaces a dev docs, notas de producto y atributos personalizados por
nodo, con herencia automática desde componentes del design system. El
trabajo principal que queda es definir con precisión el
comportamiento de cada rol semántico y su mapeo a atributos ARIA
concretos.

---

Privado — todos los derechos reservados. Ver [LICENSE](./LICENSE).
