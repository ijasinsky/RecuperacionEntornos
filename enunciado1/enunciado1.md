class Fecha {
    int dia;
    int mes;
    int anio;
}

class Nif {
    int dni;
    char letra;
}

class Persona {
    Nif nif;
    String nombreCompleto;
    Fecha fechaNacimiento;
}

class Socio extends Persona {
    String codigoAsociado;
    Fecha fechaAlta;
}