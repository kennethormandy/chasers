# Chasers

[Bourbon](http://bourbon.io) [Neat](http://neat.bourbon.io) helpers, making complex, mobile-first layouts a little easier.

## Getting started

You’ll need to install and import Bourbon and Neat before the complementary Chasers. To do this manually, [download this repository](https://github.com/kennethormandy/chasers/archive/master.zip). Alternatively, use the package manager and build tool of your choice:

#### With npm

```
npm install kennethormandy/chasers
```

#### With bower

```bash
bower install chasers
```

Then, import your Sass files or include them in your build process as necessary.

```scss
@import "path/to/bourbon";
@import "path/to/neat";
@import "path/to/chasers";
```

## Example

The following will help you get started with the mixins included with Chasers.

### Omega Reset

Currently, Neat can’t properly reset the grid as you change the number of columns in a mobile-first, responsive layout. For example, using three columns on a small screen and switching to five on a mid-sized screen will still leave the `margin-right` values on every third column from the previous breakpoint. This can be easily reset with Chaser’s included Omega Reset mixin.

Read more about the main use of [Josh Fry’s Omega Reset here](http://joshfry.me/notes/omega-reset-for-bourbon-neat).

```scss
@include media(30em)  {
  @include span-columns(6);
  @include omega(2n);
}

@include media(48em)  {
  @include omega-reset(2n); // Pass in the previous media query's omega() argument to reset it
  @include span-columns(4);
  @include omega(3n);
}
```

The `omega-reset()` mixin uses the number of columns in the current media query be default, but there may be times where you also need a reset after straying from your media query’s default. You may fix your grid in this situation by passing this number in as the second argument, like so:

```scss
// Variables
$mid: new-breakpoint(max-width 30em 6); // Use 6 columns at this breakpoint

// Elsewhere
@include media($mid)  {
  @include span-columns(8); // Intentionally break the 6 column grid
  @include omega(2n);
}

@include media(48em)  {
  @include omega-reset(2n, 8); // Reset the omega value in the context of 8, rather than 6
  @include span-columns(4);
  @include omega(3n);
}
```

Chaser’s version of `omega-reset()` support right-to-left and left-to-right layout switching, which will be documented further in the next versions.

### Media Query Helper

[Josh Fry’s Media Query Helper](http://joshfry.me/notes/sass-media-query-helper-for-designers/) displays information about the current media query you’re working within, which is useful for developing and within SCSS user interface tests.

## Running locally

```bash
git clone https://github.com/kennethormandy/chasers
cd chasers
npm install -g harp # Install Harp to run the tests
npm install # Install Bourbon and Neat
npm test # Run the tests
```

## Contributing

Thanks for considering contributing! There’s information about how to [get started contributing to Chasers here](CONTRIBUTING.md).

## License

[The MIT License (MIT)](LICENSE.md)

Copyright © 2014 [Josh Fry](http://joshfry.me/) & [Kenneth Ormandy](http://kennethormandy.com)
