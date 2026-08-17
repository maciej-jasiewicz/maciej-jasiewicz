# Maciej Jasiewicz

**Software Engineer / Web Systems Architect**  
PHP / Laravel · Application Security · Infrastructure · TypeScript / React

*Responsible technology that doesn't distract you from your business.*

I build and maintain production web systems where backend quality, security, infrastructure and maintainability matter more than framework novelty.

My primary backend stack is **PHP / Laravel** (commercially since 2022). I also work hands-on with **TypeScript / React, Linux, Docker / Kubernetes, CI/CD and network infrastructure**.

## Core stack

**Backend:** PHP 8.x · Laravel 7–9 / 11–12 · REST APIs · Eloquent · Queues / Jobs / Events · Redis

**Authentication & security:** Laravel Policies · Sanctum · session-based authentication · access / refresh tokens · TOTP MFA · Authentik · IAM · Cloudflare WAF / Zero Trust

**Data:** PostgreSQL · MySQL / MariaDB · Redis

**Frontend:** TypeScript · JavaScript · React · Next.js · Vite

**Infrastructure:** Linux · Docker · Kubernetes / K3s · Helm · Ingress · GitHub Actions · GitLab CI

**Networking:** WireGuard · MikroTik RouterOS · IPv4 / IPv6 · BGP / DN42

## Engineering principles

- **Diagnose before changing.** I investigate architecture, infrastructure and bottlenecks before deciding what should be refactored, replaced or left alone.
- **Deployment should be boring.** Configuration, automation and deployment are part of the system, not undocumented operational knowledge.
- **Design for the next engineer.** Readable code, documentation and explicit decisions matter because a system should not depend on its original author.
- **Use complexity only when it pays for itself.** I prefer the simplest architecture that satisfies the actual reliability, security and business constraints.

## Selected engineering work

### Device provisioning & administration platform

Built a Laravel-based administration and provisioning system with **Laravel Policies, TOTP MFA and recovery codes**. Integrated **Authentik**, generated **WireGuard** configuration for provisioned devices, exposed an API consumed by Bash-based setup automation, and coordinated technical requirements with the device manufacturer.

### Internal mobile workforce application

Implemented token-based authentication for an **Ionic / Capacitor** application used by warehouse and machine-operator staff. The mobile authentication flow used **access and refresh tokens**, while most browser-based systems I build use session-based authentication.

### Production security incident response

Investigated and remediated a complex **DDoS** incident involving an exposed origin server. Combined origin isolation, **Cloudflare WAF / rate limiting** and application-level caching to restore stable access for legitimate users.

### Independent network engineering

Operate **DN42 AS4242422169** with an assigned IPv6 `/48`, **BGP peering over WireGuard** and MikroTik RouterOS routing / firewall configuration.

## Systems & infrastructure practice

Beyond application development, I work with production Linux environments, Dockerized delivery, CI/CD pipelines and K3s-based infrastructure. My self-directed systems work also includes Cilium, cert-manager, Terraform, Ansible, Prometheus / Grafana and building a minimal bootable Linux environment from the Linux kernel and BusyBox.

## Open-source

I occasionally contribute fixes, translations and documentation improvements to open-source projects. My public GitHub is still intentionally small because most of my commercial work lives in private repositories.

---

**Current focus:** secure Laravel backend development · application security · enterprise identity · automated testing · platform engineering
