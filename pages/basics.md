# Basics

## Routing

Routing file `(Routes → Web)` is like an index that catches all requests and try to match it with the list of URLs included in it. To create a new route rule.

```php
// We received a root URL and returned a view by the name of "welcome".
Route::get('/',function(){ 
		return view('welcome');
});
```

## Controller

Controller is a class that can handle requests related to same purpose, usually it works as a medium between Models and Views.

To create a controller

```bash
php artisan make:controller UserController // Name must be SingularController
```

Then we can create function that handles a specific route or task

```php
public function index() {
	return view('users.index'); // calling index view in the test folder
}
```

## View

Views are the actual HTML content that will be shown to the user, and Laravel provides a templating engine called BLADE which makes it easier for us to pass data to views. Blade file has `.blade.php` extension and will be stored under **`resources→views`** folder.

To use a passed parameter from controller to view

```bash
{{$param}}
```

## Model

Model is the class that handles the communication with the DB. To create a model

```html
php artisan make:model Post
```