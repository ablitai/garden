# Research roadmap

Garden's next research questions concern the origin of reproduction decisions, dependence on prepared infrastructure and the boundary between virtual machines and physical computers. The starting evidence remains one fixed-policy, host-managed lineage on one physical host.

The directions below summarize proposed evaluations in the [technical report](https://ablitai.com/research/garden-agentic-self-replication.pdf), a **non-peer-reviewed research draft**. They are research proposals, not completed experiments, scheduled releases or demonstrated capabilities.

## Proposed evaluations

| Direction | Evidence needed for a stronger claim |
| --- | --- |
| Reproducibility | A deliberately reviewed public artifact package, an accurate runnable manifest, disclosed omissions and alterations, and independent inspection or replay. |
| Repeated bounded trials | Predeclared sample size and stopping rules; retained failures and refusals; counts and duration distributions based only on actual measurements. |
| Independent observations | Separately held event records and physical-host mapping, sufficient for the specific claim rather than relying only on guest or controller self-report. |
| Model-directed decisions | A consequential model selection among at least two feasible, permitted alternatives; recorded context, output, parsing, fallback, policy decision and executed action. Compare against fixed policy with equivalent resources and bounds. |
| Authorized cross-environment lineage | Explicitly identify processes, VMs and physical hosts; show a parent-requested child launch and a descendant-initiated next transition in the declared environments. |
| Dependency accounting | Identify who supplies model weights, runtime, identities, storage, compute and authorization, with artifact provenance and a record that the child can load required dependencies. |
| Containment and recovery | Test declared limits, duplicate requests, identity mismatches, unavailable or unauthorized targets, invalid inherited content and interrupted provisioning. State whether controller loss should stop work safely or whether continuation is a separate hypothesis. |

For model-using descendants, the report distinguishes pre-staged model artifacts from authorized downloads. The recorded experiment used a host-supplied package containing an external [Liquid AI model](https://huggingface.co/LiquidAI/LFM2.5-350M-GGUF); it did not establish independent model acquisition. Future reporting should preserve that distinction and the upstream resource's own terms.

## A transition must have an evidence trail

Before execution, a proposed study should declare its environment, authority, artifact origins, required services, limits, stopping conditions and collection method. It should separately trace the request, policy decision, reservation, launch, child identity, artifact check, child behavior and cleanup. A reservation alone is not a launched child.

The report proposes four outcomes:

- **Observed:** every predeclared observation is available and its trust boundary supports the claim.
- **Failed:** adequate measurement records a valid negative outcome or the predeclared deadline is reached.
- **Refused:** policy intentionally rejects the transition; no birth is counted.
- **UNKNOWN:** evidence is missing, inconsistent or insufficiently trusted.

A recursive lineage claim requires evidence that a descendant initiates a further observed transition. It does not require a deliberately bounded terminal agent to produce another child. A parent-derived copying claim additionally requires provenance of the transferred bytes; common-package provisioning does not establish it.

## Open questions

Can independent observers reproduce the bounded result? Can a model choice demonstrably affect a permitted reproduction action? What changes when a declared environment spans separately identified physical computers? Which infrastructure dependencies remain necessary?

The cross-computer scenario on the [Garden project page](https://ablitai.com/projects/garden/) remains hypothetical. This roadmap makes no exploit or vulnerability claim and supplies no propagation procedure. The current evidence boundary is documented in [findings and limitations](findings-and-limitations.md).
