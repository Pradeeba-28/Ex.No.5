# EXPERIMENT 5: Comparing Prompting Techniques Through Engineering Problem-Solving Scenarios
# DATE : 26-11-2026
# REG NO : 212225040306
## 1. AIM
To compare different prompting techniques and evaluate their effectiveness in solving real-world engineering problems using ChatGPT.

## 2. PROJECT TITLE
**AI-Based Smart Traffic Management System**

## 3. PROBLEM STATEMENT
Traditional traffic signal systems operate using fixed timings, regardless of the number of vehicles waiting at each junction. This leads to unnecessary waiting times, traffic congestion, and increased fuel consumption.

The proposed Smart Traffic Management System uses computer vision to detect and count vehicles on different roads. Based on the vehicle density, the system dynamically adjusts traffic signal timings to reduce congestion and improve traffic flow.

## 4. SELECTED ENGINEERING SCENARIO
**Scenario:** Developing an adaptive traffic signal system using computer vision.

The system should:
- Detect vehicles using a camera.
- Count the number of vehicles on each road.
- Identify traffic density as low, medium, or high.
- Dynamically adjust traffic signal timings.
- Give priority to emergency vehicles such as ambulances and fire trucks.

## 5. BASE PROMPT (NAÏVE PROMPT)

**Prompt:**

"Suggest a method to develop a smart traffic management system using AI."

**AI-Generated Output:**

A smart traffic management system can be developed using Artificial Intelligence and computer vision. Cameras can be installed at traffic junctions to capture real-time images of vehicles. Object detection algorithms such as YOLO can be used to detect and count vehicles.

Based on the number of vehicles, traffic density can be calculated and signal timings can be adjusted automatically. Emergency vehicles can also be detected to provide priority. Python and OpenCV can be used for implementation.

## 6. IMPROVED PROMPTS USING DIFFERENT PROMPTING TECHNIQUES

### Technique 1: Role-Based Prompting

**Prompt:**

"Act as an experienced AI and computer vision engineer. Design a smart traffic management system that detects vehicles using cameras and adjusts traffic signal timings based on vehicle density. Suggest suitable technologies, algorithms, and implementation steps. Include emergency vehicle detection."

**AI-Generated Output:**

- **Vehicle Detection:** Use YOLO object detection to identify cars, buses, trucks, motorcycles, and ambulances.
- **Image Processing:** Use OpenCV to process real-time camera footage.
- **Vehicle Counting:** Count the detected vehicles in each lane.
- **Density Calculation:** Classify traffic as low, medium, or high based on vehicle count.
- **Signal Control:** Allocate green signal time according to traffic density.
- **Emergency Priority:** Detect ambulances and fire trucks and provide priority at the junction.

**Suggested Technologies:** Python, OpenCV, YOLO, Raspberry Pi, and traffic signal controllers.

### Technique 2: Few-Shot Prompting

**Prompt:**

"Consider the following examples:

Example 1: If Road A has 10 vehicles and Road B has 30 vehicles, Road B should receive a longer green signal.

Example 2: If all roads have low traffic density, normal signal timings should be maintained.

Example 3: If an ambulance is detected, priority should be given to its road.

Now design a smart traffic management system using computer vision. Explain how vehicle detection, density calculation, and signal timing adjustment should work."

**AI-Generated Output:**

The system can use a camera to capture traffic images and YOLO to detect vehicles. The detected vehicles are counted for each road, and traffic density is calculated.

The signal controller can follow these rules:

- High traffic density: Allocate longer green signal time.
- Medium traffic density: Allocate moderate green signal time.
- Low traffic density: Allocate shorter green signal time.
- Emergency vehicle detected: Give priority to the emergency vehicle's road after ensuring safe signal transitions.

This approach helps reduce unnecessary waiting time and improves traffic flow.

### Technique 3: Step-by-Step Prompting

**Prompt:**

"Explain the development of an AI-based smart traffic management system step by step. The system should use computer vision to detect vehicles, calculate traffic density, and dynamically control traffic signals. Include the algorithm, required hardware, software, and working procedure."

**AI-Generated Output:**

**Step 1: Image Acquisition**
Install cameras at traffic junctions to capture real-time video footage.

**Step 2: Vehicle Detection**
Use YOLO to detect different types of vehicles from the captured frames.

**Step 3: Vehicle Counting**
Count the detected vehicles in each lane.

**Step 4: Traffic Density Calculation**
Calculate traffic density based on the number of detected vehicles and available road capacity.

**Step 5: Signal Timing Allocation**
Assign green signal duration according to the calculated traffic density, subject to minimum and maximum timing limits.

**Step 6: Emergency Vehicle Detection**
Identify emergency vehicles and provide appropriate signal priority.

**Step 7: System Monitoring**
Continuously monitor traffic conditions and repeat the process to update signal timings.

### Technique 4: Constraint-Based Prompting

**Prompt:**

"Design a smart traffic management system using computer vision under the following constraints:

1. Use Python as the primary programming language.
2. Use YOLO for vehicle detection.
3. Use OpenCV for image processing.
4. The system must classify traffic into low, medium, and high density.
5. Green signal duration must be between 10 and 60 seconds.
6. Emergency vehicles must receive priority.
7. The system should be affordable and suitable for a small-scale prototype.

Provide the architecture, algorithm, hardware requirements, and limitations."

**AI-Generated Output:**

**System Architecture:**

1. Camera captures live traffic footage.
2. OpenCV processes the video frames.
3. YOLO detects and classifies vehicles.
4. Vehicle counts are used to calculate traffic density.
5. A control algorithm assigns signal timings between 10 and 60 seconds.
6. Emergency vehicle detection activates a priority mechanism.
7. The signal controller updates the traffic lights.

**Hardware Requirements:**
- Raspberry Pi or computer.
- Camera module or webcam.
- Traffic signal LEDs.
- Microcontroller (if required).
- Power supply.

**Software Requirements:**
- Python.
- OpenCV.
- YOLO.
- NumPy.

**Limitations:**
- Poor lighting may affect vehicle detection.
- Heavy rain and fog may reduce camera accuracy.
- Incorrect vehicle detection may lead to improper signal timing.
- Real-world implementation requires safety mechanisms and traffic authority approval.

## 7. COMPARISON AND EVALUATION TABLE

| Prompting Technique | Quality | Accuracy | Depth |
|---|---|---|---|
| Naïve Prompt | Moderate | Moderate | Low |
| Role-Based Prompting | High | High | High |
| Few-Shot Prompting | High | High | Moderate |
| Step-by-Step Prompting | High | High | High |
| Constraint-Based Prompting | Very High | High | Very High |

## 8. ANALYSIS AND OBSERVATIONS

1. The naïve prompt generated a general overview but lacked detailed implementation steps and technical specifications.

2. Role-based prompting produced more professional and technically relevant suggestions by assigning ChatGPT the role of an experienced engineer.

3. Few-shot prompting improved the response by providing examples that helped ChatGPT understand the expected traffic control behaviour.

4. Step-by-step prompting generated a structured explanation of the complete system workflow, making implementation easier to understand.

5. Constraint-based prompting produced the most practical response because it considered specific hardware, software, timing limits, and implementation requirements.

6. Overall, improved prompts generated more detailed and relevant responses than the naïve prompt. However, simple prompts can still be effective when only a general overview is required.

## 9. FINAL SELECTED PROMPTING TECHNIQUE

**Selected Technique: Constraint-Based Prompting**

Constraint-based prompting was selected because it provides a clear set of technical requirements and limitations. It generates more focused, structured, and feasible solutions that are useful for actual engineering implementation.

## 10. REFINED / FINAL PROMPT

"Act as a professional AI and computer vision engineer. Design an AI-based Smart Traffic Management System that uses real-time camera footage to detect and count vehicles at a traffic junction.

Use Python, OpenCV, and YOLO for vehicle detection and image processing. Classify traffic density into low, medium, and high categories. Dynamically allocate green signal timings between 10 and 60 seconds based on traffic density. Include emergency vehicle detection and signal priority.

Provide a detailed system architecture, required hardware and software components, working algorithm, implementation steps, possible challenges, and methods to evaluate the system's performance. Ensure the proposed solution is affordable and suitable for a small-scale engineering prototype."

## 11. ENGINEERING VALIDATION

The proposed system can be validated through the following tests:

| Test Case | Expected Result |
|---|---|
| Low vehicle count | Shorter green signal duration |
| Medium vehicle count | Moderate green signal duration |
| High vehicle count | Longer green signal duration |
| Ambulance detected | Emergency signal priority |
| No vehicles detected | Avoid unnecessary green signal allocation |
| Multiple roads with different densities | Higher-density roads receive appropriate priority |

**Performance Evaluation Metrics:**
- Vehicle detection accuracy.
- Vehicle counting accuracy.
- Average vehicle waiting time.
- Traffic congestion reduction.
- Emergency vehicle response time.

The proposed approach is technically feasible for a small-scale prototype. Actual performance must be verified through simulation and real-time testing before deployment.

## 12. CONCLUSION

Thus, the experiment was successfully conducted using different prompting techniques in ChatGPT to solve the engineering problem of developing an AI-based Smart Traffic Management System.

The responses generated using naïve, role-based, few-shot, step-by-step, and constraint-based prompting techniques were compared based on quality, accuracy, and depth.

It was observed that improved prompting techniques produced more relevant, structured, and detailed solutions. Among the techniques evaluated, constraint-based prompting provided the most practical and implementation-oriented response.

**RESULT:** The prompt for the above-mentioned engineering problem was executed successfully, and different prompting techniques were compared and evaluated.
