# SDK Development

:warning: **status**: draft

## Introduction

The SDKs for NEM2, aka Catapult, have a set of desired properties cross languages like:

- **Provide an abstraction layer of NEM2** handling the underlying complexity and providing an easy to use SDK.
- **Reduce code duplication** of NEM2 Libraries and Applications.
- **Shared design cross languages** enabling code portability from one platform to another faster and shared knowledge between NEM Developers
- **Be Lightweight**, focusing on the minimum features required to develop in NEM2.

In order to accomplish those properties, we share this guideline to help NEM Developer Community that wants to collaborate to match the best quality with the less effort in a collaborative way.

Remember to join our slack! Click [here][slack-invitation] to get an invitation.

## Starting point, being familiar with the current nem2-sdk & API

In case you haven't used nem2-sdk or Catapult in general, we encourage you to:

1. Review the technical documentation to become familiar with the concepts at https://nemtech.github.io/ .
2. Setup the [catapult in local environment via docker][docker] or enroll the [beta program][beta-program] to access a Catapult Test Net without need to run it yourself.
3. [Check the API reference][api-ref] and play with the API endpoints.
4. Become familiar with the current [nem2-sdk via code examples][sdk-guide] & [nem2-cli][cli].

## Architecture

![sdk architecture](sdk-development-assets/sdk-architecture.png)

## Development

There are two SDKs that can be used as guide, the [TypeScript][sdk-ts] & [Java][sdk-java] SDKs. The TypeScript version is the first SDK getting the latest updated, meanwhile Java takes longer to be updated. Unfortunately, TypeScript version has one specific implementation detail, the low level implementation is separated from the SDK, called [nem2-library-js][library-js]. The reason is due to the need of low level library to perform specific chain testing, **the other SDKs don't need the low level implementation be separated in another component**, so, similar to Java, it's included in the same SDK.

### API Wrapper

TODO

### Transaction Serialization

TODO

### KeyPair and Cryptographic functions

TODO

### Abstract Models

TODO

### Exposing API via Observables

TODO

## Pushing the code for review

TODO

## Publishing the SDK as official

TODO

[sdk-ts]: https://github.com/nemtech/nem2-sdk-typescript-javascript
[sdk-java]: https://github.com/nemtech/nem2-sdk-java
[sdk-guide]: https://nemtech.github.io/guides/overview.html
[cli]: https://nemtech.github.io/cli/overview.html
[library-js]: https://github.com/nemtech/nem2-library-js
[api-ref]: https://nemtech.github.io/api/overview.html#reference-tools
[docker]: https://github.com/tech-bureau/catapult-service-bootstrap
[beta-program]: http://mijin.io/en/catapult
[slack-invitation]: https://join.slack.com/t/nem2/shared_invite/enQtMzY4MDc2NTg0ODgyLTFhZjgxM2NhYTQ1MTY1Mjk0ZDE2ZTJlYzUxYWYxYmJlYjAyY2EwNGM5NzgxMjM4MGEzMDc5ZDIwYTgzZjgyODM