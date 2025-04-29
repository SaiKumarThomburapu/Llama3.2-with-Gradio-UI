# Llama 2 with Gradio UI

This project demonstrates how to create a user interface (UI) for interacting with the Llama 2 language model using Gradio.  It allows users to send prompts to Llama 2 and view the responses within a web-based interface.

## Overview

The Jupyter Notebook `Gradio UI Building.ipynb` contains the code to set up the Gradio UI for Llama 2.  It shows how to:

* Import necessary libraries (`os`, `dotenv`, `openai`, `gradio`).
* Initialize the OpenAI client to connect to Llama 2.
* Define functions to interact with Llama 2 (`message_gpt`).
* Create Gradio interfaces for:
    * Basic text input/output.
    * Displaying Markdown output.
    * Streaming responses.
* Set system prompts to guide Llama 2's behavior.

## Setup

1.  **Install Dependencies:**

    Ensure you have the required Python libraries installed. You can install them using pip:

    ```bash
    pip install python-dotenv openai gradio
    ```

2.  **Environment Configuration:**

    * Create a `.env` file in your project directory.
    * Add your OpenAI API key and the base URL for your Llama 2 server to the `.env` file:

    ```
    OPENAI_API_KEY=your_api_key
    OPENAI_BASE_URL=http://localhost:11434/v1  # Or your specific URL
    ```

    * Load the environment variables in your notebook:

    ```python
    from dotenv import load_dotenv
    load_dotenv()
    ```

3.  **Llama 2 Setup:**

    * Make sure you have Llama 2 set up and running, accessible via the `OPENAI_BASE_URL`. This project assumes you are using `ollama`.

## Usage

1.  Open the `Gradio UI Building.ipynb` notebook in Jupyter or your preferred notebook environment.
2.  Run the notebook cells to:
    * Define the Llama 2 interaction functions.
    * Create and launch the Gradio interfaces.
3.  Interact with Llama 2 through the Gradio web interface that will appear.

## Key Functions

* `message_gpt(prompt)`: Sends a prompt to Llama 2 and returns the response.
* `stream_gpt(prompt)`:  Sends a prompt to Llama 2 and streams the response back in chunks.

## Gradio Interfaces

The notebook demonstrates several Gradio interfaces:

* A simple interface with a textbox for input and a textbox for output.
* An interface that displays Llama 2's output as formatted Markdown.
* An interface that provides a streaming output of Llama 2's response.

## Notes

* This project provides a foundation for building interactive applications with Llama 2.
* You can customize the Gradio interfaces to add more features or tailor them to specific use cases.
* Ensure your Llama 2 setup is correct and accessible for the notebook to function.
