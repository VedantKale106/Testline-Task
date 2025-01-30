# NEET Rank Prediction and College Eligibility

This project uses a Random Forest Regressor model to predict the expected rank of a student based on their NEET marks. Additionally, it provides a list of medical colleges where the predicted rank falls within the opening and closing ranks.

## Project Overview

- **Input**: NEET marks of a student (an integer value between 350 to 750).
- **Output**: Predicted NEET rank and a list of medical colleges where the student might be eligible based on their predicted rank.

## Files and Code

1. **data preparation**: The data is prepared using two datasets:
   - NEET Marks vs Expected Rank.
   - College data with opening and closing ranks.

2. **Model Training**: A Random Forest Regressor model is trained on the NEET marks and expected rank dataset.

3. **Prediction**:
   - The trained model predicts the rank for a student based on their NEET marks.
   - The model then filters and returns a list of medical colleges where the student's predicted rank falls between the opening and closing ranks.

4. **Plotting**: A plot is generated to visualize the relationship between NEET marks and predicted rank.

## Requirements

You will need the following libraries to run this code:

- \`numpy\`
- \`pandas\`
- \`matplotlib\`
- \`sklearn\`

You can install them using \`pip\`:

\`\`\`bash
pip install numpy pandas matplotlib scikit-learn
\`\`\`

## How to Run

1. Clone or download this repository.
2. Install the necessary libraries.
3. Run the script in a Python environment (Jupyter Notebook or any IDE like VS Code).

## Example Usage

\`\`\`python
# Example: Predict for a student scoring 700 marks
student_marks = 700
predicted_rank, colleges = predict_college(student_marks)

print(f\"Predicted NEET Rank for {student_marks} marks: {predicted_rank}\")
print(f\"Eligible Colleges: {', '.join(colleges)}\")
\`\`\`

This will output the predicted NEET rank and the list of eligible colleges based on the given marks.

## Warnings

- The model has been trained on a small sample of data, so predictions may not be highly accurate for all cases.
- Ensure that the NEET marks you provide are in the correct range (350 to 750) for the best predictions.

## Data Sources
The project utilizes three main data endpoints:
- Quiz Submission Data: Contains individual quiz attempt details including scores, timing, and response patterns
- Quiz Questions: Comprehensive database of questions with detailed solutions and metadata
- Historical Quiz Data: Performance trends and statistics (based on file structure)

## Features
- Quiz submission analysis
- Question-level performance tracking
- User performance metrics including:
  - Accuracy rates
  - Speed metrics
  - Trophy/achievement tracking
  - Mistake correction patterns

## Setup Instructions

### Prerequisites
- Python 3.x
- Jupyter Notebook

### Required Python Packages
```bash
pip install pandas
pip install requests
```

### Project Structure
```
vedantkale106-testline-task.git/
├── Historical Quiz Data.ipynb
├── Neet Model.ipynb
├── Quiz Submission Data.ipynb
└── Quiz_endpoint.ipynb
```

### Configuration
1. Clone the repository
2. Install the required dependencies
3. Launch Jupyter Notebook
4. Open the desired notebook file

## Technical Approach

### Data Collection
- Quiz submission data is fetched from `api.jsonserve.com`
- Question bank data is retrieved from `jsonkeeper.com`
- All API calls use the `requests` library for data fetching

### Data Processing
1. **Quiz Submissions**
   - Processes individual attempt data
   - Tracks metrics like accuracy, speed, and trophy levels
   - Monitors mistake correction patterns

2. **Question Analysis**
   - Processes question metadata
   - Includes difficulty levels and topics
   - Tracks user response patterns

3. **Performance Analytics**
   - Calculates performance metrics
   - Generates user rankings
   - Tracks improvement over time

## API Endpoints
- Quiz Submission: `https://api.jsonserve.com/rJvd7g`
- Question Bank: `https://www.jsonkeeper.com/b/LLQT`

## Data Structure
- Quiz submissions include:
  - User performance metrics
  - Timing data
  - Response mapping
  - Question-level analytics

- Question bank includes:
  - Detailed questions
  - Solutions
  - Topic categorization
  - Difficulty levels
