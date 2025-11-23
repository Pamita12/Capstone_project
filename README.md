## Contents
1. [Group Information](#group-information)
2. [Project Name](#project-name)
3. [Project Purpose](#project-purpose)
4. [Business Benefits](#business-benefits)
5. [Installation and Configuration Instructions](#installation-and-configuration-instructions)
6. [Running the project_flask Application](#running-the-project_flask-application)
7. [Appendix](#appendix)

## Group Information:
- **Project Sponsor**: Sean Bridgeman.
- **Project Coordinator**: Prof. Manjari Maheshwari 
- **Core Team Members (5-person team):**
    - Eddie Morgan: Team Lead
    - Diego Moreno
    - Sofia Alfaro
    - Pamela Gatica
    - Yazan Al-Shash. 
## Project Name
- **Retention Framework Insights**
## Project Purpose
- This project is help a local company in Tecumseh, ON, understand how users move through their learning journey.
- By analyzing where users drop off and how they engage, our final dashboard may give clear insights to improve retention, help with better decision making and show possible opportunities to make the learning experience more engaging and effective. 
- The data was sourced through a third party (Halight) via Athena; an AWS SQL Server.
## Business Benefits
- Benefit 1: Improve user retention by identifying drop-off points and enabling targeted engagement strategies.
- Benefit 2: Support data-driven decision-making for product and customer strategy teams through weekly lifecycle insights.
- Benefit 3: Increase efficiency by automating user journey reporting and reducing manual analysis time.
- Benefit 4: Discover growth opportunities by uncovering patterns in user behavior and lifecycle progression.
## Appendix:
- The deliverables for our Capstone Project are listed down below:


1. Preliminary Dashboard in Power BI

        - Displays insights about user engagement metrics, such as:
            - Online users (Current Month vs Last Month and Last Year)
            - Average Daily Engagement Score over time
            - Total & Average Lifetimes per User

2. RCS dataset (CSV)

- Route: /
- Functionality: Render homepage.html and provide navigation to other sections.

3. Exploratory Data Analysis (EDA) in Jupyter Notebook (ipynb)

- Route: /about
- Functionality: Render about.html with an overview of the dataset and application purpose.

4. Business Case & Project Charter

- Route: /data
- Functionality: Connect to the SQLite database, fetch records from student_health, and render data_table.html.

5. Group Information Page

- Route: /group
- Functionality: Render group_info.html with information about health groups.


Non-Functional Requirements:

1. Usability

- Ensure responsive and user-friendly web pages.
- Use well-styled HTML templates.

2. Performance

- Optimize database queries for efficiency.
- Ensure fast navigation between pages.

3. Portability

- Ensure the application runs on all major platforms.
- Use pathlib for cross-platform compatibility.

4. Maintainability

- Follow a clear code structure.
- Use comments and descriptive function names.

5. Security

- Use parameterized queries to prevent SQL injection.
- Avoid exposing sensitive data during debugging.


Technical Requirements:

1. Software Dependencies

- Python 3.8 or later.
- Required libraries: Flask, SQLite3, Pathlib.

2. Directory Structure

- app.py (Main application file)
- templates/ (HTML templates directory)
* homepage.html
* about.html
* data_table.html
*group_info.html

- static/ (Directory for CSS, JS, and images)
- student_health_data.db (SQLite database file)

3. Database Schema

- SQLite database: student_health_data.db
- Table: student_health
* Columns(14): [ Student_ID, Age, Gender, Heart_Rate, Blood_Pressure_Systolic, Blood_Pressure_Diastolic, Stress_Level_Biosensor, Stress_Level_Self_Report, Physical_Activity, Sleep_Quality, Mood, Study_Hours, Project_Hours, Health_Risk_Level ]


Example Use Case:
- Homepage: User gets a welcome message and sees navigation links to other sections for additional information about the project.
- About Page: User reads an overview of the dataset.
- Data Page: User views student health data entered in the data_table.
- Group Information Page: User sees the names and ID numbers of the group members who worked on the project_flask.


Testing Requirements:
- Unit tests for route responses.
- Functional tests for database connection and data retrieval.
- Integration tests to verify template rendering.

Code Implementation:
- Here's a brief overview of the project_flask code and recommendations for running it in some python environments:
[
from flask import Flask, render_template
import sqlite3
import pathlib

base_path = pathlib.Path(__file__).parent
db_name = "student_health_data.db"
db_path = base_path / db_name

app = Flask(__name__)

@app.route("/")
def homepage():
return render_template("homepage.html")

@app.route("/about")
def about_page():
return render_template("about.html")

@app.route("/data")
def data_page():
con = sqlite3.connect(db_path)
cursor = con.cursor()
students = cursor.execute("SELECT * FROM student_health").fetchall()
con.close()
return render_template("data_table.html", students=students)

@app.route("/group")
def group_info():
return render_template("group_info.html")

if __name__ == "__main__":
app.run(debug=True)
]

Recommendations for Code Execution:
- Ensure you have the necessary dependencies installed within the particular environment
- Use %run project_flask.py to run the Flask app within the notebook
- Use python project_flask.py to run the Flask within VSCode terminal
- Make sure your HTML templates are in the correct directory.
