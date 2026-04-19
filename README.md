# Ada Project - HTML Variants

A collection of AI assistant variants with different focuses and themes. Each variant is a standalone HTML file that can be opened directly in a browser.

## Variants

### Ada
**Full-featured AI assistant** with comprehensive functionality.

Ada is an AI assistant with specialized variants for different domains - including Ada.Books for literary assistance, Ada.Chat for general conversations, and other focused versions for coffee, students, and Reddit.

- **Features**: Chat interface, notes, reminders, weather lookup, calculator, translator, dark mode
- **Theme**: Sky blue gradient
- **File**: `index.html`
- **Additional**: Includes `Ada.html` and `README.md`

### Ada.Mini
**Bare minimum version** for quick interactions.

- **Features**: Simplified chat interface, dark mode
- **Theme**: Pink gradient
- **File**: `Ada.mini.html`

### Ada.Chat
**Chatbot-focused variant** optimized for conversations.

- **Features**: Chat interface, dark mode
- **Theme**: Blue gradient
- **File**: `index.html`

### Ada.Students
**Student-focused variant** for academic use.

- **Features**: Student-oriented interface, dark mode
- **Theme**: Green apple gradient
- **File**: `index.html`

### Ada.Books
**Book-focused variant** for reading and research.

- **Features**: Book-oriented interface, dark mode
- **Theme**: Red gradient
- **File**: `index.html`

### Ada.Coffee
**Geospatial Hub** with interactive map and location-based information.

- **Features**:
  - Interactive Leaflet map with draggable marker
  - Weather information (Open-Meteo API)
  - Country information (REST Countries API)
  - Global news feed (Actually Relevant News API)
  - Address search functionality
  - State/province detection for all countries
  - Population display in weather card
  - Dark mode
- **Theme**: Coffee/brown gradient
- **File**: `index.html`
- **APIs Used**:
  - Open-Meteo (weather)
  - REST Countries (country info)
  - OpenStreetMap Nominatim (geocoding)
  - Actually Relevant News (news feed)

### Ada.Reddit
**Social Intelligence** for Reddit browsing.

- **Features**:
  - Subreddit search
  - Thread list display via RSS feed
  - Threads open in new tab
  - Dark mode
- **Theme**: Reddit orange gradient
- **File**: `index.html`
- **APIs Used**:
  - Reddit RSS feed via RSS2JSON service

## Usage

### Opening a Variant
Simply open the HTML file in any modern web browser:
- Double-click the HTML file
- Right-click and "Open with" your browser
- Drag and drop into browser window

### No Installation Required
All variants are standalone HTML files with no dependencies:
- No server needed
- No installation required
- Works offline (except for API-dependent features)

### API Requirements
Some variants require internet access for API calls:
- **Ada.Coffee**: Requires internet for weather, country info, and news APIs
- **Ada.Reddit**: Requires internet for Reddit RSS feed
- Other variants: Work completely offline

## Browser Compatibility
Works in all modern browsers:
- Chrome/Edge
- Firefox
- Safari
- Opera

## File Structure
```
HTML's/
├── Ada/
│   ├── Ada.html
│   ├── README.md
│   └── index.html
├── Ada.Books/
│   └── index.html
├── Ada.Chat/
│   └── index.html
├── Ada.Coffee/
│   └── index.html
├── Ada.Mini/
│   └── Ada.mini.html
├── Ada.Reddit/
│   └── index.html
└── Ada.Students/
    └── index.html
```

## Design System
All variants use a consistent design language:
- Clean, modern UI
- Dark mode support
- Responsive layouts
- Smooth transitions
- Consistent color theming per variant

## Technical Details

### AI Fallback System
All Ada variants include an intelligent AI fallback mechanism with automatic provider switching:

**Multi-Provider Support:**
- **Groq** (llama-3.3-70b-versatile) - Fast, open-source LLM
- **Anthropic** (claude-3-5-sonnet-20241022) - Advanced reasoning
- **Google Gemini** (gemini-1.5-flash) - Multimodal capabilities
- **OpenAI** (gpt-4o-mini) - General purpose AI

**How It Works:**
1. When Ada doesn't have an answer from her internal knowledge base, she checks localStorage for previously learned responses
2. If no learned response exists, she tries the first AI provider (Groq)
3. If that provider fails or runs out of quota, she automatically switches to the next provider
4. Successful AI responses are stored in localStorage for future use (marked with "(learned)")
5. Over time, Ada "learns" from AI responses and becomes increasingly self-sufficient

**Learning Mechanism:**
- AI responses are stored in localStorage with domain-specific keys (e.g., `ada_books_learning`)
- Each variant has its own learning database
- Learned responses are retrieved instantly without API calls
- This creates a growing knowledge base personalized to user interactions

**API Keys:**
The system uses pre-configured API keys. To update keys, modify the `API_KEYS` constant in each Ada variant's HTML file.

### Ada.Coffee APIs
- **Weather**: Open-Meteo API (free, no API key required)
- **Country**: REST Countries API (free, no API key required)
- **Geocoding**: OpenStreetMap Nominatim (free, no API key required)
- **News**: Actually Relevant News API (free, no API key required)

### Ada.Reddit APIs
- **RSS Feed**: Reddit RSS via RSS2JSON service (free, no API key required)

### Limitations
- **Ada.Reddit**: Threads open in new tab due to browser security restrictions (CORS/CSP) when using file:// protocol
- **Ada.Coffee**: All features work with file:// protocol

## Notes
- All files can be opened directly from the file system
- No CORS issues for Ada.Coffee (uses APIs that support file:// protocol)
- Ada.Reddit uses RSS feed to avoid CORS issues with Reddit API
- Dark mode preference is saved to localStorage
