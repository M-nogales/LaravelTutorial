# LaravelTutorial
Tutorial de Laravel made by MartitaBoso y Manuel Nogales 

Para crear un proyecto, tras instalar composer: en el cmd dentro de la carpeta donde se quiere crear el proyecto: composer create-project laravel/laravel nombre “10.

Importar proyecto en visual studio code.

Hacer composer update y npm install en la terminal (arriba terminal, nueva terminal) porque hay archivos que no se suben por seguridad a git.

Copiar cp .\.env.example .env para copiar el .env y poder editarlo
Ponemos en el terminal : php artisan key:generate y lo copiamos en el APP_KEY
Cambiamos el nombre de la base de datos en DB_DATABASE

Activar el XAMPP de MySQL para crear la base de datos: le ponemos por ejemplo, ecommerce al nombre (para que todos coincidamos en el mismo nombre)
Escribimos “create database ecommerce;” y compilamos.
En VSC, en la terminal, escribimos php artisan migrate para meter la base de datos.

Descargar la BBDD y meterla en MySQL para ver las tablas y así hacerlo todo más rápido.

Para crear las tablas: en la terminal, php artisan make:migration create_nombre_table y se van creando en la carpeta database-migrations 
Entrando en lo que se crea, tenemos que ir añadiendo los atributos donde pone Schema::create 
Ej: Schema::create('order', function (Blueprint $table) {
            $table->id();
            $table->integer('id_product');
            $table->integer('id_user');
            $table->integer('state');
            $table->timestamps();

Cuando estéis en la rama main y queráis cambiar a vuestra rama porque os habéis equivocado, hacéis el commit (sin el push) y escribís en al terminal: git merge main. Ya estaréis en la rama vuestra y con vuestras cosas. 
Comando git reset head~1 para ir un commit, se unen los cambios anteriores a los nuevos y se hace

Seguir los apuntes de Olga para crear el log in y register.

Hay que abrir dos terminales a la vez, con el php artisan serve y otra con el npm run dev para que estén los servidores de cliente y servidor corriendo a la vez.
