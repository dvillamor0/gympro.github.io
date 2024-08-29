# gympro.github.io-
Front de manera alternativa para gympro

## Commits pesados:
```
#!/bin/bash

# Obtener la lista de archivos sin seguimiento
untracked_files=$(git ls-files --others --exclude-standard)

# Verificar si hay archivos sin seguimiento
if [ -n "$untracked_files" ]; then
    # Iterar sobre cada archivo sin seguimiento y hacer commit individual
    for file in $untracked_files; do
        # Agregar el archivo al staging area
        git add "$file"
        # Hacer commit del archivo
        git commit -m "Añadir $file"
    done
else
    echo "No hay archivos sin seguimiento en el directorio $untracked_directory para hacer commit."
fi
```

## Push por commit:
Se debe iterar la ejecucion de este comando hasta subir los archivos.
```
#!/bin/bash

# Obtener la lista de commits locales
commits=$(git log --pretty=format:"%H" origin/main..HEAD)

# Verificar si hay commits locales
if [ -n "$commits" ]; then
    # Iterar sobre cada commit y hacer push
    for commit in $commits; do
        # Hacer push del commit actual
        git push origin "$commit":main
    done
else
    echo "No hay commits locales para hacer push."
fi
```
# Remplazo js
httpServerLocation:"/assets/
httpServerLocation:"/gympro.github.io/assets/

## Renombrar y cambiar
renombrar: *_expo -> expo*

cambiar: *_expo -> ./expo* en index.html