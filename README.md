
## **Assignment Overview: Customer Data Pre-processing and Visualisation**

This assignment is a comprehensive evaluation of my ability to perform critical data preprocessing tasks and to produce insightful data visualisations using real-world-inspired customer data. It mimics a scenario commonly faced by data professionals in the industry, where raw data from company systems must be cleaned, transformed, and structured for meaningful analysis and business decision-making.

The assignment consists of **two major components**:

1. **Data Preprocessing Using Core Python Libraries**
2. **Data Visualisation Using Pandas and Seaborn**

The data provided represents customer records stored in a flat CSV file format, and my role is to programmatically convert, clean, enrich, and segregate this data into usable formats. These tasks are representative of foundational operations in data science workflows, particularly in the early stages of a data pipeline.

---

### **Part 1: Data Pre-processing**

This portion of the assignment was completed strictly using built-in Python libraries (e.g., `csv`, `json`, `os`, `sys`, `time`)—without the use of libraries such as Pandas or NumPy.

The key steps undertaken include:

* **Reading CSV Data**: Using the `csv` module, the raw customer data is read and loaded into Python for transformation.
* **Reconstruction of Nested Data**: The flat structure of the CSV is converted into nested dictionaries to represent complex fields such as vehicle details, credit card information, and addresses.
* **Data Cleaning**: Inconsistencies in the `dependants` field are detected and corrected. Problematic records are identified and logged to ensure traceability.
* **Writing Processed JSON Output**: The transformed data is written into a `processed.json` file to serve as a clean, structured source of truth.
* **Subsets Creation**: Based on the `retired` and `employer` fields, two separate JSON datasets—`retired.json` and `employed.json`—are generated to segment the population for future targeted analyses.
* **Credit Card Validation**: A dedicated function checks the duration between credit card start and end dates. Customers with cards valid for over 10 years are flagged and stored in `remove_ccard.json` for manual inspection.
* **Metric Calculation (Salary-Commute)**: A new derived metric—`Salary-Commute`—is calculated by dividing a customer's salary by their commute distance. Records are then sorted and saved to `commute.json`.

The overall goal is to ensure that downstream data analysts or machine learning practitioners can use a clean and semantically structured dataset without revisiting raw data.

---

### **Part 2: Data Visualisation**

In this section, Pandas and Seaborn are used to generate both univariate and multivariate visualisations of the original dataset. These visualisations support the client’s desire to better understand patterns within their customer base.

Key steps include:

* **Basic Statistics**: Calculation of mean salary and median age using Pandas.
* **Univariate Plots**:

  * Histogram of age with fixed bin width.
  * Dependents distribution, correcting known data issues directly within the visualisation.
  * Age distribution conditioned on marital status.
* **Multivariate Plots**:

  * Salary vs. commute distance.
  * Salary vs. age.
  * Salary vs. age, segmented by number of dependents.

All plots are created with clarity and interpretability in mind, and functionality to save them is included for report generation and presentation.

---

### **Part 3: Code Presentation and Best Practices**

The Python code submitted follows best practices in terms of structure, readability, and maintainability. Care was taken to:

* Use clear, meaningful variable names.
* Encapsulate logic into reusable functions.
* Avoid global variable leakage.
* Handle potential runtime errors (e.g., missing fields, data type mismatches).
* Clearly document code using inline comments and markdown cells in Jupyter Notebooks.

Markdown cells are used extensively to delineate sections and explain decisions, making the codebase easier to understand and navigate.

---

### **Conclusion**

This assignment not only demonstrates my ability to handle end-to-end data preprocessing but also my capability to communicate insights visually. The workflows implemented here are scalable, reusable, and can be directly applied to larger real-world datasets. These are essential skills for a data scientist, as the foundation of all advanced analytics lies in well-prepared and well-understood data.



