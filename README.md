goodbye coding 👋
# apollo-nodejs

[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg)](#contributors)

🔥💚 Using Apollo with NodeJS

## Quick start

### Install dependencies

```sh
$ yarn
```

### Run this app

```sh
$ yarn start
```

### Client

1. Query, aliases and fragments

![query1](./images/query1.png)

```
query getCat($catId: Int!) {
  cat(id: $catId) {
    id
    name
    color
  }
}
```

![query2](./images/query2.png)

```
query getCatWithFagments($catId1: Int!, $catId2: Int!) {
  cat1: cat(id: $catId1) {
    ...catFields
  },
  cat2: cat(id: $catId2) {
    ...catFields
  }
}

fragment catFields on Cat {
  id
  name
  color
}
```

![query3](./images/query3.png)

```
query getCats($color:String) {
  cats(color: $color) {
    ...CatFields
  }
}

fragment CatFields on Cat {
	name
  color
}
```

2. Mutation

![mutation](./images/mutation.png)

```
mutation updateCatColor($id: Int!, $newColor: String!) {
  updateCatColor(id: $id, newColor: $newColor) {
    ...catFields
  }
}

fragment catFields on Cat {
  id
  name
  color
}
```

🙌 Awesome

## Contributors

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
<table><tr><td align="center"><a href="http://cuongw.me"><img src="https://avatars0.githubusercontent.com/u/34389409?v=4" width="100px;" alt="Cuong Duy Nguyen"/><br /><sub><b>Cuong Duy Nguyen</b></sub></a><br /><a href="https://github.com/cuongw/thinid/commits?author=cuongw" title="Code">💻</a> <a href="https://github.com/cuongw/thinid/commits?author=cuongw" title="Documentation">📖</a> <a href="https://github.com/cuongw/thinid/commits?author=cuongw" title="Tests">⚠️</a> <a href="#review-cuongw" title="Reviewed Pull Requests">👀</a></td></tr></table>

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!

## License

MIT © [Cuong Nguyen](https://www.linkedin.com/in/cuong9/)


<!-- INSPIRATIONAL_QUOTE_START -->
> "The only way to do great work is to love what you do." - Steve Jobs
<!-- INSPIRATIONAL_QUOTE_END -->
