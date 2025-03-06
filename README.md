# RoboRangers: Autonomous Car with Deep Reinforcement Learning

## 🚀 Project Overview
RoboRangers is an **autonomous vehicle** project leveraging **Deep Reinforcement Learning (DRL)** and **ROS2** to navigate and make real-time decisions in a dynamic environment. The project integrates **robotics simulation**, **sensor fusion**, and **machine learning** to develop an efficient self-driving system.

## 📌 Features
- **Autonomous Navigation**: The vehicle follows predefined paths while adapting to environmental changes.
- **Obstacle Detection & Traffic Sign Recognition**: Uses **camera vision and LIDAR sensors** for real-time perception.
- **Path Planning & Control**: Implements **TD3 (Twin Delayed Deep Deterministic Policy Gradient)** for decision-making.
- **Simulation in Gazebo**: Tests the vehicle in a 3D environment before real-world deployment.
- **Modular ROS2 Integration**: Ensures efficient communication between system components.

## 🛠 Technologies Used
- **AI & Machine Learning**: Python, PyTorch, TensorFlow, OpenCV
- **Robotics Framework**: ROS2 (Robot Operating System 2)
- **Simulation**: Gazebo
- **Sensors**:
  - **Cameras**: Traffic sign recognition & obstacle detection
  - **LIDARs**: 3D mapping & distance measurement
- **3D Modeling**: URDF & Xacro for robot description
- **Visualization**: Rviz for sensor data visualization

## 📂 Project Structure
```
RoboRangers/
│── src/td3/                   # Core implementation of TD3 algorithm
│   ├── models/                # URDF models & sensor configurations
│   ├── scripts/               # Training & evaluation scripts
│   │   ├── train_velodyne.py  # Training with LIDAR data
│   │   ├── test_velodyne.py   # Testing with LIDAR data
│   │   ├── replay_buffer.py   # Experience replay memory
│   │   ├── point_cloud2.py    # LIDAR point cloud processing
│   ├── pytorch_models/        # Pre-trained models
│   ├── runs/                  # Training logs & TensorBoard files
│── launch/                    # ROS2 launch files
│── config/                    # Configuration files
│── worlds/                    # Simulation environments in Gazebo
```

## 🏗 Installation & Setup
### Prerequisites
- **ROS2 (Humble/Foxy)**: [Installation Guide](https://docs.ros.org/en/humble/)
- **Gazebo**: [Installation Guide](http://gazebosim.org/)
- **Python Packages**:
  ```bash
  pip install torch torchvision tensorflow opencv-python numpy
  ```

### Running the Simulation
```bash
# Clone the repository
git clone https://github.com/MEHDI57-NRG/RoboRangers.git
cd RoboRangers

# Build the ROS2 package
colcon build --symlink-install

# Source the ROS2 workspace
source install/setup.bash

# Launch the simulation in Gazebo
ros2 launch robo_rangers launch_sim.launch.py
```

## 🎯 Future Improvements
- Complete DRL training for fully autonomous behavior
- Improve path planning algorithms for dynamic environments
- Optimize computational performance for real-time decision-making

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
Feel free to contribute and enhance the RoboRangers project! 🚗💨
