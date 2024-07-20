<!-- Autor: Daniel Benjamin Perez Morales -->
<!-- GitHub: https://github.com/DanielPerezMoralesDev13 -->
<!-- Correo electrónico: danielperezdev@proton.me -->

# ***"git fetch" y "git pull"***

> *`git fetch` y `git pull` son dos comandos relacionados con la obtención de cambios desde un repositorio remoto, pero tienen algunas diferencias clave en cuanto a su funcionamiento.*

## ***`git fetch`:***

- *El comando `git fetch` descarga los últimos cambios del repositorio remoto a tu repositorio local, pero no los fusiona automáticamente con tu rama actual.*

- *Actualiza las referencias remotas (por ejemplo, `origin/main`) en tu repositorio local para que reflejen las referencias actuales del repositorio remoto.*

- *Los cambios descargados se almacenan en el repositorio local, pero no afectan tu trabajo actual.*

- *Te permite revisar los cambios antes de fusionarlos manualmente.*

---

### ***`git pull`:***

- *El comando `git pull` realiza dos acciones en una: primero, realiza un `git fetch` para obtener los últimos cambios del repositorio remoto, y luego realiza un `git merge` para fusionar automáticamente esos cambios en tu rama local.*

- *Es una forma rápida de obtener los últimos cambios del repositorio remoto y fusionarlos directamente en tu rama local.*

- *Si hay conflictos de fusión, Git intentará fusionar automáticamente los cambios si es posible. Si no es posible, te pedirá que resuelvas los conflictos manualmente.*

---

### ***Diferencias clave:***

- *`git fetch` solo descarga los cambios y actualiza las referencias remotas en tu repositorio local, sin fusionar automáticamente. Es útil si quieres revisar los cambios antes de fusionarlos.*

- *`git pull` realiza una fusión automática después de descargar los cambios, lo que puede ser conveniente si estás seguro de que quieres fusionar los cambios directamente en tu rama local.*

- **En resumen, si prefieres revisar los cambios antes de fusionarlos, utiliza `git fetch` seguido de un `git merge` o `git rebase`. Si estás seguro de que quieres fusionar los cambios directamente en tu rama local, puedes usar `git pull`.**

> [!IMPORTANT]
> *El comando `git pull` se utiliza para obtener y fusionar cambios del repositorio remoto a la rama actual. Existen varias opciones interesantes que puedes usar con `git pull` para ajustar el proceso de actualización según tus necesidades.*

---

## ***Opciones de `git pull`***

1. **`<remoto> <rama>`**
   - **Función:** *Obtiene y fusiona la rama especificada del repositorio remoto a la rama actual.*
   - **Uso:** *Permite actualizar la rama actual con los cambios de una rama específica en el remoto.*
   - **Ejemplo:**

     ```bash
     git pull origin main
     ```

2. **`--rebase`**
   - **Función:** *Realiza un rebase en lugar de una fusión al aplicar los cambios del remoto.*
   - **Uso:** *Para mantener un historial lineal al aplicar cambios en la parte superior de la rama actual en lugar de hacer una fusión.*
   - **Ejemplo:**

     ```bash
     git pull --rebase origin main
     ```

3. **`--no-rebase`**
   - **Función:** *Desactiva el rebase si está configurado por defecto y realiza una fusión tradicional.*
   - **Uso:** *Usado para forzar una fusión en lugar de un rebase si la configuración predeterminada es diferente.*
   - **Ejemplo:**

     ```bash
     git pull --no-rebase origin main
     ```

4. **`--ff-only`**
   - **Función:** *Permite la fusión solo si puede ser realizada como un avance rápido (fast-forward).*
   - **Uso:** *Para evitar fusiones que requieren una fusión de commits no lineales.*
   - **Ejemplo:**

     ```bash
     git pull --ff-only origin main
     ```

5. **`--no-commit`**
   - **Función:** *Realiza la fusión pero no hace commit automáticamente.*
   - **Uso:** *Permite revisar los cambios antes de confirmar la fusión.*
   - **Ejemplo:**

     ```bash
     git pull --no-commit origin main
     ```

6. **`--no-ff`**
   - **Función:** *Realiza una fusión sin avance rápido, creando siempre un nuevo commit de fusión.*
   - **Uso:** *Para asegurar que la fusión se registre explícitamente en el historial.*
   - **Ejemplo:**

     ```bash
     git pull --no-ff origin main
     ```

7. **`--quiet` o `-q`**
   - **Función:** *Suprime la salida del comando para que solo se muestren los errores.*
   - **Uso:** *Para una salida menos verbosa durante la actualización.*
   - **Ejemplo:**

     ```bash
     git pull --quiet origin main
     ```

8. **`--verbose` o `-v`**
   - **Función:** *Muestra información detallada sobre el proceso de actualización.*
   - **Uso:** *Para ver más detalles sobre los cambios y el proceso de fusión.*
   - **Ejemplo:**

     ```bash
     git pull --verbose origin main
     ```

9. **`--all`**
   - **Función:** *Obtiene y fusiona cambios de todas las ramas remotas.*
   - **Uso:** *Actualiza todas las ramas locales con sus ramas remotas correspondientes.*
   - **Ejemplo:**

     ```bash
     git pull --all
     ```

10. **`--squash`**
    - **Función:** *Obtiene los cambios del remoto y los aplasta (squash) en un solo commit, sin hacer una fusión completa.*
    - **Uso:** *Para combinar todos los commits de la rama remota en un solo commit.*
    - **Ejemplo:**

      ```bash
      git pull --squash origin main
      ```

*Estas opciones te permiten ajustar cómo se obtienen y aplican los cambios del repositorio remoto, proporcionando flexibilidad para manejar diferentes escenarios de actualización.*
