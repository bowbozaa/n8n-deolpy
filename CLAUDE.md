# CLAUDE.md

This file provides guidance to Claude Code when working with this repository.

## Project Overview

This is an n8n deployment project. n8n is a workflow automation tool that allows you to connect various services and automate tasks.

## Project Structure

```
n8n-deolpy/
├── README.md          # Project documentation
└── CLAUDE.md          # Claude Code instructions
```

## Development Guidelines

- Follow infrastructure-as-code best practices
- Use descriptive names for workflows and configurations
- Document any environment variables or secrets required
- Test deployments in a staging environment before production

## Common Tasks

- **Setup**: Configure deployment environment and dependencies
- **Deploy**: Deploy n8n instance to target infrastructure
- **Update**: Update n8n version or configuration
- **Backup**: Backup workflows and credentials

## Environment Variables

Document any required environment variables here:
- `N8N_HOST` - Host URL for n8n instance
- `N8N_PORT` - Port number (default: 5678)
- `N8N_PROTOCOL` - http or https

## Notes

- Keep sensitive data out of version control
- Use secrets management for credentials
