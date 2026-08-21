# Maciej Jasiewicz

**Software Engineer / Web Systems Architect**  
PHP / Laravel · Application Security · Infrastructure

I build Laravel backend systems and work across deployment, security and infrastructure when needed.

I have worked commercially with PHP since around 2021 and with Laravel since June 2022. I am currently Tech Lead & Web Systems Architect at ONEXO.pl, where I work on requirements, architecture, implementation, deployment, security and maintenance of client systems.

## Technologies

- **Backend:** PHP 8.x, Laravel 7–9 and 11–12, REST APIs, Eloquent, queues, jobs and events
- **Authentication and security:** Laravel Policies, Sanctum, sessions and cookies, access and refresh tokens, TOTP MFA, Authentik, rate limiting, Cloudflare WAF and Zero Trust
- **Data:** PostgreSQL, MySQL, MariaDB and Redis
- **Frontend:** TypeScript, JavaScript, React, Next.js, Vite and Sass
- **Infrastructure and delivery:** Linux, Docker, Kubernetes and K3s, Helm, Ingress, GitHub Actions, GitLab CI, AWS and Cloudflare
- **Networking:** WireGuard, IPv4 and IPv6; BGP, MikroTik RouterOS and DN42 in an independent project
- **Lab experience:** Terraform in a personal K3s environment

## Working practices

- **Incident diagnosis:** I check logs, request paths and infrastructure state before changing a production system. During a DDoS incident, this identified direct access to the origin as the main problem.
- **Deployment should be boring.** I keep build and deployment steps in version-controlled pipeline configuration instead of relying on commands run manually on a production server.
- **Documentation and handover:** I document architecture, dependencies, deployment and operational steps so another engineer can continue the work.
- **Scope control:** On zeskanuj.com, I used Filament for the administration layer instead of building a separate internal frontend.

## Selected commercial work

### Device provisioning platform

I built a Laravel 11 and PostgreSQL platform used to register and provision thousands of hardware devices.

The system supports individual serial numbers and configurable serial-number ranges. It uses Redis-backed queues, Laravel Policies and TOTP MFA with recovery codes. It integrates Authentik, Nginx Proxy Manager, wg-portal and WireGuard configuration generation.

A REST API exposes the provisioning workflow to Bash-based device setup automation. The application is delivered with Docker Compose.

### Internal mobile workforce application

For a confidential internal Ionic and Capacitor application, I implemented access and refresh token authentication. The application is used by warehouse and machine-operator staff.

For first-party browser applications, I normally use session and cookie authentication when it matches the product and threat model.

### Production DDoS incident

A production service was behind Cloudflare, but its origin IP was publicly discoverable and the server accepted direct connections. Attack traffic could therefore bypass Cloudflare.

I analysed Cloudflare requests, server logs and traffic patterns, rotated and isolated the origin IP, restricted direct access, and adjusted WAF and rate-limiting rules. I also added application-level caching where it reduced unnecessary database and rendering work.

These changes restored the intended Cloudflare-to-origin path and stable access for legitimate users.

## Independent, non-commercial projects

### DN42 autonomous system

I operate DN42 AS4242422169 with the assigned IPv6 prefix `fd14:e78e:db29::/48`.

The network currently has three BGP peers over WireGuard. MikroTik RouterOS handles the BGP sessions and routing policy. The export policy advertises only the exact assigned prefix, while the import policy rejects bogon prefixes.

### K3s infrastructure lab

I maintain a personal three-node K3s environment on Ubuntu Server 24.04 VPSs, with one control-plane node and two workers.

Terraform provisions the core infrastructure. K3s, Helm, Ingress and local storage form the maintained baseline. Cilium, cert-manager, Hetzner CSI, Argo CD, Flux and Ansible were tested separately and are not presented as permanent components of the environment.

### Minimal Linux environment

I built a bootable command-line environment from the Linux kernel and BusyBox as a systems-learning project.

## Public repositories

Most of my commercial work is private. My public repositories focus on independent infrastructure work, technical documentation and reproducible engineering examples.
