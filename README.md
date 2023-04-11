# api-definition

This repository contains the API definition for the backend API (beekeeper) in the Alvarium project.

See [`swagger.yaml`](./swagger.yaml) for the current version.

It is used in most of the components as a submodule of the Alvarium project to ensure that the components are aligned in terms of the specification and that the requests/responses are formed according to the specification.

##  x-oapi-codegen-extra-tags

The annotation `x-oapi-codegen-extra-tags` provides a an extra annotation for the API-generator used in the Beekeeper project. This tells the generator to include the comment `binding: required` when generating the types. This comment is used by Gin to make sure that the client's request has the necessary format because it verifies that fields with this annotation are present in the request. This tag provides one layer of the API input validation.

## Use

To use this definition, we recommend including it via a Git submodule:

```bash
git submodule add https://gitlab.cyber-threat-intelligence.com/software/alvarium/api-definition.git api
```
