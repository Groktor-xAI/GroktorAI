# Privacy Policy: Medical Image Analysis

> **Last Updated:** December 2025 | **Feature Status:** Beta

## Overview

This document describes how Groktor handles your medical images when you use the Medical Image Analysis feature. Your privacy is our priority.

## Key Privacy Commitments

| Commitment | Description |
|------------|-------------|
| **No Storage** | Your images are never saved to our servers |
| **Encrypted Transfer** | All data is transmitted via HTTPS encryption |
| **Immediate Deletion** | Images are deleted from memory immediately after analysis |
| **No Training Data** | Your images are never used to train AI models |
| **No Third-Party Sharing** | Images are only shared with the analysis provider for processing |

## How Your Image Is Processed

### Step-by-Step Data Flow

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Your Device   │ -> │   Our Server    │ -> │   xAI Grok      │
│   (Upload)      │    │   (Pass-through)│    │   Vision API    │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                      │                      │
         v                      v                      v
    You select image     Image forwarded        Analysis generated
    (stays on device     (not stored)           (returned to you)
    until upload)
```

1. **You Upload**: You select a medical image from your device
2. **Secure Transfer**: The image is sent via encrypted HTTPS to our server
3. **Pass-Through Processing**: Our server immediately forwards the image to xAI's Grok Vision API
4. **Analysis Generated**: xAI analyzes the image and returns educational observations
5. **Result Delivered**: The analysis is sent back to your browser
6. **Image Discarded**: The image is immediately removed from memory

**At no point is your image saved to disk, stored in a database, or retained after processing.**

## What Data Is Sent

When you analyze an image, the following information is transmitted:

| Data | Purpose | Retention |
|------|---------|-----------|
| Image file | Required for analysis | Deleted immediately after analysis |
| Selected language | To provide analysis in your language | Not retained |

## What Data Is NOT Collected

We do **NOT** collect or store:

- Your medical images
- Personal health information
- Analysis history
- Device identifiers linked to images
- Location data
- Any metadata from your images

## Third-Party Service: xAI

### About xAI

The Medical Image Analysis feature uses xAI's Grok Vision API (model: grok-2-vision-1212) to analyze images.

### xAI's Data Handling

- **Purpose**: Image analysis only
- **Retention**: xAI processes images to generate analysis and does not retain images after processing
- **Privacy Policy**: [xAI Privacy Policy](https://x.ai/privacy)

### What xAI Receives

- The medical image (temporarily, for analysis)
- The language preference for the response
- A system prompt instructing how to analyze the image

### What xAI Does NOT Receive

- Your name or identity
- Your location
- Your device information
- Any personal identifiers

## Security Measures

### Encryption

- **In Transit**: All data is encrypted using HTTPS/TLS
- **API Authentication**: All communications with xAI are authenticated with secure API keys

### Server-Side Protections

- Images are processed in memory only
- No disk storage of uploaded images
- No logging of image data
- Session isolation between users

## Your Control

You have complete control over your data:

| Action | How |
|--------|-----|
| **Don't upload** | You choose what images to analyze |
| **Clear preview** | Click the X button to remove the image preview |
| **Close browser** | Closes your session completely |

Since we don't store your images, there's nothing to delete from our servers after you close the page.

## File Size and Format Limits

For your security and optimal performance:

- **Maximum file size**: 10 MB
- **Supported formats**: JPEG, PNG, WebP, GIF
- **Recommended resolution**: 512x512 to 2048x2048 pixels

## Disclaimer

The Medical Image Analysis feature provides **educational observations only**. It does NOT:

- Provide medical diagnoses
- Offer treatment recommendations
- Replace professional medical consultation
- Create a doctor-patient relationship

**Always consult a qualified healthcare professional for medical concerns.**

## Questions and Concerns

If you have questions about how your medical images are handled:

- Open an issue on our [GitHub repository](https://github.com)
- Review our main [Privacy Policy](./Privacy-Policy.md)

## Summary

**Your medical images are:**
- Processed in real-time
- Never stored on our servers
- Never used for AI training
- Encrypted during transfer
- Deleted immediately after analysis

**We believe in privacy by design. Your health data belongs to you.**

---

*This policy specifically covers the Medical Image Analysis feature. For general application privacy information, see our main [Privacy Policy](./Privacy-Policy.md).*
