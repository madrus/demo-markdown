## 6. Dessert: Docsify

> __[Docsify](https://docsify.js.org/#/) is a magical light-weighted documentation site generator.__
>
> It does not require any JavaScript frameworks to use nor npm packages to install.

### Just 4 simple steps to take...

1. Create a `docs` folder at the root of your project with a `docs/images` subfolder in it.

1. Create a `sidebar.md` document inside the `docs` folder and keep your sidebar menu in it:

    ``` markdown
    - [Home](/)
    - [1. What is Markdown](/markdown.md)
    - [2. Markdown isn't for everyone](/everyone.md)
      ...
    - [References](/references.md)
    ```

1. Add a small `readme.md` in the root of the project for the home page only:

    ``` markdown
    # The Discrete Charm of Markdown

    ## Agenda

    1. [What is Markdown](/markdown.md)
    1. [Markdown isn't for everyone](/everyone.md)
    ...
    1. [References](/references.md)
    ```

1. Add `index.html` in the project root

    ``` html
    <!DOCTYPE html>
    <html lang="en">

    <head>
      <meta charset="UTF-8">
      <title>The Discrete Charm of Markdown</title>
      ...
      <link rel="stylesheet"
        href="https://cdn.jsdelivr.net/npm/docsify-themeable@0/dist/css/theme-simple.css">
      <style>
        ...
      </style>
    </head>

    <body>
      <div id="app"></div>
      <script>
        window.$docsify = {
          name: 'The Discrete Charm of Markdown',
          logo: 'docs/images/markdown.png',
          repo: '<your repository link>',
          loadSidebar: 'docs/sidebar.md',
          subMaxLevel: 1,
          auto2top: true,
        }
      </script>
      <script src="//cdn.jsdelivr.net/npm/docsify@4.11.4/lib/docsify.min.js"></script>
      <script src="//cdn.jsdelivr.net/npm/docsify@4.11.4/lib/plugins/search.min.js"></script>
      ... some more plugins for syntax colorization
      <script src="https://unpkg.com/docsify-copy-code@2"></script>
    </body>

    </html>
    ```

### Run locally

Inside your project run:

``` bash
yarn docs
```

It will open the documentation automatically in your favorite browser, e.g., on <http://localhost:3031>.

### Built-in link to the repository

If you have specified the `repo` paramater in the `index.html` file, Docsify will create a button link in the top right corner of the screen.

[![repo link](images/repo-link.png)](http://madrus4u.com/demo-markdown/)

### Free publishing on Github Pages

Here is the published version of this [Markdown Demo](http://madrus4u.com/demo-markdown/).
