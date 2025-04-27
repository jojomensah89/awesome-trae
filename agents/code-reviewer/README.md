# Code Reviewer Agent

This directory contains a custom Trae agent specialized in code review, finding bugs, security vulnerabilities, and suggesting improvements.

## Contents

- `agent.md` - Contains the agent prompt, recommended MCP servers, and usage examples

## Quick Start

To use this agent in Trae IDE:

1. Create a new agent using the Settings > Agents menu
2. Name it "Code Reviewer" or similar
3. Copy the prompt from `agent.md`
4. Add the recommended MCP servers
5. Save your configuration

You can then invoke the agent with `@CodeReviewer` in the chat.

## Example Use Cases

- Reviewing pull requests before merging
- Auditing code for security vulnerabilities
- Improving code quality in legacy systems
- Learning best practices through code review feedback