# Digital Product Research showcase

https://dpr.coop.co.uk

## Develop

Run middleman with live reload:

```
bundle exec middleman server
```

## Deploy

```
make deploy
```

## Project page structure

Experiment pages are in the root source folder. Content for each are in `source/partials` folder. This is so that we can add *just the content* for each experiment into the index page (without the Methods, Further Reading and Related Projects sections.)

Take a look at an existing experiment page, eg. `source/locally.html.erb` and its corresponding content page eg. `source/partials/experiments/locally.erb` to learn how this should look.

## Add page experiment page on source/index.html.erb

```
<div class="project" id="project-locally">
  <a href="locally" title="Read about our experiment into keeping money in the local economy">
    <%= partial('partials/experiment/locally') %>
  </a>
</div>
```

### Narrative format for experiment pages

You'll notice a format that goes like this:

1. `<header class="project-title"> ...` Put your title here
2. `<section class="situation"> ...` Outline the situation
3. `<section class="complication"> ...` The complication
4. `<section class="what-we-did"> ...` What we did
5. `<section class="question"> ...` Question
6. `<section class="answer"> ...` Answer
7. Repeat last 2 steps as necessary
8. `<section class="learning"> ...` The learning


### BEWARE!

Currently adding links to a content partial will break the page! This is because on the index page we wrap each experiments' content inside an anchor tag and therefore there'd be an anchor inside an anchor.

### Image display options

#### Aside (left sidebar)

```
<aside>
  <figure>
    <%= image_tag 'Assets/Project/image.jpg', {:alt => 'Alt text' } %>
    <figcaption>
      Caption text
    </figcaption>
  </figure>
</aside>
```

#### inline

```
<figure>
  <%= image_tag 'Assets/Project/image.jpg', {:alt => 'Alt text' } %>
  <figcaption>
    Caption text
  </figcaption>
</figure>
```

#### Inline wide

```
<figure class="img-wide">
  <%= image_tag 'Assets/Project/image.jpg', {:alt => 'Alt text' } %>
  <figcaption>
    Caption text
  </figcaption>
</figure>
```

## Embed a prototype

### Mobile device in left sidebar

The `iframe` URL needs to be given to the server admin to allow the page to display outside websites.

```
<aside class="experiment-live">
  <figure class="mobile-frame">
    <h2>Try our experiment:</h2>
    <div class="frame">
      <div class="embed">
        <iframe width="375" height="667" frameborder="0" src="https://example.com"></iframe>
      </div>
    </div>
    <figcaption>
      Caption text
    </figcaption>
  </figure>
</aside>
```

### Desktop embed full width

If a prototype is not optimised for mobile then use this.

The `iframe` URL needs to be given to the server admin to allow the page to display outside websites.

```
<aside class="experiment-live desktop-embed">
  <figure>
    <div>
      <iframe width="100%" height="600" frameborder="0" src="https://example.com"></iframe>
    </div>
    <figcaption>
      Caption text
    </figcaption>
  </figure>
</aside>
```

## Typography

### Blockquotes

Don't use quote marks as they are added for you in the styles.

```
<blockquote>
  <p>
    Quote text
  </p>
  <footer>-
    <cite>
      C, person's role, person's involvement
    </cite>
  </footer>
</blockquote>
```

### Pull quotes (displayed in left sidebar)

```
<blockquote class="pull-quote">
  <p>
    <span>
      Pull quote text
    </span>
  </p>
</blockquote>
```

## Styles

Once you've created a new experiment page you'll need to:

* duplicate an existing experiment stylesheet, eg. `source/stylesheets/_project-safer-emails.scss`
* name your new stylesheet reflecting your new experiment
* find and replace all existing colour variables. Notice eg. `$colour-project-safer-emails`
* rename the `ID` on line 5 to match the experiment on the index page
* rename the `class` on line 40 to match the slug of your experiment page, eg. `.safer-emails_index`
* use a new colour for line 1. You'll find the palette in `source/stylesheets/site.css.scss`, eg. `$base-biscay`
