
docker documentation ⇒ [link](https://hub.docker.com/r/mcp/github)

start my server locally
```sh
docker run -i  --rm  -e GITHUB_PERSONAL_ACCESS_TOKEN=$GITHUB_PERSONAL_ACCESS_TOKEN github-mcp
```

### Using remote MCP 


```json
{
  "servers": {
    "github": {
      "type": "http",
      "url": "https://api.githubcopilot.com/mcp/",
      "headers": {
        "Authorization": "Bearer ${input:github_mcp_pat}"
      }
    }
  },
  "inputs": [
    {
      "type": "promptString",
      "id": "github_mcp_pat",
      "description": "GitHub Personal Access Token",
      "password": true
    }
  ]
}

```

### Using docker configurations

```json
{
  "inputs": [
    {
      "id": "github_pat",
      "description": "GitHub personal access token",
      "type": "promptString",
      "password": true
    }
  ],
  "servers": {
    "github": {
      "type": "stdio",
      "command": "docker",
      "args": [
        "run", "-i", "--rm", "-e", "GITHUB_PERSONAL_ACCESS_TOKEN",
        "ghcr.io/github/github-mcp-server"
      ],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "${input:github_pat}"
      }
    }
  }
}
```