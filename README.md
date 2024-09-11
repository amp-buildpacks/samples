# Amphitheatre Buildpacks Sample Applications

A collection of sample applications that can be built using Amphitheatre Buildpacks.

## Prerequisites

1. Clone this repository: `git clone https://github.com/amp-buildpacks/samples`
1. [Pack](https://buildpacks.io/docs/install-pack/)

## Adding New Samples

* If the app is a part of an existing language family:
  * Add app to the appropriate language family in its own subdirectory.
  * Add a test context to the *_test.go file in the language family directory.
* If the app is a part of a new language family:
  * Create a new directory for the language family.
  * Create a new test file <language_family_name>/*_test.go containing a new
    test suite.
  * Be mindful of which builders the app is compatible with and set up test
    suites accordingly.
  * Run `./scripts/generate-test-workflow.sh -l <language_family_name>` to
    generate a Github Actions workflow that runs the tests.
* Update README.md.

## Samples

### Cairo

- [Starknet](/cairo/starknet)

### Leo

- [snarkVM](/leo/snarkvm)

### Move

- [Sui](/move/sui)
- [Aptos](/move/aptos)

### Rust

- [Solana (Native)](/rust/solana)

### Solidity

- [Hardhat](/solidity/hardhat)
- [Foundry](/solidity/foundry)

### Sway

- [Fuel](/sway/fuel)

## Testing Samples

To run integration tests that `pack build` each of the sample apps, use
`scripts/smoke.sh`. See `scripts/smoke.sh -h` for usage information.

For example, to run tests for the Move and Solidity samples with the Paketo tiny
and base builders, run:
```
./smoke.sh --builder paketobuildpacks/builder-jammy-tiny:latest \
           --builder paketobuildpacks/builder-jammy-base:latest \
           --suite move \
           --suite solidity
```

## Buildpacks Development Resources

### External Buildpacks:

- https://elements.heroku.com/buildpacks
- https://github.com/GoogleCloudPlatform/buildpacks
- https://github.com/paketo-buildpacks
- https://github.com/paketo-community

### Documentation

- [Buildpacks.io](https://buildpacks.io/) Cloud Native Buildpack website
- Buildpack Author Guide https://buildpacks.io/docs/buildpack-author-guide
- [CNB Tutorial](https://buildpacks.io/docs/app-journey/) Tutorial to get you
  started using pack, a builder, and your application to create a working OCI
  image.
- [Buildpack & Platform Specification](https://github.com/buildpacks/spec)
  Detailed definition of the interaction between a platform, a lifecycle, Cloud
  Native Buildpacks, and an application.
- [How to Build Go Apps with Paketo
  Buildpacks](https://paketo.io/docs/howto/go/) How to use the Paketo Go
  Buildpack(opens in a new tab) to build applications for several common
  use-cases.

### Examples & Samples

- https://github.com/buildpacks/samples
- https://github.com/paketo-buildpacks/samples


### Framework & Library

- [libcnb](https://github.com/buildpacks/libcnb) A non-opinionated language
  binding for the Cloud Native Buildpack Buildpack and Extension specifications
- [libpak](https://github.com/paketo-buildpacks/libpak) An opinionated extension
  to the libcnb Cloud Native Buildpack Library
- [packit](https://github.com/paketo-buildpacks/packit) Buildpacks Utils Library
- [libpak-tools](https://github.com/paketo-buildpacks/libpak-tools) A set of
  tools for managing, building and packaging libpak based buildpacks
- [libbs](https://github.com/paketo-buildpacks/libbs) A library that forms the
  basis for building the different Paketo-style build system-providing
  buildpacks

### Reference buildpacks

- A Cloud Native Buildpack for Go https://github.com/paketo-buildpacks/go
- Rust Cloud Native Buildpack https://github.com/paketo-community/rust
- A Cloud Native Buildpack for Cargo (Rust) https://github.com/paketo-community/cargo

### Tools

- https://github.com/buildpacks/github-actions
- https://buildpacks.io/docs/tools/

## Contributing

If anything feels off, or if you feel that some functionality is missing, please
check out the [contributing
page](https://docs.amphitheatre.app/contributing/). There you will find
instructions for sharing your feedback, building the tool locally, and
submitting pull requests to the project.

## License

Copyright (c) The Amphitheatre Authors. All rights reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

      https://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## Credits

Heavily inspired by

- https://github.com/buildpacks/samples
- https://github.com/paketo-buildpacks/samples
