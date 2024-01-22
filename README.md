# Food-Delivery-Chatbot Project

## Overview

This project is aimed at developing an end-to-end food delivery system with a chatbot interface. Leveraging Dialogflow for natural language understanding, FastAPI for efficient backend processing, and MySQL for database management, the system provides a seamless and user-friendly experience for ordering food.

## Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Directory Structure](#directory-structure)
- [Running the FastAPI Backend](#running-the-fastapi-backend)
- [Ngrok for HTTPS Tunneling](#ngrok-for-https-tunneling)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Conversational Interaction:** Users can place orders, modify them, and inquire about order statuses using natural language queries.
- **Efficient Backend Processing:** FastAPI ensures rapid and asynchronous handling of incoming requests, contributing to a responsive backend.
- **Database Management:** MySQL stores and retrieves data related to user profiles, menu items, and order details.
- **Order Processing Automation:** Automation logic streamlines order processing, reducing manual intervention and improving operational efficiency.
- **Real-Time Updates:** Webhooks facilitate real-time communication, providing users with instant updates on changes in order status.

## Tech Stack

- **Dialogflow:** Natural language understanding for user interactions.
- **FastAPI:** Python web framework for efficient backend processing.
- **MySQL:** Database management for storing critical information.

## Installation

1. Clone the repository:

   ```
   git clone https://github.com/your-username/food-delivery-chatbot.git
   cd food-delivery-chatbot
   ```

2. Install dependencies:

   ```
   pip install -r backend/requirements.txt
   ```

   OR

   ```
   pip install mysql-connector
   pip install "fastapi[all]"
   ```

3. Import the MySQL database dump from the `db` directory into your MySQL database using a tool like MySQL Workbench.

## Usage

- Update the Dialogflow assets in the `dialogflow_assets` directory with your own training phrases and intents.
- Configure the FastAPI backend to connect to your MySQL database.
- Follow the instructions in [Running the FastAPI Backend](#running-the-fastapi-backend) to start the server.
- Optionally, set up Ngrok for HTTPS tunneling as explained in [Ngrok for HTTPS Tunneling](#ngrok-for-https-tunneling).

## Directory Structure

```
food-delivery-chatbot/
|-- backend/
|-- db/
|-- dialogflow_assets/
|-- frontend/
|-- README.md
|-- .gitignore
```

- `backend`: Contains Python FastAPI backend code.
- `db`: Contains the dump of the database. Import this into your MySQL database.
- `dialogflow_assets`: Holds training phrases and intents for Dialogflow.
- `frontend`: Website code.

## Running the FastAPI Backend

1. Go to the `backend` directory in your command prompt.
2. Run the following command:

   ```
   uvicorn main:app --reload
   ```

## Ngrok for HTTPS Tunneling

1. Install Ngrok by downloading it from [https://ngrok.com/download].
2. Extract the zip file and place `ngrok.exe` in a folder.
3. Open the command prompt, navigate to that folder, and run:

   ```
   ngrok http 8000
   ```

   Note: Ngrok may timeout; restart the session if you encounter a session expired message.

## Contributing

Contributions are welcome! Please follow the [Contributing Guidelines](CONTRIBUTING.md).

## License

This project is licensed under the [MIT License](LICENSE).
