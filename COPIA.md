# Copia de documentos-vaticanos

Repositorio creado el 2026-07-22 como **copia** de:

https://github.com/RafaelAngelRamirez/documentos-vaticanos

## Completar la copia con todo el historial y los JSON grandes (Biblia/Catecismo)

En esta máquina el CLI `gh` no está autenticado, así que el mirror completo hay que terminarlo con un token o `gh auth login`:

```bash
gh auth login

git clone --mirror https://github.com/RafaelAngelRamirez/documentos-vaticanos.git
cd documentos-vaticanos.git
git remote set-url origin https://github.com/RafaelAngelRamirez/documentos-vaticanos-copia.git
git push --mirror
```

Eso reemplaza el contenido actual por una copia 1:1 (historial, tags, assets grandes).

## Alternativa sin borrar lo ya subido

```bash
git clone https://github.com/RafaelAngelRamirez/documentos-vaticanos.git
cd documentos-vaticanos
git remote rename origin upstream
git remote add origin https://github.com/RafaelAngelRamirez/documentos-vaticanos-copia.git
git push -u origin --all
git push origin --tags
```
