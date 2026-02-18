# Component Search

Next version of Component's [search-api](https://github.com/Unity-Billal-mesloub/search-api). Instead of having a dedicated search server, a JSON file of [crawled](https://github.com/Unity-Billal-mesloub/crawler.js) components is used in both the client and server instead. This library is available in both the browser and node.js.

The search algorithm is currently very rudimentary. Please advise!

## Node API

### var components = yield* search(options)

- `text` <String> - search through the `.name` and `.description` of components for `text`
- `keywords` <Array> - filter components by each `keyword`
- `owner` <String> - filter components by a GitHub user or organization
- `limit` <Integer> - maximum number of results

By default, components are sorted by stars/watchers, descending.

If you want to use a callback instead like the browser API, wrap `search` in `co` like: `var search = co(require('component-search2'))`.

## Browser API

### search(options, function (err, components) {})

The browser API is the same except with a callback instead.

