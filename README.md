# ApexSound Voice Engine with StyleTrace™

**ApexSound Voice Engine** is an interactive system prompt builder that combines voice forensics with AI behavior calibration.  Generate highly customized system prompts in seconds. 

## 🚀 Quick Links

**[→ Launch Live Demo](https://bndrbots.github.io/apexsound-voice-engine/)**

---

## 🎯 What It Does

Build enterprise-grade system prompts in 4 steps:

1. **Define your mission** — Role, audience, metaphor
2. **Calibrate model behavior** — Risk tolerance, depth, evidence standards
3. **Set output guardrails** — Tone, constraints, mandatory sections
4. **Lock your voice** — Optional: paste your writing, StyleTrace™ analyzes it

**Result:** Production-ready system prompt in JSON or NLP format

---

## ✨ Key Features

### 🎨 Mission Parameters
- **Primary Function**: Research, Design, Legal, Operations, Content
- **End User & Goal**: Define who reads this and what they need
- **Logic Metaphor**: Coach, Lab, Pit Crew, Compass, or Museum framing

### ⚙️ Model Calibration
- **Risk Profile** (1–5): Conservative → Extreme
- **Velocity**: Fast analysis vs. deep rigor
- **Citation Requirements**: Evidence-backed or contextual
- **Ambiguity Tolerance** (1–5): Ask questions vs. infer intent

### 🔒 Output DNA
- **Negative Constraints**: Pre-built chips (No Hype, No Hedging, No Boilerplate) + custom
- **Tone Selection**: 12 presets (Executive, Blunt, Creator, Gen-Z, etc.) + custom
- **Mandatory Sections**: Assumptions, Risks, Alternatives, Action Items
- **Length Control**: Concise, Optimal, Deep Dive

### 🧬 StyleTrace™ Voice Engine
Paste 75+ words of your writing.  The system analyzes it and locks your exact voice into the generated prompt—ensuring consistent tone, personality, and style across all AI outputs.

**Why this matters**: Most system prompts sound generic. StyleTrace™ makes the AI sound *like you*.

### 📤 Dual-Mode Export
- **JSON Mode**: Structured output for API integration
- **NLP Mode**: Readable narrative for documentation
- **Copy/Download**: Instant export or clipboard copy
- **Import/Save**: Restore previous configurations

### ✅ Real-Time QA Dashboard
- **Tone Match**: Mission reflected in output?  ✓
- **Guardrails**: Constraints enforced? ✓
- **Structure Check**: Mandatory sections included? ✓
- **LED Status**: Green (ready) or Red (fix)

---

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- JavaScript enabled
- No installation needed

### Quick Start (5 minutes)

1. **[Open the app](https://bndrbots. github.io/apexsound-voice-engine/)**

2. **Left Panel — Configure (4 stages)**
   ```
   Stage 1: Mission
   └─ Function: Choose your role
   └─ Audience: Who reads this?
   └─ Metaphor: Thinking style (Coach, Lab, etc.)

   Stage 2: Calibration
   └─ Risk: How safe vs. bold? 
   └─ Velocity: Speed vs. depth?
   └─ Evidence: Citations required?
   └─ Ambiguity: Ask or infer? 

   Stage 3: Output DNA
   └─ Constraints: What to avoid?
   └─ Tone: What personality?
   └─ Sections: What must be included?
   └─ Length: How detailed? 

   Stage 4: Voice (Optional)
   └─ Paste 75+ words of your writing
   └─ StyleTrace™ locks your voice
   ```

3. **Generate**
   - Click "GENERATE PROMPT"
   - Preview appears instantly

4. **Export**
   - Copy to clipboard
   - Download as JSON or TXT
   - Import saved configurations

---

## 🏗️ Architecture

### Frontend Stack
- **HTML5** with ARIA accessibility
- **Tailwind CSS** custom color palette
- **Vanilla JavaScript** (no dependencies)
- **Browser LocalStorage** for persistence

### Data Flow
```
Input → Analysis → Composition → QA Check → Output
```

- All processing happens **client-side** (your browser)
- No backend, no servers, no data transmission
- Settings stored locally on your machine
- 100% privacy

---

## 📋 Configuration Guide

### Mission Parameters

| Field | Options |
|-------|---------|
| **Primary Function** | Research & Intelligence, Product Design, Legal & Compliance, System Operations, High-Value Content |
| **End User & Goal** | Free text (e.g., "Founders needing actionable strategy") |
| **Logic Metaphor** | Coach, Lab, Pit Crew, Compass, Museum |

### Model Calibration

| Field | Range | Meaning |
|-------|-------|---------|
| **Risk Profile** | 1–5 | 1 = Conservative, 5 = Extreme (affects safety thresholds) |
| **Velocity** | Fast/Balanced/Deep | How much depth vs. speed |
| **Cite Sources** | Yes/No | Require evidence for claims?  |
| **Ambiguity Tolerance** | 1–5 | 1 = Ask clarifying questions, 5 = Infer intent |

### Output DNA

**Negative Constraints** (What NOT to do)
- Pre-built: No Hype, No Guarding, No Hedging, No Padding, No Lectures, No AI Boilerplate
- Custom: Type any behavior to avoid (auto-formats to "No X")

**Tone Options**
- Executive (Concise), Neutral, Blunt, Creator (Raw), Slick, Grungy
- Gen-Z, Gen-X, Millennial, Sharp+Witty, Best Friend, Analytical+Critical
- Custom (describe your own)

**Mandatory Sections**
- Assumptions, Risks, Alternatives, Action Items (toggle any/all)

**Length**
- Concise, Optimal (default), Deep Dive

### StyleTrace™ Voice Fingerprinting

**How to Use:**
1. Paste 75+ words of **your own writing** (email, article, proposal, etc.)
2. System analyzes linguistic patterns
3. When you hit 75 words: "VOICEPRINT LOCKED" appears
4. Your voice profile embeds into the generated prompt

**What Gets Locked:**
- Your tone signature
- Sentence patterns
- Vocabulary preferences
- Energy level
- Punctuation style

**Result:** Every generated prompt sounds like YOU, not generic AI. 

---

## 📤 Export Formats

### JSON Mode
Professional, structured format for:
- API integration
- Version control
- Data interchange

**Includes:**
- Metadata (role, objective, version)
- Operational modes and protocols
- Enforcement rules
- Voice profile (if provided)
- Safety protocols

### NLP Mode
Human-readable markdown for:
- Documentation
- Sharing with teammates
- Easy copying

**Includes:**
- Narrative instructions
- Bold emphasis and hierarchy
- Markdown formatting
- Same content, different presentation

### Export Options
- **Copy**: Direct to clipboard
- **Download**: As JSON or TXT file
- **Import**: Restore from saved file

---

## 🎓 Advanced Usage

### Custom Tone Creation
1. Select "Custom (Type Your Own)" in Tone dropdown
2. Input field appears
3. Describe your tone (e.g., "Socratic, curious, question-focused")
4. Your description embeds in the prompt

### Saving & Restoring Configurations

**Save Current**
```
1. Configure all parameters
2. Click "Save State"
3.  Stored to browser (no account needed)
```

**Export for Backup**
```
1. Click "Export"
2. Choose JSON or TXT
3. Download to your computer
```

**Restore from File**
```
1. Click "Import"
2. Select previously exported file
3. All settings restored instantly
```

### QA Dashboard

| Indicator | Meaning |
|-----------|---------|
| ✅ PASSED | Check successful, no action needed |
| ⚠️ FIX | Check failed, regenerate after adjusting |
| 🟢 Green LED | All systems go |
| 🔴 Red LED | One or more checks failed |

---

## 🔐 Security & Privacy

- ✅ **Client-side only**: All processing in your browser
- ✅ **No backend**: No servers, no data transmission
- ✅ **No accounts**: No sign-up, no passwords
- ✅ **No tracking**: No analytics, no cookies
- ✅ **Local storage**: Settings saved only on your machine
- ✅ **Offline capable**: Works without internet (after load)

---

## 🛠️ Troubleshooting

### "VOICEPRINT LOCKED" not appearing

**Issue**: Pasted 75+ words but status doesn't show

**Solution:**
- Verify word count (whitespace matters)
- Add 5–10 more words to be safe
- Try copying from different source (avoid PDFs)

### Settings disappear after refresh

**Issue**: Saved configuration lost

**Cause:** Browser storage disabled or private mode active

**Solution:**
- Export configuration to file (backup)
- Use non-private window
- Check browser storage settings

### Import fails

**Issue**: "Invalid JSON file" error

**Solution:**
- Ensure file ends in `. json`
- File not corrupted or modified
- Re-export from app and retry

### QA checks show red

**Issue**: One or more quality checks failing

**Solution:**
1. Select a Primary Function
2. Add at least one Negative Constraint
3. Select at least one Mandatory Section
4. Click "GENERATE PROMPT" again

---

## 💡 Use Cases

**Researchers & Analysts**
- Define rigorous research protocols
- Lock analytical tone
- Enforce citation standards

**Content Creators**
- Embed your writing style
- Maintain brand voice
- Scale without losing personality

**Legal & Compliance**
- Set strict evidence requirements
- Define mandatory sections
- Control risk posture

**Product & Design**
- Brief AI on design philosophy
- Lock vocabulary
- Enforce specific output structure

**Founders & Executives**
- Generate strategic docs
- Maintain consistent voice
- Rapid prototype ideas

---

## 📄 License

ApexSound Voice Engine with StyleTrace™ by BNDR is provided as-is.

---

## 📞 Support

For issues, questions, or feature requests → [GitHub Issues](https://github.com/BNDRBOTS/apexsound-voice-engine/issues)

---

**Live Demo:** [Launch ApexSound](https://bndrbots.github.io/apexsound-voice-engine/)  
**Version:** vX.3 APEX FORGE™  
**Last Updated:** November 30, 2025
