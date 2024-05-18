1Nombre: Nicole Alejandra Uribe Tapia

2Descripcion: 
Este proyecto se trata de crear una IA que resuelva cubos rubik aplicando todo lo que se aprendio hasta el momento en  la materia de sistemas inteligentes, en este caso se aplico A* para resolver el proyecto planteado,  usando una heurisitica basada en patrones y subpatrones, en base a los patrones que vaya encontrando ira resolviendolo.

3Requerimiento:
Para este caso solo se requiere tener instalado python y de preferencia tener el entorno de visual studio code

4Manual de uso: Para el uso de este codigo se deben realizar los siguientes pasos:
   Se crea un archivo donde se ponga un cubo en el siguiente formato:
         U:
         Y Y Y
         W W W
         W W W
         D:
         Y Y W
         Y Y W
         Y Y W
         F:
         O O O
         B G G
         R G G
         B:
         G G G
         G B B
         O B B
         L:
         R R G
         O O O
         B B B
         R:
         O O B
         R R R
         R R R
   Despues de crear el cubo  y tenerlo en el formato antes mencionado se carga el codigo de la siguiente manera:
     cubo_desordenado = CuboRubik.leer_desde_archivo('nombre_del_archivo.txt')
   Luego se crea un cubocon el mismo constructor de la clase para tener el cubo objetivo:
      cubo_objetivo = CuboRubik()
   Al tener ambos cubos creados los mandamos a la funcion resolver_cubo:
   camino_solucion = resolver_cub(cubo_desordenado, cubo_objetivo)
   De esta manera ya podremos ver el procedimiento
   Al hacer correr el codigo este devuelve:  
         Devuelve todo el camino
         Pasos
         Costo
         Movimientos 
         El estado del cubo
5Diseño eh implementacion
   1. Crear el cubo
      Para crear el cubo se definio la notacion
         F: Front (Frente)
         B: Back (Atrás)
         U: Up (Arriba)
         D: Down (Abajo)
         R: Right (Derecha)
         L: Left (Izquierda)
      Despues definimos los colores del cubo que seran
         W: white
         Y: Yellow
         G: Green
         B: Black
         O: Orange
         R: Red
      Empezamos a codificar y en la clase cubo rubik creamos el algoritmo mostrar y un algoritmo girar cara donde al definir la cara decimos a que lado la girara y realiza dicha operacion.
   Despues definimos que realizariamos este trabajo usando A* por la manera funcional y eficiente que tiene para este caso de problema.
   Luego se debia definir una heuristica, en este caso se trato de implementar 4 heurisiticas.
   1. El numero de fichas mal colocadas, consiste en contar las fichas mal colocadas en dicha cara.
   2. DIstancia Manhattan: suma las distancias horizontales mas las distancias verticales entre la posicion de cada ficha y la posicion correcta
   3. Distancia de fichas mal colocadas: se calcula la suma de las distancias entre la posición actual y la posición correcta de cada ficha.'
   4. Patrones y subpatrones: Buscar patrones especificos, en este caso se lo realizo con esquinas o aristas
   Se uso la ultima heuristica de los patrones para este caso, la heuristica llega a un maximo de 2 niveles.

6Trabajo futuro
   Mejorar la idea de la heuristica despues de aprender a armar un cubo.
   Implementar un diseño de cubo 3D
   