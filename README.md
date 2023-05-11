# SCSS Resets and Base files

I love working with scss, it gives me awesome features to make writing css easier. Still, I stumbled upon a lot of code repetition, researching a lil bit I found out about css resets, there are a lot of them, some more popular than others, this are the ones that work for me.

## What even is a reset?

CSS by default comes with some really ugly default styles, borders, margins, sizes... This resets overwrite those default values to some more standard ones, so you don't have to overwrite them yourself.

## What's the other stuff?

Apart from the reset, there are other 3 files in here, i'll explain them in a very simple way:

- **Base**: This file lets you define your global/base styles for all of your css, so it doesn't get mixed up in a lot of different files. Here you can create your own base styles that you know you'll repeat a lot in your project, it's also a great place to asign your background, font family, colors...
- **Variables**: Here you'll define your variables for your project, from colors, to fonts, margins, paddings, you name it!.
- **Mixins**: In this file you'll add your custom mixins, for this base file, there's just one, but you can create your own ones or find others on the internet.

## How to use

It depends on your project, the following steps are the way that I use them on React + Vite, but you can adapt it to your favorite framework.

First, run the following commands:

      # Create your project
      $ npm create vite@latest

      # Install dependencies
      $ npm i

      $ Install sass
      $ npm i -D sass

Then search for your global styles css file, it's usually called **index.css**, rename that bad boy to **index.scss**:

    # Find your global styles file
    |- src/
      |- index.css

    # Rename it to index.scss
    |- src/
      |- index.scss

After that, create a /styles folder in the src/ directory:

    # Create your sexy new folder
    |- src/
      |- styles/
      |- index.scss

Copy the 4 scss files of this repo into the folder you just created:

    # Copy the files of this repo in src/styles/
    |- src/
      |- styles/
        |- _base.scss
        |- _mixins.scss
        |- _resets.scss
        |- _variables.scss
      |- index.scss

> **Note**
> The leading underlines, are VERY important, don't remove them.

Now open the **index.scss** file and type the following lines:

```scss
@use "./styles/resets";
@use "./styles/base";
```

That's it, you made it! Now enjoy writing scss code.
