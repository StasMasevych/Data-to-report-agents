# Data to Report Agents

A CrewAI-powered application that automates project planning and reporting by analyzing Trello board data. This application uses a crew of AI agents to collect data from Trello, analyze it, and generate comprehensive project reports.

## 🤖 Agents

The application uses three specialized agents, each with a specific role in the data-to-report pipeline:

### 1. Project Planning Agent
- **Role**: The Ultimate Project Planner
- **Goal**: Meticulously break down projects into actionable tasks
- **Tools**: BoardDataFetcherTool, CardDataFetcherTool
- **Responsibilities**: 
  - Collect data from Trello boards
  - Organize tasks and identify dependencies
  - Create structured project plans

### 2. Estimation Agent
- **Role**: Expert Estimation Analyst
- **Goal**: Provide accurate time, resource, and effort estimations
- **Responsibilities**:
  - Analyze task complexity
  - Estimate required resources
  - Identify potential risks and uncertainties

### 3. Resource Allocation Agent
- **Role**: Resource Allocation Strategist
- **Goal**: Optimize task allocation based on skills and workload
- **Responsibilities**:
  - Match tasks to team members
  - Balance workload distribution
  - Create resource allocation charts

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

### 1. Task Breakdown
- Analyzes project requirements
- Breaks down the project into individual tasks
- Defines scope, timelines, and dependencies
- Outputs a comprehensive list of tasks with visualizations

### 2. Time & Resource Estimation
- Evaluates each task for time and resource requirements
- Uses historical data and complexity analysis
- Outputs detailed estimation reports with risk assessments

### 3. Resource Allocation
- Strategically assigns tasks to team members
- Balances workload and matches skills to requirements
- Outputs allocation charts with rationale for decisions

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

The application generates a comprehensive report that includes:
- Detailed task breakdown with descriptions and timelines
- Resource estimation for each task
- Resource allocation chart showing team member assignments
- Risk assessment and project timeline visualization

## 🔄 Workflow

1. The Project Planning Agent collects data from Trello using the custom tools
2. The collected data is passed to the Estimation Agent for analysis
3. The Resource Allocation Agent creates the final report with task assignments
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
