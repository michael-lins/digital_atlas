# Refugees for Digital Atlas

This Refugees widget was designed for the Digital Atlas.  It is composed of:
- a line graph with the total number of refugees in asylum at current country distributed in the last five years.
- a pie chart for the current year with refugees' countries of origin distribution in percentage.
- a table containing the total of refugees regarding current country and year, distributed by country of origin, gender (male/female) and total sum.

## Dependencies

It uses the following PHP libraries:

- [arrilot/laravel-widgets](https://github.com/arrilot/laravel-widgets)

## Install

This package only works with the Digital Atlas.  To install:

1. Drop this package into the *App/Widgets/* directory.
2. Register the service provider, by adding the following to the providers array of *config/app.php* file:
```
App\Widgets\Refugees\RefugeesServiceProvider::class
```
3. In terminal, migrate the database.

_Docker_
```
docker-compose run --rm da_artisan migrate
```

_Manual Installation_
```
php artisan migrate
```

4. Added the widget to the view file using `@asyncWidget('App\Widgets\Refugees\RefugeesWidget', [], $country)`.

## Configuration

To publish the configuration file, simply run the following command:

_Docker_
```
docker-compose run --rm da_artisan vendor:publish
```

_Manual Installation_
```
php artisan vendor:publish
```

Then select **Provider: App\Widgets\Refugees\RefugeesServiceProvider** from the list.
