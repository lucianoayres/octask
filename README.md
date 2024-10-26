# 🐙 Octask

![octask-banner](https://github.com/lucianoayres/octask/blob/main/images/banner_octask.png?raw=true)

[What's Octask? 🐙](#whats-octask-) · [Why Use Octask? 🤔](#why-use-octask-) · [How Does It Work? ⚙️](#how-does-it-work-) · [Who Is It For? 👥](#who-is-it-for-) · [How to Use 🛠️](#how-to-use-) · [Using Nino with Ollama 🐶](#using-nino-with-ollama-) · [Templates 📄](#templates-) · [Examples 📂](#examples-) · [License 📄](#license-) · [Contribution 🤝](#contribution-)

## Supercharge Your LLM to Get Things Done! 🚀

### What's Octask? 🐙

**Octask** is an AI model designed to help you define clear and actionable tasks from your ideas, goals, or problems. By leveraging [Ollama](https://github.com/ollama/ollama), Octask simplifies the process of task definition, enabling you to create customized AI assistants that generate comprehensive task definitions tailored to your needs. It's like having an octopus that organizes your tasks with eight times the efficiency!

### Why Use Octask? 🤔

-   **Clarity and Focus 🔍**: Automatically generate detailed task definitions without the hassle of starting from scratch.
-   **Time-Saving ⏳**: Spend less time figuring out what to do and more time actually doing it.
-   **Customization 🎨**: Provide any idea, goal, or problem, and Octask will create a task definition tailored to you.
-   **Versatility 🔄**: Fully compatible with [Ollama](https://github.com/ollama/ollama), ensuring seamless model creation and deployment.

### How Does It Work? ⚙️

Octask uses Modelfiles that define AI models capable of generating comprehensive task definitions based on user-provided input. By creating these models with Ollama, you can interact with Octask to produce detailed task definitions for your specific needs.

We offer two modes, each with its own Modelfile:

-   [**Octask-Insights1.0**](./modelfiles/Octask-Insights1.0): Enables an interactive session where the AI asks you questions to generate a tailored task definition.
-   [**Octask-Express1.0**](./modelfiles/Octask-Express1.0): Allows you to get a task definition based on minimal input, perfect for when you're in a hurry.

## Who Is It For? 👥

Octask is for anyone who wants to turn vague ideas into clear, actionable tasks without the usual confusion:

-   **Project Managers 🗂️**: Keep your projects on track with well-defined tasks.
-   **Entrepreneurs 💡**: Break down your big ideas into manageable steps.
-   **Students 📚**: Organize your study plans effectively.
-   **Individuals 🏃‍♂️**: Turn personal goals into actionable tasks.
-   **Teams 🤝**: Collaborate efficiently with clear task definitions.

## How to Use 🛠️

Follow these steps to use Octask and generate detailed task definitions:

1. **Clone the Repository**:

    ```bash
    git clone https://github.com/lucianoayres/octask.git
    cd octask
    ```

2. **Ensure Ollama is Installed**:

    Make sure you have [Ollama](https://github.com/ollama/ollama) installed on your system.

3. **Create the Octask Model**:

    Choose the mode that suits your needs and create the corresponding model.

    **For Insights Mode**:

    ```bash
    ollama create octask-insights1.0 -f ./modelfiles/Octask-Insights1.0
    ```

    **For Express Mode**:

    ```bash
    ollama create octask-express1.0 -f ./modelfiles/Octask-Express1.0
    ```

4. **Run Octask**:

    **For Insights Mode**:

    ```bash
    ollama run octask-insights1.0
    ```

    **For Express Mode**:

    ```bash
    ollama run octask-express1.0
    ```

5. **Provide Your Idea, Goal, or Problem**:

    When prompted, input your specific idea, goal, or problem. For example:

    ```
    I want to plan a surprise birthday party for my best friend.
    ```

6. **Interact with Octask (Insights Mode)**:

    If using Insights Mode, Octask will ask you a series of questions to better understand your task. Answer these questions to help Octask generate a comprehensive task definition.

7. **Review the Generated Task Definition**:

    Octask will output a detailed task definition based on your input. Review this output and make any necessary adjustments.

8. **Save the Task Definition (Optional)**:

    You can copy the output and save it as a plain text file for future reference.

## Using Nino with Ollama 🐶

You can also use [**Nino**](https://github.com/lucianoayres/nino-cli) to interact with your Ollama models more freely. Nino allows you to send prompts directly to the models from the command line without entering interactive mode, and it also allows you to export the AI's response to a local file.

### Example Command

**For Express Mode**:

```bash
nino "I want to bake the perfect sourdough bread." --model octask-express1.0 --output task_definition.txt
```

**For Insights Mode**:

Since Insights Mode involves an interactive session, using Nino may not capture the full interaction. It's recommended to use the interactive mode with `ollama run` for Insights Mode.

## Templates 📄

### Structure 🏗️

The Octask templates streamline task definition by organizing key components, making it easy to configure and customize AI models while ensuring compatibility with Ollama. The structure includes:

1. **Objective and Rules** 📜: Defines the assistant's purpose and lays out guidelines to ensure the generated task definition meets your needs.

2. **Command Specification** 🍳: Details essential commands used in a Modelfile, such as:

    - **META**: Contains metadata about the Modelfile, added as comments.
    - **FROM**: Specifies the base model version (e.g., `llama2`).
    - **PARAMETER**: Sets model parameters like `temperature`, `num_ctx`, and `top_p`.
    - **MESSAGE**: Provides initial messages or prompts for the assistant.
    - **LICENSE**: Includes licensing information for the Modelfile.

3. **Template and Configuration** 🧩: Offers a standard Modelfile template with placeholders (`<< >>`) that can be customized based on your specific idea, goal, or problem.

4. **User Input** 💡: The specific idea, goal, or problem to generate the most effective task definition.

### Prompts

The original prompt templates are available for reference in the [prompts directory](./prompts). These resources are valuable for understanding the structure of Modelfiles and can serve educational purposes.

## Examples 📂

### User Input Examples 📝

Examples of ideas, goals, or problems that you can provide to Octask:

-   **Idea**: "I want to launch an online course on digital marketing."
-   **Goal**: "Improve my physical fitness and run a marathon in six months."
-   **Problem**: "I have trouble managing my time between work and personal life."

## License 📄

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contribution 🤝

Contributions are welcome! Please fork the repository and submit a pull request if you'd like to propose any changes.
