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
# Comandos Básicos

**Agregar a stage**
```zsh
git add -A    #Agrega todos los cambios
git add -u    #Agrega las eliminaciones
```
