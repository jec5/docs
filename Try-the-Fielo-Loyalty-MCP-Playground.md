The **Loyalty Playground** is a demo Fielo Loyalty environment you drive from an AI assistant (Claude, VS Code Copilot…) through MCP. It holds one fictional program, **Bean & Leaf Rewards**, a coffee-shop chain. You can read anything in it and try everyday loyalty-manager actions.

Everything is fictional. The environment is shared with other testers and is reset from time to time.

## 1. Accept the invite

Access is by invitation only. Open the invite e-mail from the playground, set your password, and sign in once in the browser to check it works.

## 2. Connect your AI assistant

- **Server URL:** `https://loyalty-mcpplayground.app.fielo.com/dx/api/application/v2/mcp`
- **OAuth Client ID:** `YuexTuuhWNuGzq3v` (public client, no secret)

**Claude.ai / Claude Desktop:** Settings → Connectors → Add custom connector → paste the URL → Advanced settings → paste the Client ID → Connect → sign in with your playground account.

**Claude Code:**

```bash
claude mcp add --transport http --client-id YuexTuuhWNuGzq3v --callback-port 55620 fielo-loyalty https://loyalty-mcpplayground.app.fielo.com/dx/api/application/v2/mcp
```

Then run `/mcp` → `fielo-loyalty` → sign in. The sign-in lasts a few hours; when tools stop working, run `/mcp` again.

## 3. Meet the members

| Member | ID | Story |
| --- | --- | --- |
| Ana Souza | DEMO-001 | **Gold**, about 1,100 Points, badges Regular and Founding Member, in the VIP segment, redeemed a Free Coffee |
| Ben Carter | DEMO-002 | **Silver**, 355 Points, Founding Member, VIP |
| Chloe Martin | DEMO-003 | Bronze, 33 Points, 4 visits: one more visit in 30 days earns Fifth Visit Bonus |
| David Kim | DEMO-004 | Bronze, 0 Points: his only purchase was at the Airport Kiosk, which doesn't earn points |
| Emma Rossi | DEMO-005 | New member, no activity: use her for anything that writes data |

What's in the program:

- **Tiers:** Bronze from 0, Silver from 300, Gold from 1,000 Points.
- **Incentives:** Everyday Earn gives 1 Point per 1.00 spent on eligible products at participating stores. Fifth Visit Bonus gives 50 Points and the Regular badge for 5 visits in 30 days.
- **Rewards:** Free Coffee (150), 10% Off Next Visit (300), Tote Bag (800).
- **Products:** Latte, Croissant, House Beans 1 kg, and Gift Card. The Gift Card doesn't earn points.
- **Stores:** Downtown, and Airport Kiosk (not participating).
- Times are in UTC.

## 4. Things to try

Reading:

1. "What loyalty program is in the playground, and what are its tiers and rewards?"
2. "Show me Ana Souza's points, tier, badges and recent purchases."
3. "How close is Chloe Martin to the Fifth Visit Bonus?"
4. "Why didn't David Kim earn points on his last purchase?"
5. "Who is in the VIP segment?"

Writing (use **Emma Rossi** only):

6. "Register a sale for Emma Rossi at the Downtown store: 2 lattes and a croissant. How many points did she earn?"
7. "Can Emma afford a Free Coffee? If yes, redeem one."
8. "Register a new member in Bean & Leaf Rewards: Liam Novak, [liam.novak@example.com](mailto:liam.novak@example.com)."
9. "Create a product Iced Tea (code ICED-TEA, category Drinks) that earns points."
10. "Create a reward Free Muffin that costs 200 Points."
11. "Create a badge Early Bird in Bean & Leaf Rewards and give it to Emma Rossi."
12. "Create a list segment called Coffee Fans and add Emma Rossi to it."

Please don't post sales or redemptions for Ana, Ben, Chloe or David.
