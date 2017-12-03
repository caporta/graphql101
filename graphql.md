GraphQL
=======
- **language**
  - JSON-like syntax
  - operations are constructed in documents
    - queries
    - mutations

- **runtime**
  - _request lifecycle_
    - read input from an interface
    - parse into abstract syntax tree (AST)
    - invokes resolver function for nodes
    - ask services for data
    - merge data returned from services


- **graphiql**
  - in-browser GraphQL IDE
  - [graphqlhub](https://www.graphqlhub.com)

- **fields**
  - modeled after functions
    - accept arguments
    - return data in response
  - _resolver functions_ determine return values
  - _complex fields_
    - require a selection set
    - types:
      - GraphQLList
      - GraphQLNonNull

  - _scalar fields_
    - lowest level types are always scalar
    - types:
      - GraphQLInt
      - GraphQLFloat
      - GraphQLString
      - GraphQLBoolean
      - GraphQLID (special; generally for refetch; responds w/ string)

- **variables**
  - `$variableName`
  - declared as keyword argument (name: type) of the query

- **directives**
  - alters runtime execution
    - @skip
    - @include

- **aliases**
  - alias keys to modify their response property
  - helps to avoid client-side processing after response
  - helps to get different instances of the same field in a single query

- **fragments**
  - field partials of a given type used for query composition
  - can be used _inline_
    - e.g. `... on ObjectType {}`
    - useful for Union fields
      - e.g. `author` is a union of `GithubUser` and `GithubCommitAuthor`
      - allows us to get fields conditional to a type in the union

- **mutations**
  - query with runtime awareness of side effects
