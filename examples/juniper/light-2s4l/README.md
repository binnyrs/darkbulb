
This example adopts the topology with 2 Spines and 4 Leafs instances of VQFX (light).
All VQFX have peer-to-peer network interface connectivity, allowing both L2 and L3.

```

[SPINE]
SPINE01:
  E0: VAGRANT-MGMT
  E1: LEAF01-E1
  E2: LEAF02-E1
  E3: LEAF03-E1
  E4: LEAF04-E1

SPINE02:
  E0: VAGRANT-MGMT
  E1: LEAF01-E2
  E2: LEAF02-E2
  E3: LEAF03-E2
  E4: LEAF04-E2

[LEAF]
LEAF01:
  E0: VAGRANT-MGMT
  E1: SPINE01-E1
  E2: SPINE02-E1
  E3: SRV01-E1
  E4: LEAF02-E4

LEAF02:
  E0: VAGRANT-MGMT
  E1: SPINE01-E2
  E2: SPINE02-E2
  E3: SRV01-E2
  E4: LEAF01-E4

LEAF03:
  E0: VAGRANT-MGMT
  E1: SPINE01-E3
  E2: SPINE02-E3
  E3: SRV02-E1
  E4: LEAF04-E4

LEAF04:
  E0: VAGRANT-MGMT
  E1: SPINE01-E4
  E2: SPINE02-E4
  E3: SRV02-E2
  E4: LEAF03-E4

```
