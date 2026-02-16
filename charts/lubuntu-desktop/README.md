# lubuntu-desktop

Lightweight Lubuntu desktop service for Onyxia, intended to be reachable from Apache Guacamole through VNC.

## Quick Guacamole Setup

Create a VNC connection in Guacamole with:

- Hostname: `<release-name>` (Kubernetes service name)
- Port: `5901` (default)
- Password: `lubuntu.vncPassword`

When both services are in the same namespace, Guacamole can resolve the service name directly.
