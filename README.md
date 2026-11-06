### Mubtasim Shahriar

**Senior software engineer. I take systems from zero, or from someone else's prototype, to production, and keep them running.**

I'm a full-stack engineer in Dhaka. Since 2023 I've built and maintained production platforms for European enterprise clients, owning them end to end: data model, APIs, frontend, CI and releases, security and production fixes. Recent work:

- An advisor-recruitment platform I **built almost single-handedly, backend and frontend**, in production since May 2026.
- A customer-retention app I took **from prototype through UAT to production in under four weeks**, owning the codebase, releases and features.
- An advisor-hiring and product-demo platform with **8,000+ advisors onboarded and 300,000+ customers**, where I build and maintain the Angular frontend against a .NET backend.

That code is private. This account is where I build in public.

**Now building:** [Tasklane](https://github.com/Mubtasim/tasklane), a self-hosted job queue server in Go on PostgreSQL. It has leases with heartbeats and fencing tokens, retries with backoff and a dead-letter queue, long-poll leasing over gRPC and HTTP, job cancel and dead-letter redrive, backpressure when a queue is full, and a Go SDK with graceful shutdown. Invariant and chaos tests (killed workers and servers, a frozen worker, a Postgres restart) check that no job is lost or completed twice. OpenTelemetry traces follow each job from the producer's request through the queue wait and every retry. A [load test](https://github.com/Mubtasim/tasklane/blob/main/docs/benchmarks.md) with pinned CPUs and open-loop load found the bottleneck (NOTIFY's commit lock); three measured fixes raised enqueue throughput 40% and cut p99 with a 1-million-job backlog from 233 to 61 ms. A one-command demo runs two servers behind Envoy with Prometheus metrics, a Grafana dashboard and Jaeger traces: kill a worker or a server and watch the jobs recover. Next: Kubernetes with autoscaling on queue depth, TypeScript and C# SDKs, then a Raft-replicated store underneath.

**Algorithms:** Codeforces Expert (1698), LeetCode 2008, 1,700+ problems solved, mostly in Java ([archive](https://github.com/Mubtasim/competitive-programming)). Former problem setter for national programming contests in Bangladesh.

**Going deep on:** distributed systems, system design, computer networking.

**Stack:** TypeScript · Node.js (NestJS, Fastify) · React / Next.js · Angular · PostgreSQL · Azure · Docker · Java · C# / .NET · learning Go

[Website](https://mubtasim-portfolio.vercel.app) · [LinkedIn](https://www.linkedin.com/in/mubtasim91) · [Codeforces](https://codeforces.com/profile/MubtasimShahriar) · [LeetCode](https://leetcode.com/u/mubtasim91/) · [AtCoder](https://atcoder.jp/users/mubtasim91)
