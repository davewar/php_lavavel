DW NOTES
https://laravel.com/docs

CREATE PROJECT:
laravel new pizzahouse

RUN DEV SERVER:
php artisan serve

CREATE CONTROLLER (app>Http>Controllers>):
a)php artisan make:controller PizzaController
b) uncomment line 29 in "pizzahouse\app\Providers\RouteServiceProvider.php" for Controllers to work:
"protected \$namespace = 'App\\Http\\Controllers';"

Connecting to mysql db first set up:
env => advanced > enviroment variables > path > edit > new >
then paste below if not found
C:\xampp\mysql\bin

login
cmdline > mysql -u root
CREATE DATABASE pizzahouse;
control c to exit

---

CLOSE PORTS if unable via taskmanager
Control Panel\System and Security\Administrative Tools\services

---

CREATE MIGRATION FILE (in "database/migrations") ie tables
a)php artisan make:migration create_pizzas_table

To create tables in the mysql db - run migrations:
php artisan migrate

LIST OF COMMANDS = php artisan
some commands:
php artisan migrate:status
php artisan migrate:rollback << will loose data if exists>>

ALTER column to table without lossing data in the table:
a) php artisan make:migration add_price_to_pizzas_table
b) add column to migration file.
c) php artisan migrate

MODELS location: app>Models
Responsible for interacting with underlying database tables.
CREATE A model:
php artisan make:model Pizza

https://www.educba.com/laravel-models/

SET UP Authenication:
composer require laravel/ui
php artisan ui vue --auth
npm i vue-loader
npm install && npm run dev

list of routes:
php artisan route:list

New MVC shortcut setup:
php artisan make:model Kebab -mc
database>migration > add the table columns
php artisan make:migration create_kebab_table
next add controlers and routes !
