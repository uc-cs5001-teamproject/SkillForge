## Team Members:
Noah Schumacher

Ryan Broyles

Manjinder Kaur

Minh Nguyen

Akshat Chaturvedi 


## Stakeholder Map

| **Primary**                                                                                            | **Secondary**                                                         | **Hidden**                                                       |
| -------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- | ------------------------------------------------------------ |
| **Robotics Engineer** - Automatic extraction from demonstration.                                       | **VP investing in robotics development** – Company investment leader. | **Robot Teleoperator** – Spend less time manually curating data. |
| **Robotics Engineer** - Training process optimization for camera quality and viewpoint specifications. | **ML-Ops Team Lead** - Requirement of standard formats.               |                                                              |

## User Stories

**US-01:** As a VP of a manufacturing company, I want to develop advanced robotics automation capabilities so that my company minimizes costs and stays competitive.

**US-02:** As a Robotics Engineer, I want the system to extract relevant actions automatically from a demonstration, so I do not have to manually label each step.

**US-03:** As an ML-Ops Team Lead, I want the final model to be available in standard formats, so that my team does not spend time rewriting our proprietary backend to support the model format.

**US-04:** As a Robot Teleoperator, I want the robot to learn from easily generated exo-centric data, so I can spend less time curating manual robot demonstration data.

**US-05:** As a Robotics Engineer, I want the training process to require minimal requirements for camera quality and viewpoint specifications, such that data collection and training can fit my use case easily.

## INVEST Checklist

| INVEST | Independent | Negotiable | Valuable | Estimable | Small | Testable |
| ------ | ----------- | ---------- | -------- | --------- | ----- | -------- |
| US-01  |      ✓       |     ✓       |        ✓  |    ✓       |       ✓|   ✓       |
| US-02  |       ✓      |      ✓      |       ✓   |     ✓      |      ✓ |    ✓      |
| US-03  |      ✓       |       ✓     |      ✓    |      ✓     |     ✓  |     ✓     |
| US-04  |     ✓        |        ✓    |     ✓     |       ✓    |    ✓   |      ✓    |
| US-05  |      ✓       |         ✓   |    ✓      |        ✓   |   ✓    |       ✓   |

## UC-01:US-03 Use Case

**Use Case:** UI for model training 
**Actor:** ML-ops team lead (primary), Computer Vision Engineer (Secondary)

### Preconditions

* Model has been trained by the CVE/Robotics Engineer through the provided SkillForge UI.

### Main Success Flow

1. Save the model as a `.PT` (PyTorch) format.
2. Specify the model path in the proprietary format.
3. Load the PyTorch module through available open-source code and load the saved model state dictionary to initialize the correct weights.
4. Load the model using the documented and specified inputs required for deployment.
5. Obtain inference outputs (robot actions) in the documented and specified format.

### Alternative Success Flow

1. The MLOps engineer saves the model as an ONNX format.
2. The engineer uses the ONNX Runtime library to quantize the model before deployment.

### Exception Flow

1. Model inputs are in the wrong format when used.
2. The system displays an error message and provides a link to the relevant documentation.

### Postcondition

* Loaded model provides expected inference results.

## Acceptance Criteria

### AC-03.1: Main Success Flow

* **Given** the MLOps engineer has saved the model and loaded the correct model file path into their script,
* **When** the `.PT` file is loaded into the initialized model class,
* **Then** the model weights will be correctly loaded.

### AC-03.2: Exception Flow

* **Given** the model inputs (images) are in the incorrect format,
* **When** the inputs are sent to the model's forward function,
* **Then** an exception is raised, and a link is provided in the exception to documentation explaining the correct input format.
