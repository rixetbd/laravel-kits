
# Laravel - Starter Kits

We are happy to provide authentication and application starter kits to help you get a head start on developing your new Laravel application. The routes, controllers, and views required to register and authenticate users for your application are automatically scaffolded into these kits.

Although they are optional, you are welcome to use these starter kits. Installing a fresh copy of Laravel will allow you to create your own application from scratch. Regardless, we have no doubt that you'll create something fantastic!
## Auth : JavaScript & CSS Scaffolding
#### [Official Website](https://laravel.com/docs/7.x/frontend)
Even though Laravel does not impose any restrictions on the JavaScript or CSS pre-processors you employ, it does offer a fundamental starting point using Bootstrap, React, and/or Vue that will be useful for many applications. Both of these frontend packages are installed by Laravel by default using NPM.
### Installation
```bash
composer require laravel/ui
```
```bash
// Generate basic scaffolding...
php artisan ui bootstrap
php artisan ui vue
php artisan ui react
 
// Generate login / registration scaffolding...
php artisan ui bootstrap --auth
php artisan ui vue --auth
php artisan ui react --auth
```
```bash
npm install
npm run dev
```
```bash
php artisan migrate
```

Next, you may navigate to your application's /login or /register URLs in your web browser. All of Breeze's routes are defined within the routes/auth.php file.

## Auth : Laravel Breeze
#### [Official Website](https://laravel.com/docs/9.x/starter-kits#laravel-breeze-installation)
All of Laravel's authentication functionality, including as login, registration, password reset, email verification, and password confirmation, are implemented in a minimal, straightforward manner in Laravel Breeze.
### Installation
```bash
composer require laravel/breeze --dev
```
```bash
php artisan breeze:install
```
```bash
php artisan migrate
```
```bash
npm install
npm run dev
```
### Dark Mode
```bash
php artisan breeze:install --dark
```
Next, you may navigate to your application's /login or /register URLs in your web browser. All of Breeze's routes are defined within the routes/auth.php file.
## P1 - Laravel Debugbar 
#### [Official Website](https://github.com/barryvdh/laravel-debugbar)
![logo](https://i.ibb.co/ts00Br0/Laravel-Debugbar.png)

This package enables Laravel and PHP Debug Bar integration. To register the debugbar and bind it to the output, a ServiceProvider is included. Through Laravel, you may setup it and publish assets.

### Installation
Require this package with composer. It is recommended to only require the package for development.
```bash
composer require barryvdh/laravel-debugbar --dev
```
Laravel uses Package Auto-Discovery, so doesn't require you to manually add the ServiceProvider.
The Debugbar will be enabled when APP_DEBUG is true.

## P2 - Intervention Image

#### [Official Website](https://image.intervention.io/v2)
![logo](https://i.ibb.co/Jkj4cb4/Intervention-Image.jpg)
A PHP image handling and processing library called Intervention Image is free and open source. GD Library and Imagick, the two most popular image processing libraries, are supported, and it offers a simpler and more expressive approach to generate, edit, and compose images.
### Installation
```bash
composer require intervention/image
```

After you have installed Intervention Image, open your Laravel config file config/app.php and add the following lines. In the $providers array add the service providers for this package.

```bash
'providers' => [
    Intervention\Image\ImageServiceProvider::class,
];
```

Add the facade of this package to the $aliases array.

```bash
'Image' => Intervention\Image\Facades\Image::class
```

```bash
php artisan vendor:publish --provider="Intervention\Image\ImageServiceProviderLaravelRecent"
```

## P3 - Laravel Meta Manager

#### [Official Website](https://github.com/davmixcool/laravel-meta-manager)
Laravel Meta Manager is an SEO tool that you can use to enhance the SEO of a website or particular page by adding suggested meta tags to your application.

### SEO Features
- Standard Meta Tags
- Facebook OpenGraph Meta Tags
- Twitter Card Meta Tags
- Dublin Core Meta Tags
- Link Tags

### Installation
```bash
composer require davmixcool/laravel-meta-manager
```
```bash
'providers' => [
    Davmixcool\MetaManager\MetaServiceProvider::class,
];
```
```bash
php artisan vendor:publish --provider="Davmixcool\MetaManager\MetaServiceProvider"
```

### Usage
Once the configuration is complete you can then add the below at the meta area of the page you want to include meta tags;
```bash
@include('meta::manager')
```
```bash
@include('meta::manager', [
    'title'         => 'My Example Title',
    'description'   => 'This is my example description',
    'image'         => 'Url to the image',
])
```

## P4 - Agent

#### [Official Website](https://github.com/jenssegers/agent)
A PHP desktop/mobile user agent parser with support for Laravel, based on Mobile Detect with desktop support and additional functionality.
### Installation
```bash
composer require jenssegers/agent
```
```bash
'providers' => [
    Jenssegers\Agent\AgentServiceProvider::class,
];
```
```bash
'Agent' => Jenssegers\Agent\Facades\Agent::class,
```

```bash
use Jenssegers\Agent\Agent;
$agent = new Agent();
```


## P5 - Laravel Permission

#### [Official Website](https://spatie.be/docs/laravel-permission/v5/installation-laravel)
Through the Roles and Permission-based Access Control feature of Laravel Permissions, developers may provide users access control (ACL). Because of this, from the site's back end, one may change and grant users access.
### Installation
```bash
composer require spatie/laravel-permission
```
```bash
'providers' => [
    Spatie\Permission\PermissionServiceProvider::class,
];
```
```bash
php artisan vendor:publish --provider="Spatie\Permission\PermissionServiceProvider"
```
```bash
 php artisan optimize:clear
 # or
 php artisan config:clear
```
```bash
php artisan migrate
```


## Custom Sweetalert
[Custom Sweetalert](https://sweetalert2.github.io/) is a beautiful, responsive, customizable, accessibility (wai-aria) replacement for javascript popup boxes.

- [Click Link For Default Style](https://sweetalert2.github.io/)
- [Click Link For Custom and Minimal Style](https://rixetbd.github.io/sweetalert/)

## Notyf
[Notyf](https://sweetalert2.github.io/) is a simple JavaScript library for toast notifications is called Notyf. It is lightweight (3KB), responsive, A11Y compliant, and independent. React, Angular, Aurelia, Vue, and Svelte integration is simple. You can also [view On Github.](https://github.com/caroso1222/notyf)

### Usage
This section explains the base case using the minified bundle. See the quick recipes section for instructions to plug Notyf into Angular, React, Aurelia, Vue, or Svelte.

Add the css and js files to your main document:
```bash
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/notyf@3/notyf.min.css">
```
```bash
<script src="https://cdn.jsdelivr.net/npm/notyf@3/notyf.min.js"></script>
```
```bash
// Create an instance of Notyf
var notyf = new Notyf();
```
```bash
// Display an error notification
notyf.error('You must fill out the form before moving forward');

// Display a success notification
notyf.success('Your changes have been successfully saved!');
```

Please [Check Also](https://github.com/mckenziearts/laravel-notify)

## Viho Dashboard
Viho Admin is a premium, fully featured, multipurpose Bootstrap admin template created with HTML5, CSS, and JQuery. It is integrated with the most recent jQuery plugins and contains a large variety of reusable UI components. Any form of web application, including a bespoke admin panel, backend, CMS, or CRM, can use it.

[Download Source File](https://drive.google.com/file/d/1qXQ-t6ACWkLuwUa1EaGkj0frPyZK6cJ6/view?usp=sharing)

![Logo](https://i.ibb.co/F8c2nmp/01-banner-large-preview.jpg)

## License

[MIT](https://choosealicense.com/licenses/mit/)

