<!-- Autor: Daniel Benjamin Perez Morales -->
<!-- GitHub: https://github.com/DanielPerezMoralesDev13 -->
<!-- Correo electrónico: danielperezdev@proton.me  -->
# ***"git branch" y "git switch"***

> *`git branch` y `git switch` son dos comandos utilizados en Git para trabajar con ramas. Sin embargo, cumplen diferentes funciones.*

## ***`git branch`***

> *El comando `git branch` se utiliza para crear, listar, renombrar y eliminar ramas en tu repositorio. Aquí están algunas de sus funciones más comunes:*

- ***Crear una nueva rama**: `git branch <nombre_rama>`*

- ***Listar ramas**: `git branch`*

- ***Eliminar una rama**: `git branch -d <nombre_rama>`*

- ***Cambiar el nombre de una rama**: `git branch -m <nombre_actual> <nuevo_nombre>`*

**Por ejemplo, para crear una nueva rama llamada `feature`, usarías:**

```bash
git branch feature
```

### `git switch`

> *El comando `git switch`, introducido en Git 2.23, se utiliza para cambiar entre ramas o para crear y cambiar a una nueva rama en una sola operación. Algunas de sus funciones son:*

- **Cambiar a una rama existente**: `git switch <nombre_rama>`

- **Crear y cambiar a una nueva rama**: `git switch -c <nombre_nueva_rama>`

**Por ejemplo, para cambiar a la rama `feature`, usarías:**

```bash
git switch feature
```

**Para crear una nueva rama llamada `new-feature` y cambiar a ella, usarías:**

```bash
git switch -c new-feature
```

- *A partir de Git 2.23, `git switch` es preferido sobre `git checkout` para cambiar de rama, ya que `git switch` proporciona una interfaz más clara y segura para esta operación.*

- *En resumen, `git branch` se utiliza para operaciones relacionadas con ramas, como crear, listar, renombrar y eliminar, mientras que `git switch` se utiliza específicamente para cambiar entre ramas o para crear y cambiar a una nueva rama en una sola operación.*
