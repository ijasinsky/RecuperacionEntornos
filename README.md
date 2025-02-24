Este proyecto tiene como objetivo modelar y gestionar un videoclub mediante el desarrollo de un diagrama de casos de uso y un diagrama de secuencia. El sistema permitirá a los dependientes gestionar tanto las películas como los clientes, además de controlar los alquileres y devoluciones.

Descripción del Sistema
El videoclub cuenta con varios procesos clave para gestionar tanto las películas como a los clientes. A continuación, se describen los casos de uso del sistema y cómo interactúan los actores principales, como el dependiente y el cliente.

Casos de Uso
Actores Principales
Dependiente: Es el responsable de ingresar los datos de las películas y dar de alta a los clientes en el sistema.
Cliente: Es quien alquila y devuelve las películas a través de la máquina dispensadora.
Casos de Uso del Sistema
Agregar Película:
El dependiente introduce los datos de una nueva película en el sistema. Los datos necesarios incluyen el código, título, año de producción, género y país de producción.

Dar de Alta a un Cliente:
El dependiente registra a un nuevo cliente en el sistema, proporcionando su NIF, nombre, dirección, teléfono, correo, número de socio y fecha de alta.

Alquilar Película:
El cliente selecciona una película de la máquina dispensadora. El sistema verifica si el cliente tiene alguna sanción pendiente; si la tiene, no se permite el alquiler. Si el cliente está libre de sanciones, el sistema comprueba si hay existencias de la película, disminuye el stock y registra el alquiler.

Devolver Película:
El cliente devuelve la película al videoclub. El sistema incrementa el stock de la película y registra la fecha de devolución.

Gestionar Sanciones:
Si el cliente tiene alguna sanción pendiente, el sistema no permitirá el alquiler de nuevas películas hasta que la sanción se resuelva.

Diagrama de Secuencia
El diagrama de secuencia describe cómo interactúan los objetos dentro del sistema durante el proceso de alquiler de una película. A continuación, se describe el flujo de interacción:

Alquilar Película:
El cliente selecciona una película de la máquina dispensadora.
La máquina dispensadora consulta el sistema de gestión si el cliente tiene sanciones pendientes.
Si no hay sanciones, el sistema verifica la disponibilidad de la película.
Si la película está disponible, el sistema disminuye el stock y registra el alquiler.

Devolver Película:
El cliente devuelve una película a la máquina dispensadora.
La máquina incrementa el stock de la película.
El sistema registra la fecha de devolución.

Requisitos
Lenguaje de Programación: El sistema puede ser implementado en cualquier lenguaje orientado a objetos, como Java, C# o Python.
Base de Datos: El sistema debe contar con una base de datos para almacenar la información de los clientes y las películas.
Interfaz de Usuario: Puede ser una interfaz de usuario en consola o gráfica, dependiendo de la preferencia.
Conclusión
Este proyecto tiene como objetivo proporcionar una solución eficiente para gestionar las operaciones básicas de un videoclub, incluyendo el registro de películas y clientes, así como la gestión de alquileres y devoluciones. A través de los diagramas de casos de uso y secuencia, se define claramente el flujo de operaciones y las interacciones entre los actores y el sistema.
