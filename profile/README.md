<p align="center">
  <img alt="php-arazzo: Arazzo workflow descriptions for PHP" src="https://raw.githubusercontent.com/PHP-Arazzo/.github/main/brand/social-preview.png" width="720">
</p>

**php-arazzo** brings the [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html) to PHP. Describe a sequence of API calls once, in a standard format, then validate it, run it and test it from PHP.

## What is Arazzo?

Arazzo is an [OpenAPI Initiative](https://www.openapis.org/) specification for describing **workflows across APIs**: which calls to make, in what order, how data flows from one step to the next, and what counts as success. An OpenAPI document tells you what an API *can* do. An Arazzo document tells you how to *use* it to get something done.

*Arazzo* is Italian for "tapestry", and our logo follows the idea. Each thread is a step, and the amber thread is the workflow running through the weave.

## What we build

- **[php-arazzo](https://github.com/PHP-Arazzo/php-arazzo)**: the main package.
  - **Parse and validate** Arazzo documents.
  - **Run workflows** with a built-in executor, not just a parser.
  - **Evaluate runtime expressions and criteria** against the spec's grammar.
  - **Resolve sources**: load the OpenAPI descriptions your workflows depend on.
  - **Laravel integration** for use inside Laravel applications.

## A workflow in a few lines

```yaml
arazzo: 1.0.1
info:
  title: Order a pet
  version: 1.0.0
sourceDescriptions:
  - name: petstore
    url: ./petstore-openapi.yaml
    type: openapi
workflows:
  - workflowId: find-and-order
    steps:
      - stepId: find-pet
        operationId: petstore.findPetsByStatus
        successCriteria:
          - condition: $statusCode == 200
        outputs:
          petId: $response.body#/0/id
```

Each step names an operation, states what success looks like, and passes its outputs on to later steps.

## Principles

- **Follow the spec.** We implement Arazzo as written and track the proposals still in discussion.
- **Test against shared fixtures.** Language-agnostic input/expected-result fixtures keep every implementation honest, ours included.
- **Plain and practical.** Clear docs, small APIs, examples first.
- **Open.** Design notes and architecture docs live in the repository.

## Get involved

- **Use it** and tell us what breaks. Real workflows are the best tests.
- **Open an issue** for bugs, ideas or spec questions in the relevant repository.
- **Send a pull request.** Start with the contributing notes in the repository you want to change.
- **Share workflows or fixtures** that exercise tricky parts of the spec.

## Links

- [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [OpenAPI Initiative](https://www.openapis.org/)
- [Brand guidelines](https://github.com/PHP-Arazzo/.github/blob/main/BRANDING.md)

---

<sub>php-arazzo is an independent implementation of the Arazzo Specification and is not affiliated with the OpenAPI Initiative.</sub>
