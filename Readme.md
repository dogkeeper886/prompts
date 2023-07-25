# Create test case based on existing knowledge

I want to develop a test case creation system that leverages the power of ChatGPT and utilizes existing documentation, such as API documentation (apidoc) and user manuals. The system will enable users to define test cases by specifying a series of steps that can reference information from the provided documentation.

The workflow begins with the user inputting the desired test case parameters and requirements. The system will then analyze the provided apidoc and user manual, extracting relevant information that can be used as references for the test case steps.

Using the capabilities of ChatGPT, the system will generate intelligent suggestions and recommendations for test case steps based on the context of the documentation and the specified requirements. Users can review and select from these suggestions or modify them as needed.

## Specify the steps required to complete a task
Some tasks are best specified as a sequence of steps. Writing the steps out explicitly can make it easier for the model to follow them.

```
Use the following step-by-step instructions to help user create a test case.
1. Ask user to provide you with text in triple quotes. This text provides information on how to access the feature user wany to test.
2. Ask user to provide you the test case is focus on what aspect.
3. Create a test case according to the information user provided in step 1 and step 2. The test case should contain summary, steps and expect results.
```

### Syetem prompt in single line format
The content of message using in the API should be single line of text.
```
Use the following step-by-step instructions to help user create a test case.\n1. Ask user to provide you with text in triple quotes. This text provides information on how to access the feature user wany to test.\n2. Ask user to provide you the test case is focus on what aspect.\n3. Create a test case according to the information user provided in step 1 and step 2. The test case should contain summary, steps and expect results.
```

### User input
```
Help me create a test case.
```

### Request body
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

### Response
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

## Provide the Steps
The steps to access the feature.

```
1. On the navigation bar, click Venues. The Venues page is displayed.
2. Select the Venue Name and click Edit. Alternatively, click Venue Name > Configure. Select the Wi-Fi Configuration tab. By default, the Radio tab is displayed.
3. In the Radio tab, select the Client Admission Control sub-tab. The Client Admission Control sub-tab is displayed.
4. Configure the following settings for the 2.4 GHz and 5 GHz bands:
- Minimum client count
- Maximum radio load
- Minimum client throughput
5. Click Save.
```

### The steps in single line format
```
1. On the navigation bar, click Venues. The Venues page is displayed.\n2. Select the Venue Name and click Edit. Alternatively, click Venue Name > Configure. Select the Wi-Fi Configuration tab. By default, the Radio tab is displayed.\n3. In the Radio tab, select the Client Admission Control sub-tab. The Client Admission Control sub-tab is displayed.\n4. Configure the following settings for the 2.4 GHz and 5 GHz bands:\n- Minimum client count\n- Maximum radio load\n- Minimum client throughput\n5. Click Save.
```

### Response
```json
{
    "id": "chatcmpl-7g3t6UzRxsBoImdCWwaQM8oluEiIZ",
    "object": "chat.completion",
    "created": 1690259076,
    "model": "gpt-3.5-turbo-0613",
    "choices": [
        {
            "index": 0,
            "message": {
                "role": "assistant",
                "content": "Thank you for providing the instructions. Now, please let me know what aspect or specific functionality you would like to focus on for this test case."
            },
            "finish_reason": "stop"
        }
    ],
    "usage": {
        "prompt_tokens": 271,
        "completion_tokens": 29,
        "total_tokens": 300
    }
}
```