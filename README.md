# Text to PowerPoint Generator

Transform your text, markdown, or prose into professionally formatted PowerPoint presentations using AI and custom templates.

## 🚀 Features

- **Smart Text Processing**: Paste any text or markdown and watch it transform into structured slides
- **Multiple LLM Support**: Works with OpenAI, Anthropic, and Google Gemini APIs
- **Template Support**: Upload existing .pptx/.potx files to match their style
- **Customizable Output**: Choose tone, generate speaker notes, and preview before download
- **Privacy-First**: All processing happens client-side, API keys are never stored
- **No Backend Required**: Pure front-end application, easy to deploy anywhere

## 🔧 Setup & Installation

### Option 1: Use Hosted Version
Visit <a href='https://hivecase.github.io/ppt-generator/'>here</a> to use the app directly.

### Option 2: Run Locally
1. Clone the repository:
```bash
git clone https://github.com/HiveCase/ppt-generator.git
cd text-to-powerpoint
```

2. Open `index.html` in your browser (no build process required!)

### Option 3: Deploy Your Own

#### Deploy to GitHub Pages:
1. Fork this repository
2. Go to Settings > Pages
3. Set source to main branch
4. Your app will be available at `https://yourusername.github.io/text-to-powerpoint`

#### Deploy to Netlify:
1. Fork this repository
2. Connect to Netlify
3. Deploy with default settings

#### Deploy to Vercel:
1. Fork this repository
2. Import to Vercel
3. Deploy with default settings

## 📖 Usage Guide

### Basic Usage:
1. **Paste Your Text**: Enter your content in the text area (supports markdown)
2. **Add Guidance** (Optional): Provide context like "investor pitch" or "technical presentation"
3. **Configure API**: 
   - Select your LLM provider (OpenAI, Anthropic, or Gemini)
   - Enter your API key (never stored or logged)
4. **Upload Template** (Optional): Add a .pptx/.potx file to match its style
5. **Set Options**: Choose tone and enable speaker notes if needed
6. **Generate**: Click generate and preview your slides
7. **Download**: Save the final presentation

### API Key Setup:

#### OpenAI:
1. Get API key from [OpenAI Platform](https://platform.openai.com/api-keys)
2. Select "OpenAI" in the dropdown
3. Paste your key starting with `sk-`

#### Anthropic:
1. Get API key from [Anthropic Console](https://console.anthropic.com/)
2. Select "Anthropic" in the dropdown
3. Paste your API key

#### Google Gemini:
1. Get API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Select "Google Gemini" in the dropdown
3. Paste your API key

## 🎨 Supported Features

### Input Formats:
- Plain text
- Markdown formatting
- Bullet points
- Numbered lists
- Headers and sections

### Output Options:
- 5-15 slides (automatically determined)
- Title slides
- Content slides with bullets
- Two-column layouts
- Speaker notes
- Slide numbers

### Presentation Tones:
- Professional
- Casual
- Academic
- Sales Pitch
- Technical
- Creative

## 🔒 Privacy & Security

- **No Backend**: All processing happens in your browser
- **API Keys**: Never stored, logged, or transmitted to any server except the LLM provider
- **Local Processing**: Template analysis and slide generation occur client-side
- **Open Source**: Full transparency of code and operations

## 🛠️ Technical Details

### How Text is Parsed and Mapped:
The application uses a sophisticated LLM-based approach:
1. Text is sent to the LLM with structured prompts
2. LLM analyzes content density, topics, and logical flow
3. Returns JSON with slide structure, titles, and content
4. App maps this to PowerPoint elements using PptxGenJS

### Template Style Application:
When a template is uploaded:
1. File is read client-side using FileReader API
2. Style elements are extracted (colors, fonts, layouts)
3. These styles are applied to generated slides
4. Images from template can be reused in appropriate contexts

### Technologies Used:
- React 18 for UI
- PptxGenJS for PowerPoint generation
- Marked.js for Markdown parsing
- JSZip for file operations
- Modern browser APIs for file handling

## 📝 Examples

### Example Input:
```markdown
# Quarterly Business Review

## Executive Summary
Revenue increased 25% YoY
Customer satisfaction at all-time high
Three new products launched successfully

## Financial Performance
- Q3 Revenue: $2.5M
- Gross Margin: 68%
- Customer Acquisition Cost: $1,200
```

### Generated Output:
- Slide 1: Title slide with "Quarterly Business Review"
- Slide 2: Executive Summary with key points
- Slide 3: Financial Performance with metrics
- Slide 4: Thank you/Questions slide

## 🤝 Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🐛 Known Issues & Limitations

- Template style extraction is simplified (full template parsing requires complex OOXML processing)
- Large text inputs (>10,000 words) may hit API token limits
- Generated presentations use standard layouts (custom layouts from templates not fully supported)
- Image extraction from templates not implemented in current version

## 🚧 Roadmap

- [ ] Enhanced template parsing with full style extraction
- [ ] Support for images in templates
- [ ] Batch processing for multiple presentations
- [ ] Save/load presentation drafts
- [ ] More layout options and transitions
- [ ] Export to Google Slides format
- [ ] Support for charts and graphs
- [ ] Collaborative editing features

## 💬 Support

For issues, questions, or suggestions:
- Open an issue on GitHub
- Check existing issues for solutions
- Review the FAQ section below

## ❓ FAQ

**Q: Is my API key safe?**
A: Yes, API keys are only used client-side and sent directly to the LLM provider. They're never stored or logged.

**Q: Can I use this offline?**
A: The app interface works offline, but generating presentations requires an internet connection for API calls.

**Q: What's the maximum text length?**
A: This depends on your LLM provider's token limits. Generally, 5,000-10,000 words work well.

**Q: Can I customize the slide designs?**
A: Yes, by uploading a template file. The app will attempt to match its styling.

**Q: Which LLM provider is best?**
A: All work well. OpenAI GPT-4 and Anthropic Claude tend to produce the most nuanced structures.

## 🙏 Acknowledgments

- PptxGenJS for PowerPoint generation capabilities
- The open-source community for inspiration and libraries
- LLM providers for powerful AI capabilities

---

Made with ❤️ by Satyajeet Kumar
