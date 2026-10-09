# ValoNeuf for Claude

**New-build real estate in France, inside Claude.** This plugin connects Claude to
[ValoNeuf](https://valoneuf.com), the map of new-build real estate in France, and adds four
ready-made methods.

## What it does

- **Search** developments on sale by town, département, developer or around an address.
- **Open a development**: available units, floor areas, prices, delivery date.
- **Describe a town's market**: new-build prices, actual sales (DVF), building permits, recent price cuts.
- **Analyse a precise location** (free ValoNeuf account, one analysis per day).
- **Request a call back** from an ADN Family adviser — at the same price as buying directly from the developer, and only with your consent.

Search works without an account. Claude offers to sign in (email and 6-digit code) only when a
tool needs it.

## Skills

| Skill | Use it to |
|---|---|
| `/valoneuf:etude-emplacement` | assess what new-build is worth at an address |
| `/valoneuf:comparer-programmes` | compare two to four developments against the local market |
| `/valoneuf:projet-achat-neuf` | go from a buying project to a shortlist of homes |
| `/valoneuf:preparer-rdv-acquereur` | prepare a meeting with a buyer (professionals) |

## Install (Claude Code)

```bash
claude plugin marketplace add Juli1artha/valoneuf-claude
claude plugin install valoneuf@valoneuf --scope user
```

Then run `claude`, type `/mcp`, select `plugin:valoneuf:valoneuf` and choose **Authenticate**
when you want the account tools.

In claude.ai or the Claude app, you can also add the connector directly: **Customize → Connectors →
Add custom connector**, URL `https://valoneuf.com/api/public/mcp`.

## Data and privacy

Figures come from developers' inventory, French government open data (DVF, Sitadel) and SDES
surveys. ValoNeuf never reads your conversation: it only receives the questions Claude asks it.
Privacy policy: https://valoneuf.com/carte/confidentialite — Documentation: https://valoneuf.com/claude

## Support

valoneuf@adnfamily.com

---

*ValoNeuf est édité par ADN Family. L'immobilier neuf en France dans Claude : programmes, lots,
prix, marché des communes, analyse d'emplacement et demande de rappel par un conseiller.*

License: MIT
