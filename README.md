# Discuss.in.th


## Useful commands

```
composer require laravel/tinker
```

```
php artisan vendor:publish --tag=laravel-pagination
```

```
composer require barryvdh/laravel-debugbar --dev
```

for live laravel mix
```
npm run watch
```

```
php artisan route:list --name="question.index"
```

## Example codes 
best query with relationship models in method in  `SomeController.php`
```
\DB::enableQueryLog();
$questions = Question::with('user')->latest()->paginate(5);

view('question.index', compact('questions'))->render();

dd(\DB::getQueryLog());
```