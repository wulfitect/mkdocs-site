# Troubleshooting VXLAN-EVPN Deployments

This section provides guidance for diagnosing and resolving common issues.

## Common Issues

=== "**NVE Interface Down:**" 
    1. Verify source interface (loopback) configuration.
    2. Check IP reachability in the underlay network.

=== "**BGP EVPN Route Absence:**" 
    1. Ensure proper BGP neighbor relationships.
    2. Confirm EVPN address-family configuration.

=== "**VXLAN Tunnel Issues:**" 
    1. Validate VNI mappings on both sides.
    2. Check for MTU mismatches and encapsulation errors.

## Diagnostic Commands

### Cisco

```bash
show nve peers
show nve vni
show bgp l2vpn evpn summary
```