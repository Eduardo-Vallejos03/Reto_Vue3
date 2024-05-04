# RETO_VUE3

Elaborado por: Eduardo Vallejos

Ultima actualización: 3 de Mayo de 2024

<img width="1458" alt="image" src="https://github.com/Eduardo-Vallejos03/Reto_Vue3/assets/145948389/1cd64553-79ff-4722-bbfc-3658c29d8dfd">


## Instalación

Sigue estos pasos para configurar y ejecutar el proyecto en tu máquina local a traves del terminal:

:exclamation: **Importante:** Asegurate de tener instalado git, si aun no lo tienes puedes hacerlo en el siguiente link: https://git-scm.com/downloads

1. **Accede a la carpeta de almacenamiento**: 
    ```
    cd Tu-carpeta
    
    ```
    Accede a la carpeta donde quieres clonar el repositorio con cd

2. **Clona el Repositorio**: 
    ```
    git clone https://github.com/Eduardo-Vallejos03/Reto_Vue3.git
    
    ```
    Clona el repositorio en la carpeta seleccionada
   
4. **Instala las Dependencias**:
    ```
    npm install
    
    ```
    Instala todas las dependencias necesarias para el proyecto
   
3. **Inicia el servidor**:
    ```
    npm run serve
    ```
    Accede a la vista del proyecto con un servidor local

4. **Visita la Aplicación en tu Navegador**:
   
    Abre el navegador y navega al URL que se muestre en la terminal y podras tener una vista del proyecto
   

***

### Descripción del proyecto

Reto_Vue3 es un proyecto desarrolado en Vue3 desde 0 el objetivo de este proyecto es lograr un listado de productos
de diferentes tipos que tengan la capacidad de ser filtrados segun su categoria, ademas de que el diseño sea agradable, intuitivo
y totalmente responsive lo que sigmifica que se adapta a cualquier tipo de pantalla como se muestra a continuación:

<img width="1344" alt="image" src="https://github.com/Eduardo-Vallejos03/Reto_Vue3/assets/145948389/530803b1-7ed5-4203-8ccb-56d6ff17fb93">

El proyecto cuenta con los siguientes componentes:

1. **ProductsList.vue:** Componente principal que contiene la lista completa de los productos, encabezado y la barra de navegación con el que se filtra los productos.
2. **ProductCard.vue:** Componente con el cual creamos una tarjeta individual de cada producto
3. **ProductGrid.vue:** Componente que organiza los cards en columnas y filas.
4. **ProductButtons.vue:** Componente que contiene botones de detalle para cada card (actualmente solo visual)


### Consumo de datos de prodcutos

Los productos son creados con información consumida desde el archivo products.json cada uno organizado con arreglos de la siguiente manera:

<img width="323" alt="image" src="https://github.com/Eduardo-Vallejos03/Reto_Vue3/assets/145948389/8663ee1e-6550-4b8c-8761-36bc5d7a6cae">

Cada producto cuenta con:
1. **id:** Id único de producto para diferenciarlo
2. **category:** Categoria para poder organizar a los productos y poder lograr un filtrado
3. **Datos de productos** Datos de nombre, precio e imagen de cada producto

Al ser datos consumidos desde un json deben ser importados con un import el cual se encuentra en el componente productList de la siguinte manera:

<img width="421" alt="image" src="https://github.com/Eduardo-Vallejos03/Reto_Vue3/assets/145948389/524ed688-2d9f-4574-b83e-412a8b574b2e">

### Filtrado por producto

<img width="1441" alt="image" src="https://github.com/Eduardo-Vallejos03/Reto_Vue3/assets/145948389/cf80708b-de1b-4b9c-9aa5-372980676ec6">

Para lograr un filtrado de productos, se registró un evento de click a cada enlace de la siguiente manera:

<img width="659" alt="image" src="https://github.com/Eduardo-Vallejos03/Reto_Vue3/assets/145948389/9acffa7a-327c-4fb0-94ed-723195b15649">

Se utilizó el sigueinte metodo para filtrar segun el enlace al que se le dío click

<img width="1006" alt="image" src="https://github.com/Eduardo-Vallejos03/Reto_Vue3/assets/145948389/8593b87f-8c13-419b-9e7b-55940d272817">

### Futuras actualizaciones

El proyecto esta destinado a ser mas de lo que ya es, entre las futuras actualizaciones esta pensado realizar cosas extras como:

1. **Carrito de compras:** Interfaz de un carrito de compras
2. **Detalle:** Pantalla de detalle de cada producto para ser mas informativo


¡Listo! Una vez instalado el proyecto en tu maquina esta listo para revisarse, espero que sea de tu agrado y estoy abierto a cualquier sugerencia o recomendación.
