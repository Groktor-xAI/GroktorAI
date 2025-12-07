# Pets Groktor - Pet Health Assistant

> **Version:** 1.0.0 | **Last Updated:** December 2025

## Overview

Pets Groktor is an AI-powered pet health assistant that helps pet owners get preliminary guidance about their pets' health concerns. The feature provides educational information about common pet symptoms, when to seek veterinary care, and general pet wellness tips.

## Important Disclaimer

**This tool is for educational purposes only.** It does NOT provide:
- Veterinary diagnoses
- Treatment prescriptions
- Medical advice for animals

Always consult a qualified veterinarian for any pet health concerns. If your pet is experiencing a medical emergency, contact your veterinarian or emergency animal hospital immediately.

## Features

### Multi-Pet Support
Support for various pet types with tailored responses:
- Dogs
- Cats
- Birds
- Rabbits
- Fish
- Other pets

### AI-Powered Chat
- Conversational interface for describing pet symptoms
- Context-aware responses based on pet type
- Severity level indicators (Very Mild to Emergency)
- Source citations from veterinary resources

### Symptom Quick Prompts
Pre-built prompts for common pet concerns:
- Pet not eating
- Excessive scratching
- Vomiting
- Limping

### Multi-Language Support
Available in 11 languages:
- English
- Spanish (Espanol)
- French (Francais)
- German (Deutsch)
- Chinese (Zhongwen)
- Japanese (Nihongo)
- Korean (Hangugeo)
- Russian (Russkiy)
- Portuguese (Portugues)
- Hindi
- Arabic (Alarabiya)

## How It Works

### Architecture

```
+-------------------+    +-------------------+    +-------------------+
|   Pet Type        | -> |   Backend API     | -> |   xAI Grok        |
|   Selection       |    |   /api/pet-chat   |    |   LLM             |
+-------------------+    +-------------------+    +-------------------+
         |                      |                      |
         v                      v                      v
    User selects pet      Message processed      AI generates
    and describes         with pet context       veterinary guidance
    symptoms
```

### Technology Stack

| Component | Technology |
|-----------|------------|
| AI Model | xAI Grok via OpenRouter |
| Frontend | React + TypeScript |
| Backend | Express.js |
| Styling | Tailwind CSS + Shadcn UI |

## Getting Started

### Step 1: Access Pet Health
Click the "Pet Health" link in the main application header or navigate directly to `/pet-health`.

### Step 2: Select Your Pet Type
Use the dropdown menu to select your pet type (Dog, Cat, Bird, Rabbit, Fish, or Other).

### Step 3: Describe Symptoms
Type your pet's symptoms in the chat input or use one of the quick prompt buttons for common concerns.

### Step 4: Review Guidance
The AI will provide educational information including:
- Possible explanations for symptoms
- General care suggestions
- When to seek veterinary care
- Severity level indicator
- Source citations

## API Reference

### Chat Endpoint

```
POST /api/pet-chat
```

**Request Body:**
```json
{
  "message": "My dog has been vomiting for the past day",
  "petType": "dog",
  "history": [],
  "language": "English"
}
```

**Response:**
```json
{
  "response": "I understand you're concerned about your dog...",
  "severity": 3,
  "citations": [
    {
      "name": "AVMA",
      "url": "https://www.avma.org/...",
      "description": "American Veterinary Medical Association"
    }
  ]
}
```

### Severity Levels

| Level | Label | Description |
|-------|-------|-------------|
| 1 | Very Mild | Likely nothing to worry about |
| 2 | Mild | Monitor, but likely fine |
| 3 | Moderate | Consider seeing a vet if it persists |
| 4 | Serious | Should see a vet soon |
| 5 | Emergency | Seek immediate veterinary care |

## Privacy

- Chat messages are processed in real-time
- No pet health data is permanently stored
- Conversations are session-based only
- See our [Privacy Policy](./Privacy-Policy.md) for full details

## Best Practices

### When Using Pets Groktor

1. **Provide Details**: Include information about your pet's age, breed, and how long symptoms have been present
2. **Be Specific**: Describe symptoms clearly (frequency, severity, any changes)
3. **Follow Up**: Use the chat history to provide updates on your pet's condition
4. **Seek Professional Care**: Always consult a veterinarian for serious concerns

### Emergency Signs

Contact a veterinarian immediately if your pet shows:
- Difficulty breathing
- Collapse or inability to stand
- Uncontrolled bleeding
- Ingestion of toxic substances
- Severe trauma
- Seizures lasting more than a few minutes
- Inability to urinate or defecate

## Troubleshooting

### Common Issues

| Issue | Solution |
|-------|----------|
| Chat not responding | Check internet connection and refresh the page |
| Language not changing | Select language from the dropdown and wait for page update |
| Pet type not saving | Ensure you select from the dropdown before sending a message |

## Future Enhancements

- Image upload for visual symptom analysis
- Pet profile storage for recurring users
- Vaccination and medication reminders
- Integration with local veterinary services

---

**Have questions?** Return to the main [Groktor](/) application for human health guidance.
