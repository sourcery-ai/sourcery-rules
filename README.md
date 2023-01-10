# Sourcery Rules

This repo contains public rules definitions for Sourcery
[optional rules](https://docs.sourcery.ai/Reference/Optional-Rules/).

- Your contributions are welcome! 😃 Open a PR and share your cool rules here.
- The [Sourcery team](https://sourcery.ai/about/) continuously adds new rules as
  well.
- Are you having a problem where a Sourcery rule might be a good solution but
  not sure how? Open an issue here.

## Enabling Optional Sourcery Rules

The rules in this repository are bundled with each Sourcery release. You can use
them in the
[`review` command of the Sourcery CLI](https://docs.sourcery.ai/Reference/Command-Line/review/)
and add them to
[your project's configuration](https://docs.sourcery.ai/Reference/Configuration/sourcery-yaml/).

### Configure Sourcery to Use Optional Rules

You can use the `enable` configuration option in
[your project's configuration file](https://docs.sourcery.ai/Reference/Configuration/sourcery-yaml/),
to enable a rule or a tag.

In your project's `.sourcery.yaml` file:

```yaml
rule_settings:
  enable:
    - default  # Continue to enable the default rules enabled
    - gpsg-import
    - gpsg-naming-pep8
    - no-long-functions
```

### Use Optional Rules in the Command Line

You can also run the
[`review` command](https://docs.sourcery.ai/Reference/Command-Line/review/) of
the Sourcery CLI with optional rules using the (`--enable`
option)\[https://docs.sourcery.ai/Reference/Command-Line/review/#-enable\].

This is a great way to experiment when you're considering introducing some
optional rules to your project.

To find out how many issues to Google Python Style Guide would flag:

```sh
sourcery review --enable gpsg .
```

You can also run a subset of the Google Python Style Guide Rules. For example,
if you want to find out which of your modules, classes, and public functions are
missing a docstring:

```sh
sourcery review --enable gpsg-docstrings .
```

You can also run `review` with a single rule:

```sh
sourcery review --enable avoid-global-variables --enable errors-named-error .
```
