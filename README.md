# Andromeda

Andromeda is a *backend framework* for Rust, to simplify the development of the kinds of basic API services that we developers have to build so often.

## Motivation

If you've ever built an API before, the kinds of things you're doing are usually pretty similar: connect to a database, make some `get_all` queries, some `get_some` queries, add authentication somehow, add some `delete`s, some `update`s, some `add_one`s, expose it all through a server, and it's done. The logic behind all that might be doing AI sentiment analysis with self-training twelve-dimensional trans-temporal hypermodels, but the API layer is pretty darn predictable.

So, Andromeda was born! The idea is this: you, as a developer, should be able to declare the types you want to have in your database (e.g. `User`), and then say what kinds of queries you want to be accessible on that type (e.g. `get_one`, `get_some`, `add_one`, etc.), and it should *just work*. This might sound pretty familiar if you've used something like [Strapi]() before, and Andromeda is kind of like a non-GUI version of Strapi, with inbuilt support for powerful authentication without having to define a million special functions. When a user is authenticated, your resolvers get a little object that tells you about them, and you can do whatever you want with that --- wave them through, vehemently deny access, etc.

When we were building this, we realised that most APIs follow a pretty common pattern. GraphQL kind of got this in their schema of *queries*, *mutations*, and *subscriptions*, but we've taken that further to define the explicit types of queries, mutations, and subscriptions that are used in today's apps. But, if you want to do something a bit more unique in your app, you can easily define a custom resolver for it!

Oh, and aren't we all a bit fed up with having to spin up Docker instances of MongoDB on our local machines? Andromeda uses SQLite automatically in development, and comes with batteries installed. Going to production? Automatic migration to any supported database. 😎

Last thing: it's Rust. It's fast. Happy?

## Project Status

Andromeda is currently in the early stages of development and testing, with a v0.1.0 release expected hopefully before the end of 2022! It'll probably be riddled with bugs and be absurdly unergonomic, but, after a few versions, we should have sorted ourselves out! If you think Andromeda sounds like it would be useful for you, check out out [contributing guide]() to see where you might be able to help out! Every little bit helps us deliver a higher-quality library faster!

## License

See [LICENSE](./LICENSE).
