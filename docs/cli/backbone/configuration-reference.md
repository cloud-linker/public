# Configuration Reference

### Requirements

| name                  | type     | description                    |
| --------------------- | -------- | ------------------------------ |
| `vpn_provider_name`   | provider | the name of the vpn provider   |
| `cloud_provider_name` | provider | the name of the cloud provider |



### General Configuration

<table data-full-width="true"><thead><tr><th>name</th><th width="130">provider<select><option value="QbsKjGQ1nnT7" label="AWS" color="blue"></option><option value="D0G2ot8cyYFF" label="Azure" color="blue"></option><option value="ahy3dS2wFcyz" label="Google Cloud" color="blue"></option><option value="tQ9Hg09pEom8" label="All" color="blue"></option></select></th><th width="107">type </th><th width="85" data-type="checkbox">required</th><th>description</th></tr></thead><tbody><tr><td><code>name</code></td><td><span data-option="tQ9Hg09pEom8">All</span></td><td><code>string</code></td><td>true</td><td>name of the backbone</td></tr><tr><td><code>provider</code></td><td><span data-option="tQ9Hg09pEom8">All</span></td><td><code>string</code></td><td>true</td><td>provider of the backbone (selected from the provider list)</td></tr><tr><td><code>vpn_provider_name</code></td><td><span data-option="tQ9Hg09pEom8">All</span></td><td><code>string</code></td><td>true</td><td>name of the vpn provider to be connected to the backbone network</td></tr><tr><td><code>cloud_provider_name</code></td><td><span data-option="tQ9Hg09pEom8">All</span></td><td><code>string</code></td><td>true</td><td>name of the cloud provider to deploy the backbone to</td></tr><tr><td><code>region</code></td><td><span data-option="tQ9Hg09pEom8">All</span></td><td><code>string</code></td><td>true</td><td>region of the backbone</td></tr><tr><td><code>zone</code></td><td><span data-option="ahy3dS2wFcyz">Google Cloud</span></td><td><code>string</code></td><td>true</td><td>zone where the vpn connector will be deployed to</td></tr><tr><td><code>network_config</code></td><td><span data-option="tQ9Hg09pEom8">All</span></td><td><a data-mention href="configuration-reference.md#network-config">#network-config</a></td><td>true</td><td>network config of the backbone</td></tr></tbody></table>



### Network Config

<table data-full-width="true"><thead><tr><th>name</th><th width="130">provider<select><option value="QbsKjGQ1nnT7" label="AWS" color="blue"></option><option value="D0G2ot8cyYFF" label="Azure" color="blue"></option><option value="ahy3dS2wFcyz" label="Google Cloud" color="blue"></option><option value="tQ9Hg09pEom8" label="All" color="blue"></option></select></th><th width="107">type </th><th width="85" data-type="checkbox">required</th><th>description</th></tr></thead><tbody><tr><td><code>vpc</code></td><td><span data-option="tQ9Hg09pEom8">All</span></td><td><a data-mention href="configuration-reference.md#network-config">#network-config</a></td><td>true</td><td>the vpc config of the backbone</td></tr></tbody></table>

### VPC Config

<table data-full-width="true"><thead><tr><th>name</th><th width="130">provider<select><option value="QbsKjGQ1nnT7" label="AWS" color="blue"></option><option value="D0G2ot8cyYFF" label="Azure" color="blue"></option><option value="ahy3dS2wFcyz" label="Google Cloud" color="blue"></option><option value="tQ9Hg09pEom8" label="All" color="blue"></option></select></th><th width="178">type </th><th width="85" data-type="checkbox">required</th><th>description</th></tr></thead><tbody><tr><td><code>cidr</code></td><td><span data-option="tQ9Hg09pEom8">All</span></td><td><code>string</code></td><td>true</td><td>cidr range of the vpc<br><em>is is recommended to select a large range, for example, 10.0.0.0/8</em></td></tr><tr><td><code>subnets</code></td><td><span data-option="tQ9Hg09pEom8">All</span></td><td>[]<a data-mention href="configuration-reference.md#subnet-config">#subnet-config</a></td><td>false</td><td>list of the vpc subnets.</td></tr></tbody></table>

### Subnet Config

<table data-full-width="true"><thead><tr><th>name</th><th width="130">provider<select><option value="QbsKjGQ1nnT7" label="AWS" color="blue"></option><option value="D0G2ot8cyYFF" label="Azure" color="blue"></option><option value="ahy3dS2wFcyz" label="Google Cloud" color="blue"></option><option value="tQ9Hg09pEom8" label="All" color="blue"></option></select></th><th width="107">type </th><th width="85" data-type="checkbox">required</th><th>description</th></tr></thead><tbody><tr><td><code>cidr</code></td><td><span data-option="tQ9Hg09pEom8">All</span></td><td><code>string</code></td><td>true</td><td>cidr of the subnet<br><em>must be included insite the</em> <a data-mention href="configuration-reference.md#vpc-config">#vpc-config</a> <em><code>cidr</code> field</em></td></tr></tbody></table>
