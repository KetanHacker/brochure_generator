# Brochure Generator

An AI-powered tool that automatically generates company brochures by analyzing website content using OpenAI's GPT models.

## Features

- **Web Scraping**: Automatically extracts content from company websites
- **Smart Link Detection**: Uses AI to identify relevant company pages (About, Careers, etc.)
- **AI-Powered Content Generation**: Creates professional brochures using OpenAI's GPT-4
- **Streaming Output**: Real-time generation with live updates
- **Markdown Format**: Generates clean, formatted brochures in Markdown

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/KetanHacker/brochure_generator.git
   cd brochure_generator
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up your environment variables:
   ```bash
   cp .env.example .env
   ```
   
4. Edit the `.env` file and add your OpenAI API key:
   ```
   OPENAI_API_KEY=sk-proj-your-actual-api-key-here
   ```

## Usage

Open the `Brochure.ipynb` Jupyter notebook and run the cells to:

1. **Initialize the system**: Load dependencies and configure the OpenAI client
2. **Analyze a website**: Use the `Website` class to scrape content
3. **Generate a brochure**: Use either `create_brochure()` or `stream_brochure()` functions

### Example

```python
# Generate a brochure for a company
create_brochure("Company Name", "https://www.company-website.com")

# Or use streaming for real-time generation
stream_brochure("Company Name", "https://www.company-website.com")
```

## How It Works

1. **Web Scraping**: The tool scrapes the main website and extracts text content
2. **Link Analysis**: AI identifies relevant company pages (About, Careers, etc.)
3. **Content Extraction**: Scrapes additional relevant pages for comprehensive information
4. **Brochure Generation**: Uses GPT-4 to create a professional company brochure
5. **Output**: Displays the result in formatted Markdown

## Requirements

- Python 3.8+
- OpenAI API key
- Internet connection for web scraping

## Dependencies

- `requests`: For web scraping
- `beautifulsoup4`: For HTML parsing
- `python-dotenv`: For environment variable management
- `openai`: For AI content generation
- `ipython`: For Jupyter notebook display features

## Configuration

The system uses several configurable prompts:

- **Link System Prompt**: Guides AI in identifying relevant website links
- **Brochure System Prompt**: Defines the style and content of generated brochures
- **Model Selection**: Currently uses `gpt-4o-mini` (configurable)

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Security

- Never commit your `.env` file containing API keys
- Keep your OpenAI API key secure and rotate it regularly
- Be mindful of API usage costs when scraping large websites

## Troubleshooting

- **API Key Issues**: Ensure your OpenAI API key is valid and has sufficient credits
- **Scraping Failures**: Some websites may block automated requests; try different user agents
- **Rate Limiting**: Be respectful of website rate limits and API quotas

## Disclaimer

This tool is for educational and legitimate business purposes only. Always respect website terms of service and robots.txt files when scraping content.
