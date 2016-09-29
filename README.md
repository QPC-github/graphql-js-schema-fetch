[![Circle CI](https://circleci.com/gh/Shopify/graphql-js-schema-fetch.png?circle-token=3be0ebe6fbb4841442b86678696947bd4b5456d7)](https://circleci.com/gh/Shopify/graphql-js-schema-fetch)

# graphql-js-schema-fetch

It fetches the JSON representation of the GraphQL schema from a live server

## Table Of Contents

- [Installation](#installation)
- [Examples](#examples)
- [API](#api)
- [License](http://github.com/Shopify/graphql-js-schema-fetch/blob/master/LICENSE.md)

## Installation

```bash
git clone git@github.com:Shopify/graphql-js-schema-fetch.git
cd graphql-js-schema-fetch
npm install
npm link
```

## Examples

To fetch the json representation of the graphql schema from a live server that
implements the GraphQL (and optionally the Relay) spec, run:

```bash
graphql-js-schema-fetch --url https://www.my-server.com/api
```

If your server requires additional credentials or headers, use the `--header`
option:

```bash
graphql-js-schema-fetch --url https://www.my-server.com/api --header "Authorization: Basic abc123" --header "X-API-Version: 1.1"
```

If your server uses something other than the `POST` method for its API, use the
`--method` option:

```bash
graphql-js-schema-fetch --url https://www.my-server.com/api --method GET
```

## API

#### `const instance = graphqlJsSchemaFetch(url, method, [headers]);`

Params you can pass `graphqlJsSchemaFetch`:
- `url` - The url where your GraphQL API resides
- `method` - The HTTP method to use while making the request
- `headers` - A hash representing the key value pairs of headers to pass to
  `node-fetch`

## License

MIT, see [LICENSE.md](http://github.com/Shopify/graphql-js-schema-fetch/blob/master/LICENSE.md) for details.

<img src="https://cdn.shopify.com/shopify-marketing_assets/builds/19.0.0/shopify-full-color-black.svg" width="200" />
