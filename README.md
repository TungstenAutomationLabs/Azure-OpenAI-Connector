# Azure-OpenAI-Connector


Azure OpenAI Connector for TotalAgility

The TotalAgility-Azure OpenAI Connector integrates with Azure OpenAI, Microsoft's hosted rendition of
OpenAI GPT. This engine powers Chat-GPT, but for the purpose of this integration, the chat or dialog
function will not be utilized; instead, we will leverage the completions feature.

GPT operates not by directly answering questions, but by completing given prompts. The prompts
provided to GPT need not be questions; they can be any text that requires completion. To guide the
completion process, a specified number of tokens is added to the initial prompt. In the English language,
a token approximately represents four characters. Longer words may be segmented into multiple
tokens. On average, 100 tokens equate to around 75 words. For a comprehensive understanding of

tokens, refer to the OpenAI documentation: https://help.openai.com/en/articles/4936856-what-are-
tokens-and-how-to-count-them. By default, our OpenAI Connector is set to a value of XX tokens.

The OpenAI Connector is preconfigured to use temperature =0.
The temperature parameter, ranging from 0 to 1, governs the confidence level of the model
during predictions. A reduced temperature value ensures minimal risk-taking, leading to more precise
and deterministic completions. Conversely, elevating the temperature fosters greater diversity in the
completions produced.https://platform.openai.com/docs/quickstart/adjust-your-settings
Look at https://platform.openai.com/examples for ideas how to use OpenAI
User Guide
This guide will show how to ask GPT anything using a Quick Workflow.
If you are new to TotalAgilty Quick Workflow, then try out the free tutorial.

1. From the Windows Start menu, select TotalAgility Apps, and when the landing page appears,
select Quick Workflow.
2. Create a New Workflow.
3. Give it the name that is intuitive like “Test Azure OpenAI Connector”
4. Click on “Workflow”
5. Add an activity. Under “Type”, Select “Azure OpenAI GPT Completion” in the custom services
subsection
6. Set input to “Please provide a list of proof of citizenship items that the State Department would
accept for residents of Virginia applying for a new passport”
7. Set the output to a variable of type “String”. Give it an intuitive name like “GPT Response”
8. Click the “+” button below that step. This will add another task to show the response back to the
user. Add the response variable from the previous step to the “Display Data” of the task.
9. Add an end step. See screenshot below for a completed example
10. Publish the workflow

11. Open KTA Workspace
12. From the Top Navigation Bar Menu, hover over “Apps”, then “Quick Workflow”, then select your
workflow you named in step 3
13. Click the blue start button in the top right of the screen

14. Press submit
15. After a few seconds you will see a task activity – open it and you will see OpenAI’s completion to
your prompt
