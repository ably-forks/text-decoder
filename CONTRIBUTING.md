# Contributing to ably/text-decoder

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Ensure you have added suitable tests and the test suite is passing (`npm test`)
5. Push the branch (`git push origin my-new-feature`)
6. Create a new Pull Request

## Release Process

1. Make sure the tests are passing in CI for the branch you're building
2. Create a new branch for the release, for example `release/1.2.3`
3. Update the `CHANGELOG.md` with any customer-affecting changes since the last release and add this to the git index
4. Run `npm version <VERSION_NUMBER> --no-git-tag-version` with the new version and add the changes to the git index
5. Create a PR for the release branch
6. Once the release PR is landed to the `main` branch, checkout the `main` branch locally (remember to pull the remote changes)
7. Run `git tag <VERSION_NUMBER>` with the new version and push the tag to GitHub with `git push <REMOTE> <VERSION_NUMBER>` (usually `git push origin <VERSION_NUMBER>`)
8. Run `npm publish .` (should require OTP) - publishes to npm
9. Visit https://github.com/ably-forks/text-decoder/tags and create a GitHub release based on the new tag (for release notes, you can copy the notes you added to the CHANGELOG)

## Building the library

To build the library, run:

    npm run build

## Test suite

To run the tests:

    npm test

To run tests in watch mode:

    npm run test:watch

## Formatting / linting

Run the following command to fix linting issues:

    npm run lint:fix