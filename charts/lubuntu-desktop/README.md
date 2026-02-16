# lubuntu-desktop

Lubuntu desktop service for Onyxia, exposed only through VNC (port 5901) and intended to be used from Apache Guacamole.

## Guacamole connection

Create a VNC connection with:

- Hostname: `<release-name>` (Kubernetes service name)
- Port: `5901`
- Password: `vncpasswd`

If Guacamole is in another namespace, use `<release-name>.<namespace>.svc.cluster.local`.
