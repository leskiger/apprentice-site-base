# Kiger Media Apprentice Base Website


## What is it?

This is a project that Kiger Media apprentices can use to hone and confirm their basic web development skills.

## Tools

### Middleman

This project uses [Middleman](http://middlemanapp.com/), a static site generator. What's a static site generator? Basically it's a handy tool that allows you to leverage all the convenient standards and tools of modern web development to create non-database-driven websites (hence 'static').

Essentially, middle man lets you write files which are then translated into web pages. Why is this cool? Because you can do things like define a single layout file which will wrap the content of many different pages without having to actually put that code into every page. That means whenever you need to change the overall layout (say add a new navigation link) you just edit one place instead of on every single page. If you don't understand how cool that is right now, you will soon enough.

Middleman performs this magic by running the pages you write through a [Ruby](http://www.ruby-lang.org/en/)-based toolset. It includes it's own web server which does all of the translation automatically, making it easy to preview your work. Then, when you're ready to publish, you just run a single command and everything is generated as clean, complete html.

### Twitter Bootstrap

This project includes the [Twitter Bootstrap](http://twitter.github.io/bootstrap/) CSS framework. CSS is the code that makes your site look pretty. Bootstrap is a set of pre-made CSS classes (rules) which make it easier for you to make your site look pretty.

For example, Bootstrap defines a 12-column grid for your layout. So, say you want to create a three column row with the first column using half the page and the other two splitting the difference:

    .row
      .span6
        This is column 1. It is half the width of the page (it spans 6 of 12 grid lines)
      .span3
        This is column 2 It is 1/4 of the page (it spans 3 of 12 grid lines)
      .span3
        This is column 2 It is 1/4 of the page (it spans 3 of 12 grid lines)

Bootstrap also provides a lot of convenient styling for basic typography, navigation, tabs, slideshow, forms, etc. See the [example reference](http://twitter.github.io/bootstrap/scaffolding.html) for ideas.

One of the great things about Bootstrap is that it is easy to override the defaults. For example, lets say you wanted your page to have a blue background instead of a gray background. All you have to do is change the value of a variable in your screen.css.sass file:

    $bodyBackground:  #CFF1FF

Which brings us to SASS...

### SASS

This project is setup with the [SASS](http://sass-lang.org) CSS language. SASS basically makes it easy to write complicated CSS rules that would otherwise take a lot of verbosity.

For example, say you wanted some of your text to have a yellow-highlight background:

    $highlightBackground: #FFFDAB
    ...
    .highlight:
      background-color: $highlightBackground

You also want to have some columns be highlighted, so you add background-color: $highlightBackground to several places. Then you realize the yellow isn't quite right. Since you used SASS and variables, instead of having to find all the places and change them, you just change the one value for $highlightBackground from #FFFDAB to #FFF65D.

That's a simple example and if you don't yet see why this is so cool, you soon will.

The primary place to edit the styles for your site is in source/stylesheets/screen.css.sass

### Haml

SASS has a cousin called [Haml](http://haml.info/) which makes it really easy to write simple, clean html. Haml calls itself 'markup haiku,' meaning that it cuts out as much of the extra "junk" in writing html as possible.

So instead of writing:

    <div class="row">
      <div class="span6">
        <p>
          This is column 1. It is half the width of the page (it spans 6 of 12 grid lines)
        </p>
      </div>
      <div class="span3">
        <p>
          This is column 2 It is 1/4 of the page (it spans 3 of 12 grid lines)
        </p>
      </div>
      <div class="span3">
        <p>
          This is column 2 It is 1/4 of the page (it spans 3 of 12 grid lines)
        </p>
      </div>
    </div>

You can just write:

    .row
      .span6
        This is column 1. It is half the width of the page (it spans 6 of 12 grid lines)
      .span3
        This is column 2 It is 1/4 of the page (it spans 3 of 12 grid lines)
      .span3
        This is column 2 It is 1/4 of the page (it spans 3 of 12 grid lines)

This makes it not only easier to read the code, but also cuts out a lot of the possibilities for making mistakes by accidentally leaving off a < or a / or something silly like that.

## Getting Started

_Quick setup:_ Assuming you have Ruby setup, download this project, then <kdb>bundle install</kbd> and <kbd>bundle exec middleman</kbd>. Now visit <kbd>http://localhost:4567</kbd>

Check Middleman's [documentation](https://github.com/middleman/middleman) for details.

## License

* Twitter Bootstrap: Apache License v2.0
* Middleman: Copyright (c) 2010 Thomas Reynolds. MIT Licensed
* jQuery: MIT/GPL license
* highlight.js: Copyright (c) 2006, Ivan Sagalaev

Similarly, refer to each component for its license.

Everything else:

* [The Unlicense](http://unlicense.org/) (aka: public domain)
