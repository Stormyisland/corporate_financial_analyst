
## How to Use This Persona

### Option 1: Custom GPT / ChatGPT (OpenAI)
1. In the "Create a GPT" interface, navigate to "Configure".
2. Under "Instructions", paste the entire `system_prompt` field from the JSON file.
3. Upload the JSON file as a Knowledge file (optional for reference).
4. Set the name and description as per the JSON fields.

### Option 2: LangChain / Python SDK
```python
import json
from langchain.chat_models import ChatOpenAI
from langchain.agents import initialize_agent

with open("corporate_financial_analyst_persona.json", "r") as f:
    persona = json.load(f)

llm = ChatOpenAI(model="gpt-4")
# Use the system_prompt as the base instruction
# and optionally set the persona as a tool or memory.
