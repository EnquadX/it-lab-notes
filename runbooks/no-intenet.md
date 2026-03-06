# Runbook: No Internet / No Connectivity

## Symptoms
- Example: “Wi-Fi connected but no internet”
- Example: “Can’t reach websites”

## Quick Questions (What changed?)
- Did this work earlier today?
- Is it one device or everyone?
- Wired or Wi-Fi?
- Any VPN enabled?
- Any recent changes (router, updates, DNS settings)?

## Checks in order (do not skip)
1) Physical / link
- Wi-Fi connected? Ethernet link light?
- Airplane mode off?

2) IP configuration
- Windows: ipconfig /all
- Linux: ip a
- Do we have an IP address? (not 169.254.x.x)

3) Gateway reachability
- Ping default gateway
- Windows: ping <gateway>
- Linux: ping <gateway>

4) DNS test
- Windows: nslookup google.com
- Linux: dig google.com
- If DNS fails, test ping 1.1.1.1 to isolate DNS vs full outage

5) External reachability
- ping 1.1.1.1
- tracert/traceroute to confirm path

## Likely causes
- No DHCP lease / wrong IP
- Wrong gateway
- DNS misconfigured
- VPN/proxy issue
- Router/ISP outage

## Fix actions
- Renew DHCP lease
- Set correct DNS
- Disable VPN/proxy temporarily
- Restart network adapter/router (if appropriate)

## Verify fix
- Can resolve DNS
- Can ping external IP
- Websites load

## Prevention / Notes
- Keep DNS set to known good values
- Document the correct network settings
