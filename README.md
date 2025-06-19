
# PyCity Schools Analysis

## Overview

This analysis evaluates the academic performance of schools in a fictional district using budget, school type, and size metrics. By merging school-level and student-level datasets, key insights were drawn about the relationship between spending, school size, and performance.

## Key Findings

- Schools with **higher per-student spending ($645–$675)** tended to **underperform** compared to those with smaller budgets ($585 or less).
- **Smaller and medium-sized schools** consistently outperformed large schools in math performance, with pass rates around **89–91%** versus **67%** in larger schools.
- **Charter schools** outperformed **district public schools** across all metrics, but further analysis is needed to determine if this is due to operational differences or smaller average enrollments.

---

## Project Structure

- `Resources/`: Contains the original CSV data files:
  - `schools_complete.csv`
  - `students_complete.csv`
- `PyCitySchools.ipynb`: The Jupyter Notebook with all data processing and analysis steps.
- `README.md`: Documentation for the project.

---

## Technologies and Libraries Used

- **Python 3**
- **Pandas** for data manipulation
- **Pathlib** for file path handling
- **Jupyter Notebook** for interactive analysis

---

## Getting Started

### Dependencies

Install required libraries using:

```bash
pip install pandas
```

### Running the Analysis

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/pycity-schools-analysis.git
   cd pycity-schools-analysis
   ```

2. Open the notebook in Jupyter:
   ```bash
   jupyter notebook PyCitySchools.ipynb
   ```

3. Run all cells to execute the full analysis pipeline.

---

## Data Preparation

Data was read and combined using:

```python
school_data = pd.read_csv("Resources/schools_complete.csv")
student_data = pd.read_csv("Resources/students_complete.csv")
school_data_complete = pd.merge(student_data, school_data, how="left", on="school_name")
```

---

## Summary Metrics

### District-Level Metrics

- **Total Schools**: 15
- **Total Students**: 39,170
- **Total Budget**: $24,649,428
- **Average Math Score**: 78.99
- **Average Reading Score**: 81.88
- **% Passing Math**: 74.98%
- **% Passing Reading**: 85.81%
- **% Overall Passing**: 65.17%

### Top Performing Schools

| School Name           | Type     | % Overall Passing |
|----------------------|----------|-------------------|
| Cabrera High School  | Charter  | 91.33%            |
| Thomas High School   | Charter  | 90.95%            |
| Griffin High School  | Charter  | 90.60%            |

### Bottom Performing Schools

| School Name             | Type     | % Overall Passing |
|------------------------|----------|-------------------|
| Rodriguez High School  | District | 52.99%            |
| Figueroa High School   | District | 53.20%            |
| Huang High School      | District | 53.51%            |

---

## Analysis by Category

### Spending Ranges (Per Student)

| Range      | % Overall Passing |
|------------|-------------------|
| <$585      | 90.37%            |
| $585-630   | 81.42%            |
| $630-645   | 62.86%            |
| $645-680   | 53.53%            |

### School Size

| Size            | % Overall Passing |
|-----------------|-------------------|
| Small (<1000)   | 89.88%            |
| Medium (1000–2000) | 90.62%        |
| Large (2000–5000)  | 58.29%        |

### School Type

| Type     | % Overall Passing |
|----------|-------------------|
| Charter  | 90.43%            |
| District | 53.67%            |

---

## Conclusion

This analysis highlights systemic trends in the PyCity School District:
- Higher spending does not correlate with better academic performance.
- Smaller and medium schools consistently achieve higher pass rates.
- Charter schools excel across all major academic indicators.

---

## Contact

For questions or collaboration, please contact:

**Ikaneng Jack Malapile**  
📧 [YourEmail@example.com]  
🔗 [GitHub Profile](https://github.com/yourusername)
