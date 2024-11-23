### Descripción de Clases y Métodos

#### **Clase `Espacio`**

La clase `Espacio` representa un espacio forestal y contiene los detalles sobre el país, provincia, año, familia, género, especie, especies agrupadas, y diámetro.

- **Atributos**:
  - `pais`: País donde se encuentra el espacio.
  - `provincia`: Provincia dentro del país.
  - `año`: Año de referencia del espacio.
  - `familia`: Familia taxonómica de la especie.
  - `genero`: Género taxonómico de la especie.
  - `especie`: Especie de la planta.
  - `especies_agrupadas`: Lista o categoría de especies agrupadas.
  - `diametro_uni_medicion`: Unidad de medición del diámetro (por ejemplo, metros).
  - `diametro`: Diámetro de la planta o árbol.

- **Métodos**:
  - `get_pais()`: Devuelve el país del espacio.
  - `get_provincia()`: Devuelve la provincia del espacio.
  - `get_año()`: Devuelve el año de referencia.
  - `get_familia()`: Devuelve la familia taxonómica.
  - `get_genero()`: Devuelve el género taxonómico.
  - `get_especie()`: Devuelve la especie de la planta.
  - `get_especies_agrupadas()`: Devuelve las especies agrupadas.
  - `get_diametro_uni_medicion()`: Devuelve la unidad de medición del diámetro.
  - `get_diametro()`: Devuelve el diámetro de la planta.

  - `set_pais(pais)`: Establece el país del espacio.
  - `set_provincia(provincia)`: Establece la provincia del espacio.
  - `set_año(año)`: Establece el año de referencia.
  - `set_familia(familia)`: Establece la familia taxonómica.
  - `set_genero(genero)`: Establece el género taxonómico.
  - `set_especie(especie)`: Establece la especie de la planta.
  - `set_especies_agrupadas(especies_agrupadas)`: Establece las especies agrupadas.
  - `set_diametro_uni_medicion(diametro_uni_medicion)`: Establece la unidad de medición del diámetro.
  - `set_diametro(diametro)`: Establece el diámetro de la planta.

#### **Clase `EspaciosForestales`**

La clase `EspaciosForestales` gestiona los espacios forestales y proporciona métodos para almacenar, mostrar, eliminar y actualizar los registros en una base de datos.

- **Métodos**:
  - `guardar_espacio(espacio, cursor)`: Inserta un nuevo espacio forestal en la base de datos.
  - `mostrar_espacio(cursor)`: Muestra todos los registros de los espacios forestales.
  - `eliminar_espacio(id_espacio, cursor)`: Elimina un espacio forestal de la base de datos por su ID.
  - `actualizar_espacio(id_espacio, campo, nuevo_valor, cursor)`: Actualiza un campo específico de un espacio forestal en la base de datos.

#### **Clase `Productos`**

La clase `Productos` representa los productos derivados de los espacios forestales. Incluye atributos relacionados con la venta y el precio de productos como rollizos, carbón, leña, postes, entre otros.

- **Atributos**:
  - `destino`: El destino o lugar de venta del producto.
  - `moneda`: La moneda en la que se realiza la transacción.
  - `precio`: El precio de los productos.
  - `rollizos`: La cantidad de rollizos.
  - `carbon`: La cantidad de carbón.
  - `leña`: La cantidad de leña.
  - `postes`: La cantidad de postes.
  - `otros`: Otros productos relacionados.
  - `total_productos`: El total de productos disponibles.
    
- **Métodos**:
  - `guardar_producto(producto, cursor)`: Inserta un nuevo producto forestal en la base de datos.
  - `mostrar_producto(cursor)`: Muestra todos los registros de productos forestales.
  - `eliminar_producto(id_producto, cursor)`: Elimina un producto forestal de la base de datos por su ID.
  - `actualizar_producto(id_producto, campo, nuevo_valor, cursor)`: Actualiza un campo específico de un producto forestal en la base de datos.

#### **Clase `ProductosForestales`**

La clase `ProductosForestales` gestiona los productos forestales y proporciona métodos para almacenar, mostrar, eliminar y actualizar los registros en la base de datos.

#### **Tabla `EspaciosForestales`**
La tabla EspaciosForestales almacena los datos relacionados con los espacios forestales, como su ubicación geográfica, la especie de los árboles y otras características relevantes.

#### **Columnas**
id (INT, PRIMARY KEY, AUTO_INCREMENT): Identificador único del espacio forestal.
pais (VARCHAR): El país en el que se encuentra el espacio forestal.
provincia (VARCHAR): La provincia o región dentro del país.
año (INT): El año de referencia del espacio.
familia (VARCHAR): La familia taxonómica a la que pertenece la especie del árbol.
genero (VARCHAR): El género taxonómico de la especie.
especie (VARCHAR): La especie de la planta o árbol.
especies_agrupadas (VARCHAR): Especies agrupadas relacionadas.
diametro_uni_medicion (VARCHAR): La unidad de medición utilizada para el diámetro (por ejemplo, metros).
diametro (DECIMAL): El diámetro del árbol o planta en la unidad de medición especificada.

#### **Tabla `ProductosForestales`**
La tabla ProductosForestales almacena los productos derivados de los espacios forestales, como rollizos, carbón, leña, postes, y otros productos relacionados.

#### **Columnas**
id (INT, PRIMARY KEY, AUTO_INCREMENT): Identificador único del producto forestal.
destino (VARCHAR): El destino o lugar al que se destina el producto.
moneda (VARCHAR): La moneda utilizada para la transacción.
precio (DECIMAL): El precio del producto.
rollizos (DECIMAL): Cantidad de rollizos disponibles.
carbon (DECIMAL): Cantidad de carbón disponible.
leña (DECIMAL): Cantidad de leña disponible.
postes (DECIMAL): Cantidad de postes disponibles.
otros (DECIMAL): Otros productos disponibles.
total_productos (DECIMAL): El total de productos disponibles, sumando todas las cantidades.

