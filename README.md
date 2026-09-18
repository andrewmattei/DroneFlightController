# DroneFlightController
DroneFlightController/
├── .gitignore                # Ignore virtual environments and trained models
├── requirements.txt          # git+https://github.com/learnsyslab/crazyflow.git
├── README.md                 # Setup instructions for your friend
├── controllers/              # Phase 1: Physics based control
│   ├── __init__.py
│   └── pid_controller.py     # Your initial Python PID implementation
├── rl_policies/              # Phase 2: Reinforcement Learning
│   ├── __init__.py
│   ├── train.py              # Script to train your neural network
│   ├── evaluate.py           # Script to test trained weights in the MuJoCo viewer
│   └── models/               # Saved model weights
├── scripts/                  
│   └── run_sim.py            # Main entry point to launch the simulation
└── onboard/                  # Future Phase: Real drone deployment
    └── export_weights.py     # Scripts to translate Python logic into C