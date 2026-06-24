Lab Name: [نام لب]

Goal: [هدفی که سایت گفته چیست؟]

Observation: [وقتی ریکوئست را دیدم، چه چیزی در ساختارِ آن مشکوک بود؟]

Exploitation: [چه تغییری در ورودی دادم؟]

Why it worked: [تحلیلِ فنی: چرا سرور اجازه داد من به فایلِ سیستمی دسترسی داشته باشم؟ (این مهم‌ترین بخش است)]

---

# 4) Overall Roadmap Structure

# Phase 1 — Offensive Web / Bug Bounty
Goal:
- keep motivation high
- build offensive thinking
- develop exploitable security intuition
- create early income opportunity
- build real vulnerability analysis habits

# Phase 2 — Bridge Layer
Goal:
- connect web vulnerabilities to infrastructure reality
- understand Linux, containers, services, metadata, IAM, and trust boundaries
- prepare transition from “web bug hunter” to “infrastructure-aware attacker”

# Phase 3 — Cloud-Native Security
Goal:
- move from app-layer attack thinking to host/container/Kubernetes/cloud attack surface
- become specialized, rare, and valuable
- transition toward your final long-term professional path

---

# 5) Phase 1 — Offensive Web / Bug Bounty

## Objective
You are not trying to become a generic certificate-based pentester.  
You are trying to become:

- concept-driven
- exploit-capable
- report-capable
- selective
- eventually infrastructure-aware

## Phase 1 Topics

### 5.1 Attack Surface Fundamentals
Learn:
- attack surface
- trust boundary
- user input
- server-side processing
- client vs server trust
- security assumptions
- exposure points

Why:
Without this, all later topics become memorization.

Primary resources:
- PortSwigger Web Security Academy
- OWASP Top 10
- OWASP Cheat Sheet Series

---

### 5.2 Authentication and Session Management
Learn:
- authentication flow
- cookies
- sessions
- JWT basics
- password reset flaws
- session fixation
- weak MFA logic
- account takeover patterns

Why:
A huge number of real bugs are identity-flow failures, not magical exploits.

Primary resources:
- PortSwigger Authentication labs
- PortSwigger Session Management labs
- OWASP Authentication Cheat Sheet

---

### 5.3 Authorization and Access Control
Learn:
- IDOR
- horizontal privilege escalation
- vertical privilege escalation
- missing authorization checks
- role-based access control failure
- object-level authorization failure
- forced browsing

Why:
This is one of the highest practical-value areas in real bug bounty.

Primary resources:
- PortSwigger Access Control labs
- OWASP Access Control Cheat Sheet

---

### 5.4 Injection
Learn:
- SQL injection
- OS command injection
- SSTI
- XML-based injection concepts
- LDAP injection
- unsafe parser behavior
- shell interpretation boundaries

Why:
Injection teaches you how untrusted input becomes execution.

Primary resources:
- PortSwigger SQLi labs
- PortSwigger OS command injection labs
- PortSwigger SSTI labs

---

### 5.5 File Handling and Path Abuse
Learn:
- path traversal
- file read
- file upload vulnerabilities
- extension bypass
- MIME/content-type trust problems
- local file inclusion concepts
- unsafe file processing

Why:
These ideas later map well to secrets leakage, volume abuse, and filesystem misuse.

Primary resources:
- PortSwigger Path Traversal labs
- PortSwigger File Upload labs

---

### 5.6 SSRF
Learn:
- what SSRF is
- blind SSRF
- internal network reachability
- backend trust abuse
- cloud metadata access
- redirect chaining
- URL parser confusion

Why:
This is one of the strongest bridges from web to cloud.

Primary resources:
- PortSwigger SSRF labs
- OWASP SSRF Prevention Cheat Sheet

Cloud bridge resources for later:
- AWS IMDS docs
- GCP metadata server docs
- Azure instance metadata docs

---

### 5.7 Browser-Side Security
Learn:
- reflected XSS
- stored XSS
- DOM XSS
- CSRF
- CORS misconfiguration
- same-origin policy
- trust of browser state

Why:
Not your final specialization, but necessary for real offensive understanding.

Primary resources:
- PortSwigger XSS labs
- PortSwigger CSRF labs
- PortSwigger CORS labs
- OWASP XSS Prevention Cheat Sheet
- OWASP CSRF Prevention Cheat Sheet

---

### 5.8 Business Logic Vulnerabilities
Learn:
- workflow abuse
- race conditions
- state desynchronization
- price manipulation
- hidden trust assumptions
- business rule abuse

Why:
Real money in bug bounty often comes from logic flaws, not textbook payloads.

Primary resources:
- PortSwigger Business Logic labs
- PortSwigger Race Condition labs

---

### 5.9 API Security
Learn:
- BOLA / object-level authorization issues
- broken auth in APIs
- mass assignment
- excessive data exposure
- insecure state transitions
- token misuse
- API enumeration

Why:
Modern bug bounty increasingly revolves around APIs.

Primary resources:
- OWASP API Security Top 10
- PortSwigger API-related labs
- Real writeups from HackerOne / Intigriti

---

# 6) Phase 1 Supporting Resources

## Must-have practical sources
- PortSwigger Web Security Academy
- HackerOne Hacktivity
- Intigriti writeups / Hackademy
- PentesterLab
- TryHackMe Web Fundamentals
- Hack The Box Academy web modules

## Useful names to follow
- NahamSec
- TomNomNom
- Assetnote
- PortSwigger research/blog
- high-quality public writeups

---

# 7) Phase 1 Execution Model

## Your target behavior
Do not just read theory.

For each topic:
1. read the concept
2. solve labs
3. take notes
4. write your own summary
5. review public reports
6. map the concept to real targets
7. keep a checklist of test ideas

## Required artifacts
Create these markdown files as you progress:

- `attack-surface-notes.md`
- `auth-session-notes.md`
- `access-control-notes.md`
- `injection-notes.md`
- `file-handling-notes.md`
- `ssrf-notes.md`
- `browser-security-notes.md`
- `business-logic-notes.md`
- `api-security-notes.md`
- `bug-bounty-testing-checklists.md`

---

# 8) What Not To Do

Do not:
- waste serious time on CEH as your primary learning path
- become tool-addicted without understanding
- jump too early between 20 platforms
- chase only flashy XSS payload culture
- become a generic web-only bug hunter with no systems depth

Your advantage will come from:
- deeper conceptual clarity
- stronger Linux/system understanding
- better transition to infrastructure and cloud

---

# 9) Bridge Phase — From Web to Infrastructure

This phase matters because it prevents you from getting trapped forever in shallow web-only offensive work.

## Concept bridges

### SSRF → Cloud metadata theft
If you understand SSRF properly, you can later understand:
- instance metadata abuse
- credential theft from cloud environments
- internal service targeting

### Access Control → IAM / Kubernetes RBAC
If you understand authorization flaws in apps, you can later understand:
- overly broad IAM permissions
- weak service account usage
- namespace privilege problems
- Kubernetes RBAC abuse

### Injection → Shell / CI/CD / Runtime abuse
If you understand how input becomes execution, you can later map that to:
- shell injection in automation
- pipeline abuse
- container entrypoint misuse
- unsafe job execution

### File Handling → Secret Leakage / Volume Abuse
If you understand traversal and file abuse, you can later understand:
- secret exposure
- mounted volumes
- hostPath misuse
- service account token exposure

### Trust Boundaries → Service-to-Service Security
If you understand boundaries in web apps, you can later reason about:
- microservices trust
- internal APIs
- east-west traffic
- identity inside clusters

---

# 10) Phase 2 Topics — Infrastructure Bridge

Learn:
- Linux process model
- permissions and privilege boundaries
- services and sockets
- environment variables and secrets
- reverse proxy basics
- containers vs hosts
- namespaces and cgroups (conceptual first)
- service accounts
- metadata services
- IAM basics
- Kubernetes object model basics

Primary resources:
- Linux man pages and practical labs
- Docker docs
- Kubernetes docs
- OWASP Kubernetes Top 10
- KubeHunt / Kubernetes Goat / similar labs later
- cloud provider docs for IAM and metadata behavior

---

# 11) Phase 3 — Cloud-Native Security

## Objective
Transition from “I can find bugs in apps” to:
“I understand how Linux, containers, Kubernetes, and cloud trust models fail.”

## Core areas

### 11.1 Linux Security
Learn:
- privilege boundaries
- capabilities
- process visibility
- service exposure
- filesystem permissions
- sudo abuse patterns
- hardening logic

Resources:
- Linux hardening guides
- man pages
- practical VM labs
- auditing/logging basics

---

### 11.2 Container Security
Learn:
- image trust
- container runtime basics
- namespace isolation
- capabilities
- privileged containers
- mounted docker socket
- secret leakage in containers
- breakout concepts

Resources:
- Docker docs
- container security blogs/research
- practical lab environments
- Kubernetes Goat / container-focused labs when ready

---

### 11.3 Kubernetes Security
Learn:
- pods, deployments, services
- service accounts
- RBAC
- network policies
- secrets
- admission control
- pod security
- misconfiguration patterns
- exposed dashboards
- over-privileged workloads

Resources:
- Kubernetes docs
- OWASP Kubernetes Top 10
- Kubernetes Goat
- Killercoda / lab clusters
- hands-on debugging and hardening labs

---

### 11.4 Cloud & Infrastructure Security
Learn:
- IAM basics
- metadata services
- storage exposure
- credential handling
- service-to-service trust
- network segmentation concepts
- infrastructure misconfiguration

Resources:
- AWS / GCP / Azure docs
- cloud attack writeups
- open cloud security labs
- public postmortems and research blogs

---

### 11.5 Offensive Cloud-Native
Eventually learn:
- SSRF to metadata exploitation
- Kubernetes service account abuse
- weak RBAC exploitation
- secret extraction paths
- CI/CD abuse
- exposed runtime control planes
- container escape concepts
- infrastructure pivoting

This is your high-value future specialization.

---

# 12) Recommended Time Allocation

Given your personality and motivation model:

## Current recommended split
- **60%** Bug Bounty / Offensive Web
- **25%** Linux + Docker + Kubernetes foundations
- **15%** reading reports, cloud-native attack surface, and bridge concepts

Why:
- keeps dopamine and feedback loop alive
- creates earlier income potential
- avoids losing your long-term direction
- steadily prepares the future specialization

---

# 13) Milestones

## Milestone 1
You can:
- solve PortSwigger basic labs without hand-holding
- explain auth, session, access control, SSRF, injection, and XSS clearly
- write notes from memory
- read real reports and understand them

## Milestone 2
You can:
- test simple live targets systematically
- write cleaner vulnerability reports
- build repeatable checklists
- spot common app logic errors

## Milestone 3
You can:
- connect web bugs to infrastructure implications
- understand metadata and trust boundaries
- reason about container/Kubernetes misconfigurations conceptually

## Milestone 4
You can:
- begin offensive cloud-native labs
- interpret weak RBAC and service account risks
- move toward rare and higher-value security work

---

# 14) Practical Rule For You

If a resource is:
- too shallow
- too certificate-driven
- too memorization-based
- too detached from real systems
- too generic

Then it is probably not worth prioritizing.

If a resource:
- forces understanding
- forces labs
- exposes real failure modes
- improves your offensive reasoning
- can later bridge into Linux / cloud / containers

Then it is worth your time.

---

# 15) Final Identity Statement

You are not building yourself into:
- a generic CEH-style pentester
- a shallow tool operator
- a random bug hunter

You are building yourself into:
- an offensive-minded security engineer
- first through bug bounty and web exploitation
- then through infrastructure awareness
- finally toward cloud-native security specialization

That path fits your psychology better than a slow purely defensive route.

---

# 16) Recommended First Actions

1. Start PortSwigger Web Security Academy seriously
2. Keep structured markdown notes per topic
3. Read real bug bounty reports weekly
4. Start testing easy targets carefully and legally
5. Keep Linux/Docker/Kubernetes warm in parallel
6. Avoid CEH as a main investment
7. Treat bug bounty as a launchpad, not a final identity

---

# 17) Suggested Folder Structure
```text
security-roadmap/
├── 01-web/
│   ├── attack-surface-notes.md
│   ├── auth-session-notes.md
│   ├── access-control-notes.md
│   ├── injection-notes.md
│   ├── file-handling-notes.md
│   ├── ssrf-notes.md
│   ├── browser-security-notes.md
│   ├── business-logic-notes.md
│   └── api-security-notes.md
├── 02-bug-bounty/
│   ├── target-selection-notes.md
│   ├── methodology.md
│   ├── checklist.md
│   └── report-writing-notes.md
├── 03-bridge/
│   ├── cloud-metadata-notes.md
│   ├── iam-rbac-notes.md
│   ├── secrets-and-trust-boundaries.md
│   └── service-to-service-security.md
└── 04-cloud-native/
├── linux-security-notes.md
├── docker-security-notes.md
├── kubernetes-security-notes.md
└── offensive-cloud-native-notes.md
