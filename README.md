# Reto Curso Java 01

## Requerimientos
- Un autor puede tener máximo 03 blogs.
- Solo pueden tener blogs los autores mayores de 18 años.
- Solo se puede publicar un post por día.
- Solo se puede registrar posts en blogs en estado activo.
- Solo se pueden registrar comentarios en post en estado publicado.
- Al eliminar un autor, debe realizarse una eliminación en cadena de sus blogs, post y
comentarios.
- Agregar los datos de prueba (script SQL) necesarios para validar los requerimientos.

## Consideraciones
Considerar los siguientes puntos respecto a la implementación de los requerimientos solicitados para el proyecto.

- ***Para el primer requerimiento***, se ha realizado la validación a nivel de Blog para el registro y actualización. Se verifica en la entidad Blog que el Author asociado al id consignado en el registro/actualización cuente con menos de 3 Blogs.
- ***Para el segundo requerimiento***, se ha realizado la validación a nivel de Blog para el registro y actualización. Se verifica en la entidad Blog que el Author asociado al id consignado en el registro/actualización sea mayor de 18 años.
- ***Para el tercer requerimiento***, se ha realizado la validación a nivel de Post para el registro (la fecha del Post se genera automáticamente con los valores correspondientes al momento que se invocó al método POST). Se ha considerado que un Author puede realizar una publicación por día para cada uno de los Blogs que tiene; es decir, si en un Blog ya se ha superado el valor permitido, no podrá realizar el registro, pero si podrá actualizar algún otro Blog de su propiedad en el que la validación lo permita.
- ***Para el cuarto requerimiento***, se ha realizado la validación a nivel de Post para el registro y actualización. Se verifica en la entidad Post que el Blog asociado al id consignado en el registro/actualización se encuentre con estado activo.
- ***Para el quinto requerimiento***, se ha realizado la validación a nivel de Comment para el registro y actualización. Se verifica en la entidad Comment que el Post asociado al id consignado en el registro/actualización se encuentre con estado publicado.
- ***Para el sexto requerimiento***, se ha implementado la regla a nivel de Author para la eliminación. Se efectúa al momento de eliminar una entidad Author, la eliminación de los Blogs, Post y Comments asociados.
- ***Para el séptimo requerimiento***, se ha incluido la data de prueba necesaria para realizar las validaciones respectivas para cada uno de los requerimientos previos (archivo data.sql) .
- ***Finalmente***, se ha incluido un archivo de la colección de Postman para ejecutar las pruebas requeridas (archivo Reto 2.postman_collection.json). Tener en cuenta que las fuentes del proyecto se encuentran en la rama ***main*** del repositorio en GitHub.
