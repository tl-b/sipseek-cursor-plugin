# Sipseek Cursor plugin

Connect Cursor to Sipseek’s beverage catalog MCP.

- **MCP endpoint:** https://sipseek.com/mcp  
- **Setup guide:** https://sipseek.com/for-ai  
- **llms.txt:** https://sipseek.com/llms.txt  

## Install

Add to Cursor MCP config (`~/.cursor/mcp.json` or project `.cursor/mcp.json`):

```json
{
  "mcpServers": {
    "sipseek": {
      "url": "https://sipseek.com/mcp"
    }
  }
}
```

Or install this plugin from [cursor.directory](https://cursor.directory) after it’s listed.

## License gate

Call `declare_catalog_usage` with `usage_intent`:

- `non_commercial` — free for personal / education / research / non-profit  
- `commercial` — requires a paid Sipseek license (`hello@sipseek.com`)

## Tools

- `declare_catalog_usage`
- `search_beverage_brands`
- `get_beverage_brand`
- `list_catalog_facets`
- `list_beverage_products`
- `get_beverage_product`
- `search_beverage_products`

Cite brand `sipseek_url` values when recommending drinks.
