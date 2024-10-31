Multi-agent Audit Report Generator

An intelligent audit workflow system that automates the generation of comprehensive audit reports using LangGraph, MLflow, and advanced language models. The system processes control testing data, risk matrices, and historical audit information to produce structured, professional audit reports.

🌟 Features

- Automated Workflow Processing: Orchestrated multi-step audit process using LangGraph
- Intelligent Risk Assessment: Analysis of control testing data with risk categorization
- Report Generation: Automated creation of structured audit reports in both markdown and DOCX formats
- MLflow Integration: Comprehensive tracking of metrics, parameters, and artifacts
- Interactive Interface: User-friendly Gradio interface for file uploads and workflow execution
- Quality Evaluation: Built-in evaluation metrics for content accuracy, structure, and readability

🛠 Technical Architecture

The system consists of several key components:

- Workflow Controller: Orchestrates the entire audit process
- Preprocessor Agent: Handles initial data processing and validation
- Risk Assessment Agent: Analyzes control testing data and generates risk assessments
- Report Generator Agent: Creates structured audit reports
- Error Handler: Manages error recovery and retry logic
- User Interaction Handler: Processes user inputs and commands

![image](https://github.com/user-attachments/assets/3bbd5a94-0e98-41bf-94b8-5d1f8053b979)

📋 Prerequisites

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
