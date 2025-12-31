# DouBao LLM translator
A reusable Python module for interacting with Doubao's large language model API, specifically designed for text translation tasks.


## Features

- Reusable translation function with configurable parameters
- Efficient API client initialization (single instance)
- Environment-based configuration for security
- Suitable for batch processing of text documents



## Create a .env file in the root directory with your credentials:

.env
```
ARK_API_KEY=your_api_key_here
MODEL_IN_USE=your_model_name_here
```

## Basic Translation
Import the translate_text function and use it with your translation prompt:
```
from doubao_translator import translate_text

# Simple translation
result = translate_text("Translate to French: Hello, how are you?")
print(result)  # Output: Bonjour, comment allez-vous?
```

## Custom Parameters
Adjust generation parameters for different translation styles:
```
# More creative translation (higher temperature)
creative_translation = translate_text(
    "Translate to Spanish: The quick brown fox jumps over the lazy dog",
    temperature=0.8,
    max_tokens=2048
)

# More precise/consistent translation (lower temperature)
precise_translation = translate_text(
    "Translate the technical manual section to German: ...",
    temperature=0.1,
    top_p=0.7
)
```




























