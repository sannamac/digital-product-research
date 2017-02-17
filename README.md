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

## Example of side note

The `label for="..."` and `input id="..."` must match.

```
<p>
  We showed 6 independent retailers in Chorlton a prototype of Locally
  ``
  <label for="locally-description" class="margin-toggle sidenote-number"></label>
  ``

  <input type="checkbox" id="locally-description" class="margin-toggle">


  <span class="sidenote">
    Locally is a loyalty scheme
  </span>


  , a scheme that earns shoppers ‘perks’, redeemable in any participating business, when they shop with local independent retailers.
</p>
```
## Example of margin note

```
<p>If you want a sidenote without footnote-style numberings, then you want a margin note.
  <label for="mn-demo" class="margin-toggle">⊕</label>
  <input type="checkbox" id="mn-demo" class="margin-toggle">
  <span class="marginnote">
    This is a margin note. Notice there isn’t a number preceding the note.
  </span> On large screens, a margin note is just a sidenote that omits the reference number. This lessens the distracting effect taking away from the flow of the main text, but can increase the cognitive load of matching a margin note to its referent text. However, on small screens, a margin note is like a sidenote except its viewability-toggle is a symbol rather than a reference number.
</p>

```
