# AI in Healthcare Capstone: COVID-19 Detection & ICU Prediction

![Stanford Medicine](https://img.shields.io/badge/Stanford-Medicine-8C1515?style=for-the-badge&logo=stanford-university&logoColor=white)
![Data Analysis](https://img.shields.io/badge/Focus-Clinical%20Data%20Analysis-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

> **Official Certificate:** [Click here to view the Stanford credential](certificates/Stanford%20(Coursera).pdf)

## Project Overview
This repository documents my **Decision Portfolio** as the completion of the **"AI in Healthcare"** specialization by Stanford University.

In this simulated project, I acted as a **Data Analyst (Lead Analyst)**, being responsible for the **strategy, validation, and ethics** of the AI models, supervising technical decisions to ensure the technology was safe for hospital use.

---

## My Challenges and Solutions (Nursing + Data Perspective)

As a Nursing student, my role was to translate the clinical need for the development team.

### 1. Data Cleaning
* **The Problem:** There were more exams than patients.
* **My Decision:** I directed the data split by **Patient ID**. If we split randomly, the computer could "memorize" the patient instead of learning the disease (Data Leakage).

### 2. Computer Vision (X-Ray)
* **The Error Found:** The technical team applied a "Random Zoom" on the images to try to improve the model.
* **My Correction:** I identified that this cut vital parts of the lung. I vetoed the zoom and allowed only slight rotations, ensuring **Clinical Preservation** (the image needs to remain readable for a doctor).

### 3. Tabular Data (EHR)
* **Fair Validation:** Since we had few severe cases (only 300 intubations), I required the use of **Stratified Cross-Validation**. This ensures that every test has the right amount of sick patients, avoiding false successes.

---

## Metrics and Results

### Why did I reject "Accuracy"?
The model had 91% accuracy, but I realized this was misleading because the majority of patients were healthy. If the model just "guessed" that all patients were healthy, it would have a high accuracy.
* **Decision:** I chose the **AUROC** metric (0.872), which proved to be much better to distinguish who was really sick.

### 2h vs 48h Prediction
* The **2-hour** model was more accurate but useless (the patient was already visibly severe).
* I chose the **48-hour** model because, even with slightly more errors, it gives time for the nursing and medical team to prepare the ICU. **Clinical Utility > Pure Accuracy.**

---

## Ethics and Safety (FDA)

To ensure that the software could be approved by regulatory bodies (like FDA/ANVISA):
1.  **Classification:** I defined the system as **Decision Support (Level II)**. The human always has the final word.
2.  **Bias:** I requested mandatory tests in groups of different races and genders to ensure the AI was not biased.

---

## Project Limitations
This project was developed in an academic and simulated context, based on historical data and controlled scenarios. 
The presented models **must not be used directly in real clinical environments** without external validation, prospective studies, multicenter testing, and approval by appropriate regulatory agencies (e.g., FDA/ANVISA).

Additionally, data-related limitations, such as class imbalance, limited sample size for critical events, and potential population bias, may affect the generalizability of the results.

---

## Key Learnings
- Traditional metrics such as accuracy can be misleading in clinical scenarios with imbalanced datasets.
- The **clinical utility** of a model may be more important than its isolated numerical performance.
- AI applied to healthcare requires rigorous validation, ethical oversight, and a strong focus on patient safety.
- Nursing professionals play a strategic role in bridging clinical needs and data-driven solutions.
- AI models should be designed as **clinical decision support tools**, not as replacements for human judgment.

---

### Contact
**Inácio Santos Vieira**
[LinkedIn](https://www.linkedin.com/in/inaciosantosvieira/)
