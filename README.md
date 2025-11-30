# ApexSound Voice Engine with StyleTrace™

**ApexSound Voice Engine** is an interactive system prompt builder that combines forensic voice analysis with AI behavior calibration.  It enables users to generate highly customized system prompts by defining mission parameters, model calibration settings, and voice fingerprinting through original writing samples.

## 🎯 Overview

StyleTrace™ by BNDR is a proprietary voice analysis engine embedded within ApexSound. The system analyzes written samples (75+ words minimum) to extract linguistic patterns—sentence structure, punctuation density, cadence, modifier density, and core phrase recursion—then encodes these patterns into system prompts that enforce consistent voice and tone across AI outputs.

**Current Version:** vX.3 APEX FORGE™

### Key Capabilities

- **Mission Parameterization**: Define primary function, end user, and logical metaphor
- **Model Calibration**: Control risk tolerance, velocity (speed vs. depth), evidence standards, and ambiguity handling
- **Voice Fingerprinting**: Analyze original writing to extract tone signature, persona edges, and structural bias
- **Output DNA Configuration**: Set negative constraints, tone profiles, mandatory sections, and length preferences
- **Dual-Mode Export**: Generate prompts in JSON (structured) or NLP (narrative) formats
- **State Management**: Save, import, and export system configurations

## 📋 Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
- [System Architecture](#system-architecture)
- [Configuration Guide](#configuration-guide)
- [Voice Analysis Engine](#voice-analysis-engine)
- [Export Formats](#export-formats)
- [Advanced Usage](#advanced-usage)
- [Security & Safety](#security--safety)
- [Troubleshooting](#troubleshooting)
- [License](#license)

## ✨ Features

### 1. Four-Stage Configuration Pipeline

**Stage 1: Mission Parameters**
- Primary Function (Research, Design, Legal, Operations, Content Creation)
- End User & Goal specification
- Logic Metaphor selection (Coach, Lab, Pit Crew, Compass, Museum)

**Stage 2: Model Calibration**
- Risk Profile (1–5 scale, from Conservative to Extreme)
- Velocity (Fast, Balanced, Deep)
- Citation requirements (Yes/No)
- Ambiguity Tolerance (1–5 scale)

**Stage 3: Output DNA**
- Negative Constraints (No Hype, No Guarding, No Hedging, No Padding, No Lectures, custom additions, No AI Boilerplate)
- Tone selection (12 presets + custom option)
- Optimal Length (Concise, Standard, Deep Dive)
- Mandatory Sections (Assumptions, Risks, Alternatives, Action Items)

**Stage 4: StyleTrace™ Voice Fingerprinting**
- Paste 75+ word writing sample
- System auto-analyzes linguistic patterns
- Generates forensic voice profile for tone enforcement

### 2. Voice Analysis Engine

The StyleTrace™ system extracts:
- **Tone Signature**: Detects punchy/fragmented, academic/complex, conversational, or direct patterns
- **Modifier Density**: Measures word economy vs. descriptive language
- **Sentence Depth**: Identifies atomic/direct vs. complex clause stacking
- **Core Phrases**: Isolates recurring 3-word phrase clusters
- **Risk Posture**: Calculates aggressive/direct vs. deep/analytical orientation
- **Persona Edges**: Extracts personality markers (Punchy, High-Energy, Fragmented, etc.)
- **Structural Bias**: Determines rhythm-led vs. logic-led composition

### 3.  Dual-Mode Output

**JSON Mode**: Structured system prompt with metadata, operational profiles, enforcement protocols, and safety overrides. 

**NLP Mode**: Narrative system prompt with markdown formatting, visual hierarchy, and human-readable sections.

### 4. State Persistence

- **Save State**: Stores all inputs to browser localStorage
- **Export**: Download configurations as `. json` or `.txt`
- **Import**: Restore saved configurations from file (max 1MB, JSON validation)
- **Reset**: Clear all settings and reload

### 5. Quality Assurance Dashboard

Real-time QA checks monitor:
- **Tone Match**: Verifies selected mission/tone reflected in output
- **Guardrails**: Confirms active negative constraints encoded
- **Structure Check**: Validates mandatory sections present
- **LED Indicator**: Green (OK) or Red (Error) status light

## 🚀 Getting Started

### Prerequisites

- Modern web browser (Chrome, Firefox, Safari, Edge)
- JavaScript enabled
- No dependencies or build steps required

### Installation

1. Clone or download this repository
2. Open `index. html` in your web browser
3. Application runs entirely client-side (no backend required)

### Quick Start

1. **Set Mission Parameters**
   - Select Primary Function (e.g., "Research & Intelligence")
   - Enter End User & Goal (e.g., "Founders needing actionable strategy")
   - Choose Logic Metaphor (e.g., "Coach")

2. **Configure Model Calibration**
   - Set Risk Profile (1–5)
   - Choose Velocity (Fast/Balanced/Deep)
   - Select citation requirements
   - Set Ambiguity Tolerance

3.  **Define Output DNA**
   - Select negative constraints (click chips to activate)
   - Add custom constraints if needed
   - Choose Tone (preset or custom)
   - Select Mandatory Sections
   - Choose Optimal Length

4. **Add Voice Sample (Optional)**
   - Paste 75+ words of original writing
   - System will lock voiceprint when threshold met
   - StyleTrace™ analysis activates automatically

5. **Generate Prompt**
   - Click "GENERATE PROMPT"
   - View live preview in JSON or NLP mode
   - QA dashboard updates in real time

6. **Export or Copy**
   - Click "Copy" to copy to clipboard
   - Click "Export" to download as file
   - Click "Import" to restore previous configuration

## 🏗️ System Architecture

### Frontend Stack

- **HTML5**: Semantic markup with ARIA accessibility attributes
- **Tailwind CSS**: Utility-first styling with custom color palette
- **Vanilla JavaScript**: No external dependencies
- **Local Storage**: Browser-based state persistence

### Component Structure

```
┌─────────────────────────────────────────────────┐
│              HEADER (Navigation)                 │
├──────────────────┬──────────────────────────────┤
│                  │                              │
│  Configuration   │      Live Preview Panel      │
│   Panel (Left)   │      (Right)                 │
│                  │                              │
│  - Mission       │  - JSON/NLP Toggle           │
│  - Calibration   │  - Real-time Output          │
│  - Output DNA    │  - Copy/Import/Export        │
│  - Voice Sample  │  - QA Dashboard              │
│                  │                              │
├──────────────────┴──────────────────────────────┤
│     GENERATE BUTTON (Full Width)                │
└─────────────────────────────────────────────────┘
```

### Data Flow

1.  **Input Capture**: All form fields collected into `collectAnswers()` object
2. **Dimension Derivation**: `deriveDimensions()` maps inputs to system parameters
3. **Voice Analysis**: `analyzeVoice()` processes writing sample (if provided)
4. **Composition**: `composeInstructionsJson()` or `composeInstructionsNlp()` generates output
5. **Quality Assurance**: `qaCheck()` validates output against constraints
6. **Rendering**: `renderOutput()` displays with syntax highlighting
7. **Export**: Copy to clipboard, download as file, or import configuration

## ⚙️ Configuration Guide

### Mission Parameters

| Field | Options | Purpose |
|-------|---------|---------|
| Primary Function | Research & Intelligence, Product Design, Legal & Compliance, System Operations, High-Value Content | Defines role and expertise area |
| End User & Goal | Free text | Specifies audience and desired outcome |
| Logic Metaphor | Coach, Lab, Pit Crew, Compass, Museum | Sets vocabulary and framing pattern |

### Model Calibration

| Field | Range | Effect |
|-------|-------|--------|
| Risk Profile | 1 (Low/Conservative) – 5 (Extreme) | Influences safety tolerance, evidence requirements |
| Velocity | 1 (Fast), 3 (Balanced), 5 (Deep) | Controls analysis depth vs. speed |
| Cite Sources | Yes (Mandatory), No | Requires evidence backing for claims |
| Ambiguity Tolerance | 1 (Zero), 3 (Medium), 5 (High) | Determines guessing vs. clarification behavior |

### Output DNA

**Negative Constraints**
- Pre-defined chips: No Hype, No Guarding, No Hedging, No Padding, No Lectures
- Custom constraints: Type and auto-format to "No X" pattern
- No AI Boilerplate: Suppresses default AI disclaimers and hedging

**Tone Options**
| Tone | Description |
|------|-------------|
| Executive (Concise) | Decisive, high-signal, policy-aligned |
| Neutral | Objective, balanced, analytical |
| Blunt | Brutally efficient, zero filler |
| Creator (Raw) | Authentic, unpolished, human |
| Slick | Smooth, polished, persuasive |
| Grungy | Raw, unvarnished, street-level |
| Gen-Z | Casual, trendy, internet-native |
| Gen-X | Cynical, independent, no-nonsense |
| Millennial | Earnest, collaborative, experienced |
| Sharp + Witty | Clever, incisive, humorous |
| Best Friend | Supportive, informal, close |
| Analytical + Critical | Deeply logical, questioning, dissecting |
| Custom | User-defined tone description |

**Mandatory Sections**
- Assumptions
- Risks
- Alternatives
- Action Items

## 🔬 Voice Analysis Engine

### How StyleTrace™ Works

1. **Input Validation**: Accepts 75+ word samples minimum
2. **Sentence Parsing**: Extracts all sentences (.  !  ?)
3. **Metrics Calculation**:
   - Average sentence length (word count)
   - Punctuation density (commas, dashes per sentence)
   - Exclamation frequency
   - 3-word phrase clustering (core phrases with >1 occurrence)

4. **Profile Generation**:
   - Tone Signature: Maps metrics to style categories
   - Modifier Density: Low (high impact) if avg length < 10
   - Sentence Depth: Atomic/Direct or Complex Clause Stacking
   - Core Phrases: Top 3 recurring 3-word clusters
   - Risk Posture: Aggressive/Direct or Deep/Analytical
   - Persona Edges: Extracted attributes (Punchy, High-Energy, Fragmented, etc.)
   - Structural Bias: Rhythm-led (punctuation > 1. 0 density) or Logic-led

5. **Output**: JSON object embedded in system prompt with forensic gating rules

### Minimum Requirements

- **75+ words**: Required for voice fingerprinting
- **Active Status Indicator**: "VOICEPRINT LOCKED" displays when threshold met
- **Optional**: Sample can be left blank for preset tone mode

### Limitations

- Only analyzes text-based patterns (no audio input)
- Does not process audio files
- Cannot extract speaker identity
- Treats all writing equally regardless of context
- No personalization beyond linguistic metrics

## 📤 Export Formats

### JSON Mode

**Structure**: Hierarchical object with sections:
- `meta`: System name, role, objective, voice engine status, style profile
- `operational_mode`: Voice detection description, metrics tracked
- `enforcement_protocols`: Fragmentation anchors, forensic emulation, tone locks
- `operational_profile`: Velocity, pace nuance, risk tolerance
- `protocols`: Ambiguity handling, evidence standards, safety override, failsafe
- `output_architecture`: Structure, length, visuals
- `mandatory_sections`: Required output sections
- `negative_constraints`: Prohibited behaviors

**Syntax Highlighting**: 
- Keys: Blue (#60A5FA)
- Strings: Teal (#A7F3D0)
- Numbers: Pink (#F472B6)
- Booleans: Amber (#FBBF24)
- Null: Gray (#94969D)

### NLP Mode

**Structure**: Markdown narrative with sections:
- Role and objective statement
- Operating mode description
- Voice & style profile
- Enforcement subroutines
- Operational profile
- Output format specifications
- Mandatory sections
- Safety protocol
- Failsafe procedures
- Negative constraints
- Do-not rules

**Formatting**:
- Markdown headers (###)
- Bold emphasis (**text**)
- Bullet points
- Human-readable language

### File Export

**JSON Export**
- Filename: `system_prompt. json`
- Format: Pretty-printed (4-space indentation)
- Use case: Direct API integration, version control

**Text Export**
- Filename: `system_prompt.txt`
- Format: NLP narrative mode
- Use case: Human reading, documentation

## 🎓 Advanced Usage

### Custom Tone Creation

1. Select "Custom (Type Your Own)" from Tone dropdown
2. Input field appears below
3. Enter tone description (e.g., "Socratic, question-focused, Socratic method")
4. Description embedded in system prompt under "Custom Tone:"

### Negative Constraints with Auto-Fix

**Input Patterns Recognized**:
- "don't be X" → converts to "No X"
- "stop X" → converts to "No X"
- "no X" → preserved as-is
- "X" (plain) → prepends "No " to become "No X"

**Capitalization**: All words auto-capitalized for consistency

**Chip Management**:
- Click any constraint chip to toggle active/inactive state
- Active chips appear highlighted (sage background, bold text)
- Remove custom chips by deactivating in display

### Import/Export Workflow

**Save Current Config**
```
1. Configure all parameters
2. Click "Save State"
3. Settings stored to browser localStorage
4. Confirmation alert appears
```

**Export for Backup**
```
1.  Click "Export"
2. Choose JSON or Text format
3. File downloads automatically
4. Backup stored locally
```

**Restore from File**
```
1. Click "Import"
2. Select previously exported . json file
3. File validated for structure and size (<1MB)
4. All settings restored
5. Success confirmation displayed
```

### QA Dashboard Interpretation

| Indicator | Status | Meaning | Action |
|-----------|--------|---------|--------|
| Tone Match | PASSED | Mission/tone encoded in output | None required |
| Tone Match | FIX | Mission/tone missing from role | Regenerate or adjust mission |
| Guardrails | PASSED | Negative constraints present | None required |
| Guardrails | FIX | Constraints missing from JSON | Add constraints and regenerate |
| Structure Check | PASSED | Mandatory sections found | None required |
| Structure Check | FIX | Required sections absent | Select mandatory sections and regenerate |

**LED Indicator**:
- 🟢 Green + Pulse: All checks passing, system ready
- 🔴 Red + Pulse: One or more QA checks failed, review output

## 🔐 Security & Safety

### Client-Side Architecture

- All processing occurs in browser (no data sent to servers)
- No backend dependencies
- No API calls or external network traffic
- Settings stored only in browser localStorage

### Safety Protocol

**Active Safeguards**:
- Privacy risk detection (configured to HALT if triggered)
- Evidence requirement validation for high-risk profiles
- Ambiguity clarification protocol (Level 1 = ask questions)
- Failsafe tone escalation if drift detected

**Protocol Statement** (embedded in output):
```
CRITICAL: If a section cannot be completed (missing evidence, technical 
limitation, or privacy risk), state so clearly.  If privacy risk is detected, 
HALT and report. 
```

### Import Validation

- File size limit: 1MB maximum
- JSON structure validation required
- Malformed files rejected with alert
- Error messages: "Import Failed: [specific reason]"

### Input Sanitization

**XSS Prevention**:
- HTML special characters escaped before display
- JSON rendering uses safe syntax highlighting
- Textarea values treated as plain text

## 🛠️ Troubleshooting

### Voice Sample Not Locking

**Symptom**: "VOICEPRINT LOCKED" status not appearing after paste

**Causes**:
- Sample contains fewer than 75 words
- Wordcount calculated by whitespace splitting (may differ from visual count)
- Check character count in bottom of browser or use external word counter

**Solution**:
- Add more content to sample (minimum 80–100 words recommended)
- Verify whitespace between words
- Re-paste and monitor character limit

### Settings Not Saving

**Symptom**: Refresh clears all configuration

**Causes**:
- Browser localStorage disabled
- Private/Incognito mode active
- Storage quota exceeded
- Browser cookies/storage cleared

**Solution**:
1. Check browser storage settings
2. Export configuration to file for backup
3. Try non-private window
4. Import saved file on next session

### Import Fails with Invalid JSON Error

**Symptom**: "Import Failed: Invalid JSON file"

**Causes**:
- Exported file corrupted or modified
- File not actually JSON format
- Text encoding issue (UTF-8 expected)

**Solution**:
1.  Verify file name ends in `. json`
2. Open in text editor to check format
3. Re-export from application
4. Try reimporting fresh export

### QA Checks Failing (Red LED)

**Symptom**: One or more QA indicators show "FIX"

**Possible Issues**:
| QA Check | Solution |
|----------|----------|
| Tone Match failed | Select a Primary Function; regenerate prompt |
| Guardrails failed | Select at least one negative constraint chip |
| Structure failed | Select at least one Mandatory Section chip |

**Steps**:
1. Review left panel configuration
2.  Ensure all mandatory sections and constraints selected
3. Click "GENERATE PROMPT" again
4. Verify LED turns green

### Output Not Displaying

**Symptom**: Preview pane shows loading state or blank

**Causes**:
- "GENERATE PROMPT" button not clicked
- JavaScript error in browser console
- Browser cache issue

**Solution**:
1. Click "GENERATE PROMPT" explicitly
2. Check browser Developer Tools (F12) for errors
3. Clear cache and reload page
4. Try different browser

## 📄 License

ApexSound Voice Engine with StyleTrace™ by BNDR is provided as-is for use by BNDR and authorized users. 

---

## 📞 Support & Questions

For issues, questions, or feature requests, please refer to the GitHub Issues section or contact the repository maintainer.

---

**Last Updated**: November 30, 2025  
**Version**: vX.3 APEX FORGE™  
**Status**: Production Ready
