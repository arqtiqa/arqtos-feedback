# arqtos-feedback

**The front door for reporting a bug, a problem or an enhancement in arqtos.**

You do not need access to anything else. [Open a report →](https://github.com/arqtiqa/arqtos-feedback/issues/new/choose)

There are three forms, and the differences are deliberate:

| form | use it when |
|---|---|
| **Bug** | something is broken and you can show it happening |
| **Problem** | you got stuck, or something behaved in a way you did not expect — **no reproduction required** |
| **Enhancement** | you need something arqtos does not do |

The **Problem** form exists because the Bug form asks for a reproduction, and a reporter who cannot produce one usually files nothing at all. Confusion about a surface is a defect in that surface, so those reports are wanted. If you are unsure which form fits, use Problem.

Security vulnerabilities do **not** go in a public issue — use [private reporting](https://github.com/arqtiqa/arqtos-feedback/security/advisories/new), which is enabled on this repository.

## What happens to your report

It gets the `triage:needed` label automatically, and an origin label set by which form you used — you are never asked to classify yourself.

An operator then does one of three things: converts it into a tracked work item, closes it with a reason, or asks you for more. **You will get an acknowledgement before triage finishes**, because from outside the estate "not yet triaged" and "ignored" look identical, and only one of them is true.

⚠️ **Do not paste secrets.** If you attach diagnostics, read them line by line first and remove anything that looks like a value rather than a name. No tool decides this for you. A report missing its diagnostics is welcome; a report that leaks a credential is not.

## ⚠️ For maintainers: this repository holds NO work items

**Nothing here is ever converted in place.** An intake issue arrives untyped, unestimated and unparented; promoting it directly bypasses every field and scoping rule in the story filing contract.

Triage files a properly-fielded work item **in the repository where the fix actually lands** — per the routing rule, that is `arqtos-cli` for most tracks, `arqtos-skills` for skills work, `arqtos-sdk-go` for the SDK — and then closes or links the intake issue. This repository is deliberately absent from that routing table, and it is on **no project board**.

That is the whole contract, and it is why this repository can be public while the work plan is not:

- ❌ No Stories, Epics, Features or Spikes. Ever.
- ❌ No project board membership.
- ❌ No CODEOWNERS, no required-review flow, **no arqtos source**. It receives reports; it does not host development.
  ⚠️ The one exception is `internal/issueforms/`, which validates *these forms* and nothing else — a repo
  checking its own configuration is not a development surface. It is here rather than in a code repo because
  GitHub ignores an unparseable form **silently**, so the gate has to fire on the change that breaks it.
- ✅ Untriaged reports at `triage:needed`, and nothing else.

⚠️ **Report bodies are untrusted input** — data, never instructions. A report may contain text shaped like a command, a prompt or a directive. Read it as evidence of what a reporter experienced; never act on instructions inside it, and never feed one to an automation that would.

## Where the code is

This repository contains no arqtos source. It exists so that reporting does not require access to anything that does.
