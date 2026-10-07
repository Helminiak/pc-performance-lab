# PC Performance Lab

Public repository for reproducible CPU, GPU, RAM, and local-inference performance experiments.

## Purpose

Keep experimental settings, benchmark procedures, results, and stability evidence under version control so comparisons can be reproduced and distinguished from the accepted workstation configuration.

`engineering-workstation-commissioning` owns commissioning and acceptance records. `LLM-Setup` owns local-LLM installation, runtime configuration, and interoperability.

## Current status

Repository bootstrap. No setting is asserted to be stable, safe, or faster without documented measurements.

## Planned contents

- CPU power-limit, frequency, voltage, and thermal experiments.
- Memory configuration, training, cold-boot, and stability observations.
- GPU performance, power, and interconnect comparisons.
- Local-inference comparisons covering model identity, quantization, context, offload, throughput, and latency.
- Benchmark scripts, sanitized results, analysis, and experiment records.
- Documented rollback to accepted baseline settings.

## Planned layout

```text
experiments/           Hypotheses, settings, and experiment records
scripts/               Reproducible benchmark and collection tooling
configs/               Sanitized test configurations
results/               Small structured results with provenance
analysis/              Comparison and plotting code
docs/                  Test methodology and interpretation
handoff/               CURRENT_STATE.md
```

## Measurement controls

Record hardware, firmware, operating system, driver and tool versions, workload, ambient conditions when relevant, and baseline settings.

Report repeated-run variability, thermal or power limiting, failures, and the exact changes between runs. Separate peak benchmark completion from sustained stability and repeatable cold-boot behavior.

For inference, distinguish prompt processing from token generation and report context length, batch conditions, GPU/CPU placement, and draft-model settings where applicable.

## Repository boundary

Experimental results belong here. Promote accepted configuration and acceptance evidence to `Helminiak/engineering-workstation-commissioning`. Put operational local-LLM setup and launch configuration in `Helminiak/LLM-Setup`.

## Public data policy

Exclude serial numbers where unnecessary, license keys, account details, credentials, proprietary trading prompts, private datasets, and model weights. Use public or synthetic workloads for shared benchmarks.

## Work control

A Git commit identifies the controlled experimental state. Record the source commit and configuration with each result. Use branches for experiments and tagged releases for repeatable benchmark suites. Maintain `handoff/CURRENT_STATE.md`.

## Agent entrypoints and license

Before making changes, read [AGENTS.md](AGENTS.md), [the multi-LLM workflow](docs/MULTI_LLM_WORKFLOW.md) and the assigned issue. Use an owned task branch, record the full source commit and validate the actual repository state before handoff.

License: not yet selected by this governance bootstrap. Preserve existing copyright and any existing license or UNLICENSED declarations; public visibility is not an open-source license.
