---
name: aws-token-acquire-for-java-repo
description: AWS Token Acquiring Skill for Java exclusive repository. This is coupled with the normal organization repository structure of having certain scripts to acquire token 
context: fork
allowed-tools:
 - mcp ChromeDevTools
---

# AWS Token Acquire For Java Repo

This skill allows agents to acquire AWS Token for Java Specific Repositories and allows the agents to use ChromeDevTools MCP to enable chrome utilities during Token refreshes.

**When to use**: Use this skill when the agent is working on a Java repository that requires AWS Token for building, testing, or compiling, and the token has expired.

## Quick Steps

### Agent Runs Token Acquisition Method

Run :

- `assume BeiartfReader@tvlk-build-special`
- `./scripts/assume_role.sh`

This prompts the token to be refreshed.

### (Optional) If Token Requires Human Authentication

- If the token acquisition requires human authentication, the agent uses the ChromeDevTools MCP Server to open the authentication link and notifies the user.
- Once the user authenticates and the token is refreshed, the agent continues with the build, test, or compile process.

## Integrated MCP Servers

This skill allows the agents to also access the ChromeDevTools Effectively.

### ChromeDevTools MCP Server

**When to use**: For opening aws token authentication links for humans to authenticate.

- Open the token session authentication link
- Notify user by running the chrome notification sound

**Important**: Leverage this server only for AWS Token authentication and not anything else.

## When to Use This Skill

Use this skill when:

- AWS Token is expired during building, testing, or compiling
