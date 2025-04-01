---
layout: page
title: AI Dungeon Master for Tabletop RPGs
permalink: /my-projects/dnd-ai-adventure/
---

# AI Dungeon Master for Tabletop RPGs

## Project Overview

This project is an innovative web application that leverages artificial intelligence to enhance the Dungeons & Dragons (D&D) experience. Built on the .NET platform, it serves as an AI Dungeon Master, generating dynamic adventures, NPCs, and plot twists in real-time.

## Key Features

1. **Dynamic Adventure Generation**: Uses AI to create unique, on-the-fly adventures tailored to player choices and party composition.
2. **NPC Creation and Interaction**: Generates diverse NPCs with distinct personalities and backstories.
3. **Real-time Plot Twists**: Introduces unexpected elements to keep the story engaging and challenging.
4. **Voice Synthesis for NPC Dialogue**: Brings characters to life with AI-generated voices.
5. **Procedural Map Generation**: Creates detailed, context-appropriate maps for various settings.
6. **Player Decision Impact Tracking**: Analyzes and incorporates player choices to shape the ongoing narrative.

## Technical Stack

- **Backend**: C#, ASP.NET Core
- **AI Integration**: OpenAI API
- **Database**: SQL Server (for campaign management and persistence)
- **Frontend**: Blazor WebAssembly (for interactive UI components)

## Implementation Details

### AI Adventure Engine
- Utilizes OpenAI's GPT model to generate coherent and context-aware story elements.
- Implements custom prompt engineering to ensure D&D-specific content and rules adherence.

### Voice Synthesis
- Integrates with Azure Cognitive Services for Text-to-Speech capabilities.
- Matches voice characteristics to NPC attributes for immersive dialogue delivery.

### Procedural Map Generation
- Custom algorithm for creating varied and logical dungeon layouts, town maps, and wilderness terrains.
- Integrates with the story generation to ensure map relevance to the current adventure.

### Player Choice Analysis
- Tracks player decisions and party actions.
- Uses machine learning models to predict potential story directions and generate appropriate content.

## Development Challenges and Solutions

1. **Maintaining Narrative Coherence**: Implemented a context management system to ensure AI-generated content remains consistent throughout the campaign.
2. **Performance Optimization**: Used caching strategies and asynchronous processing to handle real-time AI responses without impacting user experience.
3. **Balancing AI Creativity with D&D Rules**: Developed a rules-checking module to validate AI-generated content against D&D 5e ruleset.

## Future Enhancements

- Integration with virtual tabletop platforms for seamless online play.
- Expansion of the AI model to include more game systems beyond D&D.
- Implementation of a collaborative storytelling mode where multiple human players can contribute to the narrative alongside the AI.

This project showcases the integration of cutting-edge AI technology with traditional tabletop gaming, demonstrating skills in backend development, AI implementation, and creating interactive web applications.
