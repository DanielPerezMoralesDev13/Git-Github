<!-- Autor: Daniel Benjamin Perez Morales -->
<!-- GitHub: https://github.com/DanielPerezMoralesDev13 -->
<!-- Correo electrónico: danielperezdev@proton.me  -->
# ***"git clone"***

- *El comando `git clone` se utiliza para clonar un repositorio Git existente desde un repositorio remoto (por lo general, en un servidor como GitHub, GitLab o Bitbucket) y crear una copia local del mismo en tu máquina. Aquí tienes cómo usar `git clone`:*

```bash
git clone <URL_del_repositorio> [<directorio_destino_opcional>]
```

- *`<URL_del_repositorio>` es la URL del repositorio remoto que deseas clonar. Puedes obtener esta URL desde la página del repositorio en la plataforma de alojamiento (por ejemplo, GitHub).*

- *`[<directorio_destino_opcional>]` es opcional y especifica el directorio donde se clonará el repositorio. Si no se proporciona, se creará un nuevo directorio con el nombre del repositorio.*

**Ejemplo:**

```bash
git clone https://github.com/usuario/proyecto.git
```

- **Esto clonará el repositorio `proyecto` del usuario `usuario` en GitHub y creará un nuevo directorio llamado `proyecto` en tu directorio actual.**

```bash
git clone https://github.com/usuario/proyecto.git mi_proyecto
```

```bash
git clone https://github.com/usuario/proyecto.git ../mi_proyecto
```

*Esto clonará el repositorio `proyecto` en un nuevo directorio llamado `mi_proyecto` en tu directorio actual.*

- **Una vez que hayas clonado el repositorio, tendrás una copia local completa del repositorio remoto en tu máquina, incluyendo todas las ramas y el historial de cambios. Puedes trabajar en este repositorio localmente y utilizar comandos como `git add`, `git commit`, `git push`, etc., para interactuar con el repositorio remoto.**
