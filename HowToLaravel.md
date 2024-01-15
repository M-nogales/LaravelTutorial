# HowToLaravel
### Tutorial de Laravel made by MartitaBoso y Manuel Nogales 

Para crear un proyecto, tras instalar composer: en el cmd 
dentro de la carpeta donde se quiere crear el proyecto: composer create-project laravel/laravel nombre “10.
1. Instalar Composer con el cmd
2. `composer create-project laravel/laravel "nombre projecto"`

Importar proyecto en visual studio code.

 ## Cada vez que te bajes un rep con laravel
* `composer update`
* `npm install`
(regenera archivos que no se suben por el git.ignore y seguridad)
* `cp. \.env.example .env` (copiamos el .env para modificarlo)
#### .ENV
* `php artisan key:generate` y lo generado lo copiamos en copiamos en el APP_KEY 
* cambiamos el nombre de la base de datos en DB_CONNECTION

#### XAMPP Y MYSQL
* Activar Xampp por la parte de Mysql
* Ponemos Create database "Nombre de la ddbb"
* `php artisan migrate` Para meter los datos de la ddbb en Laravel
* Para crear las tablas: `php artisan make:migration create_nombre_table`
* Entrando en lo que se crea, tenemos que ir añadiendo los atributos donde pone `Schema::create`
` 
Ej: Schema::create('order', function (Blueprint $table) {
            $table->id();
            $table->integer('id_product');
            $table->integer('id_user');
            $table->integer('state');
            $table->timestamps();
}`
Entrando en lo que se crea, tenemos que ir añadiendo los atributos donde pone Schema::create 
Ej: Schema::create('order', function (Blueprint $table) {
            $table->id();
            $table->integer('id_product');
            $table->integer('id_user');
            $table->integer('state');
            $table->timestamps();
}
Cuando estéis en la rama main y queráis cambiar a vuestra rama porque os habéis equivocado, hacéis el commit (sin el push) y escribís en al terminal: git merge main. Ya estaréis en la rama vuestra y con vuestras cosas. 
Comando git reset head~1 para ir un commit, se unen los cambios anteriores a los nuevos y se hace

Seguir los apuntes de Olga para crear el log in y register.

Hay que abrir dos terminales a la vez, con el php artisan serve y otra con el npm run dev para que estén los servidores de cliente y servidor corriendo a la vez.
