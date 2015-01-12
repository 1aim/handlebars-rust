handlebars-rust
===============

Rust templating with Handlebars.

* travis-ci: [![Build Status](https://travis-ci.org/sunng87/handlebars-rust.svg?branch=master)](https://travis-ci.org/sunng87/handlebars-rust)
* crates.io: [handlebars](https://crates.io/crates/handlebars)
* document: [rust-doc](http://sunng87.github.io/handlebars-rust/handlebars/index.html)

**Warning**: This project, like rust, is in its early stage. Breaking
  changes are constantly introduced.

## Why Handlebars?

For information about handlebars, you will go to [handlebars.js](http://handlebarsjs.com).

It's my favorite templating tool by far. I used it in
[Delicious.com](https://delicious.com) as javascript-side template in
2013. Also I maintained a Clojure wrapper for Handlebars.java,
[hbs](http://github.com/sunng87/hbs). And you may notice the
close relationship between Ember.js and Rust community, handlebars is
the default templating language of Ember.js framework, which powers
[crates.io](http://crates.io).

Reasons I prefer Handlebars:

* Never ruin your Rust with HTML
* Never ruin your HTML with Rust
* Templating without a reuse mechanism is shit
* Templating wihtout customization is nothing but shit

Handlebars provides:

* Separation of Rust and HTML
* A few control structures makes templating easier
* Few control structures stops you to put logic into templates
* Template reuse with include(`>`), `partial` and `block`
* Customize template behavior with **helper**s

Limitations:

* As a static typed language, it's a little verbose to use handlebars
* You will have to make your data `ToJson`-able, so we can render it.

## Usage

Check examples in the source. The example shows you how to:

* Create a `Handlebars` and register the template from files
* Create a custom Helper by impl `HelperDef`, and register it
* Render something
* Make your custom struct `ToJson`-able.

Run `cargo run --example render` to see results.
(or `RUST_LOG=INFO cargo run --example render`) for logging output.

## Handlebars for Iron

Due to upstream changes, the example is currently broken. I have
started a separated project
[handlebars-iron](https://github.com/sunng87/handlebars-iron) for
this, which is still working in progress.

## License

MIT, of course.

## Contact

[Ning Sun](https://github.com/sunng87) (sunng@about.me)
