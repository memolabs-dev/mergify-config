# mergify-config

The one Mergify policy of the memolabs-dev organization. A repository adopts it with a
`.mergify.yml` of one line:

```yaml
extends: mergify-config
```

plus the `Sensitive paths` workflow (`.github/workflows/sensitive-paths.yml`, copied from
memolabs-dev/memo-bridge), which labels `needs-human-review` and names the gate paths a PR touches.

What lands without a human, what waits for the owner, and how to roll back: memolabs-dev/memo-bridge
`docs/MERGIFY_FLEET_ADOPTION.md`. Changing this file changes the merge rule of every adopting
repository at once: it is a gate change, the owner merges it.
