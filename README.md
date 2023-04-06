<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

## Main Packages
- Laravel 10
- Vite with laravel-vite-plugin
- Bootstrap 5 and popperjs
- Laravel Fortify for Authentication (without prebuilt views)
## Steps
1. Create Laravel project, I use composer create-project:

    ``
    composer create-project laravel/laravel laravel-bootstrap5-from-scratch
    ``
    
    Wait until finished and cd to "laravel-bootstrap5-from-scratch"
2. Install Bootstrap5 and PopperJS

    ``
    npm i --save bootstrap @popperjs/core
    ``
    
3. Install additional dependency. In addition to Vite and Bootstrap, we need another dependency (Sass) to properly import and bundle Bootstrap’s CSS.
    
    ``
    npm i --save-dev sass
    ``
    
5. Install Laravel/Fortify using:
   
   ``
   composer require laravel/fortify
   ``
   
   Publish the configuration files and Actions and migration files using:
   
   ``
   php artisan vendor:publish --provider="Laravel\Fortify\FortifyServiceProvider"
   ``
   
   Add App\Providers\FortifyServiceProvider::class to config/app.php Service Provider Array.
   
4. Create database, update .env and review migration files. Modify migration file for users table as neeed.
5. Run migration

   ``
   php artisan migrate
   ``
5. Configure Fortify views and features using documentation at [Laravel Documentation](https://laravel.com/docs/10.x/fortify).
6. It is a time to add Bootstrap5 JavaScript file to app.js file. Add the following to js/bootstrap.js to import all of Bootstrap’s JS. Popper will be imported automatically through Bootstrap.
   
   ``
   import 'bootstrap';
   ``
   
8. Next we load the Bootstrap CSS. Create folder "sass" inside resources folder and following files; "_variables.scss", "bootstrap.scss" in the newly created folder.
9. Update your vite.config.js to load "resources/sass/app.sass".
10. It is time to create layout files and views using Bootstrap Library.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
