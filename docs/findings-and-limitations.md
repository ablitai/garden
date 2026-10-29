# Findings and limitations

The public report describes one bounded, host-managed lineage: a seed, child and grandchild on one physical Windows host. Fixed guest code requested reproduction; the host controller supplied descendants from a common package. The model generated greetings and did not make the reproduction decision.

These findings summarize the [AblitAI Technical Report on Agentic Self Replication](https://ablitai.com/research/garden-agentic-self-replication.pdf), a **non-peer-reviewed research draft** based on retrospective inspection. The primary records remain local and have not been independently replayed. This documentation is not a public reproducibility package.

## What was recorded

| Observation | Supported interpretation |
| --- | --- |
| Three replicas: seed, child and grandchild | Two dependent descendant-creation transitions in one run, not three independent trials. |
| Three unique reproduction requests | Two produced descendants; the terminal request was refused at the generation limit. |
| Matching reproduction-source digests | The host supplied common identified source; direct parent-to-child copying and full-state equality were not demonstrated. |
| Three model greetings | Local model use, without a model-selected reproduction action. No model-removal ablation was available. |
| At most two active replica VMs | Capacity scheduling was observed in the recorded configuration. |
| Repeated request identifiers | Duplicate events were recorded without extra reported VMs. |
| No listed cleanup failures | Historical cleanup observations for the experiment's resources, not a present-day host inspection or proof of secure storage erasure. |

The generation limit and total-replica cap coincided. The run therefore did not independently isolate total-cap enforcement. Reusing the same request identifier also did not test a second distinct request from the same parent against the one-child policy. These controls have observed examples, not universal correctness guarantees.

## Separate evidence stays separate

A controller-interruption record describes stopping identified resources and aborting unfinished work without replaying births. It is not another completed lineage or evidence of uninterrupted autonomous recovery. Enrollment validation, host software tests and model completions answer different questions and do not increase the main lineage's trial count.

A historical beta-readiness audit marked a later assessed revision `not_beta` and identified native acceptance gaps. That audit does not erase the earlier fixed-policy result, and the earlier result does not satisfy those later gates. Neither is a current release decision.

## What remains unestablished

- **Independent provenance:** host-controlled logs, source checks and an internally consistent journal share a common trust boundary. Matching hashes cannot independently prove historical execution, timing or resistance to wholesale rewriting.
- **Generalization:** one purposively selected run cannot establish a population success rate, reliability across environments or long-duration behavior. The total number of prior attempts and their success proportion are UNKNOWN.
- **Model authority:** the record does not establish model-directed reproduction. A greeting in the execution path is not a consequential model choice.
- **Independent provisioning:** the host supplied identities, software and VM resources. Self-acquisition of those dependencies was not demonstrated.
- **Cross-computer reach:** crossing VM boundaries on one physical host does not establish replication across physical computers.
- **Practical performance:** a per-VM allocation is not total memory use, and the recorded timer excludes earlier setup phases. Physical 4 GB operation and a general throughput claim were not tested.

## Theory is not an observed capability

The [public Garden diagram](https://ablitai.com/projects/garden/#visual) separates the recorded local lineage from a hypothetical path across computers. Its vulnerability is unspecified and unproven. No vulnerability enabling replication, exploit-enabled lineage or cross-physical-host propagation was demonstrated. Authorized prepared environments are sufficient to define a future research question; a vulnerability is not an established prerequisite.

The [roadmap](roadmap.md) sets out the report's proposed ways to strengthen future evidence. Those proposals do not retroactively expand the original result.
