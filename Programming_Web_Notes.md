- [Deep Dive: Same-Origin Policy](#deep-dive-same-origin-policy)
  - [Origin Components](#origin-components)
  - [Examples](#examples)
  - [Why Subdomains Differ](#why-subdomains-differ)
  - [Relaxing SOP for Subdomains](#relaxing-sop-for-subdomains)
  - [Security Implications](#security-implications)
# Deep Dive: Same-Origin Policy
The Same-Origin Policy (SOP) is a browser security concept that restricts how documents or scripts loaded from one “origin” can interact with resources from another. An origin is defined by three parts:
1. Scheme (protocol): http vs https
2. Host (domain and subdomain)
3. Port number

Two URLs share an origin only if ***all three*** parts match exactly.
## Origin Components
- Scheme: https://example.com is not the same as http://example.com.
- Host: siteA.com ≠ sub.siteA.com. Any difference in subdomain makes it a new origin.
- Port: https://example.com:443 is the default for HTTPS, but https://example.com:8443 is a different origin.

## Examples
| URL A                  | URL B                        | Same Origin? |
|------------------------|------------------------------|--------------|
| https://siteA.com      | https://siteA.com            | Yes          |
| https://siteA.com      | https://subdomain.siteA.com  | No           |
| https://siteA.com      | http://siteA.com             | No           |
| https://siteA.com      | https://siteA.com:8443       | No           |
| https://blog.siteA.com | https://shop.siteA.com       | No           |
| http://localhost:8080  | http://localhost:8080        | Yes          |

## Why Subdomains Differ
Browsers treat siteA.com and subdomain.siteA.com as distinct hosts. Even though they share a parent domain, SOP prevents a script on siteA.com from reading or modifying pages on subdomain.siteA.com without explicit relaxation, because the host strings differ.

## Relaxing SOP for Subdomains
You can sometimes relax SOP across subdomains by setting the JavaScript property:
js
```shell
// Both sides must set this
document.domain = "siteA.com";
```
This makes siteA.com and sub.siteA.com share an origin—only if both documents explicitly set document.domain to the same parent domain.

## Security Implications
- Prevents malicious sites from reading sensitive data on other origins.
- Stops unauthorized cross-site requests and attacks like XSS or CSRF (when combined with cookies).
- Requires explicit CORS headers or document.domain adjustments to allow controlled cross-origin access.

With this understanding, you can reason about when two pages can freely communicate in the browser and when you must use mechanisms like CORS, postMessage, or document.domain workarounds.
