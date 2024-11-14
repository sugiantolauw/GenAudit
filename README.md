# Multi-agent Audit Report Generator

An intelligent audit workflow system that automates the generation of comprehensive audit reports using LangGraph, MLflow, and advanced language models. The system processes control testing data, risk matrices, and historical audit information to produce structured, professional audit reports.

## 🌟 Features

- Automated Workflow Processing: Orchestrated multi-step audit process using LangGraph
- Intelligent Risk Assessment: Analysis of control testing data with risk categorization
- Report Generation: Automated creation of structured audit reports in both markdown and DOCX formats
- MLflow Integration: Comprehensive tracking of metrics, parameters, and artifacts
- Interactive Interface: User-friendly Gradio interface for file uploads and workflow execution
- Quality Evaluation: Built-in evaluation metrics for content accuracy, structure, and readability

## 📋 Prerequisites

- Python 3.8+
- Databricks Runtime Environment
- Required Python packages:
  - langgraph
  - langchain
  - mlflow
  - gradio
  - pandas
  - python-docx
  - databricks-sdk

## 🛠 Technical Architecture

The system consists of several key components:

- Workflow Controller: Plan and manage the entire audit report generation process
- Preprocessor Agent: Handles initial data processing and validation
- Risk Assessment Agent: Analyzes control testing data and generates risk assessments
- Report Generator Agent: Creates structured audit reports
- Error Handler: Manages error recovery and retry logic
- User Interaction Handler: Processes user inputs and commands

![image](https://github.com/user-attachments/assets/3bbd5a94-0e98-41bf-94b8-5d1f8053b979)

## Data 
Note that:
- All input files have been synthetically generated by Llama 3.1 405B

Input files:
- Risk Matrix (which details how we classify risk based on its impact)
![image](https://github.com/user-attachments/assets/09739bd1-7748-4165-81fa-d15066415371)
- Control Testing File (which details what the auditor is testing, if the control is adequate or not, and the testing results)
![image](https://github.com/user-attachments/assets/4f863512-c98d-4ad9-97fc-c3ba416b1ce0)
- Previous Audit Report (for same audit but from previous year)
![image](https://github.com/user-attachments/assets/7e4e95f7-8d2f-4242-8a1a-57170df99e7b)

## Output
![image](https://github.com/user-attachments/assets/5ab063df-1dfa-4d53-8221-5f1ed852d658)
![image](https://github.com/user-attachments/assets/af18e448-a11d-4d2e-82c7-9fa77ea42203)
![image](https://github.com/user-attachments/assets/73155e19-3454-4a6a-8de7-998a81b0c3d1)

## Demo



## Challenges
- Getting access to Llama 3.1 8B model which was resolved (Llama 3.1 only available in US region, not AU)
- File Access Issues with Databricks Apps (Couldn't properly read files uploaded to Volumes through Apps)

## Accomplishments


## Learnings

## Thank you
Thank you to Databricks team for helping us throughout this hackathon especially Brian Law and Scott Eade
