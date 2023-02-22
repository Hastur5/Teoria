Se inicializa NPM: npm init -Y
Se instala express: npm install express
Se instala Postgres: npm install pg (estilo clásico)
Se instala Nodemon: npm install nodemon -D
Se instala Sequelize: npm install sequelize (estilo fresh)

En package agregar abajo de main "type":"module"

Para mapear en automático la tabla. Instalar: npm i sequelize-auto. 

Y para ejecutar. Ahora, debemos de darle acceso a la base:

npx sequelize-auto -h localhost (host o servidor) -d zoo (nombre de la base) -u postgres (usuario) -x chapito12 (contraseña) -p 5432 (puerto) --dialect postgres (hacia qué motor de base) -o ./models (donde guardar los modelos) -l es5 (que los escriba en ecmascrib)

Posterorimente, al final de models. Se tiene que construir una relación.

Cuando la relación es 1 a 1, no vale la pena poner has one y belog to. Sin embargo, si es uno a muchos, es mejor hacerlo para asegurarnos.