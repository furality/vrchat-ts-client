# vrchat-ts-client

An ESM TypeScript client for the VRChat API, published to GH Packages as `@furality/vrchat-ts-client`.

The client is generated from the community-maintained [VRChat OpenAPI specification](https://github.com/vrchatapi/specification)
on a nightly schedule and published from CI.

## Versioning

The package version comes from `info.version` in the upstream OpenAPI spec. There is no independent
versioning of this repo — `@furality/vrchat-ts-client@1.2.3` means "generated from VRChat spec
1.2.3". Changes to this repo's workflows do not produce a release on their own.

## Manual runs

Trigger the `release` workflow from the Actions tab with two optional inputs:

- **`snapshot`** — appends a `-SNAPSHOT.<timestamp>` suffix to the version and forces the publish
  job to run even when the version is unchanged. Use this to get a build out for testing without
  waiting on upstream.
- **`spec`** — a URL to an alternate OpenAPI spec, for testing against a fork or an unreleased
  branch of the specification.
