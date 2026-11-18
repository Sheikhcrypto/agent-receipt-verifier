# agent-receipt-verifier

**Status: proposal. No code yet.** This repository sets out the scope of a planned open-source verifier for signed AI-agent decision receipts, built to work with the ERC-8004 agent identity and validation registries on Ethereum.

## Problem

AI agents increasingly take actions with financial and regulatory consequences. Today a third party usually has to trust the operator's own logs to learn which agent acted, under whose authority, and whether the record was changed afterwards.

## Planned scope

A small, dependency-light library and command-line tool that, given a signed decision receipt, checks that:

1. the signature is valid and the signing key belongs to the agent identity named in the receipt, resolved through an ERC-8004 identity registry;
2. the receipt records the authority under which the agent acted, and that authority was valid at the time;
3. the receipt has not been altered, using a hash-linked record that anyone can recompute;
4. where a validation registry entry exists, the receipt matches it.

Verification must work without relying on House of Technologies or any other receipt issuer.

## Planned outputs

- A receipt format specification, published openly.
- A reference verifier library and command-line tool.
- Test vectors, including deliberately invalid receipts.
- A short report on what the approach does and does not guarantee.

## Out of scope

Issuing receipts, agent hosting, policy decisions, and any token.

## Milestones (indicative)

1. Draft receipt format and threat model.
2. Reference verifier and test vectors.
3. Registry integration and public report.

## Licence

MIT. See `LICENSE`.

## Maintainer

House of Technologies Ltd, Northampton, UK. Contact: Junaid Sheikh, https://www.linkedin.com/in/jrsheikh/
