Nos permite consumir la información en un componente en específico sin la necesidad de enviarlo por medio de props através de todo el árbol.
De este modo, una petición a una api o lo que sea, se hace desde el componente que lo necesita y no del componente padre.
1) Rect.createContext es la función que se utiliza para crear el State Context. Ésta recibe como parámetro el valor predeterminado de dicho contexto, que pueden ser valores o funciones. Se guarda el contexto dentro de un const.

const Context = React.createContext(
    {count: 0, setCount: () => }
);

2) Crear el provedor. Éste recibe un prop value que serán los valores a compartir. 

const App = () => {
    const [count, setCount] = React.useState(0)

    return(
        <Context.Provider
            value={{
                count,
                setcount
            }}
        >
            <CounterComponent>
        </Countext.Provider>
    )
}

3) Consumir valores del contexto. useContext (es un hook). Se consumen los valores del contexto al almacenar loas valores en una variable usando el hook. useContext recibe como argumento el contexto que deseamos consumir.

const CounterComponent = () => {
    const MyContext = useContext(Context)

    return(
        <div>
            <span>{MyContext.count}</span>
            <button
                type="button"
                onClick={() => (MyContext.setCount + 1)}
            >
                Click
            </button>
        </div>
    )
}
