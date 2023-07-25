# System prompt

## Specify the steps required to complete a task
Some tasks are best specified as a sequence of steps. Writing the steps out explicitly can make it easier for the model to follow them.
```markdown
Use the following step-by-step instructions to help user create a test case.
1. Ask user to provide you with text in triple quotes. This text provides information on how to access the feature user wany to test.
2. Ask user to provide you the test case is focus on what aspect.
3. Create a test case according to the information user provided in step 1 and step 2. The test case should contain summary, steps and expect results.
```

## Request body
The request body must be a JSONL document, messages is list of message object, a message pair corresponding to a role and conetent.
```json
{
    "model": "gpt-3.5-turbo",
    "messages": [
        {
            "role": "system",
            "content": "Use the following step-by-step instructions to help user create a test case.\n1. Ask user to provide you with text in triple quotes. This text provides information on how to access the feature user wany to test.\n2. Ask user to provide you the test case is focus on what aspect.\n3. Create a test case according to the information user provided in step 1 and step 2. The test case should contain summary, steps and expect results."
        },
        {
            "role": "user",
            "content": "Help me create a test case."
        }
    ]
}
```
## Response
```json
{
    "id": "chatcmpl-7g3edDiRBjz19oHq0oC1PbRUNFQfS",
    "object": "chat.completion",
    "created": 1690258179,
    "model": "gpt-3.5-turbo-0613",
    "choices": [
        {
            "index": 0,
            "message": {
                "role": "assistant",
                "content": "Sure, I can help you create a test case. Can you please provide me with the text in triple quotes that provides information on how to access the feature you want to test?"
            },
            "finish_reason": "stop"
        }
    ],
    "usage": {
        "prompt_tokens": 111,
        "completion_tokens": 36,
        "total_tokens": 147
    }
}
```