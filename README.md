# preference-kernel

A local-first, append-only ledger of preference evidence for a single sovereign
principal.

> **Status: placeholder, and deliberately optional.** There is no code here yet.
> A red team on 2026-08-20 demoted this from the centre of the programme to a private
> module behind the sovereign boundary. See below.

## It is optional on purpose

The first draft of this programme put preference inference at the centre and gated
everything on it. That was wrong. The design principle is now:

> Do not infer what you can coordinate without knowing.

[accord](https://github.com/velvetmonkey/accord) treats a principal's acceptance
function as **opaque**. A principal that never builds a preference model at all is a
first-class participant. This kernel is a convenience for a principal that wants one,
and nothing outside the sovereign boundary may depend on it existing.

## The kernel does not infer

It defines types, provenance rules, contradiction handling, expiry, corrections and the
model interface. Inference is a plug-in behind it. Its outputs are hypotheses and
mandate candidates. **Never actions.**

## The boundary discipline is the whole product

    facts stay facts
    behaviour stays evidence
    inference stays uncertain
    endorsement stays attributable
    authority stays explicit

## Preferences are not the only reason for action

"I reject A" may mean: I dislike A. I think A will fail. A breaks a promise I made.
A harms someone who is not in this negotiation. I lack the authority to accept A.
I cannot compare A and B.

Those are different objects and collapsing them makes a system negotiate over factual
disagreement and put a price on inalienable rights.

    WorldEvidence  Belief  Forecast  Preference
    Value  Right  Duty  Constraint  Role  Authority

## Revealed behaviour is not ground truth

A choice may reveal a budget constraint, a narrow option set, a manipulative default,
a habit, social pressure, strategic behaviour, or simply the person someone used to be.
Choice-set composition alone can move observed choices in ways no stable-utility model
represents.

So stated versus revealed is not a contest where one wins. **The aggregation is itself
the research problem**, and it belongs in
[reveal-lab](https://github.com/velvetmonkey/reveal-lab).

## The invariants this programme inherits

These hold across every repository in the set. They are not decoration.

- **Legibility is not consent.** That something can be inferred does not make every use of it legitimate.
- **Inference is not authority.** An agent may believe I prefer X and still have no authority to do X.
- **Coordination does not require surrender.**
- A valid mandate is **necessary** for action. It is **not sufficient** for legitimacy.
- Use CRDTs to converge the record, not to converge the people.

## The type chain

No stage may impersonate the next. Each transition owes a two-sided test: red on the
illegal construction, green on the legal one.

    Fact
      -> PreferenceEvidence
      -> PreferenceHypothesis
      -> Endorsement
      -> Mandate
      -> Commitment
      -> Effect
      -> OutcomeReceipt

## Siblings

| Repository | Role |
|---|---|
| [accord](https://github.com/velvetmonkey/accord) | The protocol. Opaque acceptance, minimal disclosure. |
| [accord-settlement](https://github.com/velvetmonkey/accord-settlement) | Stateful commitments and composition above the effect boundary. |
| [accord-contest](https://github.com/velvetmonkey/accord-contest) | Standing, challenge, remedy, precedent. |
| [reveal-lab](https://github.com/velvetmonkey/reveal-lab) | The hostile benchmark. Lets the central claim die cheaply. |
| [preference-kernel](https://github.com/velvetmonkey/preference-kernel) | Optional private cognition, behind the sovereign boundary. |
| [agency-boundary](https://github.com/velvetmonkey/agency-boundary) | Roles, delegation and standing for persistent agents. |
| [seal](https://github.com/velvetmonkey/seal) | The finished authority boundary. One exact effect, one receipt. |

Licence: not yet chosen.
