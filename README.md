# SmartRoad

## AI-Based Road Lifecycle Management and Accountability System

SmartRoad is an AI-based road inspection and lifecycle management system designed to help identify road damage from images and organize road inspection information.

The system uses an AI object detection model to detect:

- Crack
- Pothole
- Waterlogging

The detected results are processed through a FastAPI backend and can be connected to a React frontend for visualization and further road management features.

---

# 1. Project Objective

The main objective of SmartRoad is to provide an AI-assisted system for road inspection and maintenance management.

The system aims to:

- Detect road damage using AI.
- Identify different types of road damage.
- Store and manage road inspection information.
- Provide visual inspection results.
- Support maintenance planning and prioritization.
- Provide a foundation for road health and risk analysis.
- Improve accountability and tracking of road maintenance activities.

---

# 2. System Overview

The current AI workflow is:

```text
                    SMARTROAD
                        |
                        v
                Road Image Upload
                        |
                        v
                  FastAPI Backend
                        |
                        v
                   YOLO26n Model
                        |
             +----------+----------+
             |          |          |
             v          v          v
           Crack     Pothole   Waterlogging
             |          |          |
             +----------+----------+
                        |
                        v
                Detection Results
                        |
             +----------+----------+
             |                     |
             v                     v
        JSON Response       Annotated Image