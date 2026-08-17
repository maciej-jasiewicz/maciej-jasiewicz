# Maciej Jasiewicz

**Software Engineer / Web Systems Architect**  
PHP / Laravel · Application Security · Infrastructure · TypeScript / React

*Responsible technology that doesn't distract you from your business.*

I build and maintain production web systems where backend quality, security, infrastructure and maintainability matter more than framework novelty.

**PHP / Laravel** is my primary backend stack, with commercial PHP experience since 2021 and Laravel used commercially since June 2022. I also work hands-on with **TypeScript / React, Linux, Docker / Kubernetes, CI/CD and network infrastructure**.

## Core stack

**Backend:** PHP 8.x · Laravel 7–9 / 11–12 · REST APIs · Eloquent · Queues / Jobs / Events

**Authentication & security:** Laravel Policies · Sanctum · session-based authentication · access / refresh tokens · TOTP MFA · Authentik · IAM · Cloudflare WAF / Zero Trust

**Data:** PostgreSQL · MySQL / MariaDB · Redis

**Frontend:** TypeScript · JavaScript · React · Next.js · Vite

**Infrastructure:** Linux · Docker · Kubernetes / K3s · Helm · Ingress · GitHub Actions · GitLab CI · Terraform

**Networking:** WireGuard · MikroTik RouterOS · IPv4 / IPv6 · BGP / DN42

## Engineering principles

- **Diagnose before changing.** I investigate architecture, infrastructure and bottlenecks before deciding what should be refactored, replaced or left alone.
- **Deployment should be boring.** Configuration, automation and deployment are part of the system, not undocumented operational knowledge.
- **Design for the next engineer.** Readable code, documentation and explicit decisions matter because a system should not depend on its original author.
- **Use complexity only when it pays for itself.** I prefer the simplest architecture that satisfies the actual reliability, security and business constraints.

## Selected engineering work

### Device provisioning & administration platform

Built a **Laravel 11 / PostgreSQL** administration and device-provisioning platform used to provision **thousands of hardware devices**. Implemented device registration by individual serial number and configurable serial-number ranges, Laravel Policies, TOTP MFA with recovery codes, Redis-backed queues, Authentik integration and automated WireGuard configuration generation. Exposed a REST API consumed by Bash-based device setup automation and deployed the application using Docker Compose.

### Internal mobile workforce application

Implemented token-based authentication for an **Ionic / Capacitor** application used by warehouse and machine-operator staff. The mobile authentication flow used **access and refresh tokens**, while most browser-based systems I build use session-based authentication.

### Production security incident response

Investigated and remediated a complex **DDoS** incident involving an exposed origin server. Combined origin isolation, **Cloudflare WAF / rate limiting** and application-level caching to restore stable access for legitimate users.

### Independent network engineering

Operate **DN42 AS4242422169** with the assigned `fd14:e78e:db29::/48` IPv6 prefix and **three BGP peers over WireGuard** on MikroTik RouterOS. The outbound routing policy advertises only the exact assigned prefix, while inbound filtering rejects bogon prefixes.

## Systems & infrastructure practice

Beyond application development, I work with production Linux environments, Dockerized delivery, CI/CD pipelines and K3s-based infrastructure.

I maintain an independent three-node K3s environment on Ubuntu Server 24.04, provisioned with Terraform, and use separate experiments to explore technologies and operational patterns including **Cilium, cert-manager, Hetzner CSI, Argo CD and Flux**. My systems-learning work also includes building a minimal bootable Linux environment from the Linux kernel and BusyBox.

## Open source

I occasionally contribute fixes, translations and documentation improvements to open-source projects. Most of my commercial work remains private, so my public repositories focus on reproducible engineering examples, infrastructure documentation and selected independent projects.

---

**Current focus:** secure Laravel backend development · application security · enterprise identity · automated testing · platform engineering
