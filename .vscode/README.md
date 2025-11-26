# Model Context Protocol (MCP) Configuration

This directory contains configuration for the Model Context Protocol (MCP), which enables the LLM to interact with external services and tools.

## Files

- **mcp.json**: Configuration file defining the MCP servers available to GitHub Copilot.
- **mcp1.png / mcp2.png**: Diagrams illustrating the MCP architecture.

## What is MCP?

The Model Context Protocol (MCP) is a standard for:
- **Connecting LLMs to Data**: Allowing LLMs to retrieve data from backend services via REST/RPC.
- **Tool Execution**: Enabling LLMs to perform actions and manipulate data through defined endpoints.
- **Standardization**: Providing a consistent protocol for request/response formats and authentication between the AI and the system.

## Configuration (`mcp.json`)

The `mcp.json` file in this directory configures the `github` MCP server, connecting Copilot to the GitHub API context.