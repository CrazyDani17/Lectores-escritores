# Lectores-escritores

Este problema es típico para observar la aplicación de mecanismos de sincronización y concurrencia.

Se define de la siguiente manera:
Hay un área de base de datos compartida entre un número de procesos.
Hay un número de procesos que solo leen del área de base de datos (lectores).
Y otro que sólo escriben en el área de base de datos (escritores).
Las siguientes condiciones deben satisfacerse.

1. Cualquier número de lectores pueden leer el fichero simultáneamente.
2. Sólo un escritor al tiempo puede escribir en el fichero.
3. Si un escritor está escribiendo en el fichero (base de datos) ningún lector puede leerlo.

La solución se especifica en las diapositivas y en el video, pero en resumen utilizamos monitores
como mecanismo de sincronización y exclusión mutua para así realizar las restricciones que nos
pide el problema, gracias a las operaciones:

-wait() indica que el proceso que invoca esta operación queda suspendido hasta que otro proceso invoque la operación

-signal() hace que se reanude exactamente uno de los procesos suspendidos.

link del video: https://drive.google.com/file/d/1XWNHmDpsry_0PCkBXOfrCLdj_zFLuVox/view?usp=sharing

Referencias:

Stalling. 2005. Sistemas Operativos. Aspectos internos y principios de diseño. Madrid. Pearson Educación.

Silberschatz, Galvin, Gagne. 2005. Fundamentos de sistemas operativos. Septima edicición.

Academia Usero. 2015. https://www.youtube.com/watch?v=HShMFlcAUJ0
