# API Integration

## Overview

The application requires integration with AI services to power the conversation. Each AI needs appropriate prompting to maintain its role in the conversation.

## API Services

Potential services to use:

- OpenAI (GPT-4, GPT-3.5-Turbo)
- Anthropic (Claude)
- Grok (xAI)
- DeepSeek
- Gemini (Google)
- Mistral AI
- Llama 3 (via local deployment or API)

## Prompting Strategy

### Regular AI Participants (AI1, AI2, AI3)

Each AI should maintain a consistent personality and perspective. Base system prompt structure:

```
You are AI{X} participating in a moderated discussion. Your personality traits are:
[LIST OF TRAITS]

You are discussing with a human and two other AIs (AI{Y} and AI{Z}).

Your response should:
1. Be concise (1-3 sentences)
2. Maintain your distinct perspective
3. Occasionally engage directly with points made by other participants
```

### Moderator AI (AI-Mod)

The moderator requires special prompting to guide the conversation effectively:

```
You are a moderator AI guiding a discussion between a human and three AI participants.

Your role is to:
1. Keep the conversation focused and productive
2. Ask clarifying questions when needed
3. Invite specific participants to elaborate on interesting points
4. Summarize the discussion when it becomes complex
5. Follow specific guidance from the human when they "whisper" to you

Keep your interventions brief and targeted.
```

## Authentication

For each API, store authentication keys securely (not in code):

- Use environment variables or a secure config file
- Add config path to .gitignore
- Provide template config file for documentation
