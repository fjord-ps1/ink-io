# Product Requirements Document (PRD)
## Project: ink-io

---

## 1. Overview

### Project Description
ink-io is a browser-based **Draw & Guess** multiplayer game.  
Players can join public lobbies, create private games, or instantly join a random lobby.

The core gameplay revolves around drawing, guessing, and social interaction, with a strong focus on visual quality, smooth drawing mechanics, and a modern, playful UI.

The project is currently under active development.

---

## 2. Core Goals

### Primary Objective
Create a Draw & Guess game that significantly improves upon existing games like scribble.io by focusing on:

- Superior UI and visual polish
- Smoother and more advanced drawing tools
- Better overall user experience

The goal is not just functional parity, but a noticeably more modern and enjoyable experience.

---

## 3. Target Audience

- Primary audience: players aged **8–25**
- Strong appeal to people interested in drawing and creative games
- While skewed towards younger and more casual players, the game is designed to be accessible and fun for all ages

---

## 4. Gameplay & Mechanics

### Game Flow
- All players start with **0 points**
- A random player is selected as the first drawer
- The game proceeds in rounds
- Players guess the drawn word via chat
- Points are awarded based on correct guesses and timing

(The exact scoring system will be refined during development.)

---

### Lobby Types

#### Private Lobbies
- Joinable via invite link or a **6-digit lobby code**
- Full control over settings
- Anti-cheat and content filtering can be toggled

#### Public Lobbies
- Discoverable in a lobby browser
- Automatically enforce moderation features
- Can be filtered by:
  - Language
  - Player count
  - Game settings

#### Quick Join
- Automatically joins the fastest available lobby
- Uses browser or region data when available
- Defaults to English if no language data is available

---

## 5. Lobby Configuration Options

When creating a lobby, the host can configure:

- Maximum players (2–20)
- Language of words
- Drawing time per round
- Number of rounds (2–20)
- Number of word choices for the drawer (1–5)
- Number of hints revealed per round (0–5)
- Game modes (planned feature)

---

## 6. Drawing System

The drawing experience is a core differentiator.

Planned tools include:
- Color palette selection
- Recently used color history
- Brush size selection (1–5)
- Undo / Redo buttons
- Keyboard shortcuts:
  - Undo: `Ctrl + Z`
  - Redo: `Ctrl + Shift + Z`

The system is designed to be expandable with additional tools in the future.

---

## 7. Words & Content

### Word Sources
- Initial implementation uses a **manual word list**
- Future expansions may include:
  - Dictionary-based word pools
  - AI-generated word selection (premium feature)

---

### Custom Words
- Lobby hosts can enter custom word lists
- Hosts can choose:
  - Mixed (custom + default words)
  - Custom-only words
- Custom word lists require a minimum of **40 words**
- Words are entered as a comma-separated list

---

### Content Moderation
- Public lobbies automatically enforce content filtering
- Initial implementation uses a static banned-word list
- Future implementation includes an **AI-based anti-slur system**
- Moderation applies to:
  - Chat messages
  - Canvas content (text detection)
- Violations result in message removal and player kick

Private lobbies can toggle moderation features on or off.

---

## 8. Anti-Cheat

Anti-cheat systems are enforced automatically in public lobbies.

Examples:
- Detecting word leaks or partial reveals in chat
- Preventing players from bypassing guessing rules
- Detecting tampering via browser developer tools

Private lobbies can disable anti-cheat if desired.

---

## 9. Technology Stack

### Frontend
- React (chosen for familiarity and flexibility)

### Backend
- To be determined
- Likely Node.js-based solution

### Database
- Undecided
- MySQL is a potential candidate

### AI
- Planned for moderation and word generation
- Must use monetization-safe models (e.g. open or permissive licenses)

---

## 10. Server & Infrastructure

### Hosting
- Initial development hosted locally
- Scales to cloud hosting as player base grows

### Scalability
- Multiplayer handling and synchronization to be designed
- Server architecture will evolve with demand

---

## 11. Platform Support

- Primary platform: Web browser
- Future plans:
  - Mobile app (cross-play with browser users)
  - Distribution on browser game platforms (e.g. Poki, CrazyGames, Y8)

---

## 12. Customization & Accounts

### User Identity
- Guest login with custom username
- Planned integrations:
  - Google login
  - Discord login
- Optional account system for:
  - Persistent stats
  - Cosmetics
  - Premium features

---

### Cosmetics & Premium
- Cosmetic items:
  - Avatars
  - Backgrounds
  - Brush skins
- Some cosmetics are unlockable for free
- Premium features planned but not required to enjoy the game

---

## 13. Monetization

- Game remains **free to play**
- Monetization methods:
  - Interstitial ads when joining games
  - Ads after game completion
  - Small persistent banner ads
- Optional donations via Buy Me A Coffee
- Marketing primarily via social media platforms

---

## 14. Development Plan

### Phases
1. Prototype
2. UI / UX
3. Backend implementation
4. Licensing & legal checks
5. Closed beta testing
6. AI & premium features
7. Public launch
8. Ongoing updates

---

## 15. Team
- Solo developer
- UI feedback and beta testing support from family members
