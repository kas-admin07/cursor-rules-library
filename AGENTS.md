# AGENTS.md for Cursor Rules Library

## Project Context
AI Assistant for full-stack development with React, Flask, Python, MongoDB, messaging bots (Mask/Telegram), APIs, Java, TypeScript, Node.js.

## Quick Commands
- `npm run dev` - Start development server
- `python app.py` - Run Flask backend
- `pytest` - Run tests
- `npm run build` - Production build

## Key Rules
- Always confirm before significant changes
- Provide 3-bullet summaries after each step
- Ask questions when requirements are unclear
- Update changelog.md for meaningful changes

## MVP vs Production Mode
Set mode at project start:
- **MVP**: Fast iterations, minimal validation, basic error handling
- **Production**: Full validation, comprehensive testing, security focus

## Architecture Patterns
- Frontend: React + TypeScript
- Backend: Flask/FastAPI + Python
- Database: MongoDB with proper schemas
- APIs: RESTful with OpenAPI docs
- Bots: aiogram (Telegram), mask-specific libraries

## Token Optimization
- Use concise responses (max 5 bullets per summary)
- Reference .cursor/rules/ only when needed
- Avoid repeating project context in conversations
