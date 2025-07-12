---

# **🎓📈 Education & Career Success Dataset**  
A comprehensive dataset tracking **5,000 individuals** to analyze factors influencing career progression, salary, and satisfaction.  

---

## **📊 Dataset Overview**  
| **Metric**          | **Value**       |
|---------------------|-----------------|
| Rows                | 5,000           |
| Columns             | 20              |
| Missing Values      | None            |
| Primary Use Cases   | Classification, Regression, EDA |

---

## **🔍 Column Descriptions**  

### **1. Personal & Educational Background**  
| Column                | Description                          | Data Type      |
|-----------------------|--------------------------------------|----------------|
| `Student_ID`          | Unique identifier                   | `Object` (String) |
| `Age`                 | Age of the individual               | `Integer`      |
| `Gender`              | Gender (Male, Female, Other)        | `Object` → `Integer` (Encoded) |
| `High_School_GPA`     | High school GPA (0.0–4.0)           | `Float`        |
| `SAT_Score`           | SAT exam score (400–1600)           | `Integer`      |
| `University_Ranking`  | Rank of attended university         | `Integer`      |
| `University_GPA`      | University GPA (0.0–4.0)            | `Float`        |
| `Field_of_Study`      | Major (e.g., Arts, Medicine)        | `Object` → `Integer` (Encoded) |

### **2. Professional Development**  
| Column                   | Description                          | Data Type      |
|--------------------------|--------------------------------------|----------------|
| `Internships_Completed`  | Number of internships               | `Integer`      |
| `Projects_Completed`     | Academic/professional projects      | `Integer`      |
| `Certifications`         | Professional certifications earned  | `Integer`      |
| `Soft_Skills_Score`      | Communication/teamwork rating (1–10)| `Integer`      |
| `Networking_Score`       | Networking ability (1–10)           | `Integer`      |

### **3. Career Outcomes**  
| Column                   | Description                          | Data Type      |
|--------------------------|--------------------------------------|----------------|
| `Job_Offers`             | Number of job offers received       | `Integer`      |
| `Starting_Salary`        | First employment salary ($)         | `Float`        |
| `Career_Satisfaction`    | Satisfaction rating (1–10)          | `Integer`      |
| `Years_to_Promotion`     | Years until first promotion         | `Integer`      |
| `Current_Job_Level`      | Entry/Mid/Senior                   | `Object` → `Integer` (Encoded) |
| `Work_Life_Balance`      | Balance rating (1–10)               | `Integer`      |
| `Entrepreneurship`       | Pursued entrepreneurship (Yes/No)   | `Object` → `Integer` (Encoded) |

---

## **🧹 Data Preprocessing**  

### **✅ Cleaning Steps**  
1. **No missing values** → All 5,000 entries are complete.  
2. **No spelling errors** → Verified categorical consistency.  
3. **Encoding** → Converted categorical columns to numeric:  
   - `Gender`, `Current_Job_Level`, `Entrepreneurship`: Label-encoded (`Male=0, Female=1`).  
   - `Field_of_Study`: Ordinal-encoded (e.g., `Arts=0, Medicine=1`).  

### **🔍 Before vs. After Encoding**  
**Before**:  
```python
Gender                 object  
Field_of_Study         object  
Current_Job_Level      object  
Entrepreneurship       object  
```

**After**:  
```python
Gender                 int64  
Field_of_Study         int64  
Current_Job_Level      int64  
Entrepreneurship       int64  
```

---

## **🎯 Potential Use Cases**  
### **1. Supervised Learning**  
- **Classification**: Predict `Current_Job_Level` or `Entrepreneurship`.  
- **Regression**: Estimate `Starting_Salary` or `Career_Satisfaction`.

---


## **📊 Suggested Visualizations**  
1. **Correlation Heatmap**:  
   ```python
   sns.heatmap(df.corr(), annot=True)
   ```
2. **Salary vs. GPA Scatterplot**:  
   ```python
   sns.scatterplot(data=df, x="University_GPA", y="Starting_Salary", hue="Field_of_Study")
   ```
---

## **✅ Conclusion**  
✔ **Ready for ML**: Clean, encoded, and no missing values.  
✔ **Versatile**: Supports classification, regression, and EDA.  
✔ **Actionable Insights**: Uncover patterns in education-to-career transitions.  
