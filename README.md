# n8n-nodes-cryptgeon
N8* custom node for https://github.com/cupcakearmy/cryptgeon
# n8n-nodes-cryptgeon

Cryptgeon community node for n8n - securely share secrets using Cryptgeon CLI.

## Features

- 📝 Send text secrets
- 📁 Send files
- 🔐 Password protection
- ⏱️ Expiration time control
- 👁️ View limits
- 🌐 Custom server support

## Installation

In n8n UI:
1. Settings → Community Nodes
2. Click "Install"
3. Enter: `n8n-nodes-cryptgeon`

## Usage

### Send Text
- Operation: Send Text
- Text: Your secret message
- Minutes: Expiration time
- Password: Optional protection

### Send Files
- Operation: Send File
- File Paths: Comma-separated paths
- Views: Number of views before deletion

### Open Note
- Operation: Open Note
- Note URL: Full URL to the note
- Password: If protected

## Requirements

- Cryptgeon CLI installed globally: `npm install -g cryptgeon`

## Example
```
Input:
{
  "operation": "sendText",
  "text": "My secret",
  "password": "1337",
  "minutes": 30
}

Output:
{
  "success": true,
  "url": "https://cryptgeon.org/note/...",
  "hasPassword": true
}
```

## License

MIT
