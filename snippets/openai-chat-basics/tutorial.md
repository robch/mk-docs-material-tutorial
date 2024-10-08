The `ai chat` command allows you to interact w/ OpenAI models from the command line.  

--8<-- "tips/tip-openai-prereqs.md"

### User and System Prompts

The `ai chat` command sends a user prompt to OpenAI and displays the response.

--8<-- "code-blocks/ai-chat-user-what-is-the-capital-of-france.md"

--8<-- "code-blocks/ai-chat-user-what-is-the-capital-of-france-system-always-answer-in-french.md"

--8<-- "code-blocks/ai-chat-question-what-is-the-capital-of-france.md"

### User and System prompts from Files

``` bash title="User prompt from a file"
ai chat --question "@question.txt"
```

``` bash title="System prompt from a file"
ai chat --question "What is the capital of France?" --system "@system.txt"
```

### Interactive Chat

The `--interactive` flag allows back-and-forth conversations with the model.

``` bash title="Interactive chat"
ai chat --interactive
```

``` { .bash .cli-command title="Interactive with an initial question" }
ai chat --interactive --question "What is the capital of France?"
```

``` { .plaintext .cli-output }
AI - Azure AI CLI, Version 1.0.0
Copyright (c) 2024 Microsoft Corporation. All Rights Reserved.

Press ENTER for more options.

user@CHAT: What is the capital of France?

assistant: The capital of France is Paris.

user@CHAT: What about the US?

assistant: The capital of the United States is Washington, D.C.

user@CHAT: exit

```


``` bash title="Interactive with a system prompt"
ai chat --interactive --system "Always answer in French."
```

### Answers and chat history

``` bash title="Output answer to a file"
ai chat --question "What is the capital of France?" --output-answer answer.txt
```

``` bash title="Output chat history to a file"
ai chat --interactive --output-chat-history history.jsonl
```

``` bash title="Input chat history from a file"
ai chat --interactive --input-chat-history history.jsonl
```

--8<-- "generate-code-for-scenarios-button-section.md"
