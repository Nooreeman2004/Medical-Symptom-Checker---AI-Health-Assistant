# 🩺 Medical Symptom Checker - AI Health Assistant

An intelligent symptom analysis tool that uses a two-stage AI prompting chain to help users understand their symptoms and receive personalized health guidance. Built with Groq AI and designed for educational purposes.

## ⚠️ Medical Disclaimer

**This tool is for educational and informational purposes only. It does not provide medical diagnosis or replace professional medical advice. Always consult with qualified healthcare professionals for medical concerns.**

## ✨ Features

- **🔍 Smart Symptom Extraction**: Automatically identifies symptoms, duration, and severity from natural language
- **📋 Structured Analysis**: Two-stage processing for accurate symptom parsing
- **💬 Conversational Health Summaries**: Friendly, personalized health guidance
- **🎯 Actionable Recommendations**: Clear next steps and when to seek professional help
- **🔄 Interactive Loop**: Continuous symptom checking in a single session
- **⚡ Fast Processing**: Powered by Groq's high-speed AI inference

## 🏗️ Architecture

```
User Input → Stage 1: Symptom Extraction → Stage 2: Health Summary → Output
```

### Two-Stage Prompting Chain

1. **Stage 1 - Extraction** (Temperature: 0.2)
   - Structured prompt for precise symptom identification
   - Extracts: symptoms, duration, severity
   - Low temperature for consistent parsing

2. **Stage 2 - Summary** (Temperature: 0.8)
   - Conversational prompt for natural health guidance
   - Generates personalized recommendations
   - Higher temperature for human-like responses

## 🚀 Quick Start

### Prerequisites
- Python 3.7+
- Groq API Key

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/medical-symptom-checker.git
cd medical-symptom-checker
```

2. Install dependencies:
```bash
pip install groq
```

3. Set up your Groq API key:
```python
client = Groq(api_key="your_api_key_here")
```

4. Run the application:
```bash
python symptom_checker.py
# Or run the Jupyter notebook
jupyter notebook "Medical Symptom Checker prompting chain.ipynb"
```

## 💻 Usage Example

```
Describe your symptoms (or type 'exit' to quit): I have a headache for 3 days and mild fever

Extracted Data: {
    'Symptoms': ['headache', 'fever'], 
    'Duration': '3 days', 
    'Severity': 'mild'
}

Health Summary:
It sounds like you're dealing with a headache and mild fever that's been 
going on for about 3 days. This combination could suggest a few possibilities 
like a viral infection, stress, or dehydration.

Here's what I'd recommend:
- Get plenty of rest and stay hydrated
- Consider over-the-counter pain relief if appropriate
- Monitor your temperature
- If symptoms worsen or persist beyond a week, consult a healthcare professional

Take care of yourself, and don't hesitate to seek medical attention if you're concerned.
```

## 🛠️ Technical Details

### Models & Settings
- **Model**: Groq Llama-3.3-70b-versatile
- **Stage 1**: Temperature 0.2, Max tokens 200
- **Stage 2**: Temperature 0.8, Max tokens 300

### Error Handling
- Graceful API failure handling
- Default fallback responses
- Input validation and sanitization

### Data Structure
```python
symptom_data = {
    "Symptoms": ["symptom1", "symptom2"],
    "Duration": "duration or 'not specified'",
    "Severity": "severity or 'not specified'"
}
```

## 🔧 Configuration

Customize the prompting behavior by modifying:

- **Temperature settings**: Adjust creativity vs. consistency
- **Token limits**: Control response length
- **Prompt templates**: Modify extraction and summary styles
- **Model selection**: Switch between available Groq models

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/enhancement`
3. Commit your changes: `git commit -m 'Add enhancement'`
4. Push to the branch: `git push origin feature/enhancement`
5. Open a Pull Request

### Contribution Guidelines
- Maintain medical accuracy and safety
- Include appropriate disclaimers
- Test with various symptom inputs
- Document any prompt modifications

## 📋 Roadmap

-  **Multi-language Support**: Symptom analysis in different languages
-  **Symptom History Tracking**: Session-based symptom monitoring
-  **Integration with Health APIs**: Connect to medical databases
-  **Severity Scoring**: Quantitative symptom assessment
-  **Emergency Detection**: Identify urgent medical situations

## ⚖️ Ethical Considerations

- **No Diagnostic Claims**: Provides guidance, not diagnosis
- **Professional Referrals**: Always recommends consulting healthcare providers
- **Privacy Focused**: No storage of personal health information
- **Transparent Limitations**: Clear about AI capabilities and boundaries

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Powered by [Groq](https://groq.com/) AI
- Built for educational purposes
- Inspired by the need for accessible health information

---

**Remember: This tool supplements but never replaces professional medical advice. Always consult healthcare professionals for medical concerns. 🩺**
