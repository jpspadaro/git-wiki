# SSH

## SSH VPN Syntax

` sudo ssh -w 0:0 1.2.3.4`

From man page:
```
-w
local_tun[:remote_tun]
Requests tunnel device forwarding with the specified tun(4) devices between the client (local_tun) and the server (remote_tun).

The devices may be specified by numerical ID or the keyword ''any'', which uses the next available tunnel device. If remote_tun is not specified, it defaults to ''any''. See also the Tunnel and TunnelDevice directives in ssh_config(5). If the Tunnel directive is unset, it is set to the default tunnel mode, which is ''point-to-point''. 
```

[More detailed, from Arch wiki.](https://wiki.archlinux.org/index.php/VPN_over_SSH)
