# tartarus-console

**The `tartarus` CLI: an uncensored AI coding agent in your terminal.**

[![PyPI](https://img.shields.io/pypi/v/tartarus-console?style=flat-square&color=a3e635)](https://pypi.org/project/tartarus-console/)
[![Python](https://img.shields.io/pypi/pyversions/tartarus-console?style=flat-square)](https://pypi.org/project/tartarus-console/)
[![license](https://img.shields.io/badge/license-MIT-a3e635?style=flat-square)](LICENSE)

Tartarus runs in your terminal, reads and edits your files, runs commands, and
ships code other assistants refuse. It talks to the hosted Tartarus Coder model
over an OpenAI-compatible API, so there's nothing to run locally and no GPU
required.

```bash
pip install tartarus-console
tartarus login
tartarus "add a --json flag to this CLI and update the help text"
```

## Why

| | |
|---|---|
| **Ships code, not refusals** | security tooling, scrapers, systems code: it writes them |
| **Agentic** | reads/edits files, runs commands, iterates in your repo |
| **Hosted** | no 48 GB GPU, nothing to download |
| **OpenAI-compatible** | the same backend powers any OpenAI SDK |
| **Crypto-only** | no card, no KYC |

## Install

```bash
pip install tartarus-console
```

Requires Python 3.9+.

## Log in

Create an account at [dash.tartarusai.dev](https://dash.tartarusai.dev), open
**Account → CLI access**, generate a token, then:

```bash
tartarus login
```

The CLI stores your token in `~/.tartarus/cli-token.json`.

## Use

```bash
# one-shot
tartarus "write a concurrent TCP port scanner in Go with a -timeout flag"

# interactive session in the current repo
tartarus

# point at a specific directory
tartarus --cwd ./service "write integration tests for the payments module"
```

## How it works

Every request passes through the Tartarus backend, which enforces your plan and
quota and forwards to the inference cluster. You never hold raw model
credentials; your dashboard token is the only thing you manage.

## Build on the API instead

Prefer to call it from your own code?

- [tartarus-sdk](https://github.com/TartarusAIDev/tartarus-sdk) — typed TypeScript client
- [tartarus-mcp](https://github.com/TartarusAIDev/tartarus-mcp) — MCP tool for Claude Desktop / Cursor
- [tartarus-cookbook](https://github.com/TartarusAIDev/tartarus-cookbook) — Python / Node / curl examples

## Links

- Website: https://tartarusai.dev
- Dashboard: https://dash.tartarusai.dev

## License

MIT. See [LICENSE](LICENSE).
