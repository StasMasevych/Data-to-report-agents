# Data to Report Agents

A CrewAI-powered application that automates sprint reporting by analyzing Trello board data. This application uses a crew of AI agents to collect data from Trello, analyze it, and generate comprehensive sprint reports.

## 🤖 Agents

The application uses two specialized agents, each with a specific role in the data-to-report pipeline:

### 1. Data Collection Agent
- **Role**: Data Collection Specialist
- **Goal**: Gather all relevant data from the Trello board
- **Tools**: BoardDataFetcherTool, CardDataFetcherTool
- **Responsibilities**: 
  - Collect data from Trello boards
  - Create an initial understanding of the project
  - Identify main features and team members

### 2. Analysis Agent
- **Role**: Project Analysis Expert
- **Goal**: Analyze the collected data to identify blockers, delays, and overall progress
- **Responsibilities**:
  - Identify blockers and delays
  - Assess overall project progress
  - Spot issues that may affect project timelines
  - Generate comprehensive sprint reports

## 🛠️ Custom Tools

The application includes custom tools for interacting with Trello:

### 1. BoardDataFetcherTool
- Fetches all cards from a specified Trello board
- Retrieves card data, comments, and activity
- Includes details like due dates, labels, and attachments

### 2. CardDataFetcherTool
- Fetches detailed data for a specific Trello card
- Provides in-depth information about individual tasks

## 📋 Tasks

The workflow is divided into three sequential tasks:

### 1. Data Collection
- Creates an initial understanding of the project
- Gathers information about main features and team members
- Uses Trello Data Fetcher tool to collect board data
- Outputs a comprehensive report on the project

### 2. Data Analysis
- Analyzes the Trello data to identify blockers, delays, and progress
- Evaluates the current state of the project
- Outputs a summary highlighting key issues and progress

### 3. Report Generation
- Compiles a comprehensive sprint report based on the analysis
- Includes sprint overview, task summary, identified issues
- Covers progress, delays, team performance, and recommendations
- Outputs a detailed sprint report in markdown format

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Trello API credentials

### Environment Variables
Create a `.env` file with the following variables:
```
OPENAI_API_KEY=your_openai_api_key
TRELLO_API_KEY=your_trello_api_key
TRELLO_API_TOKEN=your_trello_api_token
TRELLO_BOARD_ID=your_trello_board_id
```

### Installation

1. Clone the repository:
```bash
git clone https://github.com/StasMasevych/Data-to-report-agents.git
cd Data-to-report-agents
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Run the application:
```bash
python main.py
```

## 📊 Example Output

The application generates a comprehensive sprint report that includes:
- Sprint Overview
- Task Summary
- Identified Issues and Blockers
- Progress and Delays
- Team Performance Overview
- Action Items and Recommendations

## 🔄 Workflow

1. The Data Collection Agent gathers project information from Trello
2. The Analysis Agent processes this data to identify issues and progress
3. The Analysis Agent also generates the final sprint report
4. The complete report is returned as the crew's output

## 📝 Configuration

The behavior of agents and tasks can be customized by modifying the YAML configuration files:
- `config/agents.yaml`: Define agent roles, goals, and backstories
- `config/tasks.yaml`: Define task descriptions and expected outputs

## 🔗 Integration with Greenvi AI

This project follows the same pattern used in the Greenvi AI application for renewable energy project research:
- Uses a crew of specialized agents with defined roles
- Implements custom tools for data collection
- Processes data through sequential tasks
- Generates structured reports with actionable insights

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
