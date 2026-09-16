# nubjs/action

GitHub Actions for [nub](https://github.com/nubjs/nub), one per directory:

| Action | What it is |
|---|---|
| [`nubjs/action/setup-node`](setup-node/) | `actions/setup-node`, with nub installed: the project's own Node pin wins when no version is given, the package manager pinned in `package.json` runs through Nub's shims, and Nub's store is cached across runs. |
| [`nubjs/action/install`](install/) | The install step: replaces the line that runs `npm ci`, `pnpm install --frozen-lockfile`, `yarn install --immutable` or `bun install --frozen-lockfile`, installing the lockfile as it is with Nub's store cached across runs. Node and the package managers on PATH are left alone. |

```yaml
- uses: actions/checkout@v4
- uses: nubjs/action/setup-node@v0
- run: npm ci
```

## License

MIT
