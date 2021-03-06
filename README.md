# GraphQLBeautifierBurpSuitExt

It basically decodes the new line characters `\n` of the queries.

# E.g.

```

{"operationName":"PosLocations","variables":{},"query":"query PosLocations {\n  locations(first: 50) {\n    edges {\n      node {\n        id\n        name\n        __typename\n      }\n      __typename\n    }\n    __typename\n  }\n}\n"}

```

will turn into

```

{"operationName":"PosLocations","variables":{},"query":"query PosLocations {
  locations(first: 50) {
    edges {
      node {
        id
        name
        __typename
      }
      __typename
    }
    __typename
  }
}
"}

```

# Download

+ https://github.com/k-sau/GraphQLBeautifierBurpSuit/blob/master/dist/GraphQLBeautifierBurpSuitExt.jar

# How I did it?

+ In `\n`, \ and n were treated as two different characters.
+ I replaced the \ and n with one single character, i.e. `\n`

# Big thanks to

+ https://github.com/PortSwigger/json-beautifier
+ https://github.com/PortSwigger/example-custom-editor-tab
