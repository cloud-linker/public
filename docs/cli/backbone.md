# Backbone

### Description

The `clctl backbone` command group allows you to manage **Backbones**, which serves as the foundation for deploying private Kubernetes clusters. Each Backbone includes network and VPN configurations.

### Prerequisites

Ensure that your configuration file includes at least one VPN provider and one cloud provider from the supported list.

***

### Usage

```
clctl backbone <command> 
clctl backbone <command>
```

#### Example commands

```
clctl backbone create --config gcp-backbone.json
clctl backbone create -c gcp-backbone.json
```

### Backbone Configuration File

The configuration must be provided in JSON format. Below is an example of a **GCP Backbone configuration file**:

```
{
    "name": "production",
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

You can find the list of supported providers [here](../components/providers/).

### Command Behavior

* **Validation:** No validation checks (e.g., CIDR range overlap) are enforced yet. Ensure your network configuration is correct before deploying.

### Notes

* VPN integration is required for every Backbone.
* Each Backbone must have at least one **subnet** defined within the `vpc` section to install the VPN.

### Next Steps

* To create a new backbone, refer to the [create.md](backbone/create.md "mention") command reference
* To list all backbones, use `clctl backbone list`.
* To modify an existing backbone, use `clctl backbone edit`.
