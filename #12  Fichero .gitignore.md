# ***"Fichero .gitignore"***

> *El fichero `.gitignore` se utiliza en Git para especificar ficheros y directorios que deseas ignorar en el control de versiones. Esto significa que Git no rastreará ni incluirá los ficheros y directorios enumerados en este fichero en tus commits. Esto es útil para evitar incluir ficheros generados automáticamente, ficheros de compilación, ficheros temporales y otros ficheros que no deseas que estén bajo control de versiones.*

**Aquí hay un ejemplo simple de un fichero `.gitignore`:**

```bash
# Ignorar ficheros de compilación generados
*.o
*.out
*.py

# Ignorar todos los archivos dentro de la carpeta fotos
fotos/

# Excepto el archivo background.png dentro de la carpeta fotos
!fotos/background.png

# No ignorar "main.py" incluso si otros archivos están siendo ignorados
!main.py

# Ignorar ficheros de objetos compilados en C
*.c~

# Ignorar ficheros de respaldo de Emacs
*~

# Ignorar ficheros de configuración local
config.ini

# Ignorar directorios generados automáticamente
/build/
/node_modules/
```

```css
proyecto/
│   main.py
│
├── fotos/
│   │   foto1.jpg
│   │   foto2.jpg
│   │   background.png
│   │
│   └── subfolder/
│       │   foto3.jpg
│       │   foto4.jpg
```

*En este ejemplo:*

- *`*.o` e `*.out` y `*.py` ignorarán todos los ficheros con extensión `.o` e `.out` y `*.py`, respectivamente.

- *`fotos/` indica que se deben ignorar todos los archivos y subdirectorios dentro de la carpeta fotos.*

- *`!fotos/background.png` anula la regla anterior y especifica que el archivo background.png dentro de la carpeta fotos no debe ser ignorado. La exclamación ! se utiliza para negar la regla de ignorar.*

- *`!main.py` especifica que el archivo main.py no debe ser ignorado, incluso si otros archivos están siendo ignorados por otras reglas en el .gitignore.*

- *`*.c~` ignorará todos los ficheros que terminen en `.c~`.*

- *`*~` ignorará todos los ficheros que terminen en `~`.*

- *`config.ini` ignorará un fichero específico llamado `config.ini`.*

- *`/build/` y `/node_modules/` ignorarán los directorios llamados `build` y `node_modules`, respectivamente, junto con todo su contenido.**

- *Puedes crear y personalizar tu fichero `.gitignore` según las necesidades específicas de tu proyecto. Es importante tener en cuenta que los patrones en este fichero se aplican de manera recursiva a los subdirectorios a menos que se especifique lo contrario.*

```bash
git config --global core.excludesfile sda/sda1/directory/.gitignore
```

- *`git config --global core.excludesfile sda/sda1/directory/.gitignore`: Este comando configura un archivo `.gitignore` global para tu usuario. Especifica la ubicación del archivo `.gitignore` global en el directorio `sda/sda1/directory`. Los patrones de ignorados definidos en este archivo se aplicarán a todos los repositorios en tu sistema.*
