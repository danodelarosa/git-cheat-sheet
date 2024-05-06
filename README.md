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