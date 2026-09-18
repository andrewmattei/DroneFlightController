DroneFlightController 🚁

A modular framework for drone simulation, implementing both classical control (PID) and reinforcement learning (RL) policies, with pathways for real hardware deployment.

📁 Repository Structure

DroneFlightController/
├── .gitignore              # Ignore virtual environments and trained models
├── requirements.txt        # Dependencies (includes crazyflow)
├── README.md               # Setup and usage instructions
├── controllers/            # Phase 1: Physics-based control
│   ├── __init__.py
│   └── pid_controller.py   # Initial Python PID implementation
├── rl_policies/            # Phase 2: Reinforcement Learning
│   ├── __init__.py
│   ├── train.py            # Neural network training script
│   ├── evaluate.py         # Test trained weights in the MuJoCo viewer
│   └── models/             # Saved model weights
├── scripts/                
│   └── run_sim.py          # Main entry point to launch the simulation
└── onboard/                # Future Phase: Real drone deployment
    └── export_weights.py   # Translate Python logic into deployable C code


⚙️ Setup & Installation

[!NOTE]
We strongly recommend using uv for managing your Python environment and dependencies due to its exceptional speed and automatic Python version management.

1. Clone the Repository

git clone https://github.com/your-username/DroneFlightController.git
cd DroneFlightController


2. Create a Virtual Environment with uv

Create a dedicated virtual environment with a specific Python version (e.g., Python 3.11):

uv venv --python 3.11


Activate the virtual environment:

macOS / Linux:

source .venv/bin/activate


Windows (Command Prompt):

.venv\Scripts\activate.bat


Windows (PowerShell):

.venv\Scripts\Activate.ps1


3. Install Dependencies

Install the required packages using uv pip for lightning-fast installation:

uv pip install -r requirements.txt


(Alternatively, standard pip install -r requirements.txt will also work if preferred).
