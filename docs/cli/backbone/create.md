# create

### Description

The `clctl backbone create` command allows you to create a new **Backbone**, which serves as the foundation for deploying private Kubernetes clusters. Each Backbone includes network and VPN configurations.

### Prerequisites

Ensure that your configuration file is valid and follow the [configuration reference](configuration-reference.md)

***

### Usage

```
clctl backbone create -c <config_file> 
clctl backbone create --config <config_file>
```

#### Required Arguments

| Argument                     | Description                                                |
| ---------------------------- | ---------------------------------------------------------- |
| `--config, -c <config-file>` | Path to a JSON file containing the Backbone configuration. |

#### Example

```
clctl backbone create --config gcp-backbone.json
clctl backbone create -c gcp-backbone.json
```

### Backbone Configuration File

The configuration must be provided in JSON format. Below is an example of a **GCP Backbone configuration file**:

```
{
    "name": "dev",
    "provider": "google",
    "twingate_provider_name": "demo-account",
    "google_provider_name": "demo-account",
    "network_config": {
        "region": "us-east1",
        "zone": "us-east1-a",
        "vpc": {
            "cidr": "10.0.0.0/8",
            "subnets": [
                {
                    "cidr": "10.1.0.0/16"
                }
            ]
        }
    }
}
```

### Supported Providers

You can find the list of supported providers [here](../../components/providers/).

### Command Behavior

* **Validation:** No validation checks (e.g., CIDR range overlap) are enforced yet. Ensure your network configuration is correct before deploying.

### Notes

* VPN integration is required for every Backbone.
* Each Backbone must have at least one **subnet** defined within the `vpc` section to install the VPN.

### Next Steps

* To list all backbones, use `clctl backbone list`.
* To modify an existing backbone, use `clctl backbone edit`.
