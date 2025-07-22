# LRN MCP Service

A minimal MCP service for managing courses via HTTP API. Forked for LRN Dev Platform.

---

## Quick Start

1. Install dependencies:
   ```bash
   npm install
   ```
2. Set environment variables:
   - `APP_ENV=dev`
   - `API_TOKEN=your_token`
3. Start the service:
   ```bash
   node index.js
   ```

---

## Integration as MCP Server

You can integrate this service as an external MCP server in your platform or AI system.

**Example configuration (local node):**

```json
{
  "mcpServers": {
    "lrn-mcp-service": {
      "command": "node",
      "args": ["/path/to/lrn-mcp-service/index.js"],
      "env": {
        "APP_ENV": "dev",
        "API_TOKEN": "your_token"
      }
    }
  }
}
```

**Example configuration (npx from GitHub):**

```json
{
  "mcpServers": {
    "lrn-mcp-service": {
      "command": "npx",
      "args": ["github:AdminRHS/lrn-mcp-service"],
      "env": {
        "APP_ENV": "dev",
        "API_TOKEN": "your_token"
      }
    }
  }
}
```

---

## MCP Tools (dev)

- `get_courses`, `get_course`, `create_course`, `update_course`, `get_lessons`, `get_lesson`, `create_lesson`, `update_lesson`, `get_professions`

---

## Example Requests

**Create Course (dev):**

```json
{
  "name": "create_course",
  "arguments": {
    "title": "Course Title",
    "description": "Course description",
    "difficulty": "beginner",
    "modules": [],
    "professions": [],
    "image": "",
    "duration": 60
  }
}
```

---

## Notes

- Only `APP_ENV` and `API_TOKEN` are required.
- API URLs are hardcoded for dev mode.
- Dev: [https://lrn.oa-y.com](https://lrn.oa-y.com)
