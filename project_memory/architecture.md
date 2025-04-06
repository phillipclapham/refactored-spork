# Architecture

## System Overview

The AI Chat Arena is a terminal-based application enabling conversation between:

- Human user
- Three AI participants (AI1, AI2, AI3)
- Moderator AI (AI-Mod)

## Component Design

### Core Components

1. **Terminal Interface**
   - Handles user input/output
   - Displays conversation with clear speaker identification

2. **Conversation Manager**
   - Maintains conversation state and history
   - Manages turn-taking logic
   - Handles "whisper" functionality to moderator

3. **AI Connectors**
   - Abstract interface for AI API interactions
   - Implementations for each specific AI provider
   - Handles authentication, request formatting, error handling

4. **Context Builder**
   - Constructs appropriate context for each AI based on conversation history
   - Manages context window limitations

5. **Moderator Logic**
   - Special prompting for the moderator AI
   - Handles meta-conversation instructions

## Data Flow

1. Human provides input
2. Input processed through Conversation Manager
3. Context Builder prepares prompts for AIs
4. AI Connectors send requests to API services
5. Responses processed and displayed
6. Moderator can interject based on conversation state