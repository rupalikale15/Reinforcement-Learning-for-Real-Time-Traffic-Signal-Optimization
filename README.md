# Reinforcement-Learning-for-Real-Time-Traffic-Signal-Optimization
# Traffic Signal Optimization using Reinforcement Learning

An intelligent traffic signal control system that uses **Reinforcement Learning (RL)** to reduce congestion, waiting times, and emissions in urban intersections. The project combines **computer vision** for real-world traffic analysis and **deep RL** (PPO & DQN) for adaptive signal timing.

---

## 🎯 Overview

Traditional fixed-time traffic signals are inefficient in dynamic traffic conditions. This project develops a **smart adaptive traffic signal controller** using Reinforcement Learning that learns optimal signal phasing strategies in real time.

**Key Components:**
- Real-world vehicle detection using **YOLOv8**
- Realistic traffic simulation with **SUMO**
- Custom Gym environment for RL training
- Training and comparison of **PPO** and **DQN** agents
- Performance comparison with traditional Fixed-Time control

---

## ✨ Features

- **Vehicle Detection**: Processes real traffic videos using Ultralytics YOLOv8
- **Custom RL Environment**: `TrafficSignalEnv` built with Gymnasium
- **Deep RL Models**: PPO (best performer) and DQN trained with Stable-Baselines3
- **Multi-Metric Evaluation**: Delay, Throughput, and Queue Length
- **Visualization**: Professional comparison charts
- **Realistic Simulation**: Integration with SUMO traffic simulator

---

## 🛠 Technologies Used

| Component              | Technology                          |
|------------------------|-------------------------------------|
| RL Framework           | Stable-Baselines3, Gymnasium        |
| Simulation             | SUMO (Simulation of Urban Mobility) |
| Computer Vision        | YOLOv8 (Ultralytics)                |
| Environment            | Custom Gym Environment              |
| Visualization          | Matplotlib, Seaborn, Pandas         |
| Platform               | Google Colab (GPU)                  |

---

## 📁 Project Structure

```bash
traffic-signal-rl/
├── Traffic_signal_optimization_project.ipynb    # Main Jupyter Notebook
├── comparison_charts_final.png                  # Results visualization
├── videos/                                      # Traffic video dataset
├── models/                                      # Trained RL models (PPO, DQN)
├── env/                                         # Custom Gym environment
├── results/                                     # Performance metrics
└── README.md
🚀 Installation & Setup
Prerequisites

Python 3.8+
Google Colab (recommended) or local environment with GPU

Setup in Colab
# Clone the repository
!git clone https://github.com/yourusername/traffic-signal-rl.git
%cd traffic-signal-rl

# Install dependencies
!pip install stable-baselines3[extra] gymnasium sumo-rl opencv-python-headless ultralytics pandas matplotlib seaborn wandb tqdm

# Install SUMO
!apt-get install -y sumo sumo-tools sumo-doc
📊 Results
Performance Comparison
Algorithm,Avg. Delay (s) ↓,Throughput (veh/h) ↑,Avg. Queue ↓
Fixed Time,45,1200,35
Q-Learning,28,1450,22
DQN,22,1580,15
PPO,18,1620,12
PPO outperformed all other methods, showing 60% reduction in delay compared to fixed-time signals.
<img src="comparison_charts_final.png" alt="Results Chart">

🔄 How It Works

Data Collection: Real traffic videos → YOLOv8 vehicle detection
Environment Modeling: Custom Gym environment simulating intersections
RL Training: Agent learns to choose optimal signal phases
Evaluation: Compare against baseline controllers


🎮 Usage
Run the main notebook:
jupyter notebook Traffic_signal_optimization_project.ipynb
Or open directly in Google Colab.
🔮 Future Improvements

Multi-intersection coordination using Multi-Agent RL
Real-time deployment with edge devices
Integration with connected vehicles (V2X)
Emission and fuel consumption optimization
Sim-to-Real transfer learning


🤝 Contributing
Contributions are welcome! Feel free to:

Open issues for bugs or feature requests
Submit pull requests
Improve documentation


📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

🙋‍♂️ Author
Rupali
Pune, India

⭐ Star this repo if you found it helpful!

































