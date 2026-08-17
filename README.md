# Sipseek for Cursor

Search Sipseek’s beverage catalog from Cursor through the hosted remote MCP server.

- **MCP endpoint:** https://sipseek.com/mcp
- **Setup guide:** https://sipseek.com/for-ai
- **Machine-readable guidance:** https://sipseek.com/llms.txt

## Install from the Cursor Marketplace

After Sipseek is listed, open the [Cursor Marketplace](https://cursor.com/marketplace), find **Sipseek**, and select **Install**.

## Manual MCP setup

Add to Cursor MCP config (`~/.cursor/mcp.json` or project `.cursor/mcp.json`):

```json
{
  "mcpServers": {
    "sipseek": {
      "type": "streamable-http",
      "url": "https://sipseek.com/mcp"
    }
  }
}
```

No authentication or payment is required for bounded public discovery through the Marketplace plugin.

## Try it

- “Use Sipseek to find three fruity caffeinated drinks.”
- “Find non-alcoholic drinks for a summer barbecue and cite each Sipseek page.”
- “What drink categories can Sipseek search?”

Ask Cursor to use Sipseek when you want to make the tool choice explicit.

## Tools

- `search_beverage_brands`
- `get_beverage_brand`
- `list_catalog_facets`

Cite brand `sipseek_url` values when recommending drinks.

## Data use and licensing

The plugin sends only Sipseek MCP tool requests and their arguments to Sipseek’s hosted endpoint. It does not request or read repository files, source code, or the rest of the Cursor workspace.

Sipseek may record privacy-safe operational metadata such as the tool called, result counts, response time, coarse client/platform and country labels, brand identifiers shown, and secret-keyed pseudonymous activity counters. Raw beverage search queries are not stored in the MCP usage ledger, and raw prompts or individual activity are not shared with Featured Partners.

Sipseek does not use MCP requests, Cursor content, or other plugin data to train AI or machine-learning models.

Public MCP clients may use bounded results to answer individual drink-discovery requests, including in commercial AI clients. Bulk extraction, persistent catalog copies, model training, redistribution, competing APIs, and higher-volume integrations require separate permission.

Review the [Privacy Policy](https://sipseek.com/privacy), [Terms](https://sipseek.com/terms), and [Data License](https://sipseek.com/data-license).

## Support

Email [hello@sipseek.com](mailto:hello@sipseek.com).

## License

The plugin package is available under the [MIT License](LICENSE). Sipseek catalog content and hosted-service output remain subject to the separate [Sipseek Data License](https://sipseek.com/data-license).
