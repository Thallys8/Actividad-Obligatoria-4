# Parcial 2 - Diseño Orientado a Objectos

### Alumno: Gomes Leandro, Thallys (145287) 
### Materia: Diseño Orientado a Objetos 
### Carrera: Tecnicatura Universitaria en Programación de Sistemas 
### Profesor: Matias Velasquez 
### Año: 2024


# Introduccón
#### En este parcial estamos entregando las actividades obligatorias 3, 4 y 5 y estamos también las respuestas de las consignas del parcial.

# Actividad 3
#### Para actividad numero 3  creamos 2 Diagramas de Actividades y los 5 Diagrmas de Secuencias.

## Diagramas de Actividades:

##### 1) Préstamo de libro: [Diagrama]()
>  El Usuario solicita un libro, el bibliotecario verificará si la membresía de Socio es válida, solo si presta libro para los miembros, caso no sea, el solicitante podrá hacerse una membresía de Socio.
>  En secuencia, el bibliotecario verificará se el socio tiene o no deudas, caso sí, el socio podrá pagar esa deuda, caso contrario no se le prestará el libro.
>  Una vez que no haya deudas en nombre del socio, se verificará si el libro está o no disponible para prestamos, se está, también se verificará si es un libro restricto o no, caso sea, no se le prestará el libro, de lo contrario se se registrará el préstamo, se actualizará el stock y se entregará el libro al usuario.


##### 2) Devolución de libro: [Diagrama]()
>  El Usuario quiere devolver un libro, el bibliotecario verifica si es o no un socio, si no, solicita los datos del Socio que tomo el libro prestado (UserID) y el número de identificación unitario del libro (LibroID).
>  Con esa información el bibliotecario ingresará los datos de Socio y el sistema deberá informar si el libro fue entregue adentro del plazo de devolución.
>  Caso el plazo se haya excedido, se aplicará la multa al socio, que podrá abonar su deuda en ese momento o dejarla pendiente. 
>  En todo caso se registra la devolución del libro y se actualiza el stock, también se informa al Socio confirmando la devolución y el status de deudor (si tiene o no deuda pendiente).


## Diagrama de Secuencias:

##### 1) Prestamos de libro: [Diagrama]()
>  El socio solicita un préstamo de un libro con intención de llevarse este libro para afuera de la biblioteca, el bibliotecario debe verificar la disponibilidad del libro y si es restricto para lectura intramuros de la biblioteca.

##### 2) Devolución de libro: [Diagrama]()
>  El socio devuelve el libro para el bibliotecario, este por su vez lo registra en sistema y el sistema le informa el registro de devolución y el tiempo que el libro estuvo prestado.
>  El Bibliotecario informará el Socio que se registró la devolución y informará el estatus de devolución y si será aplicado multa al usuario caso haya excedido el tiempo de devolución. 

##### 3) Pagar Multa: [Diagrama]()
>  Socio solicita pagar una multa, el bibliotecario verifica el status de deudor y informa al Socio el status y el monto de su deuda.
>  El Socio paga la deuda, el bibliotecario registra en el sistema y luego informa al Socio su nuevo status como no deudor.

##### 4) Reservar libro: [Diagrama]()
>  El Socio no puede ir a la biblioteca en ese instante pero tiene la intención de ir mas tarde por un libro, pero le gustaría reservar uno de los libros para no correr el riesgo de ir a la biblioteca y que no haya disponibilidad de ese libro.
>  Para eso el socio entra a la pagina de la biblioteca con sus credenciales, verifica si el libro está disponible y solicita una reservación de este. 
>  El sistema le informará se el libro está o no disponible y también se es un libro que se puede prestar normalmente o solamente para lectura adentro de los límites de la biblioteca (intramuros).
>  
>  **Nota**: El Status de deudor no es necesario para la reservación online del libro, pero se hará la verificación en el momento de realizar el préstamo (ver diagrama de prestamo).

##### 5) Registrar un socio: [Diagrama]()
>  El cliente (futuro socio) solicita al Bibliotecario la creación de una nueva cuenta.
>  El bibliotecario solicitará al cliente sus datos personales, luego de tener en manos estos datos él irá registrar en el sistema, que por su vez devolverá el status de cuanta creada junco con el UserID y una contraseña temporal.
>  El Bibliotecario repasará esa información al cliente (nuevo Socio), que por su vez, ingresará a la página de la biblioteca y cambiará la contraseña temporal por una nueva de su elección.


# Actividad Obligatoria 4
#### Para la Actividad numero 4 fueron creados las Tarjetas CRC, 10 Diagrmas de casos de Uso y 3 Ensenários de casos de Uso.

## Tarjetas CRC: 


## Diagramas de Casos de Uso: 

##### 1) Registrar libro en el sistema: [Diagrama]()
>  El bibliotecario debe registrar en la base de datos las informaciones del libro.

##### 2) Registrar usuario Socio: [Diagrama]()
>  El bibliotecario debe registras registrar en la base de datos las informaciones del usuario.
>  Debe seleccionar si es un usuario Socio o Bibliotecario
>  El Socio tendrá acceso a su UserID y su contraseña temporal.

##### 3) Buscar un libro: [Diagrama]()
>  Tanto el Socio cuanto el Bibliotecario pueden buscar por un libro en la base de datos y verificar si en el libro está disponible y si es restringido.

##### 4) Reservar un Libro: [Diagrama]()
>  Tanto el Socio cuanto el Bibliotecario pueden buscar por un libro en la base de datos, se este cumple los requisitos de Disponible y No restringido, el usuario puede hacer una reserva para que el libro pueda ser retirado mas tarde.

##### 5) Dar de baja la Reserva: [Diagrama]()
>  Tanto el Socio cuanto el Bibliotecario pueden buscar por una reserva vigente y eliminar la reserva, así el libro vuelve a figurar como disponible.

##### 6) Encontrar la ubicación de un libro en su estantería: [Diagrama]()
>  Para disminuir la dependencia de las Socios para con los Bibliotecarios y mejorar la eficiencia de la atención los Socios también pueden ver en la página de la biblioteca en que sección y estantería está ubicado.
>  Solamente los Bibliotecarios pueden marca el libro como ausente. 

##### 7) Prestar un Libro: [Diagrama]()
>  Tanto el Socio cuanto el Bibliotecario pueden confirmar si el libro está disponible o reservado por el socio solicitante. También pueden ver si el socio tiene alguna deuda pendiente.
>  Solamente el Bibliotecario puede realizar el préstamo y cobrar la multa
>  Solamente el Socio puede recibir el libro y pagar a multa

##### 8) Devolver un libro: [Diagrama]()
>  El Socio entrega el libro para el bibliotecario, que lo recibe
>  El bibliotecario registra la devolución en el sistema y verifica si la fecha de devolución está excedida o no. Con base en esa información él puedo aplicar la multa al Socio, en caso de exceso. 
>  El socio puede pagar la multa.

##### 9) Devolver un libro a su lugar: [Diagrama]()
>  El Bibliotecario pone el libro en la estantería y registra en el sistema.
>  El Backend actualiza esa información en la página de la biblioteca para que los usuarios pueda tener acceso a esa información cuando hacen la búsqueda de un libro. 

##### 10) Pagar una deuda: [Diagrama]()
>  Tanto el Socio cuanto el Bibliotecario pueden ver el valor de la deuda del Socio
>  El bibliotecario puede cobrar la multa y una vez abonado el valor, él puede registrar el pago.

## Escenarios de Casos de Uso: 

##### 1) Solicitar el prestamos de un libro: [Diagrama]()
>  Es este escenario estaremos describiendo la ruta principal y los pasos para este proceso de alta prioridad para la biblioteca que es el préstamo de un libro, ya que esta es la función fin del emprendimiento. 

##### 2) Devolver un libro prestado: [Diagrama]()
>  Es este escenario estaremos describiendo la ruta principal y los pasos para este proceso de alta prioridad para la biblioteca que es la devolución de un libro, ya que de suma importancia para asegurar el registro de devoluciones y no perjudicar a la biblioteca o al >  Socio por cuenta de un error en el proceso de devoluciones de un libro y para mantener libros disponibles en stock para futuros prestamos.

##### 3) Registrar un nuevo Socio: [Diagrama]()
>  Es este escenario estaremos describiendo la ruta principal y los pasos para este proceso de alta prioridad para la biblioteca porque es la manera como la biblioteca puede registrar los Socios para quién podrá prestar libros, y registrar adecuadamente los prestamos.

# Actividad 3
#### Para actividad numero 3  creamos 2 Diagramas de Actividades y los 5 Diagrmas de Secuencias.

# Preguntás teóricas
#### [Este]() es el documento con las respuestas de las preguntas teoricas.
