# Configuración

**Nombre o correo**
```zsh
git config user.name "nombre"
git config user.email "correo@correo.com"
```

**Ver lista de valores de la configucarión**
```zsh
git config --list
git config user.name
```

**Crear una llave ssh**
```zsh
ssh-keygen -t ed25519 -C "correo@correo.com" #Genera la llave
eval "$(ssh-agent -s)"                       #Inicia al agente
ssh-add ~/ruta/.ssh/id_ed25519               #Agrega la llave
pbcopy < archivo.pub                         #Copia la llave al porta papeles
ssh -T git@github.com                        #Verifica la autenticación
```

**Agregar repositorio remoto**
```zsh
git remote add origin https://remoto
git branch -M main
got push -u origin main
```

# Comandos Básicos

**Agregar a stage**
```zsh
git add -A    #Agrega todos los cambios
git add -u    #Agrega las eliminaciones
```

# Ramas

**Crear y cambiar a nueva rama**
```zsh
git switch -c nueva-rama
```

**Renombrar rama**
git branch -m vieja-rama nueva-rama

# Merge
*Debes de moverte primero a la rama a donde quieres agregar los cambios*
```zsh
git switch main
git merge ramaNueva
```

# Comandos utiles

**Estado actual**
```zsh
git status
git -s
```
**Cambiar los colores**
```zsh
git config color.status.branch color
git config color.status.added blue
git config color.status.untracked "141 bold" #Dependerá de los colores que tu terminal pueda soportar
```

**Logs de commits**
```zsh
git log --oneline
git log -n 2        #Sólo los úlitmos 2 commits
git --format=short
```

**Diferencias entre staging y área de trabajo**
```zsh
git diff
```

**Stash area**
Es un espacio donde podremos guardar cambios que no queremos que se guarden en el historial
```zsh
git stash                         #Guarda los cambios en la pila stash
git stash list                    #Muestra la pila de stash
git stash pop                     #Restaura el primer elemento de la pila (el úlitmo agregado)
git stash save "nombre del stash" #Guarda con un nombre personalizado tu stash
git stash pop stash@{0}           #Saca de la pila un stash en especifico
```