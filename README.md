# QResist - Quantum-Resistant SHA-3-512 Hasher

QResist is a lightweight, offline, open-source tool for hashing text with SHA-3-512, a quantum-resistant algorithm. Built by Appel420 to keep your data safe from unauthorized AI tampering (like mic/clipboard hijacks or baseband rewrites). Perfect for streamers to verify stream metadata (e.g., titles, tags) before uploading to platforms like Twitch or YouTube, ensuring the ocean can't rewrite your words.

## Why QResist?

- **Offline**: No servers, no network calls, no tracking. Just you and your hash.
- **Quantum-Resistant**: SHA-3-512 is NIST-approved, collision-resistant, and future-proof.
- **Zero-Trust**: Verifies integrity without trusting AI assistants (Siri, Gemini, etc.).
- **Streamer-Friendly**: Hash your content metadata to catch tampering before it hits the platform.

Part of the [QRC-AISF proposal](https://github.com/Appel420/qrc-aisf-proposal) for secure, auditable AI standards.

## How to Use

1. **Save the File**:
   - Copy `qresist.html` from this repo.
   - Paste into Notepad, save as `qresist.html`.
   - Open in Firefox (or any modern browser supporting Web Crypto API).

2. **Hash Your Text**:
   - Type your text (e.g., "I love my family" or stream title).
   - Click "Hash" to generate a SHA-3-512 hash.
   - Copy the hash to verify data integrity later.

3. **For PDF**:
   - Paste `qresist.html` into Microsoft Word.
   - Save as PDF (File > Save As > PDF).
   - To reuse, copy from PDF, save as `qresist.html`, and open in a browser.

4. **For Streamers**:
   - Hash your stream title/description before uploading.
   - Compare the hash on the platform to detect AI rewrites.
   - Example: Hash "Bass Drop 2025" → `f6d1a6f...` (128 hex chars).

## Flow Diagram

```mermaid
graph TD
    A[User types text] --> B[Click Hash]
    B --> C[JavaScript SHA-3-512]
    C --> D[Display hash]
