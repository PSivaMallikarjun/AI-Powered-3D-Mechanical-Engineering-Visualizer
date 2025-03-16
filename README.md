# AI-Powered Mechanical Engineering Learning Tool with 3D Visualization

## Overview
This project is designed to assist students and lecturers in mechanical engineering by providing AI-powered explanations and interactive 3D visualizations of complex engineering concepts. Instead of memorizing formulas, users can engage with an AI tutor that explains topics dynamically and interact with 3D models for better understanding.

## Key Features
- **AI Tutor for Mechanical Engineering**: Utilizes self-attention mechanisms (like ChatGPT & BERT) to understand and explain mechanical engineering concepts.
- **Interactive 3D Models**: Users can manipulate 3D models to visualize topics like fluid mechanics, strength of materials, and refrigeration cycles.
- **Question-Based Learning**: Users can type any mechanical question, and the AI will generate answers based on engineering knowledge.

## Example Interaction
**Question:** "How does Reynolds number affect fluid flow?"
**AI Response:** "Reynolds number determines whether the flow is laminar (smooth) or turbulent (chaotic). If the Reynolds number is below 2000, the flow is laminar. If it's above 4000, it's turbulent."

## Setup Instructions (Google Colab)
1. Open [Google Colab](https://colab.research.google.com/).
2. Create a new notebook and install necessary dependencies:
   ```python
   !pip install openai numpy matplotlib plotly
   ```
3. Import required libraries:
   ```python
   import openai
   import numpy as np
   import matplotlib.pyplot as plt
   import plotly.graph_objects as go
   ```
4. Set up OpenAI API key (if using GPT-based AI):
   ```python
   openai.api_key = "your-api-key"
   ```
5. Implement AI-based query handling:
   ```python
   def ask_ai(question):
       response = openai.ChatCompletion.create(
           model="gpt-3.5-turbo",
           messages=[{"role": "user", "content": question}]
       )
       return response["choices"][0]["message"]["content"]
   ```
6. Create 3D visualization example (e.g., beam bending):
   ```python
   fig = go.Figure()
   fig.add_trace(go.Scatter3d(x=[0, 1], y=[0, 0], z=[0, 0.5], mode='lines', line=dict(width=10)))
   fig.update_layout(title="Beam Bending Example", margin=dict(l=0, r=0, b=0, t=40))
   fig.show()
   ```
## Screenshots
![Screenshot 2025-03-15 175116](https://github.com/user-attachments/assets/9c5f4b0d-0614-4e8e-93ae-075612c61dbb)
![Screenshot 2025-03-15 175207](https://github.com/user-attachments/assets/838d0a82-4229-4839-8e16-a6dcf9a7e749)
![Screenshot 2025-03-15 175612](https://github.com/user-attachments/assets/53e0f06a-bf60-442a-8765-b25c4fd704a8)
![Screenshot 2025-03-15 175628](https://github.com/user-attachments/assets/2d0c2cc5-6d71-4a08-a052-ac4fc223f54f)
![Screenshot 2025-03-15 181230](https://github.com/user-attachments/assets/301b6fe7-61fb-4d68-a811-9aba0bc105df)
![Screenshot 2025-03-15 181412](https://github.com/user-attachments/assets/3e2a8717-27bc-425d-837d-004f133a51ff)
![Screenshot 2025-03-15 185142](https://github.com/user-attachments/assets/8052d862-1153-4520-9057-6f41272a17b1)
![Screenshot 2025-03-15 185157](https://github.com/user-attachments/assets/4dcc0a96-3fbe-4798-87fb-51afb2c7df18)
![Screenshot 2025-03-15 185551](https://github.com/user-attachments/assets/cf40e0ac-03b0-48e3-bd2a-bba50eddc5e6)
![Screenshot 2025-03-15 185610](https://github.com/user-attachments/assets/25f3ea98-7b6e-41e2-8612-2bb8c7a70729)
![Screenshot 2025-03-15 185639](https://github.com/user-attachments/assets/8fe40914-e5be-476e-9760-4ff2e1bc63f9)

## Usage
- Run the notebook and input a mechanical engineering question.
- AI provides textual explanations.
- 3D models visualize mechanical concepts interactively.

## Future Enhancements
- Expand the AI model to include more detailed engineering explanations.
- Integrate interactive simulations for heat transfer, thermodynamics, and structural analysis.
- Support VR-based interactions for immersive learning.

## License
This project is open-source and available for educational purposes.

---
Download this README file for reference. Happy learning!

