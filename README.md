# GraphQL Restaurant

## Objectives

- Set up GraphQL for a restaurant data.
- Add mutations to get and update these data.

## queries used:

- restaurant: Gets a single restaurant based on a provided ID. 
- restaurants: Gets a list of all restaurants. 
- setrestaurant: Creates a new restaurant. 
- deleterestaurant: Deletes a restaurant based on the provided ID.
- editrestaurant: Updates a restaurant based on the provided ID.

```javaScript
mutation editrestaurants($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}

mutation setrestaurants {
  setrestaurant(input: {
    name: "Granite",
    description: "American",
  }) {
    name
    description
  }
}

mutation deleterestaurants($iid: Int = 1) {
  deleterestaurant(id: $iid) {
    ok
  }
}

query getrestaurants {
  restaurants {
    name
    description
    dishes {
      name
      price
    }
  }
}
```

## Installation

- `npm install`
- `node index.js`

## Roadmap
No further updates planned

## License

[MIT](https://github.com/anyapages/graphql-restaurant-data-exercise/blob/main/LICENSE) 
