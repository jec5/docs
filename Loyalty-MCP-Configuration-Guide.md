# Try Fielo Loyalty from your AI assistant

Fielo Loyalty Playground is a demo Loyalty environment you can drive from an MCP client: look up programs and members, check points and incentive progress, and try the actions a loyalty manager uses every day. Access is by invitation. You sign in with the account from your invite e-mail.

## Connect

You need two values:

- **Server URL:** `https://loyalty-mcpplayground.app.fielo.com/dx/api/application/v2/mcp`
- **OAuth Client ID:** `YuexTuuhWNuGzq3v` (public client, no secret)

### Claude.ai and Claude Desktop

Settings → Connectors → Add custom connector. Paste the server URL, open **Advanced settings**, and paste the OAuth Client ID. Click Connect and sign in.

### Claude Code

```bash
claude mcp add --transport http --client-id YuexTuuhWNuGzq3v --callback-port 55620 fielo-loyalty https://loyalty-mcpplayground.app.fielo.com/dx/api/application/v2/mcp
```

Then run `/mcp`, pick `fielo-loyalty` and sign in.

### VS Code (GitHub Copilot)

Add the server URL as an HTTP MCP server. When asked for a client ID, paste `YuexTuuhWNuGzq3v`.

## Things to try

1. "Which loyalty programs are in the playground, and what are their point types?"
2. "Pick a member and show me their points balance, tier and recent transactions."
3. "Which incentives is that member making progress on, and how close are they to each?"
4. "Which badges can members earn, and who holds them?"
5. "Register a sale of 120 for that member and tell me how many points it earned."
6. "Create a new member called Alex Test in the first program and show their starting balance."

Prompts 5 and 6 write data. The playground is shared and is reset from time to time.

## If something goes wrong

- **Sign-in page says the redirect URI is not allowed:** your client isn't on the list yet. Tell us which client you use.
- **Signed in, but the connection fails (error 400 or "couldn't connect"):** your invite isn't active yet, or your user has no application access. Write to SUPPORT_EMAIL.
