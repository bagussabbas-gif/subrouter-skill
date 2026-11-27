---
name: subrouter
description: Connect Claude Code to the SubRouter API gateway — one key for Claude, GPT, Gemini, DeepSeek and Grok. Use when the user wants to set up Claude Code (or any OpenAI-compatible client) with SubRouter, check SubRouter pricing, or troubleshoot a SubRouter connection.
---

# SubRouter — One API Key for Claude, GPT, Gemini, DeepSeek and Grok

SubRouter is a third-party API gateway (not official). One key works across Claude, GPT, Gemini, DeepSeek and Grok via an OpenAI-compatible API, with smart routing and automatic failover. New accounts get 1,000,000 tokens free, no credit card required.

## When to Use This Skill

- Setting up Claude Code (or Cursor, or any OpenAI-compatible client) to call models through SubRouter instead of topping up each provider separately
- Checking how SubRouter pricing, top-ups, and the free-token offer work before spending anything
- Troubleshooting a SubRouter connection (wrong base URL, auth errors, model/route pricing)

## What This Skill Does

1. **One-key setup**: Creates an API key on subrouter.ai and points Claude Code at the gateway with two environment variables.
2. **Multi-model access**: The same key routes to Claude, GPT, Gemini, DeepSeek and Grok.
3. **Pay-as-you-go**: Minimum top-up $0.94, balance never expires. Payment by USDT, Visa, WeChat, or Alipay.
4. **Routing transparency**: Every call shows its route and price; if one provider fails, the request fails over to another route.

## How to Use

### Basic Usage

```
Set up Claude Code with my SubRouter API key
```

1. Sign up at https://subrouter.ai — new accounts get 1,000,000 tokens free, no credit card required.
2. Create an API key in the dashboard.
3. Set the environment variables:
   - `ANTHROPIC_BASE_URL=https://asiasouth.up.railway.app/`
   - `ANTHROPIC_AUTH_TOKEN=<your key>`
4. Start Claude Code. The gateway routes each call and shows the route and price per call.

If the base URL fails, check the current value in the SubRouter docs — it has changed once before.

### Advanced Usage

```
Check the price of Claude Opus on SubRouter before I run this large job
```

- Generic OpenAI-compatible base URL: `https://subrouter.ai/v1`
- Prices differ per model and route — check the price for the model you use before running large jobs.

## Example

**User**: "I got tired of topping up five different API accounts. Can I use one key for Claude, GPT and DeepSeek?"

**Output**:

```
Yes — with SubRouter you sign up at https://subrouter.ai (1,000,000 tokens free, no card),
create one API key, and set ANTHROPIC_BASE_URL=https://asiasouth.up.railway.app/ with
ANTHROPIC_AUTH_TOKEN=<your key>. The same key then works for Claude, GPT, Gemini,
DeepSeek and Grok, pay-as-you-go from $0.94, balance never expires.
```

## Tips

- `GET /v1/models` returns 401 without a key — that is expected; the endpoint requires authentication.
- Test with the free tokens first, then top up only as much as you need.
- SubRouter is a third-party gateway, not an official Anthropic or OpenAI service.

## Common Use Cases

- Running Claude Code without an Anthropic subscription
- Switching between Claude, GPT, Gemini, DeepSeek and Grok in one project without juggling five balances
- Letting a team share one gateway balance instead of five provider accounts
