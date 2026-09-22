# Bitácora de incidentes
## 1. Borrado accidental
- Qué pasó: el git deja de reconocer el archivo acuerdos.md debes volver a tarer el repositorio actualizado con git pull 
- Comando que usamos: git pull, git restore - nombre archivo que quermeos restaurar, git add, git status, git commit, git push para subir nuevamente la ultima version del archivo que se elimino accidentalmente 
- Resultado: Recuperacion en github del archivo acuerdos.md eliminado accidentalmente exactamente como se encontraba en el ultimo commit guardado 

## 2. El cambio que nadie pidío 
- que pasó: Se realizó una modificación no deseada directamente en el archivo local README.md al escribir la frase ESTO NO VA al inicio del documento y guardarlo. Este cambio quedó guardado únicamente en el directorio de trabajo (working directory), sin ser añadido al área de preparación (staging area).
- comando que usamos: git diff, git restore README.MD
- Resultado: El archivo README.md se restauró inmediatamente a su estado original. La línea modificada ESTO NO VA fue eliminada por completo, dejando el archivo exactamente como se encontraba en el último commit guardado

## 3. El add equivocado 
- que pasò: Se creó un archivo local llamado borrador.txt y se ejecutó accidentalmente el comando git add ., lo que causó que este archivo no deseado fuera enviado y guardado en el área de preparación staging , quedando listo para ser incluido en el próximo commit.
- comando que usamos: git restore --staged borrador.txt, rm borrador.txt
- Resultado: El archivo borrador.txt fue eliminado  del área de preparación y posteriormente, eliminado de forma física de la computadora, evitando que se incluya en el historial del repositorio.

## 4. La auditoría
- que pasó: Surgió la necesidad de investigar el historial del proyecto para identificar con precisión qué persona redactó el documento acuerdos.md y determinar cuánto tiempo ha transcurrido desde que se realizó dicha modificación.
- comando que usamos: git log --pretty=format:"%h | %an | %ar" acuerdos.md, git show --stat <hash>
- Resultado: Se obtuvo un reporte detallado que revela la identidad del desarrollador responsable del cambio, la fecha exacta de su autoría y el impacto detallado de la modificación en el archivo auditado.
