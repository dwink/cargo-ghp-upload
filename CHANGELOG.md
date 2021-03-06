# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.3.4]

- Fixed #34: If the remote gh-pages branch is updated between executions,
             ghp-upload will now pull the changes instead of overwriting them

## [0.3.3] [YANKED]

Published a stubbed out `main()` accidentally

## [0.3.2]

- Tag builds now publish to `/[tag]/` instead of `/HEAD/`

## [0.3.1]

- Fixed builds when `./target/ghp` does not exists and the target repo has a GHP branch

## [0.3.0] [YANKED]

- Fixed builds on Travis always being picked up as a tag build instead of a branch build
- Added `--publish-tags` to publish docs for tags (GitHub releases)

## [0.2.0] [YANKED]

- Change CLI syntax so that it works as a subcommand (yanked broken 0.1)

## [0.1.1] [YANKED]

- Removed package.include key from Cargo.toml so more things are in the cargo package
- Improvements to CI

## [0.1.0] [YANKED]

- Split out of [roblabla/cargo-travis](https://github.com/roblabla/cargo-travis)
  - Includes rename from `cargo-doc-upload` to `cargo-ghp-upload`
  - Call as `cargo ghp-upload [FLAGS] [OPTIONS]`
- No longer links against `cargo`
- CLI changes:
  - New repeatable `-v`/`--verbose` flag for more logging (modulo #1)
  - New `--remove-index` flag to opt-out of maintaining `index.html`
    (It will still be clobbered if an index.html exists in the uploaded folder)
  - New `--directory <upload_directory>` option to upload from directories other than `./target/doc`
- Now can infer much more context from Git if not in Travis-like environment
- Default commit message changed

  [Unreleased]: https://github.com/crate-ci/cargo-ghp-upload/compare/0.3.4...master
  [0.3.4]: https://github.com/crate-ci/cargo-ghp-upload/compare/0.3.2...0.3.4
  [0.3.2]: https://github.com/crate-ci/cargo-ghp-upload/compare/0.3.1...0.3.2
  [0.3.1]: https://github.com/crate-ci/cargo-ghp-upload/compare/0.3.0...0.3.1
  [0.3.0]: https://github.com/crate-ci/cargo-ghp-upload/compare/0.2.0...0.3.0
  [0.2.0]: https://github.com/crate-ci/cargo-ghp-upload/compare/0.1.1...0.2.0
  [0.1.1]: https://github.com/crate-ci/cargo-ghp-upload/compare/0.1.0...0.1.1
  [0.1.0]: https://github.com/crate-ci/cargo-ghp-upload/tree/0.1.0
