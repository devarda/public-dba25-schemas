
# DBA25 Public Schema Repository

This repository contains JSON schemas and examples for standardizing configuration files across the ecosystem. These schemas provide validation, autocompletion, and documentation in development environments.

## Docker Configuration Schema

The Docker configuration schema standardizes container definitions for the ecosystem, ensuring consistent container setup and operation across projects.

### Usage with VS Code

To use these schemas in VS Code:

1. Add the following to your VS Code settings.json file:

```json
"json.schemas": [
  {
    "fileMatch": [
      "**/docker-*/docker-config.json"
    ],
    "url": "https://raw.githubusercontent.com/devarda/public-dba25-schemas/master/docker/docker-config.schema.json"
  }
]
```

2. Or directly reference the schema in your configuration files:

```json
{
  "$schema": "https://raw.githubusercontent.com/devarda/public-dba25-schemas/master/docker/docker-config.schema.json",
  // rest of your configuration
}
```

### Schema Structure

The Docker configuration schema defines:

- Container metadata and type
- Network configuration
- Port mappings
- Volume mounts
- Environment variables
- Container capabilities (e.g., backup, restore, shell)
- Health checks
- Startup options

See examples in the `docker/examples/` directory for implementation details.

## Examples

This repository includes example configurations for:

- MongoDB container
- Redis container

Each example shows proper schema usage and includes common configuration patterns.

## Contributing

To contribute to these schemas, please submit a pull request with your proposed changes.
