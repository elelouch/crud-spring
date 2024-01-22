# Correcciones
El path comienza desde src.java.main -> 
- Al JPARepository le faltaba el @Repository.
- Luego de agregar cambios en la entidad de cliente (Client), el controlador se vio afectado
y hubo que modificar el resto.
- A la clase RepresentationModelAssembler le falto el @Component.

# Recordatorios
- En general, recordar utilizar anotaciones, que son las que sacan la app andando.
- Utilizar el plugin "application" con application {mainClassName="com.elote.crud.CrudApplication"}
- Utilizar EntityModel.of() junto a methodOn y linkOf para HATEOAS.
- Tener cuidado con los cambios, hacerlos intentando no comprometer software viejo,  
pensar en retrocompatibilidad.  
NUNCA BORRAR UNA COLUMNA DE UNA TABLA.
- Un crud sencillo no es REST, hay que utilizar HATEOAS para poder asegurar la  
autonomia cliente-servidor.
- Son los metodos los que terminan mapeando a la DB, no necesariamente los fields  
del BEAN.
- REST es un conjunto de constraints utilizadas para tener servicios que escalen.
    - Cacheable  
    - Interface uniforme  
    - Stateless (Es como andar en auto con seniales en vez de utilizar un mapa).
    - Autonomia cliente-servidor.
    - Layered (Composicion jerarquica, ejemplo MVC).