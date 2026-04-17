# Ada - Independent AI Assistant

Ada is a fully independent AI assistant that doesn't rely on external APIs like OpenAI, Anthropic, or GPT. She answers questions based on a knowledge base loaded from GitHub, making her completely self-contained and private.

## Features

- **💬 Chat Interface**: Clean, modern chat interface with Ada
- **📎 File Attachments**: Send images, videos, audio, and documents
- **🎤 Speech-to-Text**: Speak your messages instead of typing
- **🔊 Text-to-Speech**: Hear Ada speak her responses
- **📚 Knowledge Base**: Load knowledge from GitHub repositories
- **🔄 Auto-read**: Automatically have Ada read her responses
- **🎨 Modern UI**: Beautiful gradient design with smooth animations

## How It Works

Ada uses a local knowledge base system that:
1. Reads knowledge files from a GitHub repository
2. Stores them locally in memory
3. Uses keyword matching and pattern recognition to answer questions
4. Generates responses from the most relevant content found

No external AI APIs are used - everything runs locally in your browser.

## Setup

1. Clone or download this repository
2. Open `index.html` in a modern web browser (Chrome, Edge, Firefox, Safari)
3. Ada will automatically load her knowledge base from the configured GitHub repository

## Knowledge Base Setup

Ada's knowledge base is configured in the code. To use your own knowledge base:

1. Create a GitHub repository with your knowledge files
2. Add `.md`, `.txt`, or `.json` files with your knowledge
3. Update the `knowledgeToken` and `knowledgeRepo` variables in `index.html`:
   ```javascript
   let knowledgeToken = 'your_github_token';
   let knowledgeRepo = 'owner/repository-name';
   ```

### Knowledge File Format

Ada reads the following file types:
- **Markdown (.md)**: Best for structured knowledge
- **Text (.txt)**: Simple text files
- **JSON (.json)**: Structured data

Organize your knowledge in clear, well-structured documents for best results.

## Usage

### Basic Chat
- Type your question in the input field
- Press Enter or click "Send"
- Ada will search her knowledge base and respond

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

## Browser Support

- **Chrome/Edge**: Full support (including speech recognition)
- **Firefox/Safari**: Full support (speech recognition may be limited)
- **Modern browsers**: All features supported

## Privacy

- All processing happens locally in your browser
- No external API calls to AI services
- Knowledge is loaded from your GitHub repository
- Token is stored locally in the page

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

- Ada uses simple pattern matching, not advanced AI
- Knowledge base must be well-structured for best results
- Speech recognition requires Chrome/Edge
- Knowledge base size limited by browser memory

## Future Enhancements

- [ ] Advanced pattern matching
- [ ] Support for more file types
- [ ] Local file-based knowledge base
- [ ] Export/import knowledge base
- [ ] Better sentence extraction
- [ ] Multi-language support

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
1. Check the knowledge base files are properly formatted
2. Verify GitHub token has read access to the repository
3. Ensure browser is up to date
4. Check browser console for errors

---

**Ada** - Your Independent AI Assistant 🤖
