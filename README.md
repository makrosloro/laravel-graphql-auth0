
# Laravel with GraphQL and secured by Auth0

This demo is for testing a Laravel API application with GraphQL integrated and secured by Auth0.

Links above:

- Laravel Framework (https://laravel.com/)
- GraphQL (https://graphql.org/)
- Auth0 (https://auth0.com/es)

## Requirements
- Php ^7.4
- Composer
- MySQL running local or remote (to run and save data)

## Running server app
Create the tables needed to persist wine `php artisan migrate`

Seed the database with the test data `php artisan db:seed`

Run the server `php artisan serve`

## Running queries
You can test demo using [Postman](https://www.postman.com/) and launch queries against current served url `localhost:8000/graphql?Authorization=Bearer xxxxxx`, where `xxxxxx` is API Token from your Auth0 Config. 

### Getting list of wines


```
{
  wines{
    name, color
  }
}
```

### Getting specific wine
Required wine id parameter.

```
{
  wine (id:1){
    name, color
  }
}
```
