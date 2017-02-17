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

### Sidenote with just text

```html
<p>
  This text could really do with an inspiring
  sidenote<%= partial("partials/annotations/_sidenote",
                      :locals => {
                        :uniqueId: "inspiring-note-1",
                        :sidenoteContent => "This is an inspiring note",
                      }) %>
</p>
```

### Side note with belief statement

```html
<p>
  This text talks about a problem in the world linked to a
  belief<%= partial("partials/annotations/_sidenote",
                    :locals => {
                      :uniqueId: "make-a-unique-id-for-this-sidenote",
                      :sidenoteContent => partial("partials/beliefs/understand_and_control"),
                    }) %>
</p>
```

The content of the beliefs themselves are stored in partials under the
directory `source/partials/beliefs/`:

- `understand_and_control`
- `technology_should_work_for_people`
- `work_together`

### Sidenote with asset

```html
<p>
  This text is dying to be backed up by the Locally
  logo<%= partial("partials/annotations/_sidenote",
                    :locals => {
                      :uniqueId: "make-a-unique-id-for-this-sidenote",
                      :sidenoteContent => partial("beliefs/understand_and_control"),
                    }) %>
</p>
```


### Image inside a margin-note

```html
<%= partial("partials/annotations/_margin_image",
            :locals => {
              :imagePath => 'Assets/Scout/image00.gif',
              :uniqueId => 'make-a-unique-id-for-this',
              :caption => "The Scout prototype showed participants real vulnerabilities for devices in their homes."
            }) %>
```
