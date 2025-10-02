# EJERCICIOS PARTE 2 – Git

Repositorio: [https://github.com/ErBusaa06/practica-git-parte1-MiguelAngel]

---

## Ejercicio 1: Ciclo básico de Git
```powershell
git add notas.md
git commit -m "feat: añade notas iniciales"
git push origin main

git commit -am "feat: amplía notas.md"
git push origin main```

## Ejercicio 2: Ramas

```git checkout -b feature-tareas
# Editar notas.md y añadir tareas
git commit -am "feat: añade lista de tareas pendientes"
git push -u origin feature-tareas

git checkout main
git merge feature-tareas
git push origin main

git branch -d feature-tareas
git push origin --delete feature-tareas````

## Ejercicio 3: Borrado y restauración

# Crear archivo temporal.txt y añadir contenido
```git add temporal.txt
git commit -m "feat: añade temporal.txt"
git push

git rm temporal.txt
git commit -m "chore: elimina archivo temporal"
git push

git restore temporal.txt ```

## Ejercicio 4: Logs y Difs

```git commit -am "feat: cambio 1 en notas.md"
git commit -am "feat: cambio 2 en notas.md"

git log --oneline --graph --all
git diff HEAD~1 HEAD```

## Ejercicio 5: Conflictos intencionados

```git checkout -b feature-conflicto
# Editar misma línea en feature-conflicto y commit
git commit -am "feat: modifica título en rama conflicto"

git checkout main
# Editar misma línea en main y commit
git commit -am "feat: modifica título en main"

git merge feature-conflicto
# Resolver conflicto manualmente en notas.md
git add notas.md
git commit -m "fix: resuelve conflicto en notas.md"
git push```

## Ejercicio 6: Tags

```git tag v1.0
git push origin --tags

git tag -a v1.1 -m "Primera versión estable"
git push origin --tags```





