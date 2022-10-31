React es una librería.
En react los componentes que no sean puros tienen un ciclo de vida.
Inicialización (montaje), actualización y desmontaje.
*Qué es el DOM? Es el vínculo entre las etiquetas y los elementos.
React trabaja con Virtual DOM que se dedica a renderizar automáticamente una página. Pero sólo se concentra en los cambios específicos, es por eso que React se usa para la programación de páginas que simulan que todo está cargado en una sola página (AIRBNB). 
Este enfoque hace posible la API declarativa de React: le dices a React en qué estado quieres que esté la IU, y se hará cargo de llevar el DOM a ese estado. Esto abstrae la manipulación de atributos, manejo de eventos y actualización manual del DOM que de otra manera tendrías que usar para construir tu aplicación.
Montaje --> Nunca se ejecuta 2 veces. Se divide en tres : componenteWillMount, render y componentDidMount(Aquí es donde se manda llamar una api, por ejemplo). 
Actualización --> Un componente se actualiza de acuerdo a propiedades o estados. Sólo se renderiza el nodo específico. Concepto a tener en cuenta: compontentDidUpdate(se ejecuta indefinidamente).
Desmontaje --> El concepto es componentWillUnmount.
Componentes se dividen en ---->
Propiedades: Son sólo de lectura y no se pueden modificar. Son el medio de comunicación entre componentes. La comunicación solamente puede ser vertical (bidireccional entre componentes padre e hijo) y no horizontal.
Estados: Es la info que se va a guardar en cada componente. Se puede guardar de manera asíncrona.
Formas de trabajar con React: class components y functional components(hooks). El class es la versión uno de react. La diferencia es el ciclo de vida de los componentes. En el primero es más difícil.
JSX - Syntax extension to JS
HTML + JS :O
Const return H5 = () =>{    JS
    return <h5 class="elPili"> Hola Fili </h5>  HTML
}
Una mala práctica de REACT es utilizar el HTML cuando ya tenemos REACT. No se debe escribir nada.
Todo componente se escribe con CapitalCase para distinguirlo de las etiquetas de HTML. 
App es el punto de partida de nuestra navegación o del DOM.
Class es la palabra reservada para un componente. Extends crea una herencia de propiedades. 
Class App extends Component{

}

//1. Class Component
// Extender de Component
//class Car extends Component{
  //atributo
  /**
   * puertas
   * neumáticos
   * asientos
   * transmision
   * motor
   */
  //métodos
  /**
   * encender()
   * moverse()
   * arrancar()
   */
  // this.puerta
  // encender()
  // moverse()

//}

Aplicar 3 pasos en App.jsx
Para acceder a valores o variables js en HTML debo de abrir llaves {}
Para acceder a un atributo: {Car.puertas}
Para acceder a una función: {encender()}
Para acceder a los estados: this.setState ({name:newValue})
En jsx, para definir clases de html se usa className.
Toda la información entre nodos viaja por properties. Y cuando va del PADRE al HIJO son atributos {this.props.count1} PEro si es al revés, de HIJO a PADRE es por medio de métodos a manera de funciones {this.props.increment()}