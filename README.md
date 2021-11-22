
## Laravel SPA with Vue 3, Auth (Sanctum), CRUD Example

<p>Original tutorial</p>https://shouts.dev/laravel-spa-with-vue3-auth-crud-example

### Important Notice
<p>Add .vue() in webpack.mix.js if Vue compoments cannot be resolved when importing in router.js</p>
<p>The webpack.mix.js should look like below:
  
Also if you're serving the app with artisan serve or PHP embedded server,be sure to include localhost:8000
in config/sactum.php. If not the app will not be able redirect after successful login. See code snipette below:
```
'stateful' => explode(',', env('SANCTUM_STATEFUL_DOMAINS', sprintf(
    '%s%s',
    'localhost,localhost:3000,127.0.0.1,127.0.0.1:8000,::1,localhost:8000',
    env('APP_URL') ? ','.parse_url(env('APP_URL'), PHP_URL_HOST) : ''
))),
```
