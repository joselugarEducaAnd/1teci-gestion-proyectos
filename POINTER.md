# Publicación — 1teci-gestion-proyectos

**URL en vivo:** https://joselugareducaand.github.io/1teci-gestion-proyectos/
**Repositorio:** https://github.com/joselugarEducaAnd/1teci-gestion-proyectos (Pages con `build_type=workflow`)
**Clon de trabajo (Mac mini):** `~/repos_publicacion/1teci-gestion-proyectos`
**Publicado:** 2026-08-04 · caso `DOCA-015`

## Cómo republicar

1. En eXeLearning 4, abrir `materiales_alumnado/exelearning/1teci-gestion-proyectos.elpx`
   y exportar a **sitio web** sobre `materiales_alumnado/exelearning/gestion-y-desarrollo-de-proyectos_web/`.
2. `rsync -a --delete` de esa carpeta a `publicado/exelearning/1teci-gestion-proyectos/` y a `~/repos_publicacion/1teci-gestion-proyectos/`.
3. En el clon: borrar `content.xml` (es la fuente editable, no va a la web), `git add -A`,
   commit y `git push` **por SSH** (el token no tiene scope `workflow`).
4. Regenerar el `ai_context` con `elp-a-md-ia` si ha cambiado el contenido.

El `.elpx` es la **fuente de verdad**: no se regenera, se parchea in situ.
