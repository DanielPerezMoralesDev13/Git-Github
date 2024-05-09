<!-- Autor: Daniel Benjamin Perez Morales -->
<!-- GitHub: https://github.com/DanielPerezMoralesDev13 -->
<!-- Correo electrónico: danielperezdev@proton.me  -->
# ***"git push"***

> *El comando `git push` se utiliza para enviar los cambios locales que has realizado en tu repositorio Git a un repositorio remoto, como GitHub, GitLab o Bitbucket. Aquí tienes cómo usar `git push`:*

```bash
git push <nombre_remoto> <nombre_rama_local>:<nombre_rama_remota>
```

- *`<nombre_remoto>` es el nombre del repositorio remoto al que deseas enviar tus cambios. Por lo general, este es `origin` si has clonado el repositorio, pero también puedes tener otros repositorios remotos configurados.*

- *`<nombre_rama_local>` es el nombre de la rama local que deseas enviar al repositorio remoto.*

- *`<nombre_rama_remota>` es el nombre de la rama en el repositorio remoto donde deseas enviar tus cambios. Por lo general, es el mismo nombre que la rama local, pero puedes enviar cambios a una rama con un nombre diferente si es necesario.*

**Ejemplo:**

```bash
git push origin main
```

- *Esto enviará los cambios de tu rama local `main` al repositorio remoto llamado `origin` y los fusionará con la rama `main` en el repositorio remoto.*

```bash
git push origin mi_rama_local:mi_rama_remota
```

- *El carácter **:** se utiliza para especificar qué ramas locales deben ser empujadas a qué ramas remotas.*

- *Esto enviará los cambios de tu rama local `mi_rama_local` al repositorio remoto llamado `origin` y los fusionará con la rama `mi_rama_remota` en el repositorio remoto.*

- *Después de ejecutar `git push`, los cambios serán enviados al repositorio remoto y estarán disponibles para otros colaboradores del proyecto. Es importante tener en cuenta que necesitas tener permisos de escritura en el repositorio remoto para poder realizar un push exitoso.*
