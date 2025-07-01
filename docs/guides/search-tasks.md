# How to Search for Tasks

The TaskBoard API provides an endpoint to search for tasks using a keyword. This is useful for filtering tasks by name or content.

## Endpoint

`GET /tasks/search?query=your-keyword`

## Example

```bash
curl "https://api.taskboard.com/tasks/search?query=meeting"
```

### Expected Response

```json
[
  {
    "id": "1",
    "title": "Team meeting notes",
    "completed": false
  },
  {
    "id": "2",
    "title": "Schedule meeting with client",
    "completed": true
  }
]
```

> **Tip**: Use specific keywords (e.g., "meeting", "urgent", "client") to narrow down results.
