This project contains all the bootstrap sass source files. This project
will be useful to create new themes using sass.

`md_bootstrap_scss` is a Sass-powered version of
\[Bootstrap\](<https://github.com/twbs/bootstrap>), ready to drop right
into your Sass powered applications.

# Usage

1 - Create a new project with next structure:

    [project_root]
      ├─ pubspec.yaml
      ├─ web
      │  ├─ index.html
      │  ├─ _variables.scss
      │  ├─ theme.scss
      │  └─ ... other files and folders ...
      └─ lib
         └─ ... lib files and folders ...

2 - In the `pubspec.yaml` file add the `md_bootstrap_scss` and
`sass_builder` dependencies as
bellow:

``` yaml
name: md_bootstrap_scss_example # change this line to have your library name
description: An absolute bare-bones web app.
environment:
  sdk: '2.1.0 < 3.0.0'
dev_dependencies:
  build_test: ^0.10.3+3
  build_runner: ^1.1.2
  build_web_compilers: ^0.4.4+2
  sass_builder: ^2.1.2
```

3 - Then in `_variables.scss` add the variables you want to modify

``` scss
//== Colors

$primary:          #e72b42;
$secondary:        #73A839;
$info:             #033C73;
$warning:          #DD5600;
$danger:           #22afc7;
```

4- In the `theme.scss` add next code:

``` scss
include::example/web/theme.scss
```

5 - Then in the `index.html` you will add the link to `theme.css` as
bellow:

``` html
  <link rel="stylesheet" href="theme.css">
```

so you will end up with an `index.html` file like next one:

    <!DOCTYPE html>
    
    <html>
    <head>
      <meta charset="utf-8">
      <meta http-equiv="X-UA-Compatible" content="IE=edge">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <meta name="scaffolded-by" content="https://github.com/google/stagehand">
      <title>md_bootstrap_scss_sample</title>
      <link rel="stylesheet" href="theme.css">
      <link rel="icon" href="favicon.ico">
      <script defer src="main.dart.js"></script>
    </head>
    
    <body>
    
    <button class="btn btn-primary">Bootstrap Primary Button</button>
    <button class="btn btn-secondary">Bootstrap Secondary Button</button>
    <button class="btn btn-success">Bootstrap Success Button</button>
    <button class="btn btn-info">Bootstrap Info Button</button>
    <button class="btn btn-danger">Bootstrap Danger Button</button>
    <button class="btn btn-warning">Bootstrap Warning Button</button>
    
    </body>
    </html>

6 - Finally to run this project you will need to use next command:

    webdev serve

# Bugs and feature requests

Have a bug or a feature request to bootstrap core? Please open a new
issue at <https://github.com/twbs/bootstrap/issues/new>.

Have a bug or a feature request to bootstrap\_sass dart port? Please
open a new issue at
<https://github.com/dart-league/md_bootstrap_scss/issues/new>.

# Copyright and license

Code and documentation copyright 2011-2018 the [Bootstrap
Authors](https://github.com/twbs/bootstrap/graphs/contributors) and
[Twitter, Inc.](https://twitter.com) Code released under the [MIT
License](https://github.com/twbs/bootstrap/blob/master/LICENSE). Docs
released under [Creative
Commons](https://github.com/twbs/bootstrap/blob/master/docs/LICENSE).
