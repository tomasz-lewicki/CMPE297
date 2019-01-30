# Levels of automation

0. obvious

1. adaptive cruise control

2. Partial automation _(e.g. lane keeping)_

3. Conditional Automation _(e.g. lange change)_

4. High automation _(human intervention only in emergency)_
5. Full automation _(no intervention)_


blue lidar
orange - radar
yellow - camera
gray - ultrasonic

# Sensors

- Camera
- LIDAR
- Ultrasonic (sound waves)
- Radar (radio waves)

# Tracking

- handles occlusion (zasłonięcie)
- preserves identity (so an object in one frame is considered the same car in another)

# Semantic segmentation

- match all pixels in the image to different categories:
    - tree pixel
    - building pixel
    - road pixel

# Prediction
(resulting in predicted trajectories of other objects on the road)

- Model based approach
    - using laws of physics, traffic laws and human behavior

- Data Driven Approach
    - using ML (e.g. RNNs)

# Planning

- Routing (find the best A->B route)
    - Needs inputs:
        - position A
        - position B
        - map
            - preferably with real-time data
            - can be represented as a graph in which streets/places are nodes and decisions are edges
        
- Trajectory generation (low level).
    ```
    The task is to find a high precision trajectory (set of waypoints) to move around the route. The waypoints are defined in 3D space (2D + time).
    ```
    - have to take constraints into account
    - Deep reinforcement learning

# Control

- input:
    - trajectory
    - state of the vehicle
- outputs:
    - steering (steering wheel, left, right)
    - acceleration/decceleration (speed of wheels)

- constrains:
    - non-holonomous robot
    - comfort of passengers

## Control algorithms

- PID
- Linear Quadratic Regulator
- Model Predictive Control

