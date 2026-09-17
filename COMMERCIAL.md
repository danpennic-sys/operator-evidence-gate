# Operator Evidence Gate — Offer Stack

Built on QuantumGuard v1 (frozen 2026-09-09).

## Problem we sell against

Operators and air-gapped teams cannot trust verifiers that:
- call registries or DNS
- depend on wall-clock freshness
- ship two implementations that silently diverge
- market "quantum" before the algorithm exists

OEG is the commercial wrapper around a single deterministic verifier.

## Who pays

1. Defense / industrial operators who already sign artifacts and need a replayable verdict.
2. Software vendors who must prove *the same verifier* ran in CI and on the air-gapped box.
3. Auditors who need a three-state model instead of a boolean that hides malformed input.

## Offer ladder

### Free (trust)
- Clone `quantumguard`
- Run `go test ./...`
- Verify the six conformance vectors
- Read `CONTRACT-v1.md`

Job of this rung: prove we are not lying.

### OEG-SEAL — $2,400 / year
- Commercial use license of the OEG packaging (not a relicensing of MIT/Apache core)
- Priority email support, 5-business-day SLA
- Appliance runbook: CLI + HTTP on the same binary surface
- Change-control note when v2 is proposed (v1 stays frozen)

### OEG-LINE — $9,600 / year
- Everything in SEAL
- Multi-site / multi-enclave deployment rights
- Replay protocol checklist
- Chain-compaction briefing (constitutional-stack alignment)
- Quarterly conformance re-run report (customer supplies vectors)

### OEG-AUDIT — $18,000 fixed
- 15-business-day engagement
- Map customer evidence flow onto CONTRACT-v1
- Produce PASS/FAIL/INDETERMINATE gap register
- Deliver a one-page operator decision memo
- No PQC theater. Gaps stay on the board.

## What is not sold

- Post-quantum signatures (reserved track, not shipped)
- Key registries, DNS, revocation
- Freshness / timestamp oracles
- A second verifier implementation

## Sales motion (all methods)

1. **GitHub** — public core + private commercial repo (this one).
2. **Direct** — Operator Pages LLC invoice, annual prepaid.
3. **Productized service** — OEG-AUDIT as a fixed-scope engagement.
4. **Content** — honest announcement only (see quantumguard/MARKETING.md).
5. **Automation** — weekly conformance reminder against public vectors.
6. **Drive / docs** — one-pager and SOW templates for buyers.

## Close language (use as-is)

> You already sign the bytes.  
> We sell a verifier that cannot change its mind.  
> Three answers. One function. No clock. No network.

## Next engineering (paid SKUs only)

- License file check in the commercial HTTP wrapper (does not touch the public verifier).
- Signed release tarball of `qg` / `qg-http` with SHA-256 published beside the tag.
- Customer vector pack format that still evaluates through the *same* verifier.
