# Revision-codigo
Violaciones a las convenciones de codificación del lenguaje:
Las advertencias de SonarLint indican violaciones a las convenciones de nombres de variables. Estas convenciones sugieren que los nombres de variables deberían ajustarse a ciertos patrones
Refactorización:
@Column(name = "especialidad_id")
private long especialidadId;

@Column(name = "usuario_id")
private long usuarioId;

Violaciones a las prácticas de Clean Code
Lo que no es una buena práctica de Clean Code. Repetir las mismas cadenas en diferentes partes del código puede generar errores y dificultades en el mantenimiento.
	Refactorización: Definir constantes para evitar la duplicación de literales.
private static final String ALUMNO_NO_ENCONTRADO = "El alumno con ese ID no existe: ";
public Alumno listarAlumnoPorId(Long id) {
   return alumnoRepository.findById(id)
.orElseThrow(() -> new ResourceNotFoundException(ALUMNO_NO_ENCONTRADO + id));}


