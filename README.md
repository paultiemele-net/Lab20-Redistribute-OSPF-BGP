# Lab20-Redistribute-OSPF-BGP
This repository contains an advanced Cisco networking lab demonstrating OSPF and BGP redistribution across multiple Autonomous Systems, combined with a GRE tunnel to enable end-to-end connectivity between distant LANs.
The internal network (AS 100) runs OSPF and represents a private enterprise infrastructure, while the external network (AS 200) runs BGP and simulates an ISP backbone using iBGP with Route Reflectors and eBGP peering.

A GRE tunnel is established between Router1 and Router8, allowing hosts located in different autonomous systems to communicate securely over a logical point-to-point link. Mutual route redistribution between OSPF and BGP ensures full reachability across the entire topology.

Key Learning Objectives

OSPF multi-router deployment in a single area (Area 0)

eBGP and iBGP configuration across multiple routers

Route Reflector design to scale iBGP

OSPF ↔ BGP route redistribution

Default route injection into OSPF

GRE tunnel configuration for site-to-site connectivity

End-to-end connectivity testing using ICMP (ping)

Real-world ISP and enterprise network design principles

Topology Overview

AS 100 (Enterprise / Internal Network)
Routers R1–R4 running OSPF

AS 200 (ISP / External Network)
Routers R5–R8 running BGP with Route Reflectors

Tunnel Network
GRE tunnel: 11.11.11.0/24

LANs

PC1: 10.10.10.0/24

PC2: 100.100.100.0/24

Validation

Connectivity is validated by:

Verifying OSPF and BGP routing tables

Ensuring successful GRE tunnel establishment

Performing ICMP ping tests between PC1 and PC2
