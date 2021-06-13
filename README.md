# breakpoint-indicator
Breakpoint indicator component for laravel blade using tailwindcss


## Usage

To get started, make sure to paste the blade component into your components directory: `resources/views/components`

Next, in order to display the breakpoint indicator, insert the component inside your master or main blade view, so it display throughout the whole application, you can display it like this:

`<x-breakpoint-indicator></x-breakpoint-indicator>`

## Display on the whole application
```
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    
    <!-- Styles -->
    <link href="{{ asset('css/app.css') }}" rel="stylesheet">
</head>
    <body>
        @yield('body')
        
        <x-breakpoint-indicator></x-breakpoint-indicator>

        <!-- Scripts -->
        <script src="{{ asset('js/app.js') }}"></script>
    </body>
</html>
```

## Display only on local and stage enviroment

You can wrap the component inside the `@env` to only show the components durant local or staging development. This way it will not be shown in production:
```
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    
    <!-- Styles -->
    <link href="{{ asset('css/app.css') }}" rel="stylesheet">
</head>
    <body>
        @yield('body')
        
        @env(['local', 'stage'])
            <x-breakpoint-indicator></x-breakpoint-indicator>
        @endenv

        <!-- Scripts -->
        <script src="{{ asset('js/app.js') }}"></script>
    </body>
</html>
```
