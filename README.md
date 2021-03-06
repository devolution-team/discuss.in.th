# Discuss.in.th

> In software engineering, **Don't Repeat Yourself (DRY)** is a principle of software development aimed at reducing repetition of software patterns, replacing it with abstractions, of repetition of the same data, using data normalization to avoid redundancy.


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


```
php artisan make:policy QuestionPolicy --model=Question
```

```
 php artisan make:policy AnswerPolicy --model=Answer
```

## Example codes 
best query with relationship models in method in  `SomeController.php`
```
\DB::enableQueryLog();
$questions = Question::with('user')->latest()->paginate(5);

view('question.index', compact('questions'))->render();

dd(\DB::getQueryLog());
```