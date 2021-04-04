# Contributing

## Introduction

Thank you for considering to contribute to Conquest Eternal's Community Directory!

Whether you want to report a bug, request a feature or contribute new resources or code, we appreciate your effort and will do our best to incorporate them into the project.

Please understand that some of your contributions might not align with our
vision for the project, which means we may reject some of your issues or pull request. When in doubt, we recommend opening an issue first in order to discuss your ideas with the maintainers, before starting to implement your changes.

### Code of Conduct

Please adhere to our [Code of Conduct](CODE_OF_CONDUCT.md) during your
interactions with this project's maintainers and community. This helps maintain a friendly and tolerant environment that everyone enjoys being a part of.

## Pull Requests

If you'd like to contribute to the project, follow these steps:

0. Make sure your change will be accepted. This may mean opening an issue to discuss your desired changes first.
1. Fork and clone the project. 
2. Start making changes! See below for some guidance.
3. Once you are ready to open your PR: Commit and push the changes to your fork, and then open a new pull request in this project's GitHub UI.
   - Please exclude potential build or install artifacts (such as `yarn.lock` or log files) from the changeset.
4. Wait for the maintainers to review your pull request. We usually require at least two approving reviews in order to merge a PR.
   - You might be asked to make additional changes, if so you can simply create a new commit and push it to the same branch you used to open the PR in the first place.

### Adding a new resource

Please use the following schema:
```js
[
  {
    "title": String, // Start with uppercase
    "slug": String, // All lowercase, eg: "/category"
    "resources": [
      {
        "title": String,
        "url": String, // See below for notes about correct format of URLs
      }
    ]
  }
]
```

We have a `<category>.json` file for each category, you can add your suggested resource by adding it to the `resources` array in the JSON file using the schema as described above. Please include all
the keys enlisted (`title`, `url`).

For URLs, please consider the following:
- Do not link to language specific pages (e.g. don't link to
  `<url>.org/en-US/docs`, instead, link to `<url>/docs` if possible).
- Do not use `'&'` as it will break the URL referencing.
- We won't allow referral links.

To add a completely new resource, add a `<category>.json` file. Make sure it follows the sceme as described above.