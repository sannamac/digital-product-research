# Digital Product Research showcase

https://coopdigital.github.io/digital-product-research

## Develop

Run middleman with live reload:

```
bundle exec middleman server
```

## Deploy

```
make deploy
```

## Using partials

### Side note with belief statement

```html
<%= partial("partials/annotations/sidenote", 
  :locals => { :sidenoteContent => partial("partials/beliefs/technology_should_work_for_people") }) %>
```
Where `sidenoteContent` 

### Sidenote with asset

```html
<%= partial("partials/annotations/sidenote", 
  :locals => { :sidenoteContent => partial("partials/assets/locally-logo") }) %>
```

### Sidenote with just text

```html
<%= partial("partials/annotations/sidenote", 
  :locals => { :sidenoteContent => "w" }) %>
```

```html
<%= partial("partials/annotations/sidenote",
  :locals => { :sidenoteId => "SomethingUnique", :sidenoteContent => partial("partials/assets/locally-logo") }) %>
```
