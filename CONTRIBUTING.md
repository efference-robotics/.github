# Contributing

This guide applies to every repository in the organization unless a repository has its own.
Much of the implementation work here is done by software agents under human review, so issues must be precise enough for an agent to finish them without guessing.

## How work flows

1. **Issue.** Open an issue from one of the templates (bug, feature or task) and fill in the acceptance criteria: observable checks that decide when the work is done.
2. **Triage.** An automated triage step labels the issue with its type, area, size and risk, or asks for missing acceptance criteria in a comment.
3. **Ready.** A maintainer reads the triaged issue and adds the `agent:ready` label when it is clear and worth doing; only people add this label.
4. **Agent pull request.** An agent picks up the ready issue, works on a branch, and opens a pull request that closes the issue and includes a demo and a test plan; agent reviews are posted as comments.
5. **Human review and merge.** A maintainer reviews the pull request and merges it; merges are always done by people.

Anyone can skip step 4 and open a pull request themselves; it goes through the same review.

## Labels

| Label | Meaning |
| --- | --- |
| `type:*` | bug, feature, docs, chore or refactor |
| `area:*` | the part of the system the issue touches |
| `size:S`, `size:M`, `size:L` | expected effort, from under a day to more than a week |
| `risk:low`, `risk:high` | whether a mistake could affect safety, security, data or releases |
| `agent:ready` | a maintainer approved the issue for an agent |
| `agent:working`, `agent:revise`, `agent:blocked` | agent progress, set automatically |
| `gpu` | needs a GPU host to verify |

## Pull requests

- Keep one concern per pull request, and link the issue it closes.
- Every pull request has a **Demo** section: a short recording of the change working; for documentation or CI changes, a recording of the rendered docs or the check output.
- Every pull request has a **Test plan**: the exact commands run and their results.
- Use conventional commit messages such as `feat: add scene loader` or `fix: reject negative rates`.
- Never commit build output, model weights, datasets, logs, or credentials.
- CI must be green before review.

## Writing style

Markdown puts one sentence per line, which keeps diffs readable.
Use a plain hyphen (-) instead of the em dash.

## Conduct and security

Everyone taking part follows our [Code of Conduct](CODE_OF_CONDUCT.md).
Report vulnerabilities privately as described in [SECURITY.md](SECURITY.md), never in a public issue.
