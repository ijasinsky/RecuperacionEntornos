class Pelicula {
    private String codigo;
    private String titulo;
    private int anioProduccion;
    private String genero;
    private String paisProduccion;
    
    // Constructor, Getters y Setters
    public Pelicula(String codigo, String titulo, int anioProduccion, String genero, String paisProduccion) {
        this.codigo = codigo;
        this.titulo = titulo;
        this.anioProduccion = anioProduccion;
        this.genero = genero;
        this.paisProduccion = paisProduccion;
    }
    
    // Métodos adicionales según necesidades
}

class Cliente {
    private String nif;
    private String nombre;
    private String direccion;
    private String telefono;
    private String correo;
    private int numeroSocio;
    private String fechaAlta;
    
    // Constructor, Getters y Setters
    public Cliente(String nif, String nombre, String direccion, String telefono, String correo, int numeroSocio, String fechaAlta) {
        this.nif = nif;
        this.nombre = nombre;
        this.direccion = direccion;
        this.telefono = telefono;
        this.correo = correo;
        this.numeroSocio = numeroSocio;
        this.fechaAlta = fechaAlta;
    }
    
    // Métodos adicionales según necesidades
}

class Alquiler {
    private Cliente cliente;
    private Pelicula pelicula;
    private String fechaAlquiler;
    private String fechaDevolucion;
    
    // Constructor, Getters y Setters
    public Alquiler(Cliente cliente, Pelicula pelicula, String fechaAlquiler, String fechaDevolucion) {
        this.cliente = cliente;
        this.pelicula = pelicula;
        this.fechaAlquiler = fechaAlquiler;
        this.fechaDevolucion = fechaDevolucion;
    }
    
    // Métodos adicionales según necesidades
}

class MaquinaDispensadora {
    private List<Pelicula> peliculasDisponibles;
    private List<Cliente> clientesRegistrados;
    
    // Constructor
    public MaquinaDispensadora() {
        this.peliculasDisponibles = new ArrayList<>();
        this.clientesRegistrados = new ArrayList<>();
    }
    
    public void registrarCliente(Cliente cliente) {
        clientesRegistrados.add(cliente);
    }
    
    public void agregarPelicula(Pelicula pelicula) {
        peliculasDisponibles.add(pelicula);
    }
    
    public Alquiler alquilarPelicula(Cliente cliente, Pelicula pelicula, String fechaAlquiler, String fechaDevolucion) {
        if (peliculasDisponibles.contains(pelicula)) {
            peliculasDisponibles.remove(pelicula);
            return new Alquiler(cliente, pelicula, fechaAlquiler, fechaDevolucion);
        } else {
            return null; // Película no disponible
        }
    }
}