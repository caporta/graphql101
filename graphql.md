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
