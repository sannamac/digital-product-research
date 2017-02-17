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

## Example of margin note

The `label for="..."` and `input id="..."` must match.

```
<p>
  We showed 6 independent retailers in Chorlton a prototype of Locally

  <label for="locally-description" class="margin-toggle sidenote-number"></label>


  <input type="checkbox" id="locally-description" class="margin-toggle">


  <span class="sidenote">
    Locally is a loyalty scheme
  </span>


  , a scheme that earns shoppers ‘perks’, redeemable in any participating business, when they shop with local independent retailers.
</p>
```
