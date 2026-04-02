# OpenClaw Setup — 02 Security and Hardening

Once OpenClaw was working properly, I wanted to make sure I was not leaving the setup exposed.

I was not trying to make it perfect. The goal was just to tighten the obvious weak points first.

## What I did
- kept OpenClaw local-only
- used SSH and Tailscale for more controlled access instead of exposing it directly
- turned on the macOS firewall
- checked sharing and remote access settings
- made sure automatic updates and security responses were enabled
- started sorting out backups instead of leaving it for later

## Main takeaway
The biggest win here was keeping OpenClaw local-only.
That removes a lot of unnecessary exposure straight away.

The rest was mostly basic hygiene:
- keep only the access I actually need
- reduce unnecessary services
- make sure the machine stays updated
- make sure recovery is part of the setup, not an afterthought

## Current state
Nothing fancy, just noticeably better than before.
That was the whole point of this step.
