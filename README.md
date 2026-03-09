# mobile-ai-project-decision-app
# AI Decision Intelligence
import anthropic

client = anthropic.Anthropic(
    # defaults to os.environ.get("ANTHROPIC_API_KEY")
    api_key="my_api_key",
)

message = client.messages.create(
    model="claude-sonnet-4-6",
    max_tokens=20000,
    temperature=1,
    messages=[
        {
            "role": "user",
            "content": [
                {
                    "type": "text",
                    "text": "AI Project Decision App\n\niçin ideal yapı:\n\nMobile App\n↓\nBackend\n↓\nLangChain Agent\n↓\nLLM"
                }
            ]
        }
    ]
)
print(message.content)
