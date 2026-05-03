---
name: tinyhat-goose
description: Pinned mirror of Goose, a general-purpose local agent harness.
license: Apache-2.0
metadata:
  tinyhat:
    harness:
      upstream_url: https://github.com/aaif-goose/goose
      upstream_ref: v1.32.0
      upstream_sha: 14a8815746e3c6ffad107f4983df50fd631ec2ce
      system_repo_url: https://github.com/tinyloophub/tld--sys--tinyhat-harness-goose
      sbom: ./sbom.spdx.json
      slsa_level: 1
      sandbox_tiers: [0, 1, 2]
      agent_skills_features:
        - progressive_disclosure
        - scripts
        - references
        - assets
      mcp_support: true
      otel_support: false
      owns_sandbox: false
      headless_driver: goose CLI/API
      supported_providers:
        - anthropic
        - openai
        - google
        - openrouter
        - azure
        - bedrock
        - ollama
        - local
---

# tinyhat-goose

Pinned mirror metadata for
[`aaif-goose/goose`](https://github.com/aaif-goose/goose), kept as
Tinyhat's general automation harness candidate.

Goose is a complete harness surface with CLI, desktop, API, broad
model-provider support, MCP extensions, and Agent Skills compatibility.
Tinyhat owns the outer sandbox/profile layer for hosted execution, so
`owns_sandbox` is false.

## What This Directory Is

This directory is the first-commit payload for
`github.com/tinyloophub/tld--sys--tinyhat-harness-goose`. The admin
seed action creates/registers that repository and seeds it from this
directory. The upstream source tree is fetched into the system repo at
the pinned `v1.32.0` snapshot during vendoring.

## Vendor Compliance

Upstream is licensed Apache-2.0. Tinyhat-side modifications belong
under `patches/` as numbered patch files; the v1 mirror payload starts
with an empty patches directory.
