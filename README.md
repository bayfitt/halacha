# Halacha research

This private repository preserves two shared conversations about electricity on Shabbat and the general-purpose Meqorist research and review assistant.

## Conversations

- [First conversation snapshot](conversations/electricity-shabbat-conversation-1.md)
- [Later conversation snapshot](conversations/electricity-shabbat-conversation-2.md) — extends the first.

These are transcriptions of the messages visible on the shared pages, not independently verified halachic conclusions. The shared pages do not expose the full contents of the conversation's canvas or its downloadable transcript. Some original citation markers may only be meaningful within the original chat; the source links are included in each file.

## Meqorist

Meqorist researches Jewish questions and reviews claims by tracing their sources and reasoning to the Gemara and Chazal. It distinguishes an explicit Gemara statement from a reasoned application, and reports the available evidence for a connection to Gemara and to other sources of Chazal separately. Later authority alone is not a substitute for a demonstrated source or argument. A missing source is a research result, not proof that no source exists.

The repository contains the canonical [Codex skill](skills/meqorist/SKILL.md) and a [GitHub Copilot custom agent](.github/agents/meqorist.agent.md). They are instructions for an assistant, not a continuously running service. Neither validates a claim merely by existing.

### Use in Codex

Invoke `$meqorist` in a Codex session, followed by a question or material to review. For example:

> `$meqorist` Review this claim: [claim]. Show the Gemara's explicit rule, any later inference, and the evidence for each.

> `$meqorist` Research [question] from the primary sources, including competing interpretations and gaps.

The skill is installed for the current user. To install it on another machine, copy the entire `skills/meqorist` directory to that user's `~/.codex/skills/meqorist`, then start a new Codex session. Copying the full directory preserves its supporting references.

### Use in GitHub Copilot

In a supported Copilot environment, select **Meqorist Review** in this repository and supply a question or a document to review. The profile is repository-scoped; to use it in another repository, copy both `.github/agents/meqorist.agent.md` and `skills/meqorist` into that repository. Agent availability depends on the Copilot product and account configuration.

The agent can verify sources only when its environment provides access to them. Web and external network capabilities vary: in particular, GitHub documents that its `web` tool is not currently available to Copilot cloud agents. If a source cannot be accessed, Meqorist should identify that limitation and work with the material available rather than claim verification. Sefaria's public texts are one useful source where access is available; its links and search results are leads to examine, not independent proof.

The [manual evaluation cases](evaluations/meqorist-review-cases.md) exercise source tracing, competing views, modern applications, and missing evidence.
