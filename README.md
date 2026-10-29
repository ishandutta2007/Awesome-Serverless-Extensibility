# Awesome-Serverless-Extensibility

## Top Serverless Extensibility Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Edge Functions, FaaS Runtimes & Self-Hosted Serverless Platforms*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Serverless Extensibility**. These tools enable developers to extend platforms and run custom logic at the edge or in the cloud—executing code in response to events, HTTP requests, or commerce workflows without managing servers, while benefiting from automatic scaling and pay-per-use pricing.



**Examples** include Shopify Functions, AWS Lambda, Cloudflare Workers, Vercel Functions, Netlify Functions, Google Cloud Functions, Azure Functions, Fastly Compute, Fastly Edge, and Supabase Functions (the category leaders).



**Open-source emphasis**: Serverless Extensibility is a domain where open-source tooling is **maturing but platform-specific**. The strongest self-hosted alternatives to Cloudflare Workers are **fn0** (V8/Wasmtime-based FaaS designed as a Workers alternative) , **open-compute** (a single-binary platform running a pinned workerd runtime with 99% compatibility for KV, R2, D1, Durable Objects, and Queues) , and **Juno** (self-hosted serverless functions in WASM containers, positioned as "Vercel + Firebase + Self-Hosting") . For a traditional FaaS on Docker, **Fn Project** provides an event-driven platform where any Docker container becomes a function . Shopify Functions is a **platform-locked extensibility model** with no open-source equivalent—its WebAssembly-based commerce logic runs only on Shopify infrastructure .



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Shopify Functions](https://shopify.dev/docs/api/functions)**  

  Serverless extensibility for Shopify's backend, allowing developers to customize discounts, shipping, payment methods, and cart/checkout validation with WebAssembly modules that execute in **under 5ms** on Shopify's infrastructure . Functions are distributed via apps and configurable by merchants without code, with API versions released quarterly (latest `2026-07`) . Some Function targets are **Shopify Plus exclusive** for custom distribution .



- **[AWS Lambda](https://aws.amazon.com/lambda/)**  

  The pioneering FaaS platform; runs code in response to events (S3, DynamoDB, API Gateway, etc.) with automatic scaling and pay-per-invocation pricing.



- **[Cloudflare Workers](https://workers.cloudflare.com/)**  

  Edge serverless platform running JavaScript/TypeScript (and WASM) on V8 isolates across Cloudflare's global network; sub-millisecond cold starts and integration with KV, R2, D1, Durable Objects, and Queues.



- **[Vercel Functions](https://vercel.com/docs/functions)**  

  Serverless functions integrated with Vercel's frontend cloud; supports Node.js, Edge Runtime, and Python with automatic scaling and Git-based deployments.



- **[Netlify Functions](https://docs.netlify.com/functions/overview/)**  

  Serverless functions for Netlify sites; supports JavaScript/TypeScript and Go with background functions and scheduled functions.



- **[Google Cloud Functions](https://cloud.google.com/functions)**  

  Google's FaaS offering with event-driven and HTTP triggers, integrated with Google Cloud services (Pub/Sub, Cloud Storage, Firestore).



- **[Azure Functions](https://azure.microsoft.com/en-us/products/functions)**  

  Microsoft's serverless compute with triggers and bindings across Azure services; supports C#, JavaScript, Python, Java, and PowerShell.



- **[Fastly Compute](https://www.fastly.com/products/compute)**  

  Edge compute platform running WebAssembly at Fastly's edge; provides local testing via **Viceroy** .



- **[Fastly Edge](https://www.fastly.com/)**  

  Fastly's edge network services, including edge computing and delivery, with Compute as the serverless extensibility layer.



- **[Supabase Functions](https://supabase.com/docs/guides/functions)**  

  Edge Functions within the Supabase platform; runs Deno-based TypeScript functions close to users with integration to Supabase Auth, Database, and Storage.



## Open-Source GitHub Projects



### Cloudflare Workers Alternatives (Self-Hosted)



- **[open-compute](https://github.com/elliottux/open-compute)**  

  Single-binary self-hosted platform running a **pinned, checksum-verified workerd runtime** with SQLite and local storage by default . Claims **99% compatibility** across Workers, KV, R2, D1, Durable Objects, Queues, Cron, Workflows, Static Assets, Service Bindings, Cache, Images, Vectorize, and AI Search—measured against real Cloudflare with **2,256 tracked API members** and 90%+ line coverage . Wrangler 4.143.0 deploys and manages supported products. **The most complete open-source Cloudflare Workers replacement** for organizations wanting Workers on their own infrastructure. Workers AI is partial (20%), Browser Run and Containers are planned .



- **[fn0](https://github.com/namseent/fn0)**  

  Fully open-source FaaS (V8 and Wasmtime-based) explicitly positioned as an alternative to Fermyon Spin and **Cloudflare Workers** for on-premise and cloud . Runs WebAssembly components (WASI 0.3, Component Model) and JavaScript/TypeScript via a V8-based runtime; includes built-in transactional document storage, S3-compatible object storage, HTTP/WebSocket support, and OpenTelemetry observability. Self-hostable with configurable infrastructure. **The most architecturally aligned open-source Workers alternative** for teams wanting a clean, WASM-first FaaS .



- **[localworker](https://github.com/oldfriendme/localworker)**  

  Minimalist self-hosted CF Worker runtime with a Go-based Web IDE and Rust-based worker runtime (using Cloudflare's open-source `workerd` core) . Runs on any VPS with no request/KV/CPU limits (unlike Cloudflare's official limits). **Explicitly positioned as a "toy"** by its author—useful for learning or unlimited-request workloads, but not production-grade .



### General-Purpose FaaS Platforms



- **[Fn Project](https://github.com/fnproject/fn)**  

  Event-driven, open-source FaaS platform (Go) that runs anywhere . Uses **native Docker containers as functions**—any language, any runtime. Supports public, private, and hybrid cloud deployments; can import Lambda functions. **The most mature Docker-native open-source FaaS** for teams wanting container-based serverless without vendor lock-in .



- **[Juno](https://github.com/junobuild/juno)**  

  Open-source serverless platform for static hosting and serverless functions (Rust & TypeScript in WASM containers) with self-hosting . Positioned as **"Vercel + Firebase + Self-Hosting"** ; includes authentication, datastore, file storage, and local-first development with a full emulator. **The closest open-source hybrid** of Vercel/Firebase DX with true data ownership .



- **[Own FaaS](https://github.com/ihidzhov/FaaS)**  

  Lightweight self-hosted FaaS in PHP + SQLite with a web-based code editor . Supports HTTP and time-based (crontab) triggers, function logging, and user preferences. **Minimal and easy to deploy** (PHP built-in server)—suitable for simple function hosting without complex infrastructure .



### Additional Strong Open-Source Options



- **Fermyon Spin** — Open-source WebAssembly framework for building and running serverless functions; an alternative to Cloudflare Workers with a focus on WASM components.

- **OpenFaaS** — Kubernetes-native FaaS platform for deploying functions and microservices as containers; popular for self-hosted serverless on K8s.

- **Nuclio** — High-performance serverless framework for data science and event-driven workloads; supports multiple runtimes and GPU acceleration.



**Frameworks for building custom systems**: For **Cloudflare Workers compatibility**, open-compute provides the most complete self-hosted replacement with 99% API coverage . For a **clean WASM-first FaaS**, fn0 offers a well-architected alternative . For **Docker-native functions**, Fn Project provides the most mature container-based serverless . For a **Vercel/Firebase hybrid with self-hosting**, Juno covers static hosting, auth, datastore, and functions . Shopify Functions has no open-source equivalent—its value is platform-locked to Shopify's commerce ecosystem .



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Serverless extensibility platforms handling application code and data must comply with applicable security policies; self-hosted deployments require proper isolation, resource limits, and monitoring to prevent abuse.

- **Open-source serverless extensibility is platform-dependent**—open-compute and fn0 provide strong self-hosted Workers alternatives, Fn Project offers Docker-native FaaS, and Juno provides a Vercel/Firebase hybrid . Shopify Functions remains platform-locked with no open-source equivalent . No open-source project matches the global edge network and zero-config DX of Cloudflare Workers or Vercel Functions.

- Verify license terms for commercial use; open-compute and fn0 are open-source (check repositories) , Fn Project is Apache 2.0 , and Juno is BSD-3-Clause .



---



**Made for edge developers, platform engineers, FaaS practitioners, and serverless architects.**  

Let's make serverless extensibility more open, but with clear eyes about which platform each tool actually extends.
