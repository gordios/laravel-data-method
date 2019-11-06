# laravel-data-method

This repo provides helpers for form submission in Laravel like link form submission, disabling submit button on form.

## Install

Via npm

```
$ npm install laravel-data-method --save
```

Via bower

```
$ bower install laravel-data-method --save
```

## Usage

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1">

        <!-- CSRF Token -->
        <meta name="csrf-token" content="FAKETOKEN">

        <title>Laravel Data Method</title>

        <!-- Styles -->
        <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">

        <!-- Scripts -->
        <script type="text/javascript" src="node_modules/jquery/dist/jquery.js"></script>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
        <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>
        <script src="https://cdn.jsdelivr.net/npm/sweetalert2@9"></script>
        <script type="text/javascript" src="./dist/data-method.js"></script>

    </head>
    <body>
        <p>
            <!-- Link form with confirmation and params -->
            <a
                href="/"
                class="btn btn-primary"
                data-method="POST"
                data-params='{"id": 4}'
                data-confirm="Are you sure?">Submit Me</a>

            <!-- Link form with confirmation with bootstrap theme -->
            <a
                href="/"
                class="btn btn-primary"
                data-method="POST"
                data-confirm="Are you sure?"
                data-title="Please confirm this action"
                data-theme="bootstrap">Submit Me with bootstrap theme</a>

            <!-- Link form with confirmation with sweetalert2 theme -->
            <a
                href="/"
                class="btn btn-primary"
                data-method="POST"
                data-confirm="Are you sure?"
                data-title="Please confirm this action"
                data-theme="sweetalert">Submit Me with Sweet Alert theme</a>

            <!-- Link form with confirmation with javascript -->
            <a
                href="javascript:dataMethod('/', {confirm: 'Are you sure?', method: 'POST'})"
                class="btn btn-primary">Submit with javascript</a>

            <!-- Link form with confirmation with javascript -->
            <a
                href="/"
                class="btn btn-primary"
                data-method="POST"
                data-params='{"id": 4}'
                data-ajax="true">Submit with Ajax</a>
        </p>

        <!-- Desable form submit button on submit event -->
        <form action="" method="post">
            <button class="btn btn-success" type="submit" data-disabled-submit>Disable form button</button>
        </form>

        <!-- Desable form submit button on submit event with confirm message -->
        <form action="" method="post" class="mt-3">
            <button class="btn btn-success"
                type="submit" data-disabled-submit
                data-confirm="Are you sure?">Disable form button with confirm</button>
        </form>

        <!-- Desable form submit button on submit event with bootstrap theme -->
        <form action="" method="post" class="mt-3">
            <button class="btn btn-primary"
                type="submit"
                data-disabled-submit
                data-confirm="Are you sure?"
                data-title="Please confirm this action"
                data-theme="bootstrap">Disable form button with confirm Bootstrap</button>
        </form>

        <!-- Desable form submit button on submit event with sweetalert theme -->
        <form action="" method="post" class="mt-3">
            <button class="btn btn-primary"
                type="submit"
                data-disabled-submit
                data-confirm="Are you sure?"
                data-title="Please confirm this action"
                data-theme="sweetalert">Disable form button with confirm Bootstrap</button>
        </form>
    </body>
</html>

```

## Development

```
$ git clone https://github.com/brexis/laravel-data-method.git
$ cd laravel-data-method
$ yarn install --production=false
$ npm run build
```
