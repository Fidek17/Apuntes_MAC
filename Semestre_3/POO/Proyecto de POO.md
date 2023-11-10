```java
import java.util.List;

class Usuario {
    private int ID;
    private String nombre;
    private String email;
    private String contrasena;
    private String sexo;
    private String cuentaDeBanco;
    private String fechaDeNacimiento;

    public Usuario(int ID, String nombre, String email, String contrasena, String sexo, String cuentaDeBanco, String fechaDeNacimiento) {
        this.ID = ID;
        this.nombre = nombre;
        this.email = email;
        this.contrasena = contrasena;
        this.sexo = sexo;
        this.cuentaDeBanco = cuentaDeBanco;
        this.fechaDeNacimiento = fechaDeNacimiento;
    }
    
    public int getID(){
        return ID;
    }
    
    public int setID(int id){
        return this.ID = id;
    }
    
    
    
    public String getNombre(){
        return nombre;
    }
    
    public String getEmail(){
        return email;
    }
    
    public String getContrasena(){
        return contrasena;
    }
    
    public String getSexo(){
        return sexo;
    }
    
    public String getCuentaDeBanco(){
        return cuentaDeBanco;
    }
    
    public String getFechaDeNacimiento(){
        return fechaDeNacimiento;
    }
    
    
}

class Oyente extends Usuario {
    private List<Cancion> listaDeCanciones;
    private List<Playlist> listaDePlaylists;

    public Oyente(int ID, String nombre, String email, String contrasena, String sexo, String cuentaDeBanco, String fechaDeNacimiento,
                  List<Cancion> listaDeCanciones, List<Playlist> listaDePlaylists) {
        super(ID, nombre, email, contrasena, sexo, cuentaDeBanco, fechaDeNacimiento);
        this.listaDeCanciones = listaDeCanciones;
        this.listaDePlaylists = listaDePlaylists;
    }
}

class Cancion {
    private int ID;
    private String titulo;
    private String artista;
    private int reproducciones;
    private String genero;
    private double duracion;

    // Constructor
    public Cancion(int ID, String titulo, String artista, int reproducciones, String genero, double duracion) {
        this.ID = ID;
        this.titulo = titulo;
        this.artista = artista;
        this.reproducciones = reproducciones;
        this.genero = genero;
        this.duracion = duracion;
    }

    // Métodos getters para acceder a los atributos privados
    public int getID() {
        return ID;
    }

    public String getTitulo() {
        return titulo;
    }

    public String getArtista() {
        return artista;
    }

    public int getReproducciones() {
        return reproducciones;
    }

    public String getGenero() {
        return genero;
    }

    public double getDuracion() {
        return duracion;
    }
}

class Playlist {
    private int ID;
    private String nombre;
    private List<Cancion> listasDeCanciones;

    // Constructor
    public Playlist(int ID, String nombre, List<Cancion> listasDeCanciones) {
        this.ID = ID;
        this.nombre = nombre;
        this.listasDeCanciones = listasDeCanciones;
    }

    // Métodos getters para acceder a los atributos privados
    public int getID() {
        return ID;
    }

    public String getNombre() {
        return nombre;
    }

    public List<Cancion> getListasDeCanciones() {
        return listasDeCanciones;
    }
}


public class Main
{
	public static void main(String[] args) {
		System.out.println("HOla mundo");
	}
}
```
