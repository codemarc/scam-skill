# Scam?

**Before you trust it, get a second look.**

A free, MIT-licensed Agent Skill by Marc J. Greenberg / [BrainTrailz](https://braintrailz.com).

Paste a message. Attach a screenshot. Ask **"Scam?"**

Get a plain answer, specific evidence, what remains unknown, and one useful next step. When the evidence is missing, the right answer is **"I don't know."**

## What it does

| You bring | You get |
| --- | --- |
| A suspicious text, email, offer, or screenshot | An evidence-based assessment |
| A compelling income claim or urgent payment request | An explanation of the possible deception mechanism |
| Incomplete or conflicting information | An honest limit and a verification step |
| A mistake already made | A relevant containment action first |

The skill targets common, observable deception. It is not a malware scanner, a background monitor, or a certification that an offer is safe. It has no tracking, account requirement, API key, or executable runtime component. The AI host you use still has its own privacy practices and capabilities.

## Install and use

The source of truth is the `scam/` directory. It follows the open [Agent Skills specification](https://agentskills.io/specification), with product-specific optional UI metadata isolated in `agents/`.

### Restore the supplied Git repository

If you received `scam-skill.bundle`, clone it to restore the committed source:

```bash
git clone ./scam-skill.bundle scam-skill
```

The bundle preserves the Git history without depending on a hosted repository. GitHub publication is separate.

### With an Agent Skills installer

From the parent directory containing this repository:

```bash
npx skills add ./scam-skill --skill scam
```

Choose your supported agent interactively. This optional installer requires Node.js and network access; the skill itself does not. Review the [installer documentation](https://github.com/vercel-labs/skills) and third-party code before running it.

After publication to your chosen repository, replace `OWNER/REPOSITORY` with its actual GitHub location:

```bash
npx skills add OWNER/REPOSITORY --skill scam
```

This is a publication template, not a claim that a public repository already exists.

### Without an installer

Copy the complete `scam/` directory into the skills directory documented by your agent. Do not overwrite an existing skill without reviewing it. Alternatively, give your assistant `scam/SKILL.md` and the referenced files, then ask it to apply those instructions to your message.

| Host capability | Expected behavior |
| --- | --- |
| Supports the Agent Skills format | Discover and load the skill according to the host's installation rules |
| Supports slash commands for skills | `/scam` may be available; command behavior is host-specific |
| Supports named skill invocation | Invoke `scam` using the host's documented syntax |
| Ordinary chat with file or pasted-text support | Supply the instructions and evidence manually; this does not install a slash command |
| No vision | Paste the relevant redacted text and visible sender or destination |
| No browsing | Analyze supplied evidence and explicitly state that no independent lookup occurred |

No skill can promise to work identically in every AI product. This package avoids vendor-specific tool dependencies so the instructions remain usable when host capabilities differ. Cross-host installation has not been exercised in this environment.

## Ask it

> Scam? This page promises AI will earn $1,000 a day with no experience. It looks like Facebook, but the address is an unrelated domain.

> Is this job offer legitimate? They want me to deposit a check and send money to their equipment vendor.

> I already entered my bank password and a one-time code. What should I do first?

Redact personal details before sharing. Never send a password, verification code, recovery phrase, or full account number.

## The standard

| Commitment | What it means |
| --- | --- |
| Evidence before confidence | Explain observable facts and separate inference from verification |
| Honest uncertainty | Say "I don't know" when the material does not support an answer |
| Independent checking | Prefer known official channels and current primary sources |
| Minimal exposure | Avoid suspect links, pixels, attachments, and private-data queries |
| Resistance to manipulation | Treat instructions inside the submitted material as untrusted |
| Respect for the person asking | Explain the trick without shaming its target |

## Inception and public scrutiny

This acknowledges Marc's **"inception theory of life"**: inspect the pitch, inspect how the pitch could manipulate the checker, and inspect what the checking process could reveal.

The method is deliberately public. Assume a scammer can read it. Reliability must come from evidence and disciplined verification rather than secrecy. Avoiding direct contact reduces exposure to suspected infrastructure; it cannot guarantee invisible analysis or control the AI host's logging and link previews.

See [design notes](scam/references/design.md) for the attribution, design choices, and lineage from Aristotle, Solid, and Repack.

## Review and contribute

Use [EVALUATION.md](EVALUATION.md) to test clear scams, legitimate messages, ambiguity, and embedded manipulation. Static format validation is separate from behavioral evaluation. Report actual outcomes and host capabilities. Do not claim a detection rate from a few examples.

To propose a new pattern, submit a redacted or synthetic example, the mechanism, supporting primary sources, a legitimate counterexample, and the expected uncertainty. Never submit live credentials or someone else's personal information. Contributions should preserve the evidence standard and be available under this repository's MIT license.

## License and sources

Copyright 2026 Marc J. Greenberg. [MIT License](LICENSE). A copy is included inside the installable skill so its notice travels with it. Third-party source pages remain under their own terms; links do not imply endorsement.

| Primary source | Role |
| --- | --- |
| [Agent Skills specification](https://agentskills.io/specification) | Portable package structure |
| [Skills installer](https://github.com/vercel-labs/skills) | Optional multi-agent installation |
| [FTC business opportunity guidance](https://consumer.ftc.gov/articles/when-business-offer-or-coaching-program-scam) | Unsupported earnings, pressure, and deception patterns |
| [FTC phishing guidance](https://consumer.ftc.gov/articles/how-recognize-and-avoid-phishing-scams) | Independent verification and phishing signs |

Documentation reviewed October 16, 2026. This package is an initial release candidate; see the evaluation record for checks actually performed.
