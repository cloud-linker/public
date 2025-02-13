# list

### Description

The `clctl backbone list` command allows you to list all your **Backbones**.

***

### Usage

```bash
clctl backbone list
```

#### Output

```bash
ID                              NAME            STATUS          CLOUD PROVIDER  REGION          NETWORK CIDR    SUBNETS                                                                           
67adb053de6a6b52a51af585        production      available       google          us-east1        10.0.0.0/8      projects/fleet-passage-448607-v6/regions/us-east1/subnetworks/subnet-choice-whale
                                                                                                                10.1.0.0/16                                                                      
                                                                                                                projects/fleet-passage-448607-v6/regions/us-east1/subnetworks/subnet-polite-elk  
                                                                                                                10.2.0.0/16// Some code
```

