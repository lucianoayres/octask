# 🐙 Octask

![octask-banner](https://github.com/lucianoayres/octask/blob/main/images/banner_octask.png?raw=true)

## Supercharge Your LLM to Get Things Done! 🚀

[What's Octask? 🐙](#whats-octask-) · [Why Use Octask? 🤔](#why-use-octask-) · [How Does It Work? ⚙️](#how-does-it-work-) · [Who Is It For? 👥](#who-is-it-for-) · [Modes of Octask 🎛️](#modes-of-octask-) · [How to Use 🛠️](#how-to-use-) · [Using Nino with Ollama 🐶](#using-nino-with-ollama-) · [Templates 📄](#templates-) · [Examples 📂](#examples-) · [License 📄](#license-) · [Contribution 🤝](#contribution-)

### What's Octask? 🐙

**Octask** is an AI model designed to help you define clear and actionable tasks from your ideas, goals, or problems. By leveraging [Ollama](https://github.com/ollama/ollama), Octask simplifies the process of task definition, enabling you to create customized AI assistants that generate comprehensive task definitions tailored to your needs. It's like having an octopus that organizes your tasks with eight times the efficiency!

Octask offers three modes to suit your needs:

-   **Octask Insights** 🔍: Engages you in an interactive session to generate a tailored task definition.
-   **Octask Express** 🚀: Provides a task definition based on minimal input—perfect for when you're in a hurry.
-   **Octask Spark** ⚡: Generates a random task based on a topic or area you provide, sparking new ideas.

### Why Use Octask? 🤔

-   **Clarity and Focus 🔍**: Automatically generate detailed task definitions without the hassle of starting from scratch.
-   **Time-Saving ⏳**: Spend less time figuring out what to do and more time actually doing it.
-   **Idea Generation 💡**: Discover new tasks related to a topic or area of interest.
-   **Customization 🎨**: Provide any idea, goal, or problem, and Octask will create a task definition tailored to you.
-   **Versatility 🔄**: Fully compatible with [Ollama](https://github.com/ollama/ollama), ensuring seamless model creation and deployment.

### How Does It Work? ⚙️

Octask uses Modelfiles that define AI models capable of generating comprehensive task definitions based on user-provided input. By creating these models with Ollama, you can interact with Octask in the mode that best suits your needs.

We offer three modes, each with its own Modelfile:

-   **Octask Insights** 🔍: Engages in an interactive session, asking you questions to generate a tailored task definition.
    -   Modelfile: [Octask-Insights1.0](./modelfiles/Octask-Insights1.0)
-   **Octask Express** 🚀: Provides a task definition based on minimal input.
    -   Modelfile: [Octask-Express1.0](./modelfiles/Octask-Express1.0)
-   **Octask Spark** ⚡: Generates a random task based on a topic or area you provide.
    -   Modelfile: [Octask-Spark1.0](./modelfiles/Octask-Spark1.0)

## Who Is It For? 👥

Octask is for anyone who wants to turn vague ideas into clear, actionable tasks without the usual confusion:

-   **Project Managers 🗂️**: Keep your projects on track with well-defined tasks.
-   **Entrepreneurs 💡**: Break down your big ideas into manageable steps.
-   **Students 📚**: Organize your study plans effectively.
-   **Individuals 🏃‍♂️**: Turn personal goals into actionable tasks.
-   **Teams 🤝**: Collaborate efficiently with clear task definitions.
-   **Creatives 🎨**: Generate new ideas and tasks in your field of interest.

## Modes of Octask 🎛️

### Octask Insights 🔍

Engages you in an interactive session, asking questions to better understand your needs and generate a comprehensive, tailored task definition.

### Octask Express 🚀

Provides a detailed task definition based on minimal input—ideal when you're short on time.

### Octask Spark ⚡

Generates a random task based on a topic or area you provide, helping you discover new ideas or focus points.

**Tip**: Use [**Catnip**](https://github.com/lucianoayres/catnip) to generate categories related to your topic. These categories can then be used with Octask Spark to generate specific tasks.

## How to Use 🛠️

Follow these steps to use Octask and generate detailed task definitions:

### 1. Clone the Repository

```bash
git clone https://github.com/lucianoayres/octask.git
cd octask
```

### 2. Ensure Ollama is Installed

Make sure you have [Ollama](https://github.com/ollama/ollama) installed on your system.

### 3. Create the Octask Models

Choose the mode(s) that suit your needs and create the corresponding model(s).

#### For Octask Insights

```bash
ollama create octask-insights1.0 -f ./modelfiles/Octask-Insights1.0
```

#### For Octask Express

```bash
ollama create octask-express1.0 -f ./modelfiles/Octask-Express1.0
```

#### For Octask Spark

```bash
ollama create octask-spark1.0 -f ./modelfiles/Octask-Spark1.0
```

### 4. Run Octask

#### Using Octask Insights

```bash
ollama run octask-insights1.0
```

#### Using Octask Express

```bash
ollama run octask-express1.0
```

#### Using Octask Spark

```bash
ollama run octask-spark1.0
```

### 5. Provide Your Input

-   **For Octask Insights and Express**: Input your specific idea, goal, or problem.
    ```
    I want to plan a surprise birthday party for my best friend.
    ```
-   **For Octask Spark**: Use a category generated by Catnip.
    ```
    Urban Farming
    ```

### 6. Interact with Octask

-   **Octask Insights**: Answer the questions posed by Octask to help generate a comprehensive task definition.
-   **Octask Express and Spark**: Review the generated task.

### 7. Review the Generated Task Definition

Octask will output a detailed task based on your input. Review this output and make any necessary adjustments.

### 8. Save the Task Definition (Optional)

You can copy the output and save it as a plain text file for future reference.

## Using Nino with Ollama 🐶

You can also use [**Nino**](https://github.com/lucianoayres/nino-cli) to interact with your Ollama models more freely. Nino allows you to send prompts directly to the models from the command line without entering interactive mode, and it also allows you to export the AI's response to a local file.

### Example Commands

#### For Octask Express

```bash
nino "I want to bake the perfect sourdough bread." --model octask-express1.0 --output task_definition.txt
```

#### For Octask Spark with Catnip Categories

First, generate categories with Catnip and then use one with Octask Spark.

```bash
nino "Sustainable Transportation" --model octask-spark1.0 --output random_task.txt
```

#### For Octask Insights

Since Insights Mode involves an interactive session, using Nino may not capture the full interaction. It's recommended to use the interactive mode with `ollama run` for Octask Insights.

## Templates 📄

### Structure 🏗️

The Octask templates streamline task definition by organizing key components, making it easy to configure and customize AI models while ensuring compatibility with Ollama. The structure includes:

1. **Objective and Rules** 📜: Defines the assistant's purpose and lays out guidelines to ensure the generated task meets your needs.

2. **Command Specification** 🍳: Details essential commands used in a Modelfile, such as:

    - **META**: Contains metadata about the Modelfile, added as comments.
    - **FROM**: Specifies the base model version (e.g., `llama2`).
    - **PARAMETER**: Sets model parameters like `temperature`, `num_ctx`, and `top_p`.
    - **MESSAGE**: Provides initial messages or prompts for the assistant.
    - **LICENSE**: Includes licensing information for the Modelfile.

3. **Template and Configuration** 🧩: Offers a standard Modelfile template with placeholders (`<< >>`) that can be customized based on your specific idea, goal, or problem.

4. **User Input** 💡: The specific idea, goal, or problem to generate the most effective task.

### Prompts

The original prompt templates are available for reference in the [prompts directory](./prompts). These resources are valuable for understanding the structure of Modelfiles and can serve educational purposes.

## Examples 📂

### Octask Insights Examples 📝

**User Input**: "I want to launch an online course on digital marketing."

**Octask's Questions and Sample Answers**:

-   **Octask**: "Who is your target audience?"
-   **You**: "Small business owners."

-   **Octask**: "What is your timeline for launching?"
-   **You**: "Within the next three months."

**Generated Task Definition**:

-   Research course content suitable for small business owners.
-   Develop a course outline and curriculum.
-   Create video lectures and supplementary materials.
-   Set up an online learning platform.
-   Launch marketing campaigns targeting small business owners.
-   Collect feedback and make necessary adjustments.

### Octask Express Examples 📝

**User Input**: "Improve my physical fitness and run a marathon in six months."

**Generated Task Definition**:

-   Create a six-month training schedule.
-   Consult a physician for a health check-up.
-   Invest in proper running gear.
-   Join a local running group for motivation.
-   Monitor progress and adjust the training plan as needed.

### Octask Spark Examples with Catnip 📝

**Using Catnip to Generate Categories**:

```bash
ollama run catnip-panorama1.0
```

**User Input**:

```
Digital Art Techniques
```

**Catnip Output**:

-   3D Modeling
-   Vector Illustration
-   Digital Painting
-   Pixel Art
-   Animation
-   Photo Manipulation

**Using a Category with Octask Spark**:

```bash
ollama run octask-spark1.0
```

**User Input**:

```
Animation
```

**Generated Random Task**:

-   Create a short animated video using open-source software to tell a personal story.

## License 📄

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contribution 🤝

Contributions are welcome! Please fork the repository and submit a pull request if you'd like to propose any changes.
