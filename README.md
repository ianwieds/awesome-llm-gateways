<p align="center"><!-- awesome:hero --><img src=".github/assets/hero.gif" width="100%" alt="Animated isometric scene: request capsules travel from three app tiles into a switchboard console, where a dial turns to send each one to one of four model towers or to a cache drawer that pops open, while a budget bar fills."><!-- /awesome:hero --></p>

<!-- awesome:title --><h1 align="center">Awesome LLM Gateways</h1><!-- /awesome:title -->

<p align="center"><!-- awesome:tagline -->Gateways, routers and proxies between applications and LLM providers: one API, routing, caching, budgets and guardrails.<!-- /awesome:tagline --></p>

<!-- awesome:badges -->
<p align="center">
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome"></a>
  <a href="contributing.md"><img src="https://img.shields.io/badge/PRs-welcome-6366F1" alt="PRs welcome"></a>
  <a href="https://github.com/ianwieds/awesome-llm-gateways/commits/main"><img src="https://img.shields.io/github/last-commit/ianwieds/awesome-llm-gateways?color=6366F1" alt="Last commit"></a>
</p>
<!-- /awesome:badges -->

An LLM gateway sits between applications and model providers, giving them one API with routing, fallbacks, caching, budgets and guardrails. This list covers open-source and hosted gateways, model routers, caches, security proxies and the research behind them; MCP gateways have their own list, [Awesome MCP Gateways](https://github.com/ianwieds/awesome-mcp-gateways).

## Contents

- [Open-source gateways](#open-source-gateways)
  - [Purpose-built gateways](#purpose-built-gateways)
  - [API gateways with AI features](#api-gateways-with-ai-features)
  - [Key pools and API distribution](#key-pools-and-api-distribution)
- [Coding agent proxies](#coding-agent-proxies)
- [Hosted gateways](#hosted-gateways)
  - [Managed services](#managed-services)
  - [Cloud platform gateways](#cloud-platform-gateways)
- [Model routers](#model-routers)
- [Inference routing](#inference-routing)
- [Caching and cost control](#caching-and-cost-control)
- [Security and privacy proxies](#security-and-privacy-proxies)
- [Client libraries](#client-libraries)
- [Research and guides](#research-and-guides)
- [Related lists](#related-lists)
- [Contributing](#contributing)

## Open-source gateways

### Purpose-built gateways

- [AISIX](https://github.com/api7/aisix) - Rust gateway from API7 with one OpenAI-compatible API, access rules and rate limits.
- [AxonHub](https://github.com/looplj/axonhub) - Self-hosted gateway that lets any SDK reach many providers with failover and tracing.
- [Bifrost](https://github.com/maximhq/bifrost) - Go gateway with adaptive load balancing, failover, budgets and a cluster mode.
- [Braintrust AI Proxy](https://github.com/braintrustdata/braintrust-proxy) - Proxy that serves many providers through one API and caches their responses.
- [Ferro AI Gateway](https://github.com/ferro-labs/ai-gateway) - Go gateway for 30+ providers with caching, guardrails, A/B tests and cost limits.
- [FreeLLMAPI](https://github.com/tashfeenahmed/freellmapi) - Router that pools the free tiers of many providers behind one OpenAI-compatible endpoint.
- [GoModel](https://github.com/ENTERPILOT/GoModel) - Go gateway with OpenAI- and Anthropic-compatible APIs, usage tracking and guardrails.
- [gproxy](https://github.com/LeenHawk/gproxy) - Rust proxy that serves OpenAI, Claude and Gemini style APIs over many upstream channels.
- [Helicone AI Gateway](https://github.com/Helicone/ai-gateway) - Rust gateway with routing, fallbacks, rate limits and caching that logs to Helicone.
- [Inference Gateway](https://github.com/inference-gateway/inference-gateway) - Go gateway that fronts hosted providers and local runtimes such as Ollama.
- [LiteLLM](https://github.com/BerriAI/litellm) - Proxy and SDK that call 100+ LLM APIs in OpenAI format with keys, budgets and fallbacks.
- [LLM API Key Proxy](https://github.com/Mirrowel/LLM-API-Key-Proxy) - Proxy with OpenAI and Anthropic endpoints that rotates keys and translates between providers.
- [LLM Gateway](https://github.com/theopenco/llmgateway) - TypeScript gateway with one API across providers plus usage and cost analytics.
- [llmio](https://github.com/atopos31/llmio) - Go gateway with weighted load balancing, request logs and cost tracking.
- [LM-Proxy](https://github.com/Nayjest/lm-proxy) - Small Python proxy with an OpenAI-format endpoint, virtual keys and model-pattern routing.
- [Manifest](https://github.com/mnfst/llm-gateway) - Gateway that sends each agent query to a fitting model, with spend limits and fallbacks.
- [Nexus](https://github.com/Nexus-Router/nexus) - Router that joins LLM providers and MCP servers behind one governed endpoint.
- [OmniRoute](https://github.com/diegosouzapw/OmniRoute) - Local or hosted gateway with fallback across hundreds of providers and coding tools.
- [OpenZiti LLM Gateway](https://github.com/openziti/llm-gateway) - Zero trust gateway with semantic routing across hosted and private model backends.
- [Otari](https://github.com/mozilla-ai/otari) - Mozilla.ai gateway with one OpenAI-compatible endpoint, virtual keys and budgets.
- [Plano](https://github.com/katanemo/plano) - Envoy-based proxy for agent apps, formerly Arch, with model routing, guardrails and traces.
- [pLLM](https://github.com/andreimerfu/pllm) - Go gateway with virtual model routes, failover, key load balancing and budgets.
- [Portkey AI Gateway](https://github.com/Portkey-AI/gateway) - Gateway with retries, fallbacks, load balancing and guardrails across many models.
- [Proxy to Gemini](https://github.com/google-gemini/proxy-to-gemini) - Google sidecar that serves Gemini models through OpenAI and Ollama style APIs.
- [Squirrel LLM Gateway](https://github.com/mylxsw/llm-gateway) - FastAPI gateway with rule-based routing, protocol conversion and cost reports.
- [ThinkWatch](https://github.com/ThinkWatchProject/ThinkWatch) - Self-hosted gateway for LLM APIs and MCP tools with SSO, RBAC and PII redaction.
- [TokenHub](https://github.com/astaxie/TokenHub) - Enterprise gateway for model routing, team access, budget control and bill matching.
- [Traceloop Hub](https://github.com/traceloop/hub) - Rust gateway with an OpenAI-compatible API and OpenTelemetry traces built in.
- [VoidLLM](https://github.com/voidmind-io/voidllm) - Self-hosted proxy with provider routing, key management, usage tracking and rate limits.
- [yolorouter](https://github.com/yolorouter/yolorouter) - Self-hosted gateway with provider failover, key rotation and an admin console.

### API gateways with AI features

- [Agent Router](https://github.com/theagentrouter/agent-router) - Envoy Gateway extension, formerly Envoy AI Gateway, that routes and rate-limits model traffic.
- [agentgateway](https://github.com/agentgateway/agentgateway) - Rust proxy that routes LLM, MCP and A2A traffic with budgets, failover and policy.
- [Apache APISIX](https://apisix.apache.org/ai-gateway/) - API gateway whose AI plugins proxy, balance and rate-limit LLM traffic.
- [APIPark](https://github.com/APIParkLab/APIPark) - Open-source AI and API gateway with model load balancing, quotas and a developer portal.
- [Barbacane](https://github.com/barbacane-dev/barbacane) - Spec-first Rust gateway that serves APIs and dispatches LLM calls with provider fallback.
- [Gravitee AI Gateway](https://www.gravitee.io/platform/ai-gateway) - API management features that govern LLM, MCP and A2A traffic in one platform.
- [Higress](https://github.com/higress-group/higress) - AI-native API gateway on Envoy with plugins for LLM routing, token limits and caching.
- [Kong AI Gateway](https://developer.konghq.com/ai-gateway/) - Kong plugins that proxy, balance, cache and guard LLM requests next to regular APIs.
- [Traefik AI Gateway](https://traefik.io/solutions/ai-gateway) - Traefik Hub feature that puts AI endpoints behind managed routes and policies.
- [Tyk AI Studio](https://github.com/TykTechnologies/ai-studio) - Tyk's AI gateway and portal for governing model access across teams.

### Key pools and API distribution

- [GPT-Load](https://github.com/tbphp/gpt-load) - Gateway that pools many keys per channel with scheduling, failover and usage logs.
- [New API](https://github.com/QuantumNous/new-api) - One API fork that converts between OpenAI, Claude and Gemini formats, with quotas and billing.
- [One API](https://github.com/songquanpeng/one-api) - Key management and distribution system that serves many providers in OpenAI format.
- [uni-api](https://github.com/yym68686/uni-api) - Config-file gateway that unifies many provider APIs without a web frontend.

## Coding agent proxies

- [ccproxy](https://github.com/starbaser/ccproxy) - Hook layer for Claude Code requests that can route them to other models by rule.
- [Claude Code Proxy (1rgs)](https://github.com/1rgs/claude-code-proxy) - Proxy that runs Claude Code on OpenAI or Gemini models through LiteLLM.
- [Claude Code Proxy (fuergaosi233)](https://github.com/fuergaosi233/claude-code-proxy) - Translates Claude Code's Anthropic API calls into OpenAI-compatible calls.
- [Claude Code Router](https://github.com/musistudio/claude-code-router) - Local router that sends Claude Code and other agent requests to the models you pick.
- [Clipal](https://github.com/PAIArtCom/Clipal) - Small reverse proxy for Claude Code, Codex and Gemini CLI with YAML routing and failover.
- [Misceo](https://github.com/MaySudo/Misceo) - Local Anthropic-compatible gateway with cheap-first routing and a cost dashboard.
- [opencodex](https://github.com/lidge-jun/opencodex) - Provider proxy that lets Codex and Claude Code run on any LLM you point it at.
- [ThinkWatch Lite](https://github.com/ThinkWatchProject/ThinkWatch-Lite) - Desktop gateway for Claude Code, Codex and other clients that switches upstreams.

## Hosted gateways

### Managed services

- [APIClaw](https://apiclaw.biz) - Flat-rate OpenAI-compatible API for Claude, GPT, DeepSeek, Qwen, Kimi and GLM models.
- [Cloudflare AI Gateway](https://developers.cloudflare.com/ai-gateway/) - Cloudflare service that adds caching, rate limits, retries and analytics to LLM calls.
- [cortecs](https://cortecs.ai) - EU-based LLM router with one OpenAI- and Anthropic-compatible API across providers.
- [Eden AI](https://www.edenai.co) - One API across many AI providers with model routing and fallback.
- [F5 AI Gateway](https://www.f5.com/products/ai-gateway) - F5 product that inspects, secures and routes traffic between apps and LLMs.
- [LangDB](https://www.langdb.ai) - Hosted AI gateway built in Rust, with LLM usage analytics and agent tracing.
- [Netlify AI Gateway](https://www.netlify.com/platform/ai-gateway/) - Netlify feature that gives apps model access with no provider keys, plus rate limits.
- [OpenRouter](https://openrouter.ai) - One API and bill for hundreds of models with provider routing and fallback.
- [Orq.ai AI Gateway](https://orq.ai/platform/ai-gateway) - Gateway in the Orq.ai platform with routing, fallbacks, caching and budgets.
- [Pydantic AI Gateway](https://pydantic.dev/ai-gateway) - Pydantic's gateway with one key for major model providers, spend limits and tracing.
- [Requesty](https://www.requesty.ai) - Gateway and router for hundreds of models with fallback, caching and spend controls.
- [Respan](https://www.respan.ai) - LLM platform, formerly Keywords AI, with a unified gateway, tracing and evals.
- [TrueFoundry AI Gateway](https://www.truefoundry.com/ai-gateway) - Enterprise gateway with model access control, rate limits, budgets and observability.
- [Vercel AI Gateway](https://vercel.com/docs/ai-gateway) - Vercel service with one endpoint for many models, budgets, fallbacks and usage monitoring.
- [Zuplo AI Gateway](https://zuplo.com/ai-gateway) - API gateway feature that routes LLM calls across providers with per-team spend caps.

### Cloud platform gateways

- [Apigee AI gateway](https://cloud.google.com/solutions/apigee-ai) - Google Cloud's Apigee used as a gateway to govern and secure LLM APIs.
- [Azure API Management AI gateway](https://learn.microsoft.com/en-us/azure/api-management/genai-gateway-capabilities) - Azure gateway policies for token limits, load balancing and semantic caching of LLMs.
- [Databricks Unity Gateway](https://docs.databricks.com/aws/en/ai-gateway/) - Databricks governance layer that routes AI traffic, applies guardrails and tracks usage.
- [MLflow AI Gateway](https://mlflow.org/docs/latest/genai/governance/ai-gateway/) - MLflow component that serves many providers behind one governed endpoint.
- [Multi-Provider Generative AI Gateway on AWS](https://github.com/aws-solutions-library-samples/guidance-for-multi-provider-generative-ai-gateway-on-aws) - AWS guidance that deploys a LiteLLM-based gateway for Bedrock and other providers.

## Model routers

- [ClawRouter](https://github.com/BlockRunAI/ClawRouter) - Local router for autonomous agents that picks a model per request and pays per call.
- [LLMRouter](https://github.com/ulab-uiuc/LLMRouter) - Library with many routing methods for training and serving LLM routers.
- [NadirClaw](https://github.com/NadirRouter/NadirClaw) - Router that sends simple prompts to cheap or local models and hard ones to stronger models.
- [Not Diamond](https://www.notdiamond.ai) - Hosted model router that picks the best model for each prompt.
- [NVIDIA LLM Router](https://github.com/NVIDIA-AI-Blueprints/llm-router) - NVIDIA blueprint that classifies each request and routes it to a fitting model.
- [NVIDIA NeMo Switchyard](https://github.com/NVIDIA-NeMo/Switchyard) - Proxy that routes across models and providers while keeping OpenAI and Anthropic APIs.
- [OptiLLM](https://github.com/algorithmicsuperintelligence/optillm) - OpenAI-compatible proxy that applies reasoning techniques and routes prompts between them.
- [OrcaRouter Lite](https://github.com/Continuum-AI-Corp/OrcaRouter-Lite) - Self-hosted OpenAI-compatible router with an auto model that absorbs provider outages.
- [SageRoute](https://github.com/codejunkie99/sageroute) - Proxy that starts agent tasks on a cheap model and escalates when the trajectory needs it.
- [Semantic Router](https://github.com/aurelio-labs/semantic-router) - Python decision layer that routes prompts to routes, tools or models by embedding similarity.
- [UncommonRoute](https://github.com/CommonstackAI/UncommonRoute) - Local trained router for coding tools that sends each request to a fitting model.
- [vLLM Semantic Router](https://github.com/vllm-project/semantic-router) - Mixture-of-models router that classifies prompts and sends them to the best-fit model.
- [Wayfinder Router](https://github.com/asdecided/WayfinderRouter) - CLI tool for rule-based routing of queries between local and hosted models.
- [Weave Router](https://github.com/weave-os/router) - Drop-in proxy for Anthropic, OpenAI and Gemini that picks a model per request.

## Inference routing

- [Gateway API Inference Extension](https://github.com/kubernetes-sigs/gateway-api-inference-extension) - Kubernetes extension that routes requests to model server pools by load and model.
- [llm-d Router](https://github.com/llm-d/llm-d-router) - Entry point for llm-d that schedules inference requests with cache and load awareness.
- [LoLLMs Hub](https://github.com/ParisNeo/lollms_hub) - Proxy in front of several Ollama instances with key-based access control.
- [Olla](https://github.com/thushan/olla) - Proxy and load balancer for local LLM backends with failover and sticky sessions.
- [ollamaMQ](https://github.com/Chleba/ollamaMQ) - Rust proxy that queues requests fairly per user across LLM backends.
- [Shepherd Model Gateway](https://github.com/smg-project/smg) - Rust gateway that routes across self-hosted engines and cloud providers with cache awareness.

## Caching and cost control

- [Context Gateway](https://github.com/Compresr-ai/Context-Gateway) - Agent proxy that compacts history and trims context before it reaches the model.
- [Fastly AI Accelerator](https://docs.fastly.com/products/ai-accelerator) - Fastly service that caches LLM API responses by semantic similarity.
- [GPTCache](https://github.com/zilliztech/GPTCache) - Python library that caches LLM responses by embedding similarity.
- [Headroom](https://github.com/headroomlabs-ai/headroom) - Library and proxy that compresses tool output, logs and files before they reach the LLM.
- [llmtrim](https://github.com/fkiene/llmtrim) - Local proxy that trims wasted tokens from prompts and history to lower API bills.
- [PromptCache](https://github.com/messkan/prompt-cache) - Self-hosted Go proxy that returns cached answers for similar prompts.
- [Redis LangCache](https://redis.io/langcache/) - Managed Redis service for semantic caching of LLM responses.
- [RelayPlane](https://github.com/RelayPlane/proxy) - Local proxy that prices each agent request and caps or stops runaway spend.
- [Semcache](https://github.com/sensoris/semcache) - Rust semantic caching proxy for OpenAI-compatible APIs that runs in memory.
- [tokview](https://github.com/headroomlabs-ai/tokview) - Local proxy and dashboard that shows token use and cost per tool call.
- [vCache](https://github.com/vcache-project/vCache) - Semantic prompt cache that bounds the error rate of the answers it reuses.

## Security and privacy proxies

- [AegisGate](https://github.com/ax128/AegisGate) - Security gateway for LLM APIs that detects prompt injection and redacts PII.
- [aifw](https://github.com/funstory-ai/aifw) - Small LLM firewall that masks PII in prompts and restores it in replies.
- [CosyRedactGateway](https://github.com/CassiopeiaCode/CosyRedactGateway) - Stateless proxy that redacts secrets before upstream calls and restores them after.
- [DontFeedTheAI](https://github.com/zeroc00I/DontFeedTheAI) - Anonymizing proxy that strips IPs, credentials and hostnames before they reach an LLM.
- [Invariant Gateway](https://github.com/invariantlabs-ai/invariant-gateway) - LLM proxy that records agent traffic so it can be observed, debugged and checked.
- [preflight](https://github.com/ghuntley/preflight) - Local proxy that scans LLM requests and attachments for secrets before they leave.
- [Privacy Filter](https://github.com/packyme/privacy-filter) - Go gateway that redacts PII and secrets from LLM traffic with low latency.
- [Sentinel Guard](https://github.com/aitechnav/Sentinel_Guard) - Security-first LLM gateway with guardrails for apps, agents and AI IDEs.

## Client libraries

- [Adaline Gateway](https://github.com/adaline/gateway) - Local TypeScript SDK with one interface for calling 200+ models.
- [AI SDK](https://github.com/vercel/ai) - Vercel's TypeScript toolkit with one API for text, objects and tools across providers.
- [aisuite](https://github.com/andrewyng/aisuite) - Python library with one chat interface across many model providers.
- [any-llm](https://github.com/mozilla-ai/any-llm) - Mozilla.ai Python interface that calls each provider's official SDK behind one function.
- [LLM](https://github.com/simonw/llm) - CLI and Python library for many hosted and local models through plugins.
- [Token.js](https://github.com/token-js/token.js) - TypeScript SDK that calls 200+ models using OpenAI's request format.

## Research and guides

- [Agent-as-a-Router](https://github.com/LanceZPF/agent-as-a-router) - Code for a paper on agentic model routing for coding tasks.
- [AI Gateway labs](https://github.com/Azure-Samples/AI-Gateway) - Microsoft labs that build AI gateway patterns on Azure API Management.
- [Avengers-Pro](https://github.com/ZhangYiqun018/AvengersPro) - Code for a paper on routing queries by performance and cost across models.
- [FrugalGPT](https://arxiv.org/abs/2305.05176) - Paper on cascading LLM calls to cut cost while keeping quality.
- [GPT Semantic Cache](https://arxiv.org/abs/2411.05276) - Paper on caching LLM answers by query embeddings to lower cost and latency.
- [Hybrid LLM](https://arxiv.org/abs/2404.14618) - Paper on routing queries between small and large models by predicted difficulty.
- [OSS LLMOps Stack](https://github.com/langfuse/oss-llmops-stack) - Reference stack that pairs LiteLLM as the gateway with Langfuse for tracing.
- [RouteLLM](https://arxiv.org/abs/2406.18665) - Paper on learning routers from preference data to pick between a strong and weak model.
- [RouteLLM blog post](https://www.lmsys.org/blog/2024-07-01-routellm/) - LMSYS write-up of the RouteLLM routers and their cost savings.
- [Router-R1](https://github.com/ulab-uiuc/Router-R1) - Code for a paper that trains an LLM to route and aggregate across models with RL.
- [RouterArena](https://github.com/RouteWorks/RouterArena) - Framework and leaderboard for evaluating LLM routers on shared datasets.
- [RouterBench](https://arxiv.org/abs/2403.12031) - Paper and benchmark for comparing multi-LLM routing systems.

## Related lists

- [Awesome AI Tokenomics](https://github.com/QuesmaOrg/awesome-ai-tokenomics) - Tools, benchmarks and reading on what tokens cost and how to cut the bill.
- [Awesome Routing LLMs](https://github.com/MilkThink-Lab/Awesome-Routing-LLMs) - Papers and code on routing between language models.

## Contributing

Contributions are welcome. Read the [contribution guidelines](contributing.md) first.

<!-- awesome:maintainer -->
Maintained by [Ian Wiedenman](https://github.com/ianwieds).
<!-- /awesome:maintainer -->
