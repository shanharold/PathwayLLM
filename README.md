<b> Indian Constitution Laws </b>
Introduction
"Indian Constitution Laws" is a real-time, scalable Augmented Generation (RAG) application designed to help users access the latest legal documents and amendments related to the Indian Constitution. Whether it's foundational laws or recent updates, this app ensures you have live access to all legal PDFs stored in the data folder. Built with Pathway, this application adapts in real-time to changes, making it an ideal solution for law students, researchers, or anyone interested in Indian laws. The app is fully containerized using Docker, providing a production-ready environment that is easy to deploy and manage. Pathway powers the live updates, and the RAG tool uses an in-memory scalable vector store that adapts dynamically to any changes in the PDFs in the data folder. You can also connect external sources like Google Drive for continuous real-time updates.

Table of Contents
What Problem It Solves
Architecture Overview
Getting Started
Demo
Contributing
Contact Information
What Problem It Solves
The "Indian Constitution Laws" app provides users with easy, real-time access to legal documents, amendments, and articles related to the Indian Constitution. Instead of manually searching through various sources, the app ingests and processes PDFs placed in the data folder for quick reference. The app is flexible and can be expanded to ingest content from more than 300+ other data sources, including Google Drive, ensuring that users always have access to the latest legal updates and documents in real time.

For more details on Pathway's capabilities, visit:

Pathway's GitHub Repository
Pathway Application Templates
Architecture Overview
Pathway:
Pathway serves as the core RAG framework for this project, managing real-time updates and live ingestion of the legal documents. It offers a scalable in-memory vector store that adapts to changes in the data instantly.

Docker:
Docker ensures the application can run consistently across any environment. The app is containerized, which means it’s production-ready and easy to deploy.

Local Data Folder for Data Ingestion:
Legal PDFs containing the latest laws, amendments, or court judgments are stored in the local data folder. The app watches this folder for changes and adapts accordingly. For dynamic setups, the data folder can be linked to a shared Google Drive, enabling real-time updates from external collaborators.

Getting Started
Prerequisites:
Docker: Make sure Docker is installed. Install Docker.
Pathway: Pathway is installed automatically within the Docker container, but it can also be installed locally using pip install pathway-ai.
Instructions:
Clone the Repository:

bash
Copy code
git clone https://github.com/yourusername/PathwayLLM.git
cd indian-constitution-laws
Build the Docker Image:

bash
Copy code
docker build -t laws-app .
Run the Docker Container:

bash
Copy code
docker run -v "$(pwd)/data:/app/data" -p 8000:8000 --env-file .env laws-app
Add Legal Documents (PDFs): Place any legal PDFs related to the Indian Constitution in the data folder. The app will automatically ingest and process the documents.

Connect Google Drive: To enable live updates from Google Drive:

Set up your Google Drive API credentials (follow the official Google Drive API documentation).
Add your Google Drive folder link to the .env file for real-time updates.

Contributing
We welcome contributions to enhance the project! Whether you’re adding new features or fixing bugs, your help is valuable.

Fork the repository.
Create a new feature branch.
Submit a pull request with detailed explanations of the changes.
Contact Information
For any questions or collaboration inquiries, please contact:


GitHub: [shanharold](https://github.com/shanharold)
