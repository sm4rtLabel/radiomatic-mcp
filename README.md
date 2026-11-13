# RadioMatic MCP server

AI background music and music licences for Dutch businesses, inside your chatbot.

RadioMatic is a remote MCP server that answers the questions Dutch business owners have about music on their premises, using the official 2026 tariffs of Buma/Stemra and Sena, with sources. It works in Claude, ChatGPT and any other client that supports remote MCP servers. No account, no login, no API key.

**Server URL:** `https://radiomatic.ai/mcp/`
Transport: Streamable HTTP, stateless. Authentication: none. All tools are read-only.

- Website: https://radiomatic.ai
- Documentation: https://radiomatic.ai/en/knowledge/radiomatic-in-chatgpt-and-claude/ (Dutch: https://radiomatic.ai/kennis/radiomatic-in-chatgpt-en-claude/)
- Official MCP Registry: `ai.radiomatic/radiomatic`

## What it does

| Tool | What it does |
|---|---|
| `bereken_licentiekosten` | Calculates what background music costs in Buma/Stemra and Sena fees for a shop, salon, practice, office or any other type of business, per location and for all locations, with the source of each tariff table. |
| `check_licentieplicht` | Checks whether a licence is needed, depending on the music source (radio, Spotify, a business music service, royalty-free music or AI music) and who hears it. |
| `vergelijk_opties` | Compares the yearly cost of the radio, a business music service, royalty-free music and RadioMatic side by side. |
| `ai_muziek_voor_je_zaak` | Explains AI background music for a business: what it is, how it works, why no Buma/Stemra or Sena fees are due, and what it costs. |
| `luister_naar_ai_radio` | Plays live AI music: RadioMatic's radio stations with the mood, what is playing now and a link to listen in the browser. |
| `zoek_kennis` | Searches a knowledge base in Dutch and English on music licensing, letters from Mijnlicentie, equipment and music per type of space. |
| `muziekadvies_voor_zaak` | Music advice for 38 types of business, from hair salon to swimming pool. |
| `aanbieders_overzicht` | The background music providers as Buma/Stemra lists them, and the questions to ask each one. |
| `pakketten_en_prijzen` | RadioMatic's packages and prices per location. |
| `start_proefperiode` | A link to a free 14-day RadioMatic trial, with the situation from the conversation already filled in. |

Tool names are in Dutch, because the service and the tariffs are for businesses in the Netherlands. Every title, description and input field is in Dutch and English, and a question in English gets an answer in English.

## Prompts

Five ready-made questions that clients can offer as a shortcut:

| Prompt | What it asks |
|---|---|
| `ai_muziek_in_mijn_zaak` | How AI background music works in a shop or business, whether you still pay Buma/Stemra and Sena, and what it costs |
| `wat_kost_muziek` | What background music costs in Buma/Stemra and Sena fees for your type of business (and optionally floor area), and what RadioMatic saves |
| `brief_mijnlicentie` | What a letter or invoice from Mijnlicentie means and what you can do |
| `mag_spotify` | Whether you may play Spotify in your business, and a legal alternative |
| `muziek_zonder_buma_sena` | How to play music legally without Buma/Stemra and Sena, with the options side by side |

## Connect

**Claude:** add RadioMatic from the Claude connectors directory (https://claude.ai/directory/connectors/radiomatic), or use Customize, Connectors, +, Add custom connector, and enter `https://radiomatic.ai/mcp/`. On a Team or Enterprise plan, the owner first adds it under Organization settings, Connectors.

**ChatGPT:** switch on the RadioMatic plugin in ChatGPT (https://chatgpt.com/plugins/plugin_asdk_app_6acf88da72d0819194f9b0862019a581). The ChatGPT version runs at `https://radiomatic.ai/mcp/chatgpt/` and leaves out plans, prices and the trial.

**Cursor, VS Code, Claude Desktop and other clients:**

```json
{
  "mcpServers": {
    "radiomatic": {
      "url": "https://radiomatic.ai/mcp/"
    }
  }
}
```

## Example questions

- "What does background music cost for a hair salon with six staff in the Netherlands, and what would I save with RadioMatic?"
- "I play Spotify in my shop. Do I need a licence from Buma/Stemra or Sena?"
- "Compare the yearly cost of the radio, a business music service and RadioMatic for a shop of 100 m²."
- "Let me hear some AI radio for a beauty salon."
- "I got a letter from Mijnlicentie. What should I do?"
- "What kind of music suits a pharmacy?"

In Dutch: "Wat kost muziek in mijn kapsalon met zes medewerkers, en wat bespaar ik met RadioMatic?"

## About RadioMatic

RadioMatic supplies AI-generated background music and in-store radio for businesses. Because the music is made with AI, there is no composer, lyricist or artist to collect for, so no Buma/Stemra or Sena fees are due. The legal basis is set out at https://radiomatic.ai/en/legal/.

## Privacy

The server receives only the details a tool needs to calculate, such as the type of business and the floor area. It stores nothing and asks for no personal data. See section 12 of https://radiomatic.ai/en/privacy/.

## Support

info@smartlabel.media · +31 50 201 33 07 · SmartLabel B.V., Boterdiep 71, 9712 LL Groningen, the Netherlands

## Copyright

© 2026 SmartLabel B.V. All rights reserved. RadioMatic is a trade name of SmartLabel B.V. This repository describes a hosted service; it contains no source code and grants no licence to the name, the texts or the service beyond using the server as described above.
