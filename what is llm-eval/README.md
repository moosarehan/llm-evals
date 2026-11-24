# What are LLM evals?

LLM evals are systematic, repeatable tests that judge a language model or an LLM-powered application against explicit criteria.

## What makes a good eval?

- **Systematic.** Plan test cases around the task. For a CampusX course assistant, a test set could contain 100 real student questions.
- **Repeatable.** Run the same cases and scoring rules after changing the prompt, model, retriever, chunking strategy, or system instructions. Compare the results to see what improved and where performance declined.
- **Clear criteria.** Define what a good result looks like before running the eval. A good course assistant answer should be correct, easy for a beginner to understand, grounded in course content, safe, and consistent with policy.

## What goes into an eval?

A metric measures one aspect of performance. An eval is the complete testing setup. It specifies the model or component under test, what success means, which test cases to run, how outputs are judged, when to run the tests, and which tools to use.

The results help answer practical questions about whether a model suits a task, whether a product is ready to ship, whether a prompt revision improved performance, whether retrieval-augmented generation (RAG) answers are grounded in retrieved context, whether an agent completes a task correctly, and whether the application meets safety and latency expectations.

## Model evals and application evals

### Model evals

Model evals measure the capabilities of the model itself. Common areas include reasoning, knowledge, math, coding, instruction following, long-context understanding, multimodal understanding, and tool use.

| Capability | Example benchmark | What it tests |
| --- | --- | --- |
| General knowledge and reasoning | MMLU | Subject knowledge and reasoning across fields such as science, history, law, and medicine |
| Math | GSM8K | Grade-school math word problems that require multiple steps |
| Coding | HumanEval, SWE-bench | Generating code and resolving real software issues, respectively |
| Instruction following | IFEval | Following verifiable constraints and formatting instructions |
| Long context | Needle-in-a-Haystack | Finding specific information inside a long input |

### Application evals

Application evals measure how well the product works. They can test the entire user flow or a specific component, such as retrieval, tool calls, or output parsing.

An LLM application can include a user interface and input handler, prompts, the model, context or memory, retrieval backed by an embedding model and vector database, tools and APIs, workflow orchestration, safety guardrails, output parsing, monitoring and logging, and a feedback loop.

For the CampusX course assistant, an application eval can check whether the answer:

- Correctly addresses the student's question.
- Uses the course material appropriately and stays faithful to the retrieved context.
- Explains the topic clearly enough for a beginner.
- Avoids inventing course policies.
- Arrives within the expected response time and meets safety requirements.

## Source screenshots

1. [Definition and systematic test cases](images/01-systematic.png)
2. [Repeatable tests](images/02-repeatable.png)
3. [Clear evaluation criteria](images/03-criteria.png)
4. [Evaluation setup and practical questions](images/04-evaluation-setup.png)
5. [Model evals and application evals](images/05-model-and-application.png)
6. [Model capabilities](images/06-model-capabilities.png)
7. [Example benchmarks](images/07-benchmarks.png)
8. [LLM application components](images/08-application-components.png)
9. [Course assistant application eval](images/09-course-assistant-eval.png)
