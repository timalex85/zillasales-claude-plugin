# ZillaSales for Claude

Find independent sales reps and commission-based opportunities directly in Claude.

## Try it in Claude

- Find technology sales opportunities and compare territories and disclosed commission terms.
- Find independent technology sales reps and compare their public experience and territory coverage.
- Show my private sample opportunity draft and explain what remains before submission.

## See it in action

![Find technology sales opportunities and compare territories and disclosed commission terms.](https://zillasales.com/developers/claude/01-opportunities.jpg)

![Find independent technology sales reps and compare their public experience and territory coverage.](https://zillasales.com/developers/claude/02-representatives.jpg)

![Show my private sample opportunity draft and explain what remains before submission.](https://zillasales.com/developers/claude/03-private-draft.jpg)


![ZillaSales](assets/icon.png)

Find independent sales opportunities and representatives, compare results, and manage your own shortlist and application or opportunity drafts.

Public opportunity and representative searches work without sign-in. Connect a ZillaSales company or rep account when you ask to save items, read private records, prepare drafts, or apply. Existing account permissions still govern access. Saving does not apply, contact anyone, unlock contact details or spend credits. Applications and moderation submissions require reviewing the exact proposed action and explicitly confirming it.

The plugin includes two skills: finding sales opportunities and building sales coverage. Interactive comparison views use MCP Apps; text results remain available when a client cannot show the view.

## Examples

- "Find commission-based industrial automation opportunities covering Texas. Show the commission terms and anything unknown."
- "Find reps for commercial LED lighting in Texas and compare their relevant experience."
- "Save this opportunity to my favorites." Sign in when prompted; saving does not submit an application.
- "Help me apply to this opportunity." Review the prepared application and confirm before it is submitted.

## Connect

Add this remote MCP URL as a custom web connector in Claude:

```text
https://zillasales.com/api/mcp/claude
```

Choose automatic OAuth client registration (DCR) and sign in when needed. Public tools do not require an account. The server supports S256 PKCE and refresh-token rotation. No API key belongs in this package or in chat.

For Claude Code, add the same endpoint with:

```sh
claude mcp add --transport http zillasales https://zillasales.com/api/mcp/claude
```

For a local checkout of this plugin package, run `claude --plugin-dir /absolute/path/to/plugin`. A public directory listing will be available only after Anthropic accepts and publishes the submission.

## Data and privacy

The skills invoke only the declared ZillaSales MCP server. The package runs no local scripts, hooks, installers or background processes. The hosted service receives tool arguments and, after OAuth consent, the account permissions needed for the requested action. It does not require the full conversation. Searches and profile/application content are processed by ZillaSales. Account records remain subject to the service retention and deletion policy. See the [privacy policy](https://zillasales.com/privacy#connected-assistants), [terms](https://zillasales.com/terms) and [developer documentation](https://zillasales.com/developers) for details.

## Support

Use [ZillaSales support](https://zillasales.com/developers#support). If authorization expires or is revoked, reconnect through Claude. If a tool reports a rate limit, wait for its retry interval. Never infer missing results from a failed request.

## License

The plugin package is MIT licensed. Hosted services and their data remain subject to their own terms.

## Install from a local marketplace

```text
/plugin marketplace add /absolute/path/to/zillasales
/plugin install zillasales@zillasales-claude
```

The plugin files are MIT licensed. The remote service uses its own terms and privacy policy linked above. Directory availability depends on Anthropic review.
