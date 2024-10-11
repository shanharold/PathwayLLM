# Indian Constitution Laws

**Indian Constitution Laws** is a real-time, scalable Augmented Generation (RAG) application designed to help users access the latest legal documents and amendments related to the Indian Constitution. Whether it's foundational laws or recent updates, this app ensures you have live access to all legal PDFs stored in the `data` folder. Built with **Pathway**, this application adapts in real-time to changes, making it an ideal solution for law students, researchers, or anyone interested in Indian laws.

The app is fully containerized using Docker, providing a production-ready environment that is easy to deploy and manage. **Pathway** powers live updates, and the RAG tool uses an in-memory scalable vector store that adapts dynamically to any changes in the PDFs in the `data` folder. You can also connect external sources like Google Drive for continuous real-time updates.

---

## Table of Contents
- [What Problem It Solves](#what-problem-it-solves)
- [Architecture Overview](#architecture-overview)
- [Getting Started](#getting-started)
- [Demo](#demo)
- [Contributing](#contributing)
- [Contact Information](#contact-information)

---

## What Problem It Solves

The **Indian Constitution Laws** app provides users with easy, real-time access to legal documents, amendments, and articles related to the Indian Constitution. Instead of manually searching through various sources, the app ingests and processes PDFs placed in the `data` folder for quick reference. The app is flexible and can be expanded to ingest content from more than 300+ other data sources, including Google Drive, ensuring that users always have access to the latest legal updates and documents in real time.

---

## Architecture Overview

### Pathway
Pathway serves as the core RAG framework for this project, managing real-time updates and live ingestion of the legal documents. It offers a scalable in-memory vector store that adapts to changes in the data instantly.

### Docker
Docker ensures the application can run consistently across any environment. The app is containerized, which means it’s production-ready and easy to deploy.

### Local Data Folder for Data Ingestion
Legal PDFs containing the latest laws, amendments, or court judgments are stored in the local `data` folder. The app watches this folder for changes and adapts accordingly. For dynamic setups, the `data` folder can be linked to a shared Google Drive, enabling real-time updates from external collaborators.

---

## Getting Started

### Prerequisites:
- **Docker**: Make sure Docker is installed. [Install Docker](https://docs.docker.com/get-docker/).
- **Pathway**: Pathway is installed automatically within the Docker container, but it can also be installed locally using `pip install pathway-ai`.

### Instructions:
1. **Clone the Repository**:
    ```bash
    git clone https://github.com/yourusername/PathwayLLM.git
    cd indian-constitution-laws
    ```

2. **Build the Docker Image**:
    ```bash
    docker build -t laws-app .
    ```

3. **Run the Docker Container**:
    ```bash
    docker run -v "$(pwd)/data:/app/data" -p 8000:8000 --env-file .env laws-app
    ```

4. **Add Legal Documents (PDFs)**:
    Place any legal PDFs related to the Indian Constitution in the `data` folder. The app will automatically ingest and process the documents.

5. **Connect Google Drive** *(optional)*:
    To enable live updates from Google Drive:
    - Set up your Google Drive API credentials (follow the official Google Drive API documentation).
    - Add your Google Drive folder link to the `.env` file for real-time updates.

---

## Demo

For a live demo, follow the setup instructions and launch the app. Visit `http://localhost:8000` to see the interface and upload or view legal documents in real-time.

---

## Contributing

We welcome contributions to enhance the project! Whether you’re adding new features or fixing bugs, your help is valuable.

1. Fork the repository.
2. Create a new feature branch.
3. Submit a pull request with detailed explanations of the changes.

---

## Contact Information

For any questions or collaboration inquiries, please contact:

- GitHub: [shanharold](https://github.com/shanharold)
