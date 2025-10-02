# AI-Powered Trip Planner

An intelligent travel planning application built with CrewAI, Streamlit, and Ollama LLM that creates personalized travel itineraries based on user preferences.

## Features

- **AI-Powered Planning**: Uses multiple AI agents (Location Expert, Guide Expert, Planner Expert) to gather and compile travel information
- **Comprehensive Itineraries**: Includes accommodations, transportation, food recommendations, local events, and budget planning
- **Web Search Integration**: Leverages DuckDuckGo search for real-time travel information
- **Streamlit Interface**: User-friendly web interface for inputting travel details
- **Downloadable Plans**: Export travel plans as text files
- **Multi-language Support**: Responds in French for French-speaking destinations

## Architecture

The application consists of three main AI agents:

1. **Location Expert**: Handles travel logistics including accommodations, visa requirements, transportation, weather, and cost of living
2. **Guide Expert**: Provides city-specific recommendations for attractions, food, and activities based on user interests
3. **Planner Expert**: Compiles all information into a structured, day-by-day itinerary

## Installation

### Prerequisites

- Python 3.8+
- Ollama installed and running locally
- Llama 3.2 model downloaded in Ollama (`ollama pull llama3.2`)

### Setup

1. Clone or download the project files
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Ensure Ollama is running with the Llama 3.2 model:
   ```bash
   ollama serve
   ollama pull llama3.2
   ```

## Usage

1. Run the Streamlit application:
   ```bash
   streamlit run app.py
   ```

2. Open your browser to the provided local URL (typically http://localhost:8501)

3. Fill in the travel details:
   - From City
   - Destination City
   - Departure Date
   - Return Date
   - Interests (e.g., sightseeing, food, adventure)

4. Click "Generate Travel Plan" and wait for the AI to create your personalized itinerary

5. Download the travel plan as a text file

## Dependencies

- `crewai`: Multi-agent AI framework
- `crewai_tools`: Additional tools for CrewAI
- `langchain`: LLM framework integration
- `langchain_community`: Community tools for LangChain
- `langchain-ollama`: Ollama integration for LangChain
- `duckduckgo-search`: Web search functionality
- `langchain-google-genai`: Google Generative AI integration (optional)
- `streamlit`: Web application framework

## Project Structure

```
├── app.py                 # Main Streamlit application
├── TravelAgents.py        # AI agent definitions
├── TravelTasks.py         # Task definitions for agents
├── TravelTools.py         # Custom tools (web search)
├── requirements.txt       # Python dependencies
├── output/                # Generated travel plans
│   └── Travel_Plan_Rome.txt  # Sample output
├── git_assets/            # UI screenshots
│   ├── 1.png
│   ├── 2.png
│   └── 3.png
└── __pycache__/           # Python bytecode cache
```

## Screenshots

### Main Interface
![Main Interface](git_assets/1.png)

### Travel Plan Generation
![Plan Generation](git_assets/2.png)

### Sample Output
![Sample Output](git_assets/3.png)

## Sample Output

See `output/Travel_Plan_Rome.txt` for a sample travel plan generated for Rome, focusing on accommodation recommendations.

## Technical Details

- **LLM**: Uses Ollama with Llama 3.2 model running locally
- **Process**: Sequential agent execution for comprehensive planning
- **Tools**: DuckDuckGo web search for real-time information
- **Output Format**: Markdown-structured travel itineraries
- **Language**: Python 3.x with async capabilities

## Configuration

The application uses the following configurations:
- Max iterations per agent: 5
- Verbose logging: Enabled
- Full output: Enabled
- Delegation: Disabled (agents work independently)

## Troubleshooting

- Ensure Ollama is running before starting the application
- Check that the Llama 3.2 model is downloaded
- Verify all dependencies are installed
- For web search issues, ensure internet connectivity

## Future Enhancements

- Support for multiple LLMs
- Integration with booking APIs
- Mobile app version
- Multi-language interface
- Real-time flight/hotel pricing

## License

This project is for educational purposes. Please check individual library licenses for commercial use.