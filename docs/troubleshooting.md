# Troubleshooting VXLAN-EVPN Deployments

This section provides guidance for diagnosing and resolving common issues.

## Common Issues

- **NVE Interface Down:** 
  - Verify source interface (loopback) configuration.
  - Check IP reachability in the underlay network.
- **BGP EVPN Route Absence:** 
  - Ensure proper BGP neighbor relationships.
  - Confirm EVPN address-family configuration.
- **VXLAN Tunnel Issues:** 
  - Validate VNI mappings on both sides.
  - Check for MTU mismatches and encapsulation errors.

## Diagnostic Commands

### Cisco

```bash
show nve peers
show nve vni
show bgp l2vpn evpn summary
