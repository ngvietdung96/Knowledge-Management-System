Tags: #SecondBrain 
Status: #open, #unprocessed
Related: [[Home Server]], [[Open Source]], [[VPN]]

---

### How tailscale works 
- https://tailscale.com/blog/how-tailscale-works

### Is Tailscale Open source?
QA: https://tailscale.com/opensource
Mostly. Tailscale daemon client code is open source. Where the operating system is open source, the daemon and GUI are open source, and where the operating system is closed, the daemon is open source and the GUI is closed source.

Tailscale’s DERP server code is also open source. This lets you verify and build these components yourself. "Tailscale’s coordination server is closed source". If you want to run your own coordination server at home, check out [Headscale](https://github.com/juanfont/headscale).


Github of tailscale (Only Client):
- https://github.com/tailscale/tailscale
Server Host Open source (working with tailscale client)
- [Headscale](https://github.com/juanfont/headscale) is an open source coordination server for Tailscale clients. It is independent from Tailscale.
## Exit node:
- https://tech.stonecharioteer.com/posts/2026/tailscale-exit-nodes/

## Device connection:
https://tailscale.com/docs/reference/device-connectivity



## DERP servers:
https://tailscale.com/docs/reference/derp-servers

## Peer relays
https://tailscale.com/blog/peer-relays-international-networks

---
# References
Official website:
Wikipedia:
Youtube: