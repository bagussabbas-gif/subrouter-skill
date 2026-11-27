# SubRouter Skill for Claude Code

Connect Claude Code to the SubRouter API gateway — one key for Claude, GPT, Gemini, DeepSeek and Grok. Install in five minutes: copy `SKILL.md` into your Claude Code skills folder, sign up at https://subrouter.ai (1,000,000 tokens free, no credit card required), create an API key, and set `ANTHROPIC_BASE_URL` and `ANTHROPIC_AUTH_TOKEN`.

## Install

**Claude Code (manual):** copy `SKILL.md` to `~/.claude/skills/subrouter/SKILL.md`, then restart Claude Code.

**skills.sh:** `npx skills add bagussabbas-gif/subrouter-skill`

## Setup

1. Sign up at https://subrouter.ai — new accounts get 1,000,000 tokens free, no credit card required.
2. Create an API key in the dashboard.
3. Set the environment variables:
   - `ANTHROPIC_BASE_URL=https://asiasouth.up.railway.app/`
   - `ANTHROPIC_AUTH_TOKEN=<your key>`
4. Start Claude Code. The gateway routes each call and shows the route and price per call.

If the base URL fails, check the current value in the SubRouter docs — it has changed once before.

## Facts

- Generic OpenAI-compatible base URL: `https://subrouter.ai/v1`
- Pay-as-you-go, minimum top-up $0.94. Balance never expires.
- Payment: USDT, Visa, WeChat, Alipay.
- Smart routing with automatic failover. `GET /v1/models` returns 401 without a key — that is expected.

## Notes

SubRouter is a third-party gateway, not an official Anthropic or OpenAI service.

## License

MIT
