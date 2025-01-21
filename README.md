# Quiz Performance Analysis

## Project Overview

This project analyzes quiz performance data (historical and current) to provide personalized insights and recommendations for users looking to improve their performance. It integrates data from two sources, cleans and processes the data, and provides visualizations of performance trends over time. Additionally, the project identifies weak quizzes and suggests areas for improvement, including personalized recommendations based on the user's score and accuracy.

## Approach

1. **Data Loading and Cleaning**:  
   - Historical and current data are loaded from external APIs in JSON format.
   - The `score` and `accuracy` columns are cleaned by removing unnecessary characters (e.g., percentages and commas) and converted into numeric formats for analysis.

2. **Data Merging**:  
   The historical and current datasets are merged into a single DataFrame for comprehensive analysis. This allows performance to be compared across different periods.

3. **Performance Analysis by Quiz**:  
   - Aggregates performance data by `quiz_id` (quiz identification number).
   - Calculates mean and standard deviation for scores and accuracy across all quizzes.
   - Identifies quizzes with low performance (scores/accuracy < 60%) to highlight weak areas.

4. **Time-Based Performance Trends**:  
   - Analyzes performance over time to detect trends in scores and accuracy.
   - Visualizes these trends to track progress or identify periods of stagnation.

5. **User-Specific Performance**:  
   - Extracts individual user performance data based on the `user_id`.
   - Tracks user score improvement over time and provides personalized feedback.

6. **Weakness and Gaps Identification**:  
   - Identifies quizzes where the user has performed poorly (accuracy < 60% or score < 60%).
   - Provides suggestions on which quizzes the user should focus on for improvement.

7. **Advanced Recommendations**:  
   - Suggests focusing on easier quizzes with low scores for improvement.
   - Provides personalized suggestions based on the user’s performance (Beginner, Intermediate, or Advanced).

8. **Student Persona Analysis**:  
   - Defines a user’s learning persona (Beginner, Intermediate, Advanced) based on average scores.
   - Provides specific focus areas for improvement based on the persona.

## Requirements

- Python 3.x
- Libraries:  
  - `pandas`  
  - `requests`  
  - `matplotlib`  
  - `seaborn`

To install the required libraries, run:

```bash
pip install pandas requests matplotlib seaborn

## Cloning the Repository

To clone the repository and set up the project on your local machine, follow these steps:

1. Open your terminal (or command prompt).
2. Clone the repository using the following command:

   ```bash
   git clone https://github.com/yourusername/quiz-performance-analysis.git

Navigate to the project directory:

```bash
cd quiz-performance-analysis
## Running the Script

Once you've cloned the repository and installed the necessary dependencies, you can run the script to analyze the quiz performance data:

1. Run the script:

   ```bash
   python analysis.py
