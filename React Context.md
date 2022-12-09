Nos permite consumir la información en un componente en específico sin la necesidad de enviarlo por medio de props através de todo el árbol.
De este modo, una petición a una api o lo que sea, se hace desde el componente que lo necesita y no del componente padre.
1) Rect.createContext es la función que se utiliza para crear el State Context. Ésta recibe como parámetro el valor predeterminado de dicho contexto, que pueden ser valores o funciones. Se guarda el contexto dentro de un const.
