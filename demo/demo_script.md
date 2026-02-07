# Follow the Money — 3-Minute Demo Script

## 0:00 — 0:30 | The Problem

Five billionaires and two family dynasties control the majority of American news. Most people don't know who owns what they read — or what conflicts of interest come with that ownership.

*Follow the Money* makes this visible. Two AI characters investigate media ownership using real-time data, then debate what it means — out loud.

## 0:30 — 2:00 | Live Demo

1. Open the app at localhost:8000
2. Click **The Washington Post**
3. Watch agents "investigate" in real-time (loading sequence with status messages)
4. Hit **Start Investigation** to hear the conversation
5. Andrew (Reporter) digs into Bezos ownership, Amazon contracts, recent layoffs
6. FJ (Insider) adds industry context, irony, insider perspective
7. Expand any turn to read the full transcript
8. Click the globe logo to go back, select another publication

**Key moment:** The agents reference events from *this week* — the 300 layoffs, Caroline O'Donovan fired from the Amazon beat, Bezos hosting the Defense Secretary at Blue Origin. All found via live web search.

## 2:00 — 2:30 | How It Works

**Claude** powers both agent personalities + web search for real-time data. **Cartesia TTS** gives each character a distinct voice (American reporter, British insider). **Notion** stores the curated ownership database, queried at runtime alongside web search.

6 publications. Each conversation is generated from 3 data sources: curated JSON, Notion database, and live web search.

Pipeline per publication:
1. Data added to publications.json
2. Migrated to Notion database via API
3. Orchestrator feeds data to Claude with web_search enabled
4. Claude's two personalities alternate 4 turns
5. Cartesia TTS converts each turn to audio
6. Saved as pre-baked demo, UI loads instantly

## 2:30 — 3:00 | What's Novel

- **Expressive:** Two distinct voices with real personalities, not generic AI
- **Advanced Reasoning:** Connects ownership to conflicts of interest, government contracts, editorial decisions
- **Situationally Aware:** Every conversation pulls current events via web search
- **Notion Bonus:** Structured ownership data queried from Notion at runtime

Bias and factuality ratings sourced from **Ground News**.

Built by @mmazco for the Cartesia x Anthropic Voice Agents Hackathon, SF Feb 2026.
