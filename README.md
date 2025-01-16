# Legal Team Agent

A Streamlit application that simulates a full-service legal team using multiple AI agents to analyze legal documents and provide comprehensive legal insights. Each agent represents a different legal specialist role, from research and contract analysis to strategic planning, working together to provide thorough legal analysis and recommendations.

## Features

### AI Agent Specialists

- **Legal Researcher**
  - Conducts comprehensive legal research
  - Finds and cites relevant cases and precedents
  - Uses DuckDuckGo search integration
  - References specific document sections in findings

- **Contract Analyst**
  - Reviews contracts in detail
  - Identifies key terms and obligations
  - Highlights potential legal issues
  - Provides clause-specific analysis

- **Legal Strategist**
  - Develops legal strategies
  - Assesses risks and opportunities
  - Provides actionable recommendations
  - Creates strategic implementation plans

- **Team Lead**
  - Coordinates between specialists
  - Ensures comprehensive analysis
  - Verifies source citations
  - Maintains document reference accuracy

### Analysis Types Available

- **Contract Review**: Detailed analysis by Contract Analyst
- **Legal Research**: In-depth research by Legal Researcher
- **Risk Assessment**: Combined analysis by Legal Strategist and Contract Analyst
- **Compliance Check**: Comprehensive review by all specialists
- **Custom Query**: Flexible analysis using all available agents

## Prerequisites

- **Docker**: Make sure Docker is installed on your system. You can download it from [Docker's official website](https://www.docker.com/get-started).
- **Install Docker** (Windows):
  1.  Download the Docker Desktop installer from the [Docker Hub](https://hub.docker.com/editions/community/docker-ce-desktop-windows).
  2.  Run the installer and follow the instructions.
  3.  After installation, you can run Docker using the command:
  ```bash
  docker run -p 6333:6333 -d qdrant/qdrant
  ```
  - **Port Mapping**: The command maps port `6333` on your local machine to port `6333` on the Qdrant container. This is the default setting and should work for most users. However, if you have another service running on port `6333`, you can change it by modifying the command:
  ```bash
  docker run -p <host_port>:6333 -d qdrant/qdrant
  ```
  Replace `<host_port>` with the desired port number.

## How to Run

1. **Setup Environment**

   ```bash
   # Clone the repository
   git clone https://github.com/shireen168/legal_team_agent.git
   cd legal_team_agent

   # Install dependencies
   poetry install
   ```

2. **Configure API Keys**

   - Get OpenAI API key from [OpenAI Platform](https://platform.openai.com)
   - Get Qdrant API key and URL from [Qdrant Cloud](https://cloud.qdrant.io)

3. **Run the Application**
   ```bash
   poetry run streamlit run main.py
   ```
4. **Use the Interface**
   - Enter API credentials
   - Upload a legal document (PDF)
   - Select analysis type
   - Add custom queries if needed
   - View analysis results

## Notes

- Supports PDF documents only
- Uses GPT-4o for analysis
- Uses text-embedding-3-small for embeddings
- Requires stable internet connection
- API usage costs apply
