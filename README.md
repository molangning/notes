# Notes repo 

A very simple list of commands/information that helped me a lot in pentesting.

[stabilize-shell.md](stabilize-shell.md) contain information on stabilizing reverse shell

## Cloudflare fronting for detecting ip

We can abuse cloudflare's `trace` to get the external ip. Useful for when we need to evade ioc detection.

https://<YOUR_DOMAIN>/cdn-cgi/trace

Response will be in this format `KEY=VALUE`. We are only interested in the key `ip`'s value
