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

##### 1) Préstamo de libro: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/05cd2996-cfd4-4a9c-a954-6f36069a6c0a)
>  El Usuario solicita un libro, el bibliotecario verificará si la membresía de Socio es válida, solo si presta libro para los miembros, caso no sea, el solicitante podrá hacerse una membresía de Socio.
>  En secuencia, el bibliotecario verificará se el socio tiene o no deudas, caso sí, el socio podrá pagar esa deuda, caso contrario no se le prestará el libro.
>  Una vez que no haya deudas en nombre del socio, se verificará si el libro está o no disponible para prestamos, se está, también se verificará si es un libro restricto o no, caso sea, no se le prestará el libro, de lo contrario se se registrará el préstamo, se actualizará el stock y se entregará el libro al usuario.


##### 2) Devolución de libro: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/6162ffb8-d39b-4fd6-83c5-78160156335d)
>  El Usuario quiere devolver un libro, el bibliotecario verifica si es o no un socio, si no, solicita los datos del Socio que tomo el libro prestado (UserID) y el número de identificación unitario del libro (LibroID).
>  Con esa información el bibliotecario ingresará los datos de Socio y el sistema deberá informar si el libro fue entregue adentro del plazo de devolución.
>  Caso el plazo se haya excedido, se aplicará la multa al socio, que podrá abonar su deuda en ese momento o dejarla pendiente. 
>  En todo caso se registra la devolución del libro y se actualiza el stock, también se informa al Socio confirmando la devolución y el status de deudor (si tiene o no deuda pendiente).


## Diagrama de Secuencias:

##### 1) Prestamos de libro: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/6f10a8db-5cc2-4c8f-a78c-06dbc0f6532f)
>  El socio solicita un préstamo de un libro con intención de llevarse este libro para afuera de la biblioteca, el bibliotecario debe verificar la disponibilidad del libro y si es restricto para lectura intramuros de la biblioteca.

##### 2) Devolución de libro: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/5e07e905-aaf1-4c3d-8866-77c2030f25c2)
>  El socio devuelve el libro para el bibliotecario, este por su vez lo registra en sistema y el sistema le informa el registro de devolución y el tiempo que el libro estuvo prestado.
>  El Bibliotecario informará el Socio que se registró la devolución y informará el estatus de devolución y si será aplicado multa al usuario caso haya excedido el tiempo de devolución. 

##### 3) Pagar Multa: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/e1d45ece-8090-4be9-96b6-a8a681384997)
>  Socio solicita pagar una multa, el bibliotecario verifica el status de deudor y informa al Socio el status y el monto de su deuda.
>  El Socio paga la deuda, el bibliotecario registra en el sistema y luego informa al Socio su nuevo status como no deudor.

##### 4) Reservar libro: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/649a262b-4711-4c82-8935-30796a7f43cf)
>  El Socio no puede ir a la biblioteca en ese instante pero tiene la intención de ir mas tarde por un libro, pero le gustaría reservar uno de los libros para no correr el riesgo de ir a la biblioteca y que no haya disponibilidad de ese libro.
>  Para eso el socio entra a la pagina de la biblioteca con sus credenciales, verifica si el libro está disponible y solicita una reservación de este. 
>  El sistema le informará se el libro está o no disponible y también se es un libro que se puede prestar normalmente o solamente para lectura adentro de los límites de la biblioteca (intramuros).
>  
>  **Nota**: El Status de deudor no es necesario para la reservación online del libro, pero se hará la verificación en el momento de realizar el préstamo (ver diagrama de prestamo).

##### 5) Registrar un socio: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/ce96450b-5b9f-4de5-a41d-52104f40293b)
>  El cliente (futuro socio) solicita al Bibliotecario la creación de una nueva cuenta.
>  El bibliotecario solicitará al cliente sus datos personales, luego de tener en manos estos datos él irá registrar en el sistema, que por su vez devolverá el status de cuanta creada junco con el UserID y una contraseña temporal.
>  El Bibliotecario repasará esa información al cliente (nuevo Socio), que por su vez, ingresará a la página de la biblioteca y cambiará la contraseña temporal por una nueva de su elección.


# Actividad Obligatoria 4
#### Para la Actividad numero 4 fueron creados las Tarjetas CRC, 10 Diagrmas de casos de Uso y 3 Ensenários de casos de Uso.

## Tarjetas CRC: 
##### • Clase Libro: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/aedaa5b2-dbbe-4d0e-bd01-2ba50dcc544a)
##### • Clase Ubicacion: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/cc6b281f-09dd-4512-87bb-8de991b987e3)
##### • Clase Usuario: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/48194fec-5ad4-449c-8ca2-01f1ad7e3c29)
##### • Clase Socio: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/e1917db8-80f0-40d3-a9ed-8a62ea2ae388)
##### • Clase Bibliotecario: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/b75ce23e-5b19-4a6a-917f-738a1a3a7e17)
##### • Clase Reserva: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/6f8c4b32-eee3-4241-b26d-b33696a5a1db)
##### • Clase Prestamo: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/4b5c9f5a-d07d-4a6c-9d9f-3a52f0aaf1dd)
##### • Clase QuitarMulta: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/0468fe3e-d8e6-4cfb-b5a9-fe80c2673b07)
##### • Clase Credenciales: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/c883a2a7-7ed6-4924-a2bb-a7c73db67989)
##### • Clase SocioComun: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/b9276ff9-1ffc-44e7-a66c-7d365d37a618)
##### • Clase SocioPremium: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/114a4f40-9030-49b0-9f95-d812cb80ac4e)
##### • Clase Interfase EstanteriaVirtual: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/fc6d3bf1-a796-41c1-bfd7-d3cd08268147)

## Diagramas de Casos de Uso: 

##### 1) Registrar libro en el sistema: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/328de8e3-89dd-4beb-85ce-6275f74bf982)
>  El bibliotecario debe registrar en la base de datos las informaciones del libro.

##### 2) Registrar usuario Socio: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/effc28ce-a1c9-4dfa-838c-c410032a3798)
>  El bibliotecario debe registras registrar en la base de datos las informaciones del usuario.
>  Debe seleccionar si es un usuario Socio o Bibliotecario
>  El Socio tendrá acceso a su UserID y su contraseña temporal.

##### 3) Buscar un libro: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/8ed7b493-2bda-4e94-bfd4-33e69875702f)
>  Tanto el Socio cuanto el Bibliotecario pueden buscar por un libro en la base de datos y verificar si en el libro está disponible y si es restringido.

##### 4) Reservar un Libro: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/5bbd8bd2-bb0f-483f-99a8-545630cdf4e0)
>  Tanto el Socio cuanto el Bibliotecario pueden buscar por un libro en la base de datos, se este cumple los requisitos de Disponible y No restringido, el usuario puede hacer una reserva para que el libro pueda ser retirado mas tarde.

##### 5) Dar de baja la Reserva: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/bc075482-1757-47a5-8367-6d895cf0871a)
>  Tanto el Socio cuanto el Bibliotecario pueden buscar por una reserva vigente y eliminar la reserva, así el libro vuelve a figurar como disponible.

##### 6) Encontrar la ubicación de un libro en su estantería: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/43a27399-4a31-47f6-b461-e8e8394e9cf7)
>  Para disminuir la dependencia de las Socios para con los Bibliotecarios y mejorar la eficiencia de la atención los Socios también pueden ver en la página de la biblioteca en que sección y estantería está ubicado.
>  Solamente los Bibliotecarios pueden marca el libro como ausente. 

##### 7) Prestar un Libro: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/e41f4bf5-867a-4e47-9eda-438ce0a06c8b)
>  Tanto el Socio cuanto el Bibliotecario pueden confirmar si el libro está disponible o reservado por el socio solicitante. También pueden ver si el socio tiene alguna deuda pendiente.
>  Solamente el Bibliotecario puede realizar el préstamo y cobrar la multa
>  Solamente el Socio puede recibir el libro y pagar a multa

##### 8) Devolver un libro: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/c8d83527-18b0-4809-bb4c-fbbcf0c64f58)
>  El Socio entrega el libro para el bibliotecario, que lo recibe
>  El bibliotecario registra la devolución en el sistema y verifica si la fecha de devolución está excedida o no. Con base en esa información él puedo aplicar la multa al Socio, en caso de exceso. 
>  El socio puede pagar la multa.

##### 9) Devolver un libro a su lugar: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/a4bd64da-7847-4120-9e4c-0c6fda822903)
>  El Bibliotecario pone el libro en la estantería y registra en el sistema.
>  El Backend actualiza esa información en la página de la biblioteca para que los usuarios pueda tener acceso a esa información cuando hacen la búsqueda de un libro. 

##### 10) Pagar una deuda: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/c33642cf-a560-4a8e-8a77-278f910d8d43)
>  Tanto el Socio cuanto el Bibliotecario pueden ver el valor de la deuda del Socio
>  El bibliotecario puede cobrar la multa y una vez abonado el valor, él puede registrar el pago.

## Escenarios de Casos de Uso: 

##### 1) Solicitar el prestamos de un libro: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/e1e3c889-d4ee-4477-9fde-3cef998d6898)
>  Es este escenario estaremos describiendo la ruta principal y los pasos para este proceso de alta prioridad para la biblioteca que es el préstamo de un libro, ya que esta es la función fin del emprendimiento. 

##### 2) Devolver un libro prestado: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/5497906c-06fc-43e7-8add-f5eb11059c7d)
>  Es este escenario estaremos describiendo la ruta principal y los pasos para este proceso de alta prioridad para la biblioteca que es la devolución de un libro, ya que de suma importancia para asegurar el registro de devoluciones y no perjudicar a la biblioteca o al >  Socio por cuenta de un error en el proceso de devoluciones de un libro y para mantener libros disponibles en stock para futuros prestamos.

##### 3) Registrar un nuevo Socio: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/12ce7e0c-0059-43ac-a256-0e52577f1f2a)
>  Es este escenario estaremos describiendo la ruta principal y los pasos para este proceso de alta prioridad para la biblioteca porque es la manera como la biblioteca puede registrar los Socios para quién podrá prestar libros, y registrar adecuadamente los prestamos.

# Actividad 5
#### Para actividad numero 5 actualizamos el Diagramas de Clases y los 5 Diagrmas de Secuencias.

## Diagrama de Clases:

#### 1) Diagrama de Clases: [Diagrama](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/9bbd96f3-b99e-4fd3-806e-cdd1cd50c1eb)

## Matriz CLAE

#### 2) [Matriz](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/c120bc58-e725-4e7a-949d-cd2bbf632c5c)

# Preguntás teóricas
#### [Este](https://github.com/user-attachments/files/16059655/Leandro_T_Parcial_02.pdf) es el documento con las respuestas de las preguntas teoricas.
#### Para mejor compreención del proceso dejo mi diagrama de clase como estaba [Antes](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/012cff53-f0f0-4101-aff7-6ec508648a70) de aplicar los principios **SOLID** y [Después](https://github.com/Thallys8/Actividad-Obligatoria-4/assets/171758911/9bbd96f3-b99e-4fd3-806e-cdd1cd50c1eb) de aplicarlos.
