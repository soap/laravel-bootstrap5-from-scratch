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
    npm i --save-dev sass
    ``
    
3. Install Laravel/Fortify using:
   
   ``
   composer require laravel/fortify
   ``
   Publish the configuration files and Actions and migration files using:
   
   ``
   php artisan vendor:publish --provider="Laravel\Fortify\FortifyServiceProvider"
   ``
4. Create database, update .env and review migration files. Modify migration file for users table as neeed.
5. Run migration

   ``
   php artisan migrate
   ``
   
## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
