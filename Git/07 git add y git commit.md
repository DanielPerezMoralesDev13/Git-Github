<!-- Autor: Daniel Benjamin Perez Morales -->
<!-- GitHub: https://github.com/DanielPerezMoralesDev13 -->
<!-- Correo electrónico: danielperezdev@proton.me -->

# ***"git add" y "git commit"***

---

## ***Agregar cambios***

> [!NOTE]
> *Para agregar cambios a tu repositorio, primero necesitarás agregar los ficheros modificados al área de preparación con `git add`. Puedes agregar todos los ficheros modificados con `git add .`, o agregar ficheros específicos con `git add [nombre del fichero]`.*

```bash
git add .
```

```bash
git add fichero.py
```

## **`git commit`**

> *El comando `git commit` crea un nuevo commit con los cambios que has agregado al área de preparación. Un commit es como un "punto de control" en tu proyecto al que puedes volver más tarde si es necesario.*

```bash
git commit
```

### ***`git commit -m`***

> *La opción `-m` te permite especificar un mensaje de commit directamente en la línea de comandos. Esto es útil si tu cambio es lo suficientemente simple como para describirlo en una sola línea.*

```bash
git commit -m "Tu mensaje de commit aquí"
```

---

### ***`git commit --message=`***

> *La opción `--message=` es equivalente a `-m`. Te permite especificar un mensaje de commit directamente en la línea de comandos.*

```bash
git commit --message="Tu mensaje de commit aquí"
```

---

#### ***`Eliminar commits`***

*Hay varias formas de eliminar un commit en Git, dependiendo de tus necesidades y de si el commit que deseas eliminar ya ha sido compartido con otros o no. Aquí te muestro algunas formas comunes:*

1. **`git reset`:** *Puedes usar `git reset` para eliminar el commit y opcionalmente mover la rama hacia atrás en la historia. Ten en cuenta que esto puede eliminar el commit y deshacer los cambios locales, así que úsalo con precaución. Por ejemplo:*

   ```bash
   git reset --hard HEAD~1
   ```

   *Esto eliminará el último commit y todos los cambios asociados.*

2. **`git revert`:** *Esta opción crea un nuevo commit que revierte los cambios realizados en el commit que deseas eliminar. No modifica la historia existente, lo que la hace más segura si el commit ya ha sido compartido con otros. Por ejemplo:*

   ```bash
   git revert <ID_del_commit>
   ```

   *Esto creará un nuevo commit que deshace los cambios introducidos por el commit especificado.*

3. **`git rebase -i`:** *Puedes usar la opción interactiva de rebase para eliminar un commit. Esto te permite reescribir la historia de la rama. Por ejemplo:*

   ```bash
   git rebase -i HEAD~2
   ```

   *Esto abrirá un editor interactivo donde puedes elegir eliminar el commit.*

4. **`git cherry-pick`:** *Puedes usar `git cherry-pick` para seleccionar los cambios de otros commits y aplicarlos en una nueva rama, sin incluir el commit que deseas eliminar.*

5. **`git reset --soft`:** *Similar a `git reset --hard`, pero mantiene los cambios en el área de preparación (staging), lo que te permite modificar los archivos y realizar un nuevo commit sin perder los cambios. Por ejemplo:*

   ```bash
   git reset --soft HEAD~1
   ```

   *Esto deshace el último commit pero mantiene los cambios en el área de preparación.*

6. **`git revert --no-commit`:** *Similar a `git revert`, pero no realiza un commit inmediato, lo que te permite realizar cambios adicionales antes de crear el commit de reversión. Por ejemplo:*

   ```bash
   git revert --no-commit <ID_del_commit>
   ```

   *Luego puedes hacer más cambios y luego hacer un commit cuando estés listo.*

- *Estas son algunas de las formas comunes de eliminar commits en Git. Cada método tiene sus propias implicaciones y es importante entender cómo afectarán a tu historial de commits y a cualquier colaborador que esté trabajando en el mismo repositorio.*

> [!NOTE]
> **Nota:** *Recuerda que los mensajes de commit deben ser descriptivos y significativos para ayudar a otros desarrolladores (o a ti mismo en el futuro) a entender qué cambios se realizaron en cada commit.*
