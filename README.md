# RootlessRouter

This is a WIP project called "Rootless Router". 

It can establish multiple wireguard sessions with other DN42 players, but all the stacks can run as a normal user without root / in an unprivileged docker container.
This program receives `wireguard encrypted udp packet` -> `decrypt it` -> `do bgp routing` -> `encrypt` -> `send to another peer`, all processes are done in the userspace.

The host OS can only see this app receives and sends udp packets, but doesn't know it established multiple BGP sessions to other people and routing for it.

Based on my current plan, the software stack of my nodes looks like this:
![Node](https://raw.githubusercontent.com/KusakabeSi/RootlessRouter/main/pics/Node.png)

As you can see, there are no componient are running in the kernel. 

I will host multiple node to form a cluster, like this
![Node](https://raw.githubusercontent.com/KusakabeSi/RootlessRouter/main/pics/Overview.png)

There are some my projects are related to this project:

1. https://github.com/KusakabeSi/EtherGuard-VPN
1. https://github.com/KusakabeSi/wireguard-go-vpp
1. https://github.com/KusakabeSi/DN42-AutoPeer-vpp
1. https://github.com/KusakabeSi/bird-vpp-route-syncer
1. https://github.com/KusakabeSi/bird-lg-go
1. https://github.com/KusakabeSi/vpp
1. https://github.com/KusakabeSi/BIRD-vpp
1. https://github.com/KusakabeSi/RootlessRouterDocker
1. https://github.com/KusakabeSi/RootlessRouter
1. https://github.com/KusakabeSi/RRstate
