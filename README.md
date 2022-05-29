# GraphQL Restaurant Data Exercise 🍽

Sample API (GraphQL) queries and [CRUD](https://rapidapi.com/blog/api-glossary/crud/) implementaion solution.

## Tasks:

- Set up GraphQL for a restaurant data.
- Add mutations to get and update these data.

## List of GraphQL queries used:

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
- Run the index.js file on `http://localhost:5500/graphql` in order to make queries with GraphQL.

## Usage

<img src = 'https://raw.githubusercontent.com/anyapages/graphql-restaurant-data-exercise/main/image.png?token=ATDMTEB7ZUUGO34UBGIMEGTBLLXHK' width="550" height="440"> 

## Learn More

To learn GraphQL, queries and mutations, check out the [GraphQL documentation](https://graphql.org/), [Queries and Mutations](https://graphql.org/learn/queries/).

## License

[MIT](https://github.com/anyapages/graphql-restaurant-data-exercise/blob/main/LICENSE) 
