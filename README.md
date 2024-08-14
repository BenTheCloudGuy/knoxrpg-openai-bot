# KnoxRPG OpenAI Bot for Call of Cthulhu Games

Welcome to the KnoxRPG OpenAI Bot repository, designed to provide an interactive and immersive experience for Call of Cthulhu tabletop role-playing games. This bot leverages the power of Azure OpenAI, Azure CosmosDB, and Azure App Services to offer a seamless and efficient solution for gamers and game masters alike.

## Table of Contents

- [KnoxRPG OpenAI Bot for Call of Cthulhu Games](#knoxrpg-openai-bot-for-call-of-cthulhu-games)
  - [Table of Contents](#table-of-contents)
  - [Overview](#overview)
  - [Architecture](#architecture)
  - [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Services Used](#services-used)
  - [Installation](#installation)
  - [Usage](#usage)
    - [Features](#features)
  - [Contributing](#contributing)
  - [License](#license)

## Overview

This project aims to build a custom Retrieval-Augmented Generation (RAG) chatbot tailored for Call of Cthulhu games. The bot uses Azure OpenAI's GPT-4 model to understand and generate text, while integrating with Azure CosmosDB for storing and retrieving game-related content. The bot is designed to be a helpful companion during your gaming sessions, providing rules, tips, and lore from the core rule books uploaded to an Azure Storage Account.

## Architecture

The bot architecture is built on several Azure services, each serving a critical role in delivering a high-quality experience:

1. **Azure OpenAI**: Powers the language model (ChatGPT-4) used for natural language processing and content generation.
2. **Azure CosmosDB**: Provides a scalable and globally distributed database service for storing vector embeddings and performing efficient vector searches.
3. **Azure App Services**: Hosts the web application, providing a user-friendly front-end interface to interact with the bot.
4. **Azure Storage Account**: Stores the core rule books and game content that the bot will use to provide accurate responses.

![Architecture Diagram](path-to-your-diagram.png)

## Getting Started

### Prerequisites

To run this project, you will need:

- An Azure subscription with access to Azure OpenAI, CosmosDB, and App Services.
- A GitHub account to clone the repository and contribute to the project.
- Core rule books for Call of Cthulhu, uploaded to your Azure Storage Account.

### Services Used

1. **Azure OpenAI**:  
   - *Service Name*: Azure OpenAI  
   - *Description*: This service provides the GPT-4 model, which is the backbone of our chatbot’s natural language understanding and generation capabilities.
   - *Documentation*: [Azure OpenAI Service](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/)

2. **Azure CosmosDB**:  
   - *Service Name*: Azure CosmosDB (FreeTier)  
   - *Description*: Used to store vector embeddings and perform vector searches for retrieving relevant content from the uploaded game books.
   - *Documentation*: [Azure CosmosDB](https://learn.microsoft.com/en-us/azure/cosmos-db/)

3. **Azure App Services**:  
   - *Service Name*: Azure App Services  
   - *Description*: Hosts the front-end web application where users interact with the bot.
   - *Documentation*: [Azure App Services](https://learn.microsoft.com/en-us/azure/app-service/)

4. **Azure Storage Account**:  
   - *Service Name*: Azure Storage Account  
   - *Description*: Used to store the core rule books and other game-related content.
   - *Documentation*: [Azure Storage Account](https://learn.microsoft.com/en-us/azure/storage/)

## Installation

1. **Clone the repository**:
  
   ```bash
   git clone https://github.com/BenTheCloudGuy/knoxrpg-openai-bot.git
   cd knoxrpg-openai-bot
   ```

2. **Configure your Azure resources**:
   - Set up the Azure Storage Account, and upload your Call of Cthulhu rule books.
   - Deploy an Azure CosmosDB instance (FreeTier) and configure it for vector search.
   - Ensure your Azure OpenAI service is provisioned and has access to the GPT-4 model.
   - Deploy the web application using Azure App Services.

3. **Update configuration files**:
   - Modify the configuration files to include your Azure Storage Account, CosmosDB, and OpenAI keys.
   - Ensure the connection strings and API keys are properly configured.

4. **Run the application**:

   ```bash
   # For local testing
   python app.py
   ```

5. **Deploy to Azure App Services**:
   - Follow the Azure documentation to deploy your application to Azure App Services.

## Usage

Once deployed, users can interact with the bot through the web interface. The bot will use the uploaded game content to answer queries, provide rules explanations, and assist with game narration based on the Call of Cthulhu core rule books.

### Features

- **Rulebook Search**: Quickly look up rules, descriptions, and lore from the uploaded Call of Cthulhu books.
- **Game Assistance**: Get real-time help with game mechanics, character creation, and more.
- **Lore Exploration**: Dive deep into the rich lore of Call of Cthulhu with AI-guided exploration.

## Contributing

We welcome contributions from the community! Whether it’s fixing a bug, adding a new feature, or improving documentation, your help is appreciated.

1. **Fork the repository**.
2. **Create a new branch**:

   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Make your changes**.
4. **Commit your changes**:

   ```bash
   git commit -m 'Add some feature'
   ```

5. **Push to the branch**:

   ```bash
   git push origin feature/your-feature-name
   ```

6. **Open a pull request**.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
