

- **Alumno:** Vanessa Victoria Wilczek
- **Bloque:** B0 — Prerrequisitos
- **Fase / ejercicio:** Fase 0.8
- **Fecha de inicio:** 23/10/2026
- **Fecha de entrega:** 23/10/2026

---

## 🎯 Qué se pedía

(Dos o tres líneas con tus palabras: qué había que conseguir.)
Se tenía que crear un inventario desde 0, guardarlo en tres versiones y volver a la primera antes de volver a main y para finalizar cuando se complete la bitacora, se hará un cuarto commit.
## ⌨️ Comandos y pasos importantes

- `comando` — para qué sirve.
git --version = Muestra la versión de Git instalada; no instala ni actualiza nada.

git config --global user.name = Muestra el nombre global que Git usará como autor; debe ser el tuyo.

git config --global user.email = Muestra el correo global del autor de los commits; debe ser el tuyo.

ls -l ~/.ssh/id_ed25519 ~/.ssh/id_ed25519.pub = Comprueba que existen los archivos de clave privada y pública; no muestra su contenido.

ssh -T git@github.com = Prueba la autenticación con GitHub. El saludo debe identificar tu usuario; no abre una shell ni sube archivos.

pwd = Muestra la carpeta actual. Contrasta su ruta con la indicada en este paso antes de seguir.

git init = Crea el repositorio local en la carpeta que acabas de comprobar.

git branch -M main = Establece main como nombre de la rama actual.

git status = Muestra la rama main, sin commits todavía, y los archivos iniciales sin seguimiento.

git remote add origin git@github.com:TU-USUARIO/sor-web-prestamo-portatiles-casa.git = Registra origin con la dirección SSH de tu repositorio vacío; todavía no envía archivos.

git remote -v = Muestra las direcciones de lectura y envío de los remotos; origin debe ser el de este proyecto.

git add . = Prepara todos los archivos no ignorados que hay bajo esta 
carpeta: en esta primera entrega, gitignore, bitácora y portada.

git commit -m = Guarda localmente una versión con los cambios preparados y el mensaje indicado.

git push -u origin main =  Sube main por primera vez a origin y configura su seguimiento para las siguientes subidas.

git diff -- = Compara la portada del disco con el índice: antes de prepararla verás la frase anterior con - y la nueva con +. No compara dos archivos diferentes.

git add web/index.html = Prepara únicamente el contenido actual del archivo indicado para el próximo commit; no sube nada.

git push = Envía los commits pendientes al remoto ya configurado. Comprueba que termina sin errores.

git status --short --untracked-files=all = Muestra el estado abreviado y enumera cada archivo sin seguimiento por su ruta completa, en lugar de agruparlos por carpetas. --short abrevia la salida; --untracked-
files=all despliega los nuevos.

git check-ignore -v web/videos/revision-01.mp4 web/videos/revision-02.mp4 = Indica, para cada ruta, el archivo de reglas, su número de línea y el patrón que la ignora. `-v` pide esos detalles.

git status --short --untracked-files=all = Muestra de nuevo qué está preparado y qué sigue sin preparar. Observa el archivo recién seleccionado.

git diff --cached --stat = Resume los cambios preparados en el índice: nombres y estadísticas. --cached selecciona lo preparado; --stat pide un resumen, no todas las líneas.

git log --oneline = Enumera los commits con código abreviado y mensaje, del más reciente al más antiguo. 

git switch --detach CODIGO_PRIMER_COMMIT = Cambia los archivos seguidos a la versión del commit indicado. --detach permite consultar ese commit sin situarte en una rama.

git switch main = Vuelve a la rama main, recuperando sus archivos seguidos.
## 🛠️ Qué he hecho

(Los pasos que has seguido. No copies el enunciado: cuenta lo que hiciste tú.)
Yo empecé primero leyendo el PDF, seguí todos los pasos 1 por 1, primero comprobé que tenía Git disponible, que fuera mi identidad y que mi SSH funcionara. A continuación empecé con la bóveda, cree sus carpetas correspondidas y las notas que se necesitabas dentro de las carpetas, en una de ellas hice un .gitignore en git bash, para que no me aparezcan archivos con ciertas extensiones. Luego, hice el primer inventario de equipos que se pide y luego me asegure de hacer la ruta y el primer git init. Proseguí con hacer el repositorio en Github, asegurándome de que copie el SSH público. A continuación hice el primer commit y push de esa página, y luego en el siguiente apartado me pidieron cambiarlo y tuve que volver a hacer un commit y push, luego tuve que crear más carpetas y notas y cambiar dos cosas, una en README.md y otra en equipos.csv, y comprobar que con un git status cambie algo. Después tuve que comprobar porque los videos quedaban fuera, una vez hice eso prepare las páginas que cambie, revisando la selección completa, lo guarde y lo subí, me asegure de que la entrega fue terminada. Finalmente se me pidió que localizase la primera entrega y entrara en ella para comprobar que los archivos desaparecían y luego de volver al main, los archivos volvían.

## 🚩 Qué me ha fallado y cómo lo he resuelto

(El mensaje de error LITERAL y qué hiciste. Si no falló nada, escribe "nada"
— pero piénsalo dos veces antes.)
Solo me dio un fallo al escribir mal, pero lo solucione al momento.
## 🤔 Respuestas a las preguntas

1. ¿Por qué el repositorio está en 01_Proyecto y no en la raíz de la bóveda?
El repositorio esta en 01_Proyecto, porque las carpetas con las que hemos trabajo están ahí, para mantener ese control y orden.

2. ¿Qué dos celdas de datos cambiaste en la segunda versión y cómo se ven en diff?
Primero cambie que el aula 1 pase a ser aula 3 y luegopase el estado de EQ02 de disponible a mantenimiento.

3. ¿Qué diferencia hay entre editar una fila y preparar ese cambio con add?
Editar modifica directamente el contenido del archivo en el directorio de trabajo mientras que prepararlo con add traslada esas modificaciones al área de preparación previa a la confirmación.

4. ¿Por qué la ficha nueva aparece en status y no en el diff de equipos.csv?
La ficha nueva figura en el estado como no rastreada pero no aparece en el diff de equipos porque diff solo compara las diferencias en archivos que ya forman parte del historial.

5. ¿Qué archivos preparaste individualmente en la ampliación y qué mostró diff --cached?
Prepare README.md y equipos.csv .
El comando diff cached mostró la lista exacta de cambios almacenados en el área de preparación listos para el commit.

6. ¿Cómo demostraste que los clips existen y están ignorados sin subirlos?
Se demostró al comprobar la existencia física de los clips de vídeo en la carpeta mientras que el estado o la regla en gitignore confirmaban que el sistema los ignora de forma deliberada.

7. ¿Qué ubicación y estado recuperaste al visitar el primer commit y qué ocurrió con EQ03?
Al volver al primer commit se recuperó el estado original e inicial de la bóveda provocando que la ficha del equipo EQ03 desapareciera por completo al no haber sido creada en esa fecha.

8. ¿Por qué este CSV necesita historial y qué limitaciones tiene frente a un inventario multiusuario real?
El historial sirve para saber quién cambió qué y cuándo pero este CSV falla frente a un programa real porque dos personas no pueden tocarlo a la vez sin romperlo.

9. ¿Cómo comprobaste la subida de la bitácora y por qué su cierre ocurre después del vídeo?
La comprobé cuando metiéndome en github y viendo que en el repositorio esta ahí, y su cierre ocurre después del video para completar la ficha y hacer un último push.

## 🔗 Enlaces

- **Vídeo de esta fase:** https://youtu.be/xDkf6ke7vIE?si=pBo6xOmTJ72hjYtu
- **Playlist:** https://www.youtube.com/playlist?list=PLSp1hE6Dadjk

## 💭 Dudas / a repasar

- Todo claro, ya voy más fluida y me doy cuenta de mis fallos, ya que son solo de escribir.