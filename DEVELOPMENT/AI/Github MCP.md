

1. Install MCP: [`DOCUMENTATION`](https://github.com/github/github-mcp-server)
2. Use MCP in VSCode: [`DOCUMENTATION`](https://learn.microsoft.com/en-us/visualstudio/ide/mcp-servers?view=vs-2022)
3. 


The GitHub MCP (Model Context Protocol) server facilitates interaction with GitHub repositories using AI agents, such as GitHub Copilot Chat in Visual Studio Code. Here's a tutorial on setting it up and using it:

>[!NOTE]
>**PAT**: Personal Access Token

1. Generate a GitHub Personal Access Token (PAT):

- Navigate to your GitHub profile settings > Developer settings > Personal access tokens.
- Generate a new classic token, providing the necessary permissions for the MCP server to access and perform actions on your repositories.
- Copy and securely save this token because it will be lost after this

2. Install the GitHub MCP Server (in VS Code):

- Open VS Code Insiders (or VS Code with the necessary extensions).
- Go to the Extensions view and search for "MCP servers."
- Locate and install the GitHub MCP server.
- Authenticate using the PAT you generated in the previous step 

3. Configure the MCP Server (Optional, for Workspace-Specific Settings):

- Create a `.vscode/mcp.json` file in your workspace folder.
- Add the JSON configuration for the GitHub MCP server, including your PAT (consider using input variables or environment files for sensitive information).
- Alternatively, use the "MCP: Add Server" command from the Command Palette and choose the GitHub MCP server type. 

4. Using the GitHub MCP Server with Copilot Chat:

- Open Copilot Chat in VS Code (click the icon in the title bar).
- Select "Agent" mode in the prompt box.
- Click the "Tools" icon and select "MCP Server: GitHub" to see available actions.
- Type a command or question related to the action you want to perform (e.g., "create a new issue," "list pull requests," "retrieve repository information").
- The GitHub MCP server will process your request and respond in the chat. You may be prompted for additional information or permissions to complete the action. 

5. Testing the MCP Server Locally (for Custom MCP Servers):

- If you are building your own custom MCP server (e.g., a .NET web app), run the application locally.
- Open Copilot Chat in VS Code and select "Agent" mode.
- Select "Tools" > "Add More Tools..." > "Add MCP Server."
- Choose "HTTP" and provide the local URL of your custom MCP server (e.g., `http://localhost:5093/api/mcp`).
- Give the server an ID and choose to save the configuration to workspace settings.
- In a new Copilot Chat window, interact with your custom MCP server using relevant commands.


### Example

Add a `.vscode/mcp.json` file to your repository and add the following content:
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

And now open the `github copilot` chat and select the `agent mode`