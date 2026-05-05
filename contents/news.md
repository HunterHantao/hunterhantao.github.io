#### ICML 2026

**RepetitionCurse: Measuring and Understanding Router Imbalance in Mixture-of-Experts LLMs under DoS Stress**

**Authors:** Ruixuan Huang, Qingyue Wang, **Hantao Huang**, Yudong Gao, Dong Chen, Shuai Wang, Wei Wang

**Venue:** International Conference on Machine Learning (**ICML**), **2026**. [[arXiv]](https://arxiv.org/abs/2512.23995)

#### Abstract

Mixture-of-Experts architectures have become the standard for efficient LLM scaling, typically employing expert parallelism to distribute experts across devices. However, the absence of explicit load balancing constraints during inference allows adversarial inputs to trigger severe routing concentration. We demonstrate that out-of-distribution prompts can manipulate the routing mechanism such that all tokens are routed to the same set of top-k experts, which creates computational bottlenecks on certain devices while forcing others to idle. This converts an efficiency mechanism into a denial-of-service attack vector, leading to violations of service-level agreements for time-to-first-token (TTFT). We propose **RepetitionCurse**, a black-box strategy to exploit this vulnerability. By identifying a universal flaw in MoE router behavior, RepetitionCurse constructs attack prompts using simple repetitive token patterns in a model-agnostic manner. On widely deployed MoE models hosted on 8-GPU clusters, our method increases TTFT by 20% to 148%, significantly degrading service quality.
