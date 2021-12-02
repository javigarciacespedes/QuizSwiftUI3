# QuizSwiftUI_3
Práctica 3 de la asignatura IWEB.
Enunciado
Modifique la práctica 2 - Quiz con Swift para que los quizzes no se carguen del fichero p1_quizzes.json, sino que se descargan de la URL:

https://core.dit.upm.es/api/quizzes/random10wa?token=TOKEN
Añada en la barra del NavigationView un botón que permita recargar otros 10 quizzes de forma aleatoria.

El contador de los quizzes acertados debe reiniciarse a 0 cada vez que se descarguen nuevos quizzes.

Es obligatorio usar GCD, para que la aplicación responda con suavidad y no se bloquee cuándo hay problemas de acceso al servidor o en la descarga de las fotos.

Mejora opcional 1: Actualizar Favoritos

Actualmente, la pantalla de jugar a un quiz muestra un botón con una estrella iluminada o apagada para indicar si un quiz es favorito del usuario o no.

Esta mejora consiste en convertir esa estrella en un botón que cambie el valor de favorito de ese quiz en el servidor core.dit.upm.es y en la app.

Para marcar como favorito un quiz, dado su id, para el usuario asociado al token de la petición, hay que realizar una petición PUT a la ruta:

/users/tokenOwner/favourites/quizId?token=TOKEN
Y para desmarcarlo hay que realizar una petición DELETE a la ruta:

/users/tokenOwner/favourites/quizId?token=TOKEN
Si las peticiones se realizan con éxito, el código de la respuesta HTTP será 200.

Mostrar una animación hasta que se reciba la respuesta.
