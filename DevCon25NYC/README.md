# AI Native DevCon '25 NYC: Supercharge Your Coding Agents

**When:** November 18th, 3:35-5:35pm (2 hours)
**Format:** Short intro + hands-on workshop

You've heard of "Spotify Wrapped", "Apple Music Replay", and "YouTube Music Recap".

Now it's time to make _"Your Wrapped."_

## Workshop Goal

Use an AI coding agent (Cursor, Claude Code, Copilot, etc.) to create a personalized year-in-review dashboard using your own interesting data.

Focus on creativity, having fun, and experimentation rather than technical perfection! You'll have two hours to build something personal and potentially demo it to others if you'd like.

### What You'll Learn

* How to work effectively with AI coding agents
* Using Tessl's registry to give your agent better context about libraries
* Rapid prototyping and iteration with AI assistance
* Sharing tiles and patterns with other workshop participants

### What to Bring

* **Your own AI agent setup** - Cursor, Claude Code, GitHub Copilot, or any agent you prefer (see [TIPS.md](TIPS.md) for options)
* **Your own API keys** - We won't be providing keys; use your personal accounts
* **Personal data** - Download/export data from any service you want to analyze (see ideas below)
* **Creativity** - The most important thing!

### Prerequisites

Before the workshop, make sure you have:
1. Git installed on your machine
2. Cloned or forked this repository (see main [README](../README.md) for instructions)
3. Your preferred AI coding agent installed and configured
4. Optionally: Tessl CLI installed (`npm install -g @tessl/cli`)

## What is Tessl?

Tessl is an agent enablement platform that helps you get more out of coding agents by providing them with better context. It offers:

* **Public Registry**: Version-aware usage documentation on 10,000+ open-source libraries
* **Usage Specs (Tiles)**: Structured documentation that agents can use to understand libraries and APIs correctly
* **MCP Integration**: Works with most coding agents (Claude Code, Cursor, etc.) via Model Context Protocol

**How it works:**

Set up & install the Tessl CLI tool & MCP server by following [the quick start guide](https://docs.tessl.io/introduction-to-tessl/quick-start-guide).

**Learn more:**
* [What is Tessl?](https://docs.tessl.io/overview/readme)
* [Quick Start Guide](https://docs.tessl.io/introduction-to-tessl/quick-start-guide)
* [Better Code with Usage Specs](https://docs.tessl.io/common-workflows/better-code-with-usage-specs)

## Data Source Ideas

Here are some ideas for data sources you can use:

**Financial Data:**
* **Banking/Credit Cards**: Download CSV exports from your bank or credit card (Chase, Bank of America, Capital One, etc.)
  - Spending by category, merchant patterns, monthly trends
  - Where did most of your money go in 2025?
* **Venmo/PayPal/Zelle**: Export your payment history
  - Who do you exchange money with most often?
  - What were your most common payment descriptions?

**Social & Communication:**
* **Email**: Export from Gmail, Outlook, or Thunderbird (mbox format)
  - What time of day do you send the most emails?
  - Who are your top correspondents?
  - Longest email threads?
* **Text Messages**: Export from your phone
  - Message volume over time, top contacts
  - Response time patterns
* **Social Media**: Request data download from Twitter/X, Instagram, Facebook, LinkedIn
  - Posts per month, engagement trends
  - Your most popular content

**Entertainment & Media:**
* **Streaming Services**:
  - Spotify: Use Spotify API or request data download for listening history
  - Netflix/Hulu: Viewing history data
  - YouTube: Watch history from Google Takeout
  - Apple Music: Request your library data
  - Plex/Jellyfin: Export watch history from your media server
* **Gaming**:
  - Steam: Use Steam API for play time stats
  - PlayStation/Xbox: Export your gaming activity
  - Nintendo Switch: Check your year-in-review data

**Health & Fitness:**
* **Apple Health/Google Fit**: Export health data
  - Steps, workouts, heart rate, sleep patterns
  - Did you meet your goals?
* **Strava**: Running/cycling activities via API
* **MyFitnessPal/Cronometer**: Nutrition tracking data
* **Peloton/Mirror**: Workout history and stats

**Transportation:**
* **Car Data**: Many modern cars (BMW, Tesla, Ford) offer data downloads
  - Miles driven, trips taken, charging patterns
  - Fuel efficiency over time
* **Uber/Lyft**: Request ride history
  - Most visited locations, total spending, time in rides
* **Public Transit**: Many transit apps (Ventra, Clipper, OMNY) have history exports
* **Flight Tracking**: TripIt, Google Flights history, or airline frequent flyer data

**Productivity & Digital Life:**
* **Calendar**: Google Calendar, Outlook Calendar exports
  - Meeting time analysis, busiest days
  - Work/life balance visualization
* **GitHub**: Contributions, commits, pull requests via API
  - Your coding patterns and activity
* **RescueTime/Screen Time**: Digital wellness data
  - App usage, productive vs. distracting time
* **Amazon**: Order history (available in your account settings)
  - Spending patterns, most-ordered categories

**Food & Dining:**
* **DoorDash/Uber Eats/Grubhub**: Request order history
  - Favorite restaurants, spending on delivery
  - What time do you order most often?
* **Yelp**: Review history and check-ins
* **OpenTable**: Restaurant reservation patterns

**Reading & Learning:**
* **Kindle**: Reading history and highlights
* **Goodreads**: Books read, ratings given
* **Pocket/Instapaper**: Articles saved and read
* **Audible**: Audiobook listening stats

**Home & Life:**
* **Smart Home**: Data from Nest, Ring, Philips Hue
  - Home/away patterns, energy usage
* **Weather**: Personal weather station data
* **Photos**: Analyze your photo library metadata
  - Most photographed locations, time of day patterns

## Setup

1. **⚠️ Put your data in the `data/` folder**
   ```bash
   cp ~/Downloads/my-transactions.csv data/
   ```
   The `data/` folder is gitignored to prevent committing personal data.

2. **Install Tessl CLI** (optional but recommended)
   ```bash
   npm install -g @tessl/cli
   tessl init  # Authenticate and configure your agent for MCP
   ```
   You'll be invited to the workshop workspace during setup!

3. **Set up your AI agent**
   See [TIPS.md](TIPS.md) for setup instructions. Optionally use [.mcp.json.example](.mcp.json.example) to configure MCP servers.

4. **Check examples**
   Browse [examples/](examples/) for inspiration.

## Getting Started

Once you've chosen a data source from the ideas above:

1. **Parse your data**: Ask your agent to help you load and parse the data
2. **Build the dashboard**: Create visualizations and insights
3. **Add some flair**: Make it fun and personal!
4. **Optional demo**: Share your "Wrapped" dashboard at the end if you'd like!

Remember: This is about **vibe coding** and having fun! The goal isn't technical perfection - it's creating something personal and interesting in two hours. Get creative!

## Leveraging Tessl Tiles

The Tessl registry has tiles (usage specs) that can help you build faster and with fewer errors.

Running `tessl init` will automatically scan your dependencies and pull in any Tessl tiles that exist for them to help your agent work better with those dependencies.

Alternatively, you can manually search for tiles:

```bash
tessl search react          # For React components
tessl search nextjs         # For Next.js apps
tessl search vue            # For Vue.js
tessl search recharts       # For data visualization
tessl search chartjs        # Alternative charting library
tessl search tailwind       # For Tailwind CSS styling
```

Or ask your agent:
```
Search the Tessl registry for Next.js and Recharts tiles and install them
```

### Workshop Tessl Workspace

Once you've logged in to Tessl with `tessl login`, please share your username with us in the Discord thread so we can add you to the workspace we'll use for collaborating in this workshop. You can find your username by running `tessl whoami`.

*Top tip: you can change your username from [https://tessl.io/account](https://tessl.io/account)*

Once you're in, you can:
- **Discover tiles** created by other workshop participants in real-time
- **Publish your own tiles** to share useful patterns with others
- **Search for tiles other attendees have published**

**You'll receive a workspace invitation during the workshop setup!**

### Creating and Publishing Tiles to Tessl Registry

If you create something reusable during the workshop, consider publishing it as a tile:

**What could make a useful Tile?:**
- Coding guidelines (how to structure tests, how to organise files)
- Agent style choices (always ask me for confirmation, talk like a pirate)
- Styling systems (color schemes, typography patterns)
- Security patterns (data sanitization, gitignore templates)
- Reusable UI patterns (carousel layouts, card designs, etc.)

**How to publish:**
1. Ensure you have been invited into the workshop workspace
2. Create a directory with one or more markdown files to describe your instructions to the agent
3. In this directory, also create `tile.json` with the below format
4. Run `tessl publish path/to/tile/directory` to publish your tile to the workshop's workspace to share with other workshop attendees

Example `tile.json`:

```json
{
  "name": "aindworkshop/<tile-name>-<user-name>", // give your tile a unique name appended with your name
  "version": "0.1.0", // you can increment this to publish new updates
  "summary": "<brief-description>", // e.g. ""A colorful logging formatter for pretty terminal output."
  "steering": { // map of instructions for the agent for your tile
    "instruction-name": {"rules": "instruction-file.md"},
  },
  "private": true
}
```

Once published, other workshop attendeed will be able to search for it and install it: `tessl search wrapped-carousel`.

**Naming convention:** Use your name or GitHub username as a suffix to avoid collisions (e.g., `wrapped-vaporwave-theme-alan`)

### Ideas for Tiles you could publish

#### Mobile & UI Pattern Tiles

For specific UI patterns, search for:
- Carousel/swiper libraries for that mobile "swipe through your year" feel
- Animation libraries for smooth transitions
- Mobile-first responsive design patterns

#### Fun & Creative Styling Ideas

Get creative with your dashboard! Try prompting your agent with style suggestions, and look for relevant tiles:

**Retro vibes:**
- "Style this in Windows 95 aesthetic with nostalgic UI elements"
- "Make it look like a Geocities page from 1999"
- "Design it like an old terminal/DOS interface"

**Modern trends:**
- "Use a brutalist design style"
- "Make it look like a Bento grid layout"
- "Include brain rot aesthetics" 💀
- "Style it like a vaporwave music video"

**Accessibility & themes:**
- "Use an accessible color scheme that works for colorblind users"
- "Create a dark mode version"
- "Make it dyslexia-friendly with appropriate fonts"
- "Use high contrast colors for better readability"

**Data visualization styles:**
- "Present data in infographic style"
- "Make charts look hand-drawn/sketchy"
- "Use a minimalist data-ink ratio approach"

### Security Reminders

When building with personal data:
- ⚠️ **Always put personal data in the `data/` folder** (it's gitignored)
- Run `git status` before committing to verify no personal files are staged
- Don't commit API keys or tokens (use `.env.local`, not `.env`)
- If deploying publicly, make sure no personal data is exposed in the build
- When sharing tiles, never include actual personal data - only code patterns

## After the Workshop

### Share Your Work!

If you created something cool:

1. **Commit to your fork:**
   ```bash
   git add .
   git status  # Double-check no personal data is included!
   git commit -m "Add my 2025 wrapped dashboard"
   git push origin main
   ```

2. **Don't create PRs to the main repo** - Your personal projects should stay in your fork

3. **Share your fork!**
   - Post your fork URL on social media
   - Show others what you built
   - Inspire future workshop participants

### Publish Your Tiles

If you created reusable tiles during the workshop:
- Keep them published in the Tessl registry for others to use
- Update documentation if you improve them later
- Share them in the AI Native Dev community

### Star the Repo

If you found this workshop helpful, ⭐ **star the repository** at [AI-Native-Dev-Community/AIND-Workshops](https://github.com/AI-Native-Dev-Community/AIND-Workshops) to help others discover it!
