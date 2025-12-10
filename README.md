# 🥗 Nutri-Bot: Reinforcement Learning Demo

## 🎯 Project Overview
**Nutri-Bot** is an interactive Reinforcement Learning (RL) agent that learns dietary preferences through Human-in-the-Loop (HITL) feedback.

This project demonstrates the transition from **Manual Data Labeling** to **AI Domain Specialization**. Instead of hard-coding rules (e.g., `if apple then eat`), the system uses a **Q-Learning algorithm** to develop a policy based on real-time feedback from a human expert.

## How It Works
1.  **Observation:** The Agent observes a state (e.g., an image of a Salad or a Burger).
2.  **Action:** The Agent chooses an action (Eat or Pass) based on its current Q-Table (Brain).
3.  **Feedback (RLHF):** The Human Expert (User) provides a reward signal:
    * **+1 Reward:** Correct decision.
    * **-1 Penalty:** Incorrect decision.
4.  **Learning:** The Agent updates its Q-Values using the Bellman Equation logic, reinforcing positive behaviors and deterring negative ones.

## Technical Stack
* **Frontend:** HTML5, CSS3 (Modern Flexbox/Grid), Vanilla JavaScript (ES6+).
* **Algorithm:** Tabular Q-Learning (Reinforcement Learning).
* **No External Dependencies:** Lightweight and runs entirely in the browser.

## Skill Demonstration
This application highlights three key stages of AI development:

### 1. Data Annotation (The "Teacher")
In the early stages of training, the human user acts as a Data Labeler, manually verifying every decision the bot makes. This mirrors the industry process of creating "Ground Truth" datasets.

### 2. Model Training (The "Student")
As interaction continues, the application visualizes the **Exploration vs. Exploitation** trade-off.
* **Exploration:** The bot tries random actions to learn (e.g., trying to eat a burger to see what happens).
* **Exploitation:** The bot uses its learned Q-Values to make the best decision.

### 3. Domain Specialization (The "Architect")
The visualized **Q-Table** allows us to inspect the "Black Box." By analyzing the weights assigned to "Eat" vs "Pass" for each item, we can verify if the model has converged on a healthy policy or if it requires fine-tuning (e.g., adjusting the Learning Rate or Epsilon).

## Future Improvements
* **Computer Vision Integration:** Incorporate TensorFlow.js (MobileNet) to allow the agent to recognize *real* food photos uploaded by the user, rather than static emojis.
* **Complex States:** Add variables for "Hunger Level" or "Time of Day" to make the decision matrix multidimensional.

## 💻 How to Run
1.  Download `index.html`.
2.  Open it in any web browser (Chrome, Firefox, Safari).
3.  Start training your agent!
