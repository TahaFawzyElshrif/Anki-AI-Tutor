# Anki

This repository contains a modified version of the source code for the computer version of [Anki](https://apps.ankiweb.net/), with an integrated AI-powered English vocabulary tutor.

## About

Anki is a spaced repetition program. Please see the [official website](https://apps.ankiweb.net/) to learn more.

This repository extends the original Anki Desktop application with an AI-powered vocabulary learning experience while preserving its existing learning and review system.

## AI Vocabulary Tutor Integration

### Overview

The AI Vocabulary Tutor integrates Google Gemini directly into Anki Desktop to help users remember and actively use previously studied English vocabulary.

Rather than simply memorizing definitions, users can practice recalling words, understanding their meanings, and using them in different contexts through AI-assisted conversations and exercises.

The AI assistant complements Anki's existing spaced repetition system; it does not replace the normal studying process.

### Features

- **AI Conversational Assistant:** Interact with an AI tutor and ask questions through a conversational interface.
- **Practice Vocabulary:** Recall a previously studied word by understanding its meaning and using it in a sentence.
- **Generate Paragraph:** Generate short, contextual paragraphs using vocabulary from the current Anki deck.
- **Choose the Better Word:** Practice understanding vocabulary usage by identifying a more suitable word in a given context.
- **Contextual Learning:** Use previously studied vocabulary to create more relevant learning activities.
- **Conversation Context:** Maintain conversation history and a consistent vocabulary selection throughout the current chat.

### Technical Implementation

- **AI Integration:** Integrated Google Gemini using the official `google-genai` Python SDK.
- **Vocabulary Retrieval:** Retrieves previously studied vocabulary directly from Anki's collection and the currently selected deck.
- **Background Processing:** Uses Anki's `QueryOp` to handle vocabulary retrieval and AI requests without blocking the main interface.
- **User Interface:** Built using Anki's existing Qt environment and integrated into its Desktop interface.
- **Credential Security:** Uses Python `keyring` to store the user's Gemini API key in the operating system's credential storage rather than ordinary profile configuration data.
- **Anki Integration:** Connects the AI tutor to Anki's Overview interface through a dedicated entry point.

### Current Limitations

- Conversation history is not saved after the active session.
- Requests require an internet connection and a valid Gemini API key.
- The interface is currently supported only on English.
- The feature is only available on Windows (x86 architecture).

For more technical details about the implementation, see the [AI Integration Documentation](docs/AI_INTEGRATION.md).

## Getting Started

### Contributing

Want to contribute to Anki? Check out the [Contribution Guidelines](docs/contributing.md).

For more information on building and developing, please see [Development](docs/development.md).

#### Contributors

The following people have contributed to Anki: [CONTRIBUTORS](CONTRIBUTORS).

### Anki Betas

If you'd like to try development builds of Anki but don't feel comfortable building the code, please see [Anki Betas](https://docs.ankiweb.net/releases/betas/intro).

## License

Anki's license: [LICENSE](LICENSE).

---

**Note:** This repository contains modifications to the original Anki source code. It is an independent project and is not an official Anki release.