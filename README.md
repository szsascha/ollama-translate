# Ollama Translate

Use Ollama to translate languages locally. Created for translations in projects with data that is covered by data protection regulations. It can also be used for highly confidential data. There is no call to an external service. All data is processed locally on your own system.

## Features

- Translates text between several languages
- Uses the [aya-expanse](https://ollama.com/library/aya-expanse:8b) model (Consider using the 32b model for better results)
- Outputs the translated text as markdown

## Requirements

- Ollama
- Hardware with enough power to run 8b models (see Ollama specifications)

## Setup

1. Clone this repo
2. Create the model you want (e.g. for german to english translation: `ollama create de_en -f ./de_en.Modelfile`)
3. Optional: Run the ollama service: `ollama serve`

## Usage

### CLI

`ollama run en_de "Why is the sky blue?"`

### REST

```
POST http://localhost:11434/api/generate

{
  "model": "en_de",
  "prompt":"Why is the sky blue?",
  "stream": false
}
```