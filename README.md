# Containerlab collectors test

This containerlab was forked from [this example](https://github.com/karimra/gnmic/tree/main/examples/deployments/1.single-instance/4.prometheus-output) in order to play with gnmic and Telegraf collectors.

## How to start me

1. install containerlab
2. stand up the lab instance

`sudo containerlab deploy --topo prometheus.clab.yml`

On the first run the telegraf container will always fail as it won't be able to mount the certificates since they're created on the first run. So a reboot of the lab is needed:

`sudo containerlab destroy --topo prometheus.clab.yml`

`sudo containerlab deploy --topo prometheus.clab.yml`