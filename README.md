# Ada - AI Assistant with Multiple API Integrations

Ada is a powerful AI assistant that combines multiple free APIs to provide comprehensive information and services. She doesn't rely on paid AI services like OpenAI or Anthropic, making her completely free to use.

## Features

- **💬 Chat Interface**: Clean, modern chat interface with intelligent responses
- **� Notes Tab**: Save and manage personal notes with localStorage persistence
- **⏱️ Reminders Tab**: Set time-based reminders with countdown timers
- **🌤️ Weather Modal**: Current weather information via Open-Meteo API
- **🧮 Calculator Modal**: Mathematical calculations with support for percentages, exponents, and trigonometry
- **� Translator Modal**: Translate text to 14 different languages
- **� Multiple Search APIs**: Wikipedia, DuckDuckGo, Dictionary, Gutendex, and more
- **📎 File Attachments**: Send images, videos, audio, and documents
- **🎤 Speech-to-Text**: Speak your messages instead of typing
- **🔊 Text-to-Speech**: Hear Ada speak her responses
- **🌙 Dark Mode**: Toggle between light and dark themes
- **📚 Knowledge Base**: Load knowledge from GitHub repositories
- **🔄 Auto-read**: Automatically have Ada read her responses
- **💻 Code Snippets**: Pre-built code examples with copy button
- **🎉 Quick Chips**: One-click prompts for common tasks
- **� Toast Notifications**: Feedback for user actions
- **😀 Reactions**: React to messages with emojis
- **🎨 Modern UI**: Beautiful design with CSS variables and smooth animations

## API Integrations

Ada integrates with the following free APIs:

### Dictionary API
- Word definitions and synonyms
- Pronunciation and part of speech
- Examples and usage
- Source: [dictionaryapi.dev](https://dictionaryapi.dev/)

### Gutendex API
- Search for books from Project Gutenberg
- Author information
- Download counts
- Subject categories
- Source: [Gutendex](https://gutendex.com/)

### MediaWiki REST API (Wikipedia)
- Wikipedia article summaries
- Fuzzy matching for misspelled names
- Professional formatting
- Source: [Wikipedia REST API](https://en.wikipedia.org/api/rest_v1/)

### Open-Meteo Weather API
- Current weather data
- Temperature, wind speed, humidity
- Global coverage with geocoding
- Source: [Open-Meteo](https://open-meteo.com/)

### MyMemory Translation API
- Translation to 14 languages
- No API key required
- Source: [MyMemory](https://mymemory.translated.net/)

### DuckDuckGo Search API
- Web search capabilities
- Instant answers
- Related topics
- Fallback when Wikipedia fails
- Source: [DuckDuckGo](https://duckduckgo.com/)

## How It Works

Ada uses a multi-layered approach to answer questions:

1. **Greeting Detection**: Recognizes and responds to common greetings
2. **Fun Facts**: Returns random interesting facts when requested
3. **Weather Lookup**: Checks Open-Meteo API for weather queries
4. **Calculator**: Evaluates mathematical expressions
5. **Translation**: Uses MyMemory API for translation requests
6. **Code Snippets**: Provides pre-built code examples
7. **Dictionary Lookup**: Checks for word definitions
8. **Wikipedia Search**: Uses MediaWiki REST API with fuzzy matching
9. **DuckDuckGo Fallback**: Searches the web if Wikipedia fails
10. **Book Search**: Uses Gutendex for book-related queries
11. **Knowledge Base**: Searches loaded GitHub knowledge files
12. **Professional Formatting**: Applies clarity guidelines to all responses

No paid AI APIs are used - everything runs using free, public APIs.

## Setup

1. Clone or download this repository
2. Open `index.html` in a modern web browser (Chrome, Edge, Firefox, Safari)
3. Ada is ready to use immediately

## Usage

### Chat Tab
- **Ask questions**: Type your question and press Enter
- **Word definitions**: "Define serendipity" or "What does X mean?"
- **Wikipedia queries**: "Who is Barack Obama?" or "What is quantum mechanics?"
- **Book searches**: "Find books by Jane Austen" or "Search for Pride and Prejudice"
- **Weather in chat**: "What is the weather in London?" or "Weather in Tokyo"
- **Calculator in chat**: "Calculate 15% of 240" or "2^10" or "sqrt(144)"
- **Translation in chat**: "Translate hello to French" or "Translate 'good morning' to Spanish"
- **Code requests**: "Write a Python hello world" or "Show me a JavaScript function"
- **Fun facts**: "Tell me a fun fact" or "Surprise me"
- **Greeting responses**: "Hi", "Hello", "How are you?"
- **Quick chips**: Click any chip for instant prompts

### Notes Tab
- Type a note in the text area
- Press Ctrl+Enter or click "Save" to store the note
- Notes are saved to localStorage (persists between sessions)
- Click the × button to delete a note

### Reminders Tab
- Enter what you want to be reminded about
- Select a date and time
- Click "Set Reminder"
- Reminders are saved to localStorage and checked every 10 seconds
- When a reminder triggers, Ada will notify you in chat
- Click the × button to delete a reminder

### Weather Modal
- Click the 🌤️ button in the header
- Enter a city name (e.g., "London", "New York")
- Click "Get Weather"
- View current temperature, wind speed, humidity, and conditions

### Calculator Modal
- Click the 🧮 button in the header
- Enter a mathematical expression (e.g., "2^10", "sqrt(144)", "15% of 200", "sin(90)")
- Click "Calculate"
- View the result

### Translator Modal
- Click the 🌐 button in the header
- Enter text to translate
- Select target language from the dropdown (14 languages available)
- Click "Translate"
- View the translation

### File Attachments
- Click the paperclip icon
- Select files (images, videos, audio, documents)
- Files will be previewed before sending
- Click "Send" to attach files to your message

### Speech-to-Text
- Click the microphone icon
- Speak your message
- Ada will transcribe and send it automatically
- Available in Chrome and Edge

### Text-to-Speech
- Click the speaker icon next to Ada's messages
- Ada will speak her response
- Enable the 🔊 toggle in the header to auto-read all responses

### Dark Mode
- Click the 🌙/☀️ button in the header to toggle dark mode
- Theme preference is saved to localStorage

## Knowledge Base Setup (Optional)

Ada can load additional knowledge from GitHub repositories. To use this feature:

1. Create a GitHub repository with your knowledge files
2. Add `.md`, `.txt`, or `.json` files with your knowledge
3. Update the JavaScript variables in the code:
   ```javascript
   const KB_TOKEN = 'your_github_token';
   const KB_REPO = 'owner/repository-name';
   ```
4. Knowledge loads automatically on page initialization

### Knowledge File Format

Ada reads the following file types:
- **Markdown (.md)**: Best for structured knowledge
- **Text (.txt)**: Simple text files
- **JSON (.json)**: Structured data

Organize your knowledge in clear, well-structured documents for best results.

## Browser Support

- **Chrome/Edge**: Full support (including speech recognition)
- **Firefox/Safari**: Full support (speech recognition may be limited)
- **Modern browsers**: All features supported

## Privacy

- No external AI API calls to paid services
- All search APIs are free and public
- Knowledge is loaded from your GitHub repository
- Notes and reminders are stored in your browser's localStorage
- No data is sent to AI companies

## Customization

### Theme
Modify the CSS variables in the `<style>` section to change colors:
```css
:root{
  --accent:#5b6af0;
  --accent-dark:#4453d6;
  --bg:#f4f5f7;
  --surface:#fff;
  --border:#e2e4e9;
  --text:#1a1c22;
  --muted:#6b7280;
}
```

### Knowledge Base
Update the JavaScript variables to change Ada's knowledge source:
```javascript
const KB_TOKEN = 'your_github_token';
const KB_REPO = 'owner/repository-name';
```

### Response Logic
Modify the `generateResponse()` function to customize how Ada answers questions.

## Limitations

- Ada uses free public APIs, not advanced AI
- Some APIs may have rate limits
- Speech recognition requires Chrome/Edge
- Notes/reminders are stored in localStorage (browser-specific)
- Fuzzy matching may not always find the correct Wikipedia article
- Reminders only trigger when the page is open

## Future Enhancements

- [ ] Additional API integrations
- [ ] Support for more file types
- [ ] Local file-based knowledge base
- [ ] Export/import notes and reminders
- [ ] Better sentence extraction
- [ ] Multi-language support
- [ ] Image recognition via file attachments
- [ ] Sync notes/reminders across devices

## License

This project is open source and available for personal and commercial use.

## Contributing

Contributions are welcome! Feel free to:
- Report issues
- Suggest features
- Submit pull requests
- Improve documentation

## Support

For issues or questions:
1. Check the API endpoints are accessible
2. Verify browser is up to date
3. Check browser console for errors
4. Ensure internet connection for API calls

---

**Ada** - Your Free AI Assistant 🤖
