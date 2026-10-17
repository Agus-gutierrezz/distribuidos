# Trabajo Práctico Ingeniería Inversa

El objetivo de esta actividad es lograr que ambos proyectos corran de manera simultánea en sus computadoras y extraer de ellos toda la información sobre como se conectan diferentes microservicios.

Trabajando en grupos (o de forma individual según indique el profesor), realicen un informe técnico o documento Markdown (README.md) que responda y detalle lo siguiente:

Mapa de Endpoints: Liste las rutas (URLs, métodos HTTP y parámetros) que ofrece cada microservicio basándose estrictamente en el código fuente.

Estructura del Proyecto: Describan brevemente cómo están organizadas las capas en cada proyecto (Controladores, Servicios, Repositorios, Entidades/Modelos).

Independencia vs. Comunicación: Analicen si los microservicios operan completamente aislados o si existe algún punto de contacto o dependencia entre ellos.

**Conclusiones:** Redacten una breve reflexión sobre las ventajas de separar un sistema monolítico en estos dos microservicios.





>Este ejemplo práctico está basado en los materiales educativos desarrollados por la ingeniera y creadora de contenido Luisina de Paula (TodoCode Academy). Todo el mérito por la estructura inicial del código corresponde a su labor docente y de divulgación en tecnología.

## 1.
### Mapa de Endpoints de Pacientes: @PostMapping ("/pacientes/crear"), @GetMapping ("/pacientes/traer"), @DeleteMapping("/pacientes/borrar/{id}"),  @PutMapping ("/pacientes/editar/{id_original}"), @GetMapping ("/pacientes/traer/{id}"), @GetMapping ("/pacientes/traerdni/{dni}").

### Mapa de Endpoints de Turnos: @RequestMapping ("/turnos"),  @PostMapping ("/crear"), @GetMapping ("/traer"), @DeleteMapping("/borrar/{id}"), @PutMapping ("/editar/{id_original}"), @GetMapping ("/traer/{id}").

## 2.
### Paquete model: Contiene las clases con sus respectivos atributos que se convertiran en nuestras tablas en la base de datos.
### Paquete controller: basicamente tiene las clases que nos sirve como puente para poder comunicarnos entre la vista y la implementación.
### Paquete service: Contiene las interfaces donde se hará las firmas de los metodos, y tambien las clases donde se implementarán los metodos de las interfaces y se los sobreescribirá
### Paquete repository: contiene las interfaces que extenderán de los metodos JPA para poder trabajar los datos ingresados junto con la base de datos.

## 3.
### Trabajan en conjunto, ya que turno necesita de un paciente existente para poder crearse.