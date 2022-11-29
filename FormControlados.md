Formularios Controlados vs No controlados.

Los componentes NO controlados es aquel que se obtiene o es manejada desde el propio DOM. Esto es bajo los términos del propio React.
Los valores son tomados directamente del DOM. Es por eso que un hacker puede cambair los valores desde el navegador mismo. Estos no son predecibles porque pueden ser cambiado por otras fuentes.

Los componentes controlados maneja la información con estados (useEffect). Entonces, la info se guarda en un estado y así React puede validarlo. Estos son predecibles. Si algo afecyta a los elementos del formulario, los valores siempre estarán seguros en un estado local. En ese sentido, están controladas las validciones de un formulario. Es por ello que uno decide si la info puede o no puede ser capturada.