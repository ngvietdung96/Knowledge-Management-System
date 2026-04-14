Tags: #SecondBrain 
Status: #open, #unprocessed
Related: [[Home Server]], [[Open Source]], [[Virtual Private Network (VPN)]], [[WireGuard]]

---
## Alternative
- Headscale


## How tailscale works 
- https://tailscale.com/blog/how-tailscale-works
- explain of [[NAT traversal]], NAT hole punching


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

## Subnet router:


## Device connection:
https://tailscale.com/docs/reference/device-connectivity

### Relay peer
- https://tailscale.com/blog/peer-relays-international-networks
- https://tailscale.com/blog/peer-relays-ga


### DERP servers:
https://tailscale.com/docs/reference/derp-servers




## Note

STUN server
derp3g.tailscale.com



---
# References
Official website:
Wikipedia:
Youtube: