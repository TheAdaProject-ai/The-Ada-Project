# Ada - AI Assistant with Multiple API Integrations

Ada is a powerful AI assistant that combines multiple free APIs to provide comprehensive information and services. She doesn't rely on paid AI services like OpenAI or Anthropic, making her completely free to use.

## Features

- **💬 Chat Interface**: Clean, modern chat interface with intelligent responses
- **🔍 Multiple Search APIs**: Wikipedia, DuckDuckGo, Dictionary, Gutendex, and more
- **🌤️ Weather Tab**: Current weather information via Open-Meteo API
- **📰 News Tab**: Curated news from Actually Relevant API
- **🎲 Facts Tab**: Random and daily facts from uselessfacts API
- **🔎 Search Tab**: Web search via DuckDuckGo API
- **📎 File Attachments**: Send images, videos, audio, and documents
- **🎤 Speech-to-Text**: Speak your messages instead of typing
- **🔊 Text-to-Speech**: Hear Ada speak her responses
- **📚 Knowledge Base**: Load knowledge from GitHub repositories
- **🔄 Auto-read**: Automatically have Ada read her responses
- **🎨 Modern UI**: Beautiful gradient design with smooth animations
- **📝 Professional Formatting**: Responses use professional clarity guidelines

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
- Temperature, wind speed, conditions
- Global coverage with geocoding
- Source: [Open-Meteo](https://open-meteo.com/)

### Actually Relevant News API
- Curated news stories
- Humanitarian and important topics
- No API key required
- Source: [Actually Relevant](https://actuallyrelevant.news/)

### Random Facts API
- Random useless facts
- Daily facts
- Multiple languages
- Source: [uselessfacts.jsph.pl](https://uselessfacts.jsph.pl/)

### DuckDuckGo Search API
- Web search capabilities
- Instant answers
- Related topics
- Fallback when Wikipedia fails
- Source: [DuckDuckGo](https://duckduckgo.com/)

## How It Works

Ada uses a multi-layered approach to answer questions:

1. **Greeting Detection**: Recognizes and responds to common greetings
2. **Dictionary Lookup**: Checks for word definitions
3. **Wikipedia Search**: Uses MediaWiki REST API with fuzzy matching
4. **DuckDuckGo Fallback**: Searches the web if Wikipedia fails
5. **Book Search**: Uses Gutendex for book-related queries
6. **Professional Formatting**: Applies clarity guidelines to all responses

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
- **Greeting responses**: "Hi", "Hello", "How are you?"

### Weather Tab
- Enter a city name (e.g., "London", "New York")
- Click "Get Weather"
- View current temperature, wind speed, and conditions

### News Tab
- Click "Load News"
- View curated news stories from Actually Relevant
- Read full articles via provided links

### Facts Tab
- Click "Get Random Fact" for a random useless fact
- Click "Get Today's Fact" for today's featured fact

### Search Tab
- Enter any search query
- Click "Search"
- View DuckDuckGo search results with instant answers

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
- Enable "Auto-read Ada's messages" to hear all responses automatically

## Knowledge Base Setup (Optional)

Ada can load additional knowledge from GitHub repositories. To use this feature:

1. Create a GitHub repository with your knowledge files
2. Add `.md`, `.txt`, or `.json` files with your knowledge
3. Click the "Knowledge Base Configuration" button in the UI
4. Enter your GitHub Personal Access Token
5. Enter your repository in the format `owner/repository-name`
6. Click "Load Knowledge"

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
- Token is stored locally in the page
- No data is sent to AI companies

## Customization

### Colors
Modify the gradient in the CSS to change the color scheme:
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Knowledge Base
Update the JavaScript variables to change Ada's knowledge source:
```javascript
let knowledgeToken = 'your_token';
let knowledgeRepo = 'owner/repo';
```

### Response Logic
Modify the `generateResponse()` function to customize how Ada answers questions.

## Limitations

- Ada uses free public APIs, not advanced AI
- Some APIs may have rate limits
- Speech recognition requires Chrome/Edge
- Knowledge base size limited by browser memory
- Fuzzy matching may not always find the correct Wikipedia article

## Future Enhancements

- [ ] Additional API integrations
- [ ] Support for more file types
- [ ] Local file-based knowledge base
- [ ] Export/import knowledge base
- [ ] Better sentence extraction
- [ ] Multi-language support
- [ ] Image recognition via file attachments

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
