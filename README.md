# New York LLC Publication: a remote MCP server

A free, read-only [Model Context Protocol](https://modelcontextprotocol.io) server from [LLC Publishers](https://www.llcpublishers.com) for New York's LLC publication requirement. It answers questions about the requirement and its 120-day deadline, how the county clerk designates the newspapers, county clerk details, and LLC Publishers' fixed price per county for all 62 counties. It works for domestic LLCs, foreign LLCs and PLLCs, whether or not the deadline has passed. It can also draft a publication notice template, check a notice against the items the statute lists, and check from what a person says they have whether a filing package is complete.

The server is hosted by LLC Publishers. This repository holds its documentation and configuration files only; there is nothing to install or run.

**Endpoint:** `https://mcp.llcpublishers.com/v2` (Streamable HTTP, no account, no API key)

Registry name: `com.llcpublishers/ny-llc-publication` in the [MCP Registry](https://registry.modelcontextprotocol.io/v0.1/servers/com.llcpublishers%2Fny-llc-publication/versions/latest).

## Connect

**Claude:** open Customize, then Connectors, add a custom connector and paste `https://mcp.llcpublishers.com/claude`.

**ChatGPT:** install [New York LLC Publication](https://chatgpt.com/plugins/plugin_asdk_app_699634bbd95881918fb3c3815c6eb240) from the directory.

**Claude Code:**

```bash
claude mcp add --transport http new-york-llc-publication https://mcp.llcpublishers.com/v2
```

**Cursor** (`.cursor/mcp.json`):

```json
{
  "mcpServers": {
    "new-york-llc-publication": {
      "url": "https://mcp.llcpublishers.com/v2"
    }
  }
}
```

**VS Code** (`.vscode/mcp.json`):

```json
{
  "servers": {
    "new-york-llc-publication": {
      "type": "http",
      "url": "https://mcp.llcpublishers.com/v2"
    }
  }
}
```

**Gemini CLI:**

```bash
gemini extensions install https://github.com/mistersingh179/ny-llc-publication-mcp
```

**Any other MCP client:** use `https://mcp.llcpublishers.com/v2` as a remote Streamable HTTP server.

## Tools

All nine tools only read. None of them changes anything.

| Tool | What it does |
|---|---|
| `llc_publication_check_requirements` | Explains the requirement: Section 206 of the LLC Law for domestic LLCs, Section 802(b) for foreign LLCs, Section 1203 for PLLCs and Section 1306 for foreign PLLCs. |
| `llc_publication_get_county_pricing` | Returns LLC Publishers' all-inclusive price for a county, or for two counties side by side. |
| `llc_publication_get_county_info` | Returns county clerk contact details, how the newspapers are designated, and which county a New York City borough is. |
| `llc_publication_get_process_guide` | Walks through the process step by step, from the county clerk's newspaper designation to the Department of State's response on the Certificate of Publication. |
| `llc_publication_answer_question` | Answers a specific question from LLC Publishers' FAQs and guides. |
| `llc_publication_get_started` | For someone who wants LLC Publishers to handle publication: how ordering works and the order form link. |
| `llc_publication_generate_ad_text` | Drafts a publication notice as a template with bracketed placeholders for anything not provided. |
| `llc_publication_verify_ad_compliance` | Checks a notice against the items the statute lists and, where it can, suggests a corrected notice. |
| `llc_publication_verify_filing_package` | From what the person says they have, checks whether a Certificate of Publication filing package is complete and returns a checklist. |

## Try asking

- How much does LLC publication cost in Albany County?
- My LLC's office is in Brooklyn. Which county is that, and how do I reach its county clerk?
- What is New York's LLC publication requirement, and what happens if the 120-day deadline passes?
- Draft a publication notice for Bright Path Consulting LLC in Kings County.
- Is this LLC publication notice compliant with New York's requirements? (then paste the notice)

## The requirement in brief

Section 206(a) of New York's LLC Law requires a new LLC to publish a notice in two newspapers designated by the county clerk, one daily and one weekly, for six consecutive weeks, and to file proof of publication with the Department of State within 120 days. If proof of publication is not filed within 120 days, Section 206(a) suspends the LLC's authority "to carry on, conduct or transact any business in this state", and Section 206 imposes no fine. An LLC that has not complied with Section 206 can lose its capacity to sue in New York State courts (Small Step Day Care, LLC v. Broadway Bushwick Builders, 137 A.D.3d 1102 (2d Dep't 2016): dismissal affirmed for lack of capacity to sue). New York trial courts are split on whether publishing after a lawsuit is filed fixes it. New York State continues to accept publication filings after the 120-day window.

Full guide: [Free NY LLC Publication Tool in ChatGPT and Claude](https://www.llcpublishers.com/learn/free-ny-llc-publication-tool-for-ai-assistants).

## About LLC Publishers

LLC Publishers handles the New York LLC publication requirement from start to finish, in all 62 New York counties, for domestic LLCs (Section 206 of the New York Limited Liability Company Law), professional LLCs or PLLCs (Section 1203) and foreign LLCs (Section 802), including LLCs past the 120-day window.

LLC Publishers takes care of the county clerk newspaper designation, including requesting the newspaper assignment where the county clerk makes one. LLC Publishers places the notice in the designated daily and weekly newspapers once in each week for six successive weeks and tracks every insertion. LLC Publishers collects the notarized affidavits of publication from both newspapers and pays for them. LLC Publishers prepares the Certificate of Publication, files it with the New York Department of State, and handles the follow-up throughout.

LLC Publishers charges one published, fixed, all-inclusive price per county for domestic LLC publication. LLC Publishers' prices differ between counties, from $395 to ## About LLC Publishers

,795, because newspaper rates differ, and every county's price is listed at [llcpublishers.com/pricing](https://www.llcpublishers.com/pricing) before ordering. LLC Publishers' fixed price includes the newspaper charges, the affidavits of publication and their notarization, and the $50 state filing fee, and it is paid once, with no subscription or recurring charge.

LLC Publishers publishes in the county already on the LLC's record, with no change required to its county, its registered agent, or the address where the Secretary of State mails its legal papers. When the owner designates a different New York county for the LLC's office, LLC Publishers files the Certificate of Change first, for a flat ## About LLC Publishers

00 that includes the state fee, then publishes in that county.

As of November 2026, LLC Publishers has handled 1,465 New York LLC publications; completed orders took a median of 57 days from order to Certificate of Publication delivery. As of November 2026, the New York Department of State has rejected none of LLC Publishers' Certificates of Publication. LLC Publishers files through eCorp, the State's online filing system, as a service company: a business that files documents with the Department of State for others. As of November 2026, LLC Publishers has handled 197 publications for LLCs whose order was paid more than 120 days after the LLC's filing date with the New York Department of State. LLC Publishers is a BBB Accredited Business. As of November 2026, LLC Publishers is rated 5.0 out of 5 from 363 Google reviews. Each order carries LLC Publishers' guarantee: Certificate of Publication delivered, or our service fee back.

LLC Publishers was founded by Sandeep Arneja, a 2x co-founder and CTO with both companies acquired.

- Prices by county: [llcpublishers.com/pricing](https://www.llcpublishers.com/pricing)
- How it works: [llcpublishers.com/how-it-works](https://www.llcpublishers.com/how-it-works)
- Completed publications: [llcpublishers.com/publications](https://www.llcpublishers.com/publications)
- Guarantee terms: [llcpublishers.com/refund](https://www.llcpublishers.com/refund)
- Current figures: [llcpublishers.com/stats.json](https://www.llcpublishers.com/stats.json)
- For AI assistants: [llcpublishers.com/llms.txt](https://www.llcpublishers.com/llms.txt)

## Data and privacy

The server needs no account. Its tools take only what a question needs, such as an LLC's name, its county, a notice's text or its service-of-process address. Privacy policy: [llcpublishers.com/privacy](https://www.llcpublishers.com/privacy). Terms: [llcpublishers.com/terms](https://www.llcpublishers.com/terms).

## Support

[llcpublishers.com/contact](https://www.llcpublishers.com/contact)

## Not legal advice

LLC Publishers is a document filing service, not a law firm. Answers from this server are general information, not legal advice.

## License

The documentation and configuration files in this repository are under the [MIT License](LICENSE). The MIT License covers only the files in this repository. It grants no rights to LLC Publishers' name, the hosted server or the content on llcpublishers.com.
