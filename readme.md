# Lab details for London Hyperfabric switches

There are two pairs of switches in the field lab; 2x Sirens and 2x Caribs. The hardware is physically located in racks L09 and L16 in the London data center. 

The switches are cabled to allow for multiple topologies:

- leaf only
- full mesh
- spine/leaf

Details can be found in the [/images](/images/) directory, along with connectivity details to the lab core. 

Each Hyperfabric environment has a unique AS along with lab local subnets from the 10.2.0.0/16 range. Workloads on the lab local subnets can access the internet via the lab NAT gateway. Both Hyperfabric environments attach directly to the lab core ![lab core](images/lab-core.png)

Each Hyperfabric also rack has 3x (very) old C series servers attached to the Siren switches. 

### Rack L09: AS65109

[Rack-l09 details](/images/hyperfabric-l09/rack-layout.png)

- 10.2.1.0/24
- 10.2.2.0/24
- 10.2.3.0/24
- 10.2.4.0/24
- 10.2.5.0/24
- etc

### Rack L16: AS65116

[Rack-l16 details](/images/hyperfabric-l16/rack-layout.png)

- 10.2.101.0/24
- 10.2.102.0/24
- 10.2.103.0/24
- 10.2.104.0/24
- 10.2.105.0/24
- etc


### ACI connectivity

Both Hyperfabric racks are also attached to the aci-dev-01 fabric. This is still being commissioned, however it **should** be cabled as follows:

- L09 FDO283909CB eth 1/62 - aci-dev-01 leaf 1101 eth 1/17
- L09 FDO283909CH eth 1/62 - aci-dev-01 leaf 1102 eth 1/17
- L16 FDO283909DB eth 1/62 - aci-dev-01 leaf 2101 eth 1/17
- L16 FDO283909D8 eth 1/62 - aci-dev-01 leaf 2102 eth 1/17
