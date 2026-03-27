# DeerFlow Harness

![long-horizon](https://img.shields.io/badge/long--horizon-blue?style=flat-square) ![workflow](https://img.shields.io/badge/workflow-blue?style=flat-square) ![persistence](https://img.shields.io/badge/persistence-blue?style=flat-square)

A long-horizon task framework for agents to manage weeks-long projects with state persistence.

## Overview
DeerFlow Harness provides a robust infrastructure for AI agents to execute complex, multi-stage workflows that span extended timeframes. It bridges the gap between instantaneous LLM responses and real-world project management by maintaining a verifiable state across system restarts and long idle periods.

## Features
*   **Stateful Persistence:** Automatically saves and restores agent memory and task progress to ensure continuity over weeks of operation.
*   **Checkpointing:** Granular versioning of project states, allowing agents to backtrack or branch workflows without data loss.
*   **Resource Throttling:** Built-in mechanisms to manage API usage and compute costs during long-duration autonomous tasks.
*   **Event-Driven Architecture:** Supports asynchronous triggers that wake agents based on external environment changes or time-based schedules.

## Installation
Clone the repository and install the dependencies using `pip`:

```bash
git clone https://github.com/username/deer-flow-harness.git
cd deer-flow-harness
pip install -r requirements.txt
```

## Usage
To start a new project or resume an existing one, run the main entry point:

```bash
python main.py --project "launch-campaign" --config configs/default.yaml
```

**Brief Example:**
```python
from deer_flow import Harness

# Initialize the harness with persistent storage
harness = Harness(project_id="website-rebuild")

# Define a long-running task
harness.run(task="Audit current SEO and suggest improvements over the next 14 days.")
```

## Contributing
We welcome contributions to improve the reliability and scalability of long-horizon agent workflows. Please submit a Pull Request with a detailed description of your changes, and ensure all tests pass before submission.

## License
This project is licensed under the [MIT License](LICENSE).