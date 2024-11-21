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

## Demo (click on the image below)
<a href="https://www.youtube.com/watch?v=2V_gO0vBh2U" target="_blank">
    <img src="https://img.youtube.com/vi/2V_gO0vBh2U/0.jpg" alt="YouTube Video" width="600">
</a>

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




## Challenges
Our journey to implement and evaluate the multi-agent LLM architecture came with several hurdles.  

- Accessing the Llama 3.1 8B model was initially a roadblock due to regional restrictions, as it was only available in the US, but we successfully resolved this.  

- Exploring LangGraph and multi-agent architecture highlighted significant cost implications, with Databricks Model Serving expenses surpassing $100 USD within days of prototyping, prompting us to identify a cost-effective workaround. 

- Throughout the development of the LLM agents, we observed the sensitivity of LLM outputs to prompt instructions, emphasizing the importance of crafting specific and detailed prompts. The complexity of prompt engineering required significant consideration to ensure 
 the desired outputs were consistently achieved. 

- The iterative nature of multi-agent architecture introduced complexity, as each agent's output directly influenced subsequent agents, leading to repetitive and at times daunting experimentation cycles.  

- Testing various prompt variations led to rapid usage spending on the Databricks testing account, further highlighting the cost implications of iterative development. Additionally, the selection of the right model for task-specific requirements proved critical, given   
 the numerous options available, each with distinct strengths and limitations. 

- Additionally, we encountered file access challenges with Databricks Apps, where uploaded files on Volumes were not read properly, requiring in-depth exploration of the Databricks SDK documentation. 

- Given the confidentiality of our input files, we synthetically generated them using Llama 3.1 405B, ensuring our prompts provided sufficient context to produce meaningful test cases. This process was time-intensive but necessary for maintaining data privacy.  

- Finally, balancing this project with full-time responsibilities on multiple projects-imposed time constraints, driving us to focus on simplicity and iterative improvement over feature expansion. 

## Accomplishments
- Our journey pushed boundaries beyond mere technical implementation. We evolved from an ambitious multi-agent design to a **simplified** architecture that prioritizes reliability and maintainability. Through this process, we not only mastered emerging technologies like 
 LangGraph and Databricks platform capabilities but also developed crucial insights into building production-ready AI solutions. Through rigorous experimentation, we transformed this complexity into an elegant, on-demand audit solution that makes sophisticated AI 
 capabilities accessible through a simple web interface 

- We successfully implemented an **evaluation framework** leveraging LLMs as a judge to assess the quality of audit reports generated by our multi-agent LLM model. By defining multiple metrics such as accuracy, completeness, relevancy, and professionalism, we ensured a 
 comprehensive evaluation of the generated reports against control testing data. This approach provided consistent, scalable, and nuanced feedback, enabling iterative improvements in the model's performance and output quality.


## Learnings
- This project underscored the importance of keeping solutions **simple**. While our initial ambition to develop a complex multi-agent system was technically exciting, it introduced cascading debugging challenges where each agent’s output impacted subsequent processes. We 
 learned that architectural elegance often lies in simplicity, enabling better maintainability and streamlined problem-solving.   

- **Collaboration** emerged as a key lesson. Our initial approach of developing agents in silos quickly revealed its inefficiencies. Shifting to a more unified, team-based development strategy fostered knowledge sharing, collective problem-solving, and accelerated 
 progress, transforming our workflow into a synergistic effort.   

- The experience also honed our **communication** skills. Crafting presentations, videos, and documentation required us to distil complex technical concepts into clear, engaging narratives. This ability to effectively convey both the technical sophistication and practical 
 value of our solution proved invaluable for diverse audiences.    

- From a **technical** perspective, we gained hands-on expertise in emerging technologies. Mastering LangGraph’s orchestration, navigating Databricks’ advanced features, and designing intuitive user experiences with Gradio deepened our understanding of modern AI 
 infrastructure. Additionally, exploring Databricks training series and hackathon tutorials broadened our exposure to tools and solutions for building GenAI applications.

## Thank you
Thank you to Databricks team for helping us throughout this hackathon especially June Tan, Jon Levine, Brian Law and Scott Eade
