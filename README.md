# Hi, I'm Priyanshu Kumar Singh

**Backend / Systems Engineer**

I build backend systems, execution infrastructure, and developer-facing applications with a focus on **correctness, isolation, performance, and operational reliability**.

My work sits close to the system boundary: processes, containers, networking, asynchronous execution, authentication, databases, and Linux.

[Portfolio](https://priyanshu22.vercel.app) · [LinkedIn](https://linkedin.com/in/yansh08) · [Email](mailto:pksingh.backend@gmail.com)

---

## What I Work With

**Languages**
Python · C · JavaScript

**Backend & Distributed Systems**
FastAPI · Node.js · PostgreSQL · Redis · Celery

**Systems & Infrastructure**
Linux · Docker · Docker Compose · Azure · Nginx · Caddy

**Networking & Security**
HTTP/HTTPS · SSL/TLS · DNS · CORS · JWT · JWKS

**Frontend**
Next.js · React · TailwindCSS

---

## Selected Work

### Containerized Code Execution Platform

**FastAPI · Next.js · Docker · Redis · Celery · PostgreSQL · Azure**

A sandboxed code execution platform designed around isolated workloads, asynchronous execution, and constrained infrastructure.

* Deployed the execution backend on a **1 GB Azure Ubuntu VM**, using custom swap and Docker Compose to operate FastAPI, Redis, Celery, and PostgreSQL within tight memory limits.
* Designed **container-level CPU and memory constraints** with Docker-based process isolation for submitted code.
* Decoupled execution workloads from the FastAPI event loop using **Redis + Celery**, preserving API responsiveness under concurrent load.
* Achieved **81+ RPS with 11 ms p95 latency across 51K+ requests** on the constrained VM.
* Sustained **50+ concurrent sandboxed submissions** without OOM kills.
* Configured Caddy as the reverse proxy with automated **Let's Encrypt TLS**, alongside Azure NSGs for HTTPS-only traffic.
* Resolved cross-origin and mixed-content issues across a **Vercel frontend → Azure backend** deployment.
* Validated access tokens against an external **JWKS endpoint** before accepting execution requests.
* Built a long-polling Next.js client representing execution state transitions:
  `QUEUED → RUNNING → SUCCESS / ERROR`
* Used adaptive polling intervals to reduce unnecessary server load while maintaining responsive execution feedback.

[Live Demo](https://oopsengine.vercel.app/) · [GitHub](https://github.com/yansh07/OopsEngine)

---

### Abyss Shell

**C · Linux Kernel API · POSIX**

A Unix shell implemented from the ground up in C, focusing on process lifecycle, IPC, file descriptors, and command execution.

* Implemented process creation and lifecycle management using `fork()`, `execvp()`, and `waitpid()`.
* Built **multi-stage pipelines** with dynamic file-descriptor and IPC management across child processes.
* Implemented I/O redirection using `dup2()` and `open()`, including both overwrite (`>`) and append (`>>`) semantics.
* Designed a **two-phase tokenizer** to correctly handle nested pipe contexts where `strtok()` state collisions became problematic.
* Manually tracked heap allocations and deallocations, maintaining **zero memory leaks and segmentation faults across 500+ REPL test iterations**.

[GitHub](https://github.com/yansh07/abyss-shell)

---

## Problem Solving

**180+ LeetCode problems solved in Python**, including the complete **NeetCode 150**.

Focus areas:

`Arrays` · `Hashing` · `Sliding Window` · `Trees` · `Graphs` · `Dynamic Programming` · `Binary Search` · `Heaps` · `Backtracking`

---

## Engineering Principles

I care about:

* **Isolation** — contain untrusted or expensive workloads at the process/container boundary.
* **Concurrency** — move blocking and compute-heavy work away from latency-sensitive paths.
* **Resource discipline** — design for explicit CPU, memory, and I/O constraints rather than assuming unlimited infrastructure.
* **Systems understanding** — understand what happens beneath the framework, from file descriptors and processes to TLS and reverse proxies.
* **Operational correctness** — deployment, networking, authentication, observability, and failure modes are part of the system.
* **Measured performance** — benchmark first, optimize against actual bottlenecks.

---

## Currently

Deepening my understanding of **distributed systems, operating systems, networking, and backend architecture** while building systems that are increasingly close to the metal.

---

### Contact

If you're working on backend infrastructure, systems engineering, developer tools, or distributed systems, I'd be happy to connect.

[LinkedIn](https://linkedin.com/in/yansh08) · [Email](mailto:pksingh.backend@gmail.com)
