# Sourcery Rules

Hello 👋

This repo contains public rules definitions for Sourcery.

## Enabling Sourcery rules

These rules are bundled with each Sourcery release. You can use enable them in
your config file or directly from the command line.

In your project's `.sourcery.yaml` file:

```yaml
rule_settings:
  enable:
    - default  # Continue to enable the default rules enabled
    - rule-id-1
    - tag-1
```

From the command line:

```sh
sourcery review --enable rule-id-1 --enable tag-1 .
```
