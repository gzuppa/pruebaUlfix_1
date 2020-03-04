# Prueba técnica Ulfix
# CRUD React

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

![](https://imgur.com/76zNUkW)


### Todas las iteraciones deben mostrarse en una pantalla que pueda ser reflejada en el localhost
# ¡Éxito!
