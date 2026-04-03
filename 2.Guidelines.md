# 2.Guidelines

- the first principle is to write clear and specific instructions.

- the second principle is to give the model time to think.


## Operation

1. on windows 10, open "Anaconda Prompt"
2. create a virtual environment
```bash
conda create -n env_name python=3.12
```
3. activate the new virtual environment
```bash
conda activate env_name
```
4. install OpenAI Python library
We will use OpenAI Python library to access the OpenAI API.
```
pip install openai
```
5. install jupyter-notebook
```bash
jupyter-notebook
```

## 2.1.Principle 1
- Write clear and specific instructions.

### Tactic 1: Use delimiters

Triple quotes: """

Triple backticks:` ``` `,

Triple dashes: ---,

Angle brackets: <>,

XML tags: ` <tag> </tag> `


Anything that just kind of makes this clear to the model that this is a separate section. 

Using delimiter is also a helpful technique to try and avoid prompt injections.

#### Avoid Prompt Injections

Prompt Injections: if a user is allowed to add some input into your prompt, they might give kind of conflicting instructions to the model that might kind of make it follow the users instructions rather than doing what you wanted it to do.

![Possible "Prompt Injection"](images/Guidelines//04-58.png)


### Tactic 2: Ask for structured output
HTML, JSON

### Tactic 3: Check whether conditions are satisfied
Check assumptions are required to do the task.

### Tactic 4: Few-shot prompting
Give successful examples of completing tasks, then ask the model to perform the task.


## 2.2.Principle 2
- Give the model time to think.


### Tactic 1: Specify the steps required to complete the task
Step 1: ...

Step 2: ...

...

Step N: ...

### Tactic 2: Instruct the model to work out its own solution before rushing to a conclusion


## 2.3.Model Limitations

### 2.3.1.Hallucination
The model is not able to verify whether the information it is giving is real or not.
Makes statements that sound plausible but are not true.

Reducing hallucinations:
First find relevant information,
then answer the question based on the relevant information.