# Git CheatSheets
Opciones de resumenes rapidios de comandos en git
- [Git official website](https://git-scm.com/cheat-sheet)
- [GitHub education](https://education.github.com/git-cheat-sheet-education.pdf)
- [Gitea](https://about.gitea.com/)

# Git Roadmap
Ruta de aprendizaje para implementación de Git/GitHub
- [GitHub roadmap](https://roadmap.sh/git-github)

# Vinculación local con cuenta en repositorio remoto
Ademas de [GitHub](), esto puede aplicar repositorios como:
- [GitLab](https://about.gitlab.com/)
- [Codeberg](https://codeberg.org/)

```bash
ssh-keygen -t ed25519 -C "tu_email" -f ~/.ssh/id_ed25519
eval "$(ssh-agent -s)" && ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
git clone git@github.com:NiengLee/configuraciones.git
```

# Creación de archivos que no estaran en el control de versiones
Este archivo se usa mucho para variables de entorno para proteger información sensible o que no se desea realizar control de versiones

```bash
touch .gitignore
```

# Comandos generales

| Comando                                                                                                                 | Acción                                                                                                       | flags comunes                        |
| ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ | ------------------------------------ |
| git config --global user.name "Tu Nombre"<br><br>git config --global user.email "[tu@correo.com](mailto:tu@correo.com)" | Configura nombre y correo que Git usa para firmar commits (a nivel global del usuario).                      | --global<br><br>--local              |
| git clone <ruta_repositorio>                                                                                            | Clona un repositorio remoto y crea una copia local con su historial.                                         | --depth 1<br>--branch rama           |
| git init                                                                                                                | Inicializa un repositorio Git vacío en el directorio actual (crea .git).                                     | --initial-branch rama                |
| git status                                                                                                              | Muestra el estado del working tree y staging area (cambios, archivos listos, no rastreados).                 | -sb                                  |
| git add archivo o .                                                                                                     | Agrega cambios al staging area (prepara archivos para commit).                                               | -A<br>-p                             |
| git commit -m "comentario"                                                                                              | Crea un commit con lo que está en staging, con un mensaje descriptivo.                                       | -m "msg"<br>--amend                  |
| git push                                                                                                                | Envía commits locales al repositorio remoto (actualiza la rama remota).                                      | -u origin rama<br>--force-with-lease |
| git fetch all                                                                                                           | Descarga referencias y commits del remoto sin mezclar con tu rama local.                                     | --all<br>--prune                     |
| git pull                                                                                                                | Trae cambios del remoto y los integra en la rama actual (fetch + merge/rebase).                              | --rebase<br>--ff-only                |
| git branch                                                                                                              | Lista, crea, renombra o borra ramas locales.                                                                 | -a<br>-m nueva<br>-D rama            |
| git log                                                                                                                 | Muestra el historial de commits.                                                                             | --oneline<br>--graph                 |
| git checkout                                                                                                            | Cambia de rama o “checkout” a un commit/estado específico (modo antiguo; hoy se usa también switch/restore). | -b <rama_nueva>  <br>--  archivo     |
| git stash                                                                                                               | Guarda cambios no comprometidos en un “stash” temporal y limpia el working tree.                             | push<br>pop                          |
| git merge                                                                                                               | Fusiona otra rama en la rama actual.                                                                         | --no-ff<br>--abort                   |
| git restore .                                                                                                           | Restaura archivos del working tree desde el índice/HEAD (revierte cambios no commiteados).                   | --staged<br>--source ref             |