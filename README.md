# Elderly Voice Assistant 🎤

A comprehensive voice assistant application designed specifically for elderly users, featuring emergency alerts, medication reminders, entertainment, and multilingual support.

## 🌟 Features

### Core Functionality
- **Voice Recognition**: Speech-to-text input for hands-free interaction
- **Text-to-Speech**: Natural voice responses for accessibility
- **Multilingual Support**: English and Tamil language support
- **Web Interface**: User-friendly web dashboard

### Emergency Features 🚨
- **Emergency Detection**: Automatically detects emergency keywords
- **SMS Alerts**: Sends emergency SMS via Twilio
- **Voice Calls**: Makes emergency calls with pre-recorded messages
- **Location Sharing**: Includes location data in emergency alerts

### Daily Assistance
- **Medication Reminders**: Timely reminders for medications
- **Time & Date**: Provides current time and date information
- **Greeting Responses**: Context-aware greetings throughout the day
- **General Conversation**: Rule-based chatbot for companionship

### Entertainment 🎵
- **YouTube Integration**: Play music and videos via voice commands
- **Voice Commands**: Simply say "play [song/artist]" to enjoy music

## 🏗️ Architecture

```
elderly_voice_assistant-main/
├── app.py                 # Main Flask application
├── config.py             # Configuration settings
├── requirements.txt      # Python dependencies
├── .gitignore           # Git ignore file
├── static/
│   └── style.css        # Application styles
├── templates/
│   ├── index.html       # Main interface
│   ├── chat.html        # Chat interface
│   ├── dashboard.html   # User dashboard
│   ├── reminders.html   # Medication reminders
│   └── settings.html    # Application settings
└── utils/
    ├── __init__.py
    ├── chatbot_ai.py        # AI chatbot logic
    ├── emergency_alert.py   # Emergency alert system
    ├── intent_classifier.py # Intent recognition
    ├── logger.py           # Logging utilities
    ├── reminder_manager.py  # Reminder management
    ├── speech_to_text.py   # Speech recognition
    ├── summarizer.py       # Text summarization
    ├── text_to_speech.py   # Text-to-speech conversion
    └── translator.py       # Language translation
```

## 🚀 Installation

### Prerequisites
- Python 3.7 or higher
- pip package manager

### Setup Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/Arya-2606/Elderly-Voice-Assistant.git
   cd Elderly-Voice-Assistant/elderly_voice_assistant-main
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set up environment variables**
   Create a `.env` file in the root directory:
   ```env
   # Twilio Configuration (for emergency alerts)
   TWILIO_ACCOUNT_SID=your_twilio_account_sid
   TWILIO_AUTH_TOKEN=your_twilio_auth_token
   TWILIO_NUMBER=your_twilio_phone_number
   VERIFIED_NUMBER=emergency_contact_number
   VOICE_MP3_URL=url_to_emergency_voice_message

   # Deployment Configuration
   RENDER=false  # Set to "true" when deploying on Render
   ```

4. **Run the application**
   ```bash
   python app.py
   ```

5. **Access the application**
   Open your web browser and navigate to `http://localhost:10000`

## 🔧 Configuration

### Twilio Setup (for Emergency Features)
1. Create a Twilio account at https://www.twilio.com
2. Get your Account SID and Auth Token from the Twilio Console
3. Purchase a Twilio phone number
4. Verify your emergency contact number
5. Add these credentials to your `.env` file

### Optional: Voice Message for Emergency Calls
Upload a pre-recorded emergency voice message to a hosting service and add the URL to the `VOICE_MP3_URL` environment variable.

## 📱 Usage

### Basic Commands
- **"Good morning"** - Get a morning greeting
- **"What time is it?"** - Hear the current time
- **"What day is it?"** - Hear the current day
- **"What's the date?"** - Hear the current date
- **"Medicine"** - Get medication reminder
- **"Play [song/artist]"** - Play music from YouTube

### Emergency Commands
- **"Help"** - Trigger emergency alert
- **"Emergency"** - Trigger emergency alert
- **"Save me"** - Trigger emergency alert
- **"உதவி" (Tamil for "Help")** - Trigger emergency alert

## 🌐 Deployment

### Local Development
Run the application locally using the provided setup instructions.

### Cloud Deployment (Render)
The application is optimized for deployment on Render:
1. Connect your GitHub repository to Render
2. Set environment variables in the Render dashboard
3. Deploy automatically

## 🔒 Security Features

- **Rate Limiting**: Emergency alerts have a 15-second cooldown
- **Input Validation**: All user inputs are sanitized
- **Environment Variables**: Sensitive data stored in environment variables
- **CORS Protection**: Cross-origin requests properly configured

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **Flask** - Web framework
- **Twilio** - SMS and voice services
- **YouTube DL** - Video/audio streaming
- **pyttsx3** - Text-to-speech conversion
- **Speech Recognition libraries** - Voice input processing

## 📞 Support

For support, please open an issue on GitHub or contact the project maintainer.

---

**Note**: This application is designed to assist elderly users but should not replace professional medical care or emergency services. Always have a backup emergency plan in place.
