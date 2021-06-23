# List of TODOs

NOTE: Developers did not have time to make code better (simplier and more readable)

1. Add tests
1. Add linter
1. Store responses from API calls in local storage (data won't be updated often)
1. Add pre-push to main hook to check if version in app.json was updated
1. Add decision tree diagram
1. We pull issuer keys from `${issuerURL}/.well-known/jwks.json`.
How do we check that `issuerURL` actually belongs to the issuer?
1. Complete code refactoring -> code looks scrappy, use [styleguide](https://gitlab.com/affinidi/coding-styleguide) for reference:
  - Use logger, instead of console.log
  - Proper error handling instead of console.log
  - Implement JWK certificate chain validation (commented out)