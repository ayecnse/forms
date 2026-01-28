# AyeCNSe Forms

**AI-First Browser-Based Interface Specification Builder**

[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)
[![FOSS](https://img.shields.io/badge/FOSS-100%25-green.svg)](https://github.com/ayecnse/ayecnse-forms)

> "To see life is not to observe pixels, signals, or data. It is to remain coherent while sensing, thinking, and acting in the world."

AyeCNSe Forms is a declarative interface specification builder that uses conversational AI (Claude) to design forms, control panels, and human-machine interfaces without writing code.

## The AyeAI Triad

AyeCNSe Forms is part of the AyeAI ecosystem:

- **AyeAI** - Cognition, reasoning, learning. Models of the world and of the self.
- **AyeCNSe** - The nervous system. Timing, sensing, coherence, and transport.
- **AyeAM** - Embodiment. Action in the physical and simulated world.

Remove any one element and intelligence collapses. Together, they form a living loop.

## Features

### 🤖 AI-Powered Design
- Describe your interface in natural language
- Claude AI creates complete specifications through conversation
- Voice or text interaction supported

### 🎨 Manual Builder
- Visual editor for hands-on control
- Drag-and-drop field creation
- Full customization of form elements

### 💬 Conversational Form Filling
- Users can fill forms by talking to Claude AI
- Natural conversations generate structured data
- JSON output for easy integration

### 🔒 Privacy First
- No backend required
- No APIs at runtime
- No tracking
- Everything runs in your browser
- Data never leaves your device

### 📦 Declarative Architecture
- Pure JSON specifications
- No embedded scripts
- No conditional logic
- Fully serializable
- Deterministic runtime

## Supported Field Types

- Text input (with regex validation)
- Text area
- Number (with min/max constraints)
- Checkbox
- Radio buttons
- Dropdown
- Date picker
- Read-only display fields

## Getting Started

### Option 1: Direct Use

1. Download `index.html` and `ayecnse-forms.html`
2. Open `index.html` in any modern web browser
3. The app will auto-launch after 60 seconds (or click "Launch App Now")

### Option 2: Host on GitHub Pages

1. Fork this repository
2. Go to Settings → Pages
3. Select main branch as source
4. Your form builder will be live at `https://yourusername.github.io/ayecnse-forms/`

### Option 3: Local Development

```bash
# Clone the repository
git clone https://github.com/ayecnse/ayecnse-forms.git
cd ayecnse-forms

# Open in browser
open index.html
# or
python -m http.server 8000
# Then visit http://localhost:8000
```

## Usage

### Creating a Form

#### Using AI Design
1. Click "🤖 AI Design" button
2. Claude AI opens in a new tab
3. Describe your form requirements
4. Copy the generated JSON
5. Paste it back into the app

#### Manual Design
1. Click "+ Add Field"
2. Configure field properties:
   - Type (text, number, checkbox, etc.)
   - Label and section
   - Priority (normal, critical, optional)
   - Validation rules
3. Repeat for all fields
4. Preview updates in real-time

### Filling a Form

#### AI-Assisted Fill
1. Click "🤖 AI-Assisted Fill"
2. Claude AI opens with your form specification
3. Have a conversation to provide answers
4. Claude outputs filled JSON
5. Click "📋 Paste Filled JSON"
6. Paste the JSON to populate the form

#### Manual Fill
- Simply fill in the form fields
- All validation rules apply
- Click "Submit Form" to see structured output

### Configuration Management

- **Download**: Save form configuration as JSON
- **Upload**: Load configuration from file
- **GitHub**: Load from raw GitHub URL
- **Local Storage**: Automatically saves last config

## Use Cases

- Survey and questionnaire design
- Medical intake forms
- Industrial control panels
- IoT device interfaces
- Robotics command interfaces
- Research data collection
- Educational assessments
- Customer feedback forms

## Technical Architecture

### Design Principles

1. **Declarative Over Imperative**: Everything is specified, nothing is executed
2. **AI at Design Time, Not Runtime**: Claude helps build, but isn't needed to run
3. **Zero Backend**: Complete client-side operation
4. **Language Neutral**: Built with Project Hindawi's philosophy of mother tongue computing
5. **Safety First**: Explicit modes, confirmations, and constraints

### JSON Specification Format

```json
{
  "formTitle": "Example Form",
  "mode": "simulation",
  "sections": ["Section 1", "Section 2"],
  "fields": [
    {
      "type": "text",
      "label": "Name",
      "section": "Section 1",
      "priority": "critical",
      "required": true,
      "regex": "^[A-Za-z ]+$"
    },
    {
      "type": "number",
      "label": "Age",
      "section": "Section 1",
      "priority": "normal",
      "required": true,
      "min": 0,
      "max": 150
    }
  ]
}
```

## Related Projects

### Foundation Projects

- **[Project Hindawi](https://hindawi.in)** - Programming in Your Mother Tongue (मातृभाषा में प्रोग्रामिंग)
- **[Project ILM](https://ilm.codes)** - Integrative Linguistic Multiscript
- **[Project VIKRAM](https://hindawi.in)** - Language neutrality across technical domains
- **[TWISHA](https://ayeai.xyz)** - The Women in Self Health Awareness

### The Ecosystem

- **[AyeAI](https://ayeai.xyz)** - Cognition and reasoning layer
- **[AyeCNSe](https://ayecnse.net)** - Nervous system and transport layer
- **[AyeAM](https://ayeam.org)** - Embodiment and action layer

## Contributing

We welcome contributions! See [CONTRIBUTORS.md](CONTRIBUTORS.md) for details.

### Ways to Contribute

- Report bugs and suggest features
- Submit pull requests
- Improve documentation
- Add translations
- Share use cases and examples
- Test on different platforms

### Development Setup

```bash
# Fork and clone
git clone https://github.com/yourusername/ayecnse-forms.git
cd ayecnse-forms

# Make changes
# Test in browser

# Submit PR
git checkout -b feature/my-feature
git commit -am "Add my feature"
git push origin feature/my-feature
```

## License

GPL v2 License - see [LICENSE](LICENSE) file for details

Copyright 2026 Abhishek Choudhary

This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the License, or (at your option) any later version.

## Support

### Financial Support

Support the development of AyeCNSe Forms and related projects:

- [Razorpay Payment Link] *(Add your link here)*

All contributions are used to support language-neutral, open source AI development.

### Community Support

- GitHub Issues: [Report bugs or request features](https://github.com/ayecnse/ayecnse-forms/issues)
- LinkedIn: [Project Hindawi](https://www.linkedin.com/company/हिंदवी)
- Facebook: [Hindawi Programming](https://www.facebook.com/Hindawi-Programming-System-196804757588931)

## Philosophy

> "True freedom can only be achieved in the most creative states of mind. The mind is most creative when free to work with the mother tongue."

AyeCNSe Forms embodies the principle that technology should serve humanity in its natural languages, not force humanity to adapt to English-only interfaces.

---

**AyeCNSe · FOSS · CNS for Earth**

© 2026 Abhishek Choudhary

First archived https://archive.is/zgcrb 28 Jan 2026 07:44:47 UTC
