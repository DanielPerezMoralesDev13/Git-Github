# ***"git fetch" y "git pull"***

> *`git fetch` y `git pull` son dos comandos relacionados con la obtención de cambios desde un repositorio remoto, pero tienen algunas diferencias clave en cuanto a su funcionamiento.*

## ***`git fetch`:***

- *El comando `git fetch` descarga los últimos cambios del repositorio remoto a tu repositorio local, pero no los fusiona automáticamente con tu rama actual.*

- *Actualiza las referencias remotas (por ejemplo, `origin/main`) en tu repositorio local para que reflejen las referencias actuales del repositorio remoto.*

- *Los cambios descargados se almacenan en el repositorio local, pero no afectan tu trabajo actual.

- Te permite revisar los cambios antes de fusionarlos manualmente.*

### ***`git pull`:***

- *El comando `git pull` realiza dos acciones en una: primero, realiza un `git fetch` para obtener los últimos cambios del repositorio remoto, y luego realiza un `git merge` para fusionar automáticamente esos cambios en tu rama local.*

- *Es una forma rápida de obtener los últimos cambios del repositorio remoto y fusionarlos directamente en tu rama local.*

- *Si hay conflictos de fusión, Git intentará fusionar automáticamente los cambios si es posible. Si no es posible, te pedirá que resuelvas los conflictos manualmente.*

### ***Diferencias clave:***

- *`git fetch` solo descarga los cambios y actualiza las referencias remotas en tu repositorio local, sin fusionar automáticamente. Es útil si quieres revisar los cambios antes de fusionarlos.*

- *`git pull` realiza una fusión automática después de descargar los cambios, lo que puede ser conveniente si estás seguro de que quieres fusionar los cambios directamente en tu rama local.*

- **En resumen, si prefieres revisar los cambios antes de fusionarlos, utiliza `git fetch` seguido de un `git merge` o `git rebase`. Si estás seguro de que quieres fusionar los cambios directamente en tu rama local, puedes usar `git pull`.**
