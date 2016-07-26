# \<alijaya-masonry\>

masonry layout in polymer, inspired by desandro/masonry

## Demo and API Docs

[*Demo and API Docs*](http://alijaya.github.io/iron-accordions/components/alijaya-masonry/)

## Example

``` html
<alijaya-masonry cols="4" cell-ratio="1" gutter="10">
  <alijaya-masonry-item col="2">1</alijaya-masonry-item>
  <alijaya-masonry-item>2</alijaya-masonry-item>
  <alijaya-masonry-item col="2" row="2">3</alijaya-masonry-item>
  <alijaya-masonry-item col="2" row="1">4</alijaya-masonry-item>
  <alijaya-masonry-item col="1" row="2">5</alijaya-masonry-item>
  <alijaya-masonry-item col="1" row="2">6</alijaya-masonry-item>
  <alijaya-masonry-item row="3">7</alijaya-masonry-item>
  <alijaya-masonry-item col="2" row="2">8</alijaya-masonry-item>
  <alijaya-masonry-item col="2" row="2">9</alijaya-masonry-item>
</alijaya-masonry>
```

## `gutter`

Define the spacing between the items.

## `cell-width`, `cell-height`, and `cell-ratio`

One of this value can be derived from the other value.

If `cell-width` is missing, it can be derived from `cell-height` * `cell-ratio`.

If `cell-height` is missing, it can be derived from `cell-width` / `cell-ratio`.

If `cell-width` and `cell-height` are missing, it will find `cell-width` using `cols`
(See Next Section), and derive `cell-height` using the same way.

If `cell-width`, `cell-height`, and `cell-ratio` are set, then `cell-ratio` is ignored.

## `alijaya-masonry` width, `cols` and `cell-width`

If `cols` is missing, it can be derived from `alijaya-masonry` width / `cell-width`.

If `cell-width` is missing, it can be derived from `alijaya-masonry` width / `cols`.

If `cols` and `cell-width` are set, `alijaya-masonry` width could be the
`cols` * `cell-width` if the `display` style of `alijaya-masonry` is set to `inline`.

## `rows`

If `rows` is missing, the component will take the full height.

If `rows` is set, then the component will take the `cell-height` * `rows`.

## `col` and `row` in `alijaya-masonry-item`

Default to 1. Define how much column and row that item takes.

## Item `col` is bigger than `cols`

The item `col` will be truncated.

## Can't derive `cell-height`

If after all of the effort, we can't still derive the `cell-height`, then the
item will take its original height, `row` will be ignored.

And the component will take the full height, `rows` will be ignored too.
