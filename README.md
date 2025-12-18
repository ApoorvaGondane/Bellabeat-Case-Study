
---

# Bellabeat Data Analysis: Unlocking Growth with Machine Learning

### 📌 Project Overview

This project analyzes smart device usage data from **Bellabeat**, a high-tech manufacturer of health-focused products for women.

**The Goal:** To identify opportunities for growth in Bellabeat's marketing strategy by analyzing user behavior.
**The Approach:** Unlike standard descriptive analysis, this project utilizes **Python** for longitudinal data processing and **Unsupervised Machine Learning (K-Means Clustering)** to segment users into distinct personas, providing data-driven recommendations for app features and notification scheduling.

---

### 📂 Dataset & Data Engineering

The analysis is based on the [FitBit Fitness Tracker Data](https://www.kaggle.com/arashnic/fitbit) (CC0: Public Domain).

**Key Technical Challenges Solved:**

* **Longitudinal Merging:** Integrated two distinct time periods (March–April and April–May 2016) to create a continuous 60-day timeline.
* **Data Reconstruction:** Engineered a "Sleep Reconstruction" pipeline to recover missing summary statistics for the March–April period by aggregating over 20,000 raw minute-level logs.
* **Feature Engineering:** Created new features such as `Sleep Efficiency` (Time Asleep / Time in Bed) and `Active Minutes Ratio`.

---

### 🛠 Tech Stack

* **Language:** Python 3.x
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn (StandardScaler, K-Means Clustering)

---

### 📊 Key Findings & Analysis

#### 1. User Segmentation (K-Means Clustering)

Using K-Means clustering on activity and sleep variables, I identified three distinct user personas:

| Persona | Characteristics | Health Risk |
| --- | --- | --- |
| **Active Achievers** | High daily steps (>12k), High intensity, Good sleep efficiency. | Low |
| **Balanced Casuals** | Moderate steps (~6k), **Best sleep duration (~7.5 hrs)**. Consistent but low intensity. | Low |
| **At-Risk / Insomniacs** | Moderate steps, **Severe sleep deprivation (<4 hrs)**, High sedentary time (>16 hrs). | **High** |

#### 2. Behavioral Trends

* **The "Double Peak":** Users are most active at **12:00 PM** and **6:00 PM**, with a significant slump in the mid-afternoon (2–4 PM).
* **The "Sunday Dip":** Physical activity drops significantly on Sundays, while sleep duration increases.
* **Sedentary Lifestyle Impact:** A strong negative correlation was found between Sedentary Minutes and Sleep Duration. Users who sit longer sleep worse.

---

### 🚀 Strategic Recommendations

Based on the data, I propose the following marketing strategies:

**1. "Sleep Rescue" Campaign (Targeting At-Risk Users)**

* **Insight:** A subgroup of users (Cluster 1) is physically active but severely sleep-deprived.
* **Action:** Stop generic "Step Count" notifications for this group. Instead, prioritize "Wind Down" alerts at 9 PM and promote Bellabeat’s meditation features to prevent burnout.

**2. Smart Notification Scheduling**

* **Insight:** Activity peaks at 12 PM and 6 PM.
* **Action:** Schedule motivational notifications 30 minutes prior (11:30 AM and 5:30 PM) to catch users before their natural activity windows.

**3. The "Sunday Reset" Pivot**

* **Insight:** Users naturally rest on Sundays.
* **Action:** Shift app interface highlights from "High Intensity" to "Rest & Recovery" on Sundays. Promote Yoga and Sleep Hygiene content to align with user behavior rather than fighting it.

---

### 💻 How to Run This Project

1. Clone the repository:
```bash
git clone https://github.com/YOUR_USERNAME/Bellabeat-Case-Study.git

```


2. Install dependencies:
```bash
pip install -r requirements.txt

```


3. Run the Jupyter Notebook:
```bash
jupyter notebook Bellabeat_Case_Study.ipynb

```



