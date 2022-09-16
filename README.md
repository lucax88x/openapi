# OpenAPI Spec
OpenAPI (Swagger) spec for Livingdocs Public API

This file makes it very easy to test and share our API enpoints.

## Supported environments
### edit.livingdocs.io
### localhost (WIP)

## How to use it (for now)
Import the openapi.yml file into insomnia as a design document, here you can test the APIs and add new endpoints.
For authenticated requests you need an API token from your Livingdocs project.

### Example endpoint
```yaml
  /channels/{channelHandle}:
      get:
        security: 
        - bearerAuth: [public-api:read]
        parameters:
        - name: channelHandle
          in: path
          description: Optional channelHandle. Will return first channel of a project if none is passed.
          required: true
          schema:
            type: string
            example: ""
        tags:
          - Project
        summary: details and configuration of this project.
        operationId: getChannel
        responses:
          "200":
           description: ok
```
## How to contribute
Keep the same structure as our documentation [docs](https://docs.livingdocs.io/reference-docs/public-api/)
Many API endpoints are still missing. Please mark the category as completed when all its endpoints are registered in the spec.
- Project ✅
- Composition API
- Publications 
- Search
- Document Lists
- Document Categories
- Routing
- Media Library
- Imports
- Sitemaps
- Health
- Add Delivery Status


## TODOs and future ideas
- add all the api endpoints
- share the OpenAPI spec file on edit.livingdocs/api/openapi.yml

