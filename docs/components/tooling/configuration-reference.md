# Configuration reference

### Overview

All tools installed by CloudLinker follow a common configuration structure. This ensures a standardized deployment process while allowing flexibility for specific tool settings.

Each tool requires a JSON configuration file with the following base structure:

```
{
    "name": "signoz",
    "cluster_id": "67b2fa756e01faed8f380656",
    "chart_id": "67b3523e11bc3500027b49eb",
    "chart_version": "latest",
    "enabled": true,
    "config": {
        <TOOL_SPECIFIC_CONFIG>
    }
}
```

### Configuration Fields

| Field           | Type    | Description                                                                |
| --------------- | ------- | -------------------------------------------------------------------------- |
| `name`          | string  | The name of the tool being installed.                                      |
| `cluster_id`    | string  | The ID of the Kubernetes cluster where the tool will be deployed.          |
| `chart_id`      | string  | The ID of the tool to be installed.                                        |
| `chart_version` | string  | The version of the tool to install (e.g., `latest` or a specific version). |
| `enabled`       | boolean | Determines whether the tool is enabled or disabled.                        |
| `config`        | object  | Tool-specific configuration settings (varies per tool).                    |

### Tool-Specific Configuration

The `config` field is highly flexible and varies depending on the tool being installed. Each tool may require different parameters to be set within this field. Refer to individual tool documentation for detailed configuration options.

### Example Configurations

#### Example 1: SigNoz

```
{
    "name": "signoz",
    "cluster_id": "67b2fa756e01faed8f380656",
    "chart_id": "67b3523e11bc3500027b49eb",
    "chart_version": "latest",
    "enabled": true,
    "config": {
        "domain_id": "67b3513411bc3500027b49ea"
    }
}
```

#### Example 2: NGINX Ingress Controller

```
{
    "name": "nginx-ingress",
    "cluster_id": "67b2fa756e01faed8f380656",
    "chart_id": "67b3abcde11bc3500027b123",
    "chart_version": "1.2.3",
    "enabled": true,
    "config": {
        "public": true
    }
}
```

### Notes

* The `config` object will have different fields based on the tool being deployed.
* Ensure that required fields for each tool are correctly set to avoid installation issues.
* Future updates may introduce additional parameters, so always check the latest documentation.
