# Professional Biography
## Contact Information
Email: schumanc@mail.uc.edu

Phone #: 419-819-6226

## Work Experience
### Machine Learning Engineer

#### **Etegent Technologies** - 6 co-op Semesters

**Machine Learning Engineer II** December 2025 – Present
* Developed novel neural network architectures, training strategies, and temporal modeling techniques for small-target object detection, reducing false alarms by over 1,000× while helping secure significant followon customer work 
* Served as technical lead for a 3-engineer research effort into explainable AI for model monitoring and dataset development, enabling localization of subtle anomalies within 10 million+ pixel imagery and supporting technical demonstrations to executive leadership and customers 
* Redesigned legacy synthetic data pipeline using a modular pipe-and-filter architecture and implemented RL-based simulation parameter optimization, increasing recall by 10% on a low-shot object detection task 

**Machine Learning Engineer I** January 2025 – December 2025 
* Led development of object detection model to meet strict contractual performance thresholds, improving accuracy via custom rotated detection head, multi-stage training on curated large pretraining data, and ensembling small and large target models 
* Architected internal ML EDA web app using Dash and Redis, enabling rapid dataset exploration, cleaning, model evaluation and feature-performance analysis, reducing model iteration time across 4 core projects 
* Rescued failing remote sensing object detection project by eliminating data leakage, optimizing training with CLAHE preprocessing and hyperparameter tuning, refining bounding boxes with SAM2, and building an improved inference pipeline with tuned NMS and an SVM recognition filter, thus boosting model accuracy and client satisfaction in 2 weeks 
* Served as primary maintainer of core MLOps inference pipeline used by every team project 

**Machine Learning Engineer Intern** May 2023 – January 2025

## Senior Design Project Sought
To expand on my current work in computer vision, reinforcement learning, and synthetic data development, I am seeking an opportunity to work on deep learning-based approaches within a variety of applied fields, including world models for synthetic data development and embodied-agent training.

**Dream Project Description**

My dream project would be working on utilizing and researching improvements for training robots through exo-centric video-based data.  This task involves training humanoid robots to perform tasks without requiring curated human demonstration data.  This field of work, if perfected, can allow for much greater scaling of embodied agents due to allowing training of robot actions through all available security camera/YouTube-style footage.
The envisioned (but not perfected) pipeline would look like:
* Use 2-D -> 3-D generative models such as VGGT to produce voxel-like representations from camera footage of a single industrial task
* Leverage another model to produce gaussian-splats of the task video and convert this into 3-D meshes or CAD models ingestible by a RL training gym like Issac Sim
* Utilize imitation learning and/or techniques such as from this paper (Tool-as-Interface: Learning Robot Policies from Observing Human Tool Use) to train a simulated agent to perform the task
* If this could all be done, additional research could include:
* World models for simulating additional data
* Testing model in a physical agent (would likely require additional partnerships)
* Training multiple skills into single policy model / Using router network to utilize multiple disparate models to coordinate more complex simulated tasks
The end product would be an endpoint where a video sequence of a human task could be uploaded, and a few hours/days later a robot policy would be automatically produced with the capability to reasonably imitate the provided task.

**Alternative areas of interest**

While the above work would be super cool, I am totally cool with doing any deep-learning focused research and development work.
