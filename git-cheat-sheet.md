## Git Cheat sheet

### Instalacion windows

- Descargar aplicacion de la pagina principal
- Instalar la aplicacion en tu sistema operativo

### Configurar

Una vez instalado en tu sistema operativo verificar que se haya instalado correctamente y esto se hace habriendo el bash de git y tipeando `git --version`

Si podemos ver correctamente la versión, eso quiere decir que se ha instalado correctamente. Posterior verifada la instalación pasamos a configurar git.

```bash
$ git config --global user.name "Jonh Doe"
$ git config --global user.email "jonh@doe.com"
$ git config --global colors.ui true
```

### Comandos

| comando  | descripción |
|:---------|:-------------|
| `q` | Salir de información de git como cuando ejecutamos `git log` |
| `pwd` | Verficicar en que directorio nos encontramios |
| `git init` | Inicia un proyecto a monitorear |
| `git status` | Verifica el estado de un proyecto |
| `git add [*, -A, namefile]`| Archivos a agregar al commit |
| `git commit -m "mensaje"` | Crear un commit|
| `git log` | Lista los commit´s creados nos muestra los `SHA` |
| `git checkout SHA` | Comando para viajar entre commits |
| `git checkout master` | Nos redireccionamos a la rama(branch) master |
| `git reset --soft SHA` | Borra commit  |
| `git reset --mixed SHA` |   |
| `git reset --hard SHA` | Borra codigo y commit  |
| `git branch` | Muestra las ramas creadas|
| `git branch dev` | Crea una nueva rama con el nombre `dev` |
| `git checkout dev` | Nos movemos a la rama `dev` |
| `git branch -D dev` | Elimina la rama `dev` |
| **Fusionar ramas** | Fusionar rama `dev` cuando las pruebas fueron satisfactorias|
| `git checkout master` | Pasamos a la rama `master` - Rama que absorve |
| `git merge dev` | rama a la cual `master` absorve  |
|-|-|
| `git checkout -b dev` | Crea y nos mueve a la rama recien creada |
| `git remote add origin master` | Atamos la rama `master` al repositorio local |
| `git remote -v` | comprobamos atadura de las ramas |
| `git remote remove origin` | borramos la atadura de origin |
| `git push origin master` | Subimos al repositorio la rama `master` |
|-|-|
| `git commit --amend -m "nuevo mensaje"` | Cambiar texto commit hecho previamente |
| `git push origin master -f` | subir de nuevo un mensaje de un commit al repositorio |
|**Tags**| |
| `git tag `| Lista las etiquetas que se tengan|
| `git tag -a v0.0.1 -m "mensaje" SHA` | tag a un commit especifico dado por el codigo `SHA` |
| `git tag v0.0.1 SHA` | tag sin descripcion a un commir en especifico |
| `git show v0.0.1` | Ver informacino de un tag en especifico |
| `git push origin v0.0.1` | Compartimos/subimos el tag con el repositorio |
| `git push origin --tags` | Compartimos/subimos todos los tags en local al repositirio |
|**Workflows**| |
| `git fetch origin` | descargamos el codigo que tenemos en `master` o `dev` remoto |
| `git branch -a` | Ver ramas ocultas |
| `git merge origin/master` | fusionamos la rama oculta especificada `origin/master` o `origin/dev` |


### Ayuda

- **commit** es donde se guarda los cambios en archivos o archivos nuevos
- **pull request** es lo que hacemos para mandar nuestro trabajo a una rama master
- **issue** lista de errores detectados, nuevas caracteristicas o una idea nueva
- **milestones** grupos de issues, configuramos fecha de finalizacion proyecto
- **labels** nos sirve para organizar errores, featureds, etc. secciona por etiquetas
- **SHA** codigo que idetifica un commit ej: `84b572f7cf6d8709fe7c7fed678c1b2fc831384b` lo obtenemos con `git log`
- **rama** se le llama a si a los `branch` que podriamos tener
- **HEAD** nos referimos a que commit estamos situados ahora
- **Rama Master** esta es la que se crea cuando hacemos `git init`
- **Fast-Froward** fusión que generalmente se hace cuando se trabaja solo
- **Manual Merge** fusión que se realiza manualmente y es cuando se trabaja en equipo
- **rama dev** es la rama que generalmente se usara para hacer cosas nuevas, probar codigo que otro miembro del equipo haya hecho, despues de probar la funcionalidad se hace el `git merge master`
- **tags** las etiquetas son puntos especificos en la historia de un proyecto, igual podemos llamarlas como las versiones de un proyecto
- **tags anotadas** son tipos de tags al cual le pones un mesaje, mas descriptivo
- **tags ligeras** son tangs que no son descriptivos