# Location Autocomplete - Applying API Mocks

This application allows you to autocomplete location search texts, providing
suggestions with the
[Google Maps Places API](https://developers.google.com/maps/documentation/places/web-service).

## 1. Access

[![Open in Stackblitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/diego-aquino/api-mocking-app-autocomplete?startScript=dev&file=README.md)

## 2. Project

Important files:

- [`src/server/app.ts`](./src/server/app.ts): main application file where the
  server is implemented.
- [`src/clients/GoogleMapsPlacesClient.ts`](./src/clients/googleMaps/GoogleMapsPlacesClient.ts):
  class that makes HTTP calls to the Places API.
- [`tests/autocomplete.test.ts`](./tests/autocomplete.test.ts): file for
  location autocomplete tests.

Useful commands:

- `npm install`: installs the project **dependencies**.
- `npm run dev`: starts the **server** in development mode.
- `npm run test`: runs the application **tests** in watch mode.
- `npm run types:check`: checks for **type errors** in the code.

Mock tools:

- **MSW**: https://github.com/mswjs/msw
- **Zimic**: https://github.com/zimicjs/zimic/wiki

## 3. Google Maps Places API

- OpenAPI Documentation:
  - Current version:
    [`openapi.yaml`](https://gist.githubusercontent.com/diego-aquino/21b772332f2455a827166ac3b64db052/raw/b9aed7f76a91bf216cee5fb37fe2fd1e0d959c80/google-maps-places-api-current.openapi.yaml)
    ([View in Swagger UI](https://editor-next.swagger.io/?url=https://gist.githubusercontent.com/diego-aquino/21b772332f2455a827166ac3b64db052/raw/b9aed7f76a91bf216cee5fb37fe2fd1e0d959c80/google-maps-places-api-current.openapi.yaml))
  - New version:
    [`openapi.yaml`](https://gist.githubusercontent.com/diego-aquino/a0554434e8ac73ece2f5d787727b227f/raw/b9a8cac11b2f186130ba72379d52ba142ba4a2f7/google-maps-places-api-new.openapi.yaml)
    ([View in Swagger UI](https://editor-next.swagger.io/?url=https://gist.githubusercontent.com/diego-aquino/a0554434e8ac73ece2f5d787727b227f/raw/b9a8cac11b2f186130ba72379d52ba142ba4a2f7/google-maps-places-api-new.openapi.yaml))

### 3.1. Query Autocomplete

- [Documentation](https://developers.google.com/maps/documentation/places/web-service/query)
  - [Status codes](https://developers.google.com/maps/documentation/places/web-service/query#PlacesAutocompleteStatus)

Request examples:

- Success
  ```bash
  npm run example current success
  ```
- Error
  ```bash
  npm run example current error
  ```

### 3.2. Autocomplete (New)

- [Documentation](https://developers.google.com/maps/documentation/places/web-service/place-autocomplete)
- [Migration guide](https://developers.google.com/maps/documentation/places/web-service/migrate-autocomplete)

Request examples:

- Success
  ```bash
  npm run example new success
  ```
- Error
  ```bash
  npm run example new error
  ```
