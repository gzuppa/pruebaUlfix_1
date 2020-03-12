# Prueba técnica Ulfix
# CRUD React / Conexión a API

Para esta prueba tendrás que crear una pequeña app con un CRUD para mostrar en pantalla un catálogo de comidas con sus aportes alimenticios

## Requerimientos (será necesario que tengas una cuenta de git, en caso de no tenerla abrirla para evaluar los conocimientos en control de versiones)

- Hacer fork a este repositorio
- Clonar el repositorio en una ubicación local de este equipo

## Git actions

```
git add .
git commit -m "done"
git push origin master
```

Será necesario hacer un pull request y mantener el repositorio público para revisión.

## Instrucciones

### Instalación de Bulma (se utilizará dicho framework para el diseño)

```sh
$ npm install bulma --save
```

```javascript
import 'bulma/css/bulma.css';
```

### Importar el JSON
Será necesario que importes el json `foods.json` que se incluye en este repo para obtener toda la información de los alimentos

## Acerca del diseño
Para que no ocupes demasiado tiempo en la parte del diseño puedes utilizar el template `style-guides.html` que está en el directorio `starter-code` 

### Primer prueba | Crear un componente `FoodBox`
Crea un componente llamado `FoodBox` que tome `food` como una prop y muestre toda la información por ingrediente. Para que no pierdas tiempo en el diseño de la caja de contenido, puedes utilizar el siguiente snippet

```html
<div className="box">
<article className="media">
<div className="media-left">
<figure className="image is-64x64">
<img src="https://i.imgur.com/eTmWoAN.png" />
</figure>
</div>
<div className="media-content">
<div className="content">
<p>
<strong>Pizza</strong> <br />
<small>400 cal</small>
</p>
</div>
</div>
<div className="media-right">
<div className="field has-addons">
<div className="control">
<input
className="input"
type="number" 
value="1"
/>
</div>
<div className="control">
<button className="button is-info">
+
</button>
</div>
</div>
</div>
</article>
</div>
```

Al final deberás obtener algo parecido a lo siguiente:

![](https://i.imgur.com/bY9i5Rw.png)

### Segunda prueba | Mostrar todos los alimentos como iteración

En el componente `App`, deberás mostrar todos los elementos `FoodBox` que existen en tu variable `foods` (tip: utiliza correctamente las props)

Al final deberás mostrar algo como lo siguiente:

![](https://i.imgur.com/3TVQJDO.png)

### Tercer prueba | Agregar un nuevo alimento

Crea un botón para agregar elementos.
Cuando des click deberá aparecer un form con los campos "nombre", "número de calorías" y una imagen
Cuando el usuario de click en el botón que tenga la propiedad onClick submit, el alimento deberá ser agregado a la lista (tip: si tu modelo está correcto, esto será sumamente sencillo)
Adicional: el form deberá desaparecer cuando des el click submit (recuerda utilizar los componentDidMount, etcétera)

### Cuarta prueba | Crear una barra de búsqueda 

Genera un componente `Search` para realizar búsquedas

![](https://i.imgur.com/76zNUkW.png)


### Todas las iteraciones deben mostrarse en una pantalla que pueda ser reflejada en el localhost


# Conexión a api
### Primer prueba | Crear una vista dinámica para la prueba de conexión a API

Deberás crear en el routing una nueva vista a la que puedas acceder desde un link y que tenga regreso a la vista principal. En esa vista desarrollarás lo siguiente.

Para esta prueba será necesario generar un chart utilizando las siguientes herramientas:

API | Coindesk [CoinDesk](http://www.coindesk.com/) 
Para este ejercicio deberás conectarte a la API de Coindesk con los datos de [Bitcoin Price Index](https://web.archive.org/web/20191106152143/https://www.coindesk.com/api). Requeriremos que realices la representación de dichos datos de manera programática.

Representación gráfica | [Chart.js](http://www.chartjs.org/) 

# Instrucciones
Al final, deberás representar algo parecido a lo siguiente

![](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_b94d2137d3737b49ecf92ee8709f5a14.png)

## Primer iteración: Obtener data del API

Primero deberás obtener la data de la API para ser representada en el chart. Para ello utilizaremos la siguiente API [CoinDesk API Documentation](https://web.archive.org/web/20191106152143/https://www.coindesk.com/api)

Tendrás que hacer una presentación del histórico de datos en el chart haciendo una petición `GET` hacia la siguiente URL `http://api.coindesk.com/v1/bpi/historical/close.json` (puedes utilizar testing en Postman). El response deberá ser un objeto json.

Deberás realizar un AJAX request por lo tanto es necesario que importes el CDN de Axios.
TIP: Para probar tu request a la URL utiliza un `console.log()` para estar seguro de la petición.

## Segunda iteración: Crear el chart

Una vez que la petición sea exitosa, deberás mostrar el chart en la vista. Usaremos [Chart.js](http://www.chartjs.org/) por lo que será necesario que agregues el CDN.
Una vez agregada la referencia CDN deberás representar la información obtenida en el json del paso 1 en un [Line Chart](http://www.chartjs.org/docs/#line-chart-introduction)

## Tercer iteración: Filtrar fechas

Como puedes observar, por default, la API proporciona los datos del último mes. En esta iteración agregarás dos `input` de fecha para poder hacer ese filtro.
Revisa la documentación de [CoinDesk API](https://web.archive.org/web/20191106152143/https://www.coindesk.com/api) para ver como obtener datos entre dos fechas.
Recuerda que la información debe cambiar cada que eliges dos fechas distintas por lo que te recomendamos agregar listeners o triggers en tu función.

# Login

Tendrás que crear un login básico (si utilizas librerías como jsonwebtoken o bcrypt es un plus) en el que integres la autentificación con Google. Deberá contar con un logout y si incluyes algún rol de usuario o super usuario será un excelente bonus.

## En total son tres actividades: CRUD, conexión a API y Login. Siéntete libre de utilizar algun framework para Front End diferente al sugerido. Asimismo, cualquier adicional que desees integrar en los ejercicios será muy bien valorado. Mucho éxito.
