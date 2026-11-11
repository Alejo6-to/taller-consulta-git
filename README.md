# Guía de Actividad: Dominando Git, GitHub y GitFlow

**Modalidad:** Individual.

Esta actividad está dividida en dos grandes secciones: primero, una investigación teórica que deberán entregar directamente a mi repositorio mediante un *Pull Request*; y segundo, una simulación práctica del flujo de trabajo **GitFlow** que realizarán en sus propias cuentas.

---

## Parte 1: Contextualización e Investigación

Antes de escribir comandos, es crucial entender las herramientas. Deberán investigar los siguientes puntos. Las respuestas formarán parte de su entregable.

1. **¿Qué es Git y qué problema resuelve en el desarrollo de software?**
2. **Diferencias clave entre Git y GitHub.** (Expliquen por qué no son lo mismo).
3. **¿Qué es una nube de repositorios?** Expliquen este concepto y mencionen al menos tres alternativas diferentes en el mercado (por ejemplo, además de GitHub, ¿qué otras plataformas existen?).
4. **Glosario básico:** Definan con sus propias palabras, de forma clara y **agregando un ejemplo práctico para cada uno**, los siguientes conceptos fundamentales de Git:
   * *Commit*
   * *Branch* (Rama)
   * *Merge* (Fusión)
   * *Pull* y *Push*
   * *Pull Request (PR)*
   * *Clone* (Clonar)
   * *Upstream* (y su diferencia con *Origin*)
5. **La importancia de las ramas (Branches):** ¿Por qué se deben crear ramas en un proyecto de software? Expliquen para qué sirven y qué ventajas ofrecen tanto en el trabajo individual como en equipo.
6. **¿Qué es GitFlow?** Expliquen brevemente la estructura de sus ramas principales (`master`, `develop`, `feature`, `release`, `hotfix`).

---

## Parte 2: Entrega de la Investigación (Flujo Fork y Pull Request)

He creado un repositorio base para esta clase. Este repositorio ya cuenta con las ramas `master` y `develop`. Para entregar su investigación, deberán seguir estrictamente estas fases.

### Fase 1: Hacer Fork del repositorio
Un *Fork* es una copia exacta de mi repositorio original, pero guardada en su cuenta personal de GitHub.
1. Entren al enlace del repositorio que les he compartido.
2. En la esquina superior derecha de la página de GitHub, hagan clic en el botón que dice **"Fork"**.
3. Seleccionen su cuenta de GitHub personal como destino.
4. **¡Muy importante!** Desmarquen la casilla inferior que dice **"Copy the `master` branch only"** (Copiar solo la rama master). Necesitamos que se copien todas las ramas (`master` y `develop`) a su fork.
5. Hagan clic en **"Create fork"**. Ahora tienen su propia copia del repositorio.

### Fase 2: Clonar el repositorio, crear una rama y abrir el editor
Ahora deben llevar ese repositorio de la nube a su computadora local y aislar su trabajo.
1. En su repositorio *forkeado*, hagan clic en el botón verde **"<> Code"** y copien la URL (HTTPS o SSH).
2. Abran su terminal o línea de comandos.
3. Ejecuten: `git clone <URL_QUE_COPIARON>`
4. Entren a la carpeta del proyecto: `cd <nombre-del-repo>`
5. **Crear una nueva rama:** Como buena práctica, no trabajarán en la rama principal. Ejecuten el comando para crear y moverse a una nueva rama con su nombre: 
   `git checkout -b consulta-SuNombre` *(Ejemplo: `git checkout -b consulta-AnaGomez`)*
6. Abran la carpeta en su editor de código (por ejemplo, `code .` para VS Code).

### Fase 3: Creación del archivo de entrega
1. Dentro de su nueva rama, creen un archivo Markdown (`.md`).
2. El nombre del archivo **debe** seguir exactamente esta estructura: `CC-Nombre.md` (Por ejemplo: `10203040-AnaGomez.md`).
3. En este archivo, redactarán las respuestas de la investigación de la **Parte 1**.

### Fase 4: Un Commit por cada punto de consulta (¡Importante!)
Para demostrar el control de versiones, **no pueden subir todo de una sola vez**. Deben hacer un *commit* separado por cada punto que respondan.

1. Respondan el **Punto 1** en su archivo.
   * Guarden el archivo y ejecuten: `git add .`
   * Ejecuten: `git commit -m "docs: agregar definicion y proposito de Git"`
2. Respondan el **Punto 2** en su archivo.
   * Guarden el archivo y ejecuten: `git add .`
   * Ejecuten: `git commit -m "docs: explicar diferencias entre git y github"`
3. Repitan este proceso (guardar, `add`, `commit`) para los **Puntos 3, 4, 5 y 6**. Asegúrense de usar mensajes de commit descriptivos para cada uno.
4. Una vez tengan todos los commits listos, suban su nueva rama a su repositorio en GitHub: 
   `git push origin consulta-SuNombre`

### Fase 5: Crear el Pull Request (PR) de entrega
1. Vayan a la página de GitHub de su repositorio *forkeado*.
2. Verán un aviso de que han subido una nueva rama. Hagan clic en **"Compare & pull request"**.
3. Asegúrense de que el "base repository" sea mi repositorio original (apuntando a mi rama `develop` o `master`, según les indique en clase) y el "head repository" sea su fork en la rama `consulta-SuNombre`.
4. Pónganle un título claro a su PR (Ej: *Entrega Investigación - Su Nombre*).
5. Hagan clic en **"Create pull request"**. ¡Listo! Han enviado su investigación.

---

## Parte 3: Simulación Individual de GitFlow

Ahora que entienden los conceptos, van a simular el ciclo de vida de **GitFlow** ustedes mismos dentro de su propio repositorio forkeado.

### Paso a Paso del Flujo:

1. **Posicionarse en Develop:** 
   * En su terminal, regresen a la rama de desarrollo: `git checkout develop`
   *(Si por alguna razón no tienen los últimos cambios, hagan un `git pull origin develop`).*
2. **Crear un Feature:**
   * Imaginen que van a desarrollar una nueva funcionalidad. Creen una rama feature: `git checkout -b feature/mi-practica`
   * Creen un archivo llamado `practica.txt`, escriban algo, guárdenlo.
   * Hagan el ciclo de guardado: `git add .`, `git commit -m "feat: agregar archivo de practica"`, y finalmente `git push origin feature/mi-practica`.
3. **Integrar el Feature a Develop:**
   * Vayan a su GitHub (en su fork) y creen un Pull Request desde su rama `feature/mi-practica` hacia su propia rama `develop`.
   * Aprueben y hagan el *Merge* de ese Pull Request.
4. **Preparar el Release:**
   * Vuelvan a su terminal y actualicen su develop local: `git checkout develop` y luego `git pull origin develop`.
   * Creen una rama de lanzamiento: `git checkout -b release/v1.0`
   * Creen un archivo `changelog.md` detallando que se agregó la práctica.
   * Hagan `add`, `commit` y `push` de esta rama `release/v1.0`.
5. **Paso a Producción (Master):**
   * En GitHub, abran un PR desde su rama `release/v1.0` hacia su rama `master`. 
   * Hagan el *Merge*. 
   * (Opcional pero recomendado en GitFlow real: Abran otro PR de `release/v1.0` hacia `develop` para asegurar que los cambios del release también queden en la línea de desarrollo).

---
**¡Mucho éxito dominando las ramas y los flujos de trabajo!**