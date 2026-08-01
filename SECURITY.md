# Security policy

## Reporting a vulnerability

**Do not open a public issue.**

Use [private vulnerability reporting on this repository](https://github.com/arqtiqa/arqtos-feedback/security/advisories/new) — **Security → Report a vulnerability**. It opens a channel visible only to the maintainers, and it is enabled here, so the form will render for any GitHub account.

You do not need access to any other arqtiqa repository to use it.

Include what you would put in a normal report — what you did, what happened, and what you expected — plus anything that helps establish impact. A working reproduction is welcome but not required; a credible description of the mechanism is enough to start.

⚠️ **Do not paste credentials, tokens or environment dumps**, not even to demonstrate the issue. Describe the shape of what leaked rather than the value. If a value is genuinely necessary to show the problem, say so in the report and it will be requested through a channel suited to it.

## Scope

This repository is an intake surface and contains no arqtos source. A vulnerability reported here is triaged the same way regardless of which arqtos component it affects — the CLI, the SDK, the skills or the published documents. You do not need to work out which repository owns the fix; that is the maintainers' job.

## What to expect

You will get an acknowledgement that the report was received and read, before any assessment is complete. If the report turns out not to be a vulnerability it will be said plainly, with the reasoning, rather than left to lapse.
