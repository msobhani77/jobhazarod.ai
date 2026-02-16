# 🚨 SafetyWatch - AI-Powered Hazard Reporting System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![AI: Claude](https://img.shields.io/badge/AI-Claude%204-orange.svg)](https://www.anthropic.com/)

**SafetyWatch** is an intelligent hazard reporting system that helps technicians report workplace safety hazards with AI assistance. Features include photo analysis, automatic categorization, form completion help, and AI-generated safety recommendations.

![SafetyWatch Dashboard](screenshots/dashboard.png)

## ✨ Features

### 🤖 AI-Powered Capabilities
- **📸 Photo Analysis** - Upload hazard photos for automatic AI detection and classification
- **🏷️ Auto-Categorization** - Intelligent classification of hazard types and severity levels
- **✍️ Smart Form Assistant** - AI helps write professional, detailed descriptions
- **🛡️ Safety Recommendations** - Context-aware safety guidance for each hazard
- **💬 Interactive AI Chat** - Ask questions about safety procedures and best practices

### 📊 Core Features
- **Real-time Dashboard** - View all reports with statistics and trends
- **Persistent Storage** - Reports saved across sessions
- **Severity Classification** - Low, Medium, High, and Critical levels
- **Photo Upload & Preview** - Visual documentation of hazards
- **Professional UI** - Industrial safety design with intuitive navigation

## 🚀 Quick Start

### Option 1: Demo Mode (No Setup Required)

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/safetywatch.git
cd safetywatch
```

2. **Open the demo**
```bash
# Simply open in your browser
open demo/index-demo.html
```

The demo uses simulated AI responses - perfect for testing the UI without API setup.

### Option 2: Full AI Mode (Requires API Key)

1. **Get an Anthropic API Key**
   - Sign up at [console.anthropic.com](https://console.anthropic.com/)
   - Create an API key
   - ⚠️ **Never commit your API key to GitHub**

2. **Configure the application**
   - Open `index.html` in a browser
   - Click the "⚙️ Settings" button
   - Enter your API key (stored locally in browser only)
   - Start using full AI features

### Option 3: Production Deployment (Recommended)

For production use, deploy with a backend server to keep API keys secure.

**Quick Deploy with Node.js:**
```bash
cd backend
npm install
cp .env.example .env
# Edit .env and add your ANTHROPIC_API_KEY
npm start
```

See [TECHNICAL_ARCHITECTURE.md](TECHNICAL_ARCHITECTURE.md) for complete deployment guide.

## 📁 Project Structure

```
safetywatch/
├── index.html                  # Main application (requires API key input)
├── demo/
│   └── index-demo.html        # Demo version with mock AI responses
├── backend/                    # Backend server (Node.js/Express)
│   ├── server.js
│   ├── routes/
│   ├── models/
│   └── package.json
├── screenshots/                # Application screenshots
├── docs/
│   └── TECHNICAL_ARCHITECTURE.md
├── README.md
├── LICENSE
└── .gitignore
```

## 🔐 Security & Privacy

### ⚠️ Important Security Notes

1. **API Keys**
   - Never commit API keys to Git
   - Use environment variables for backend deployments
   - Client-side keys are for testing only - use backend for production

2. **Data Storage**
   - Demo version: Data stored in browser localStorage (client-side only)
   - Production: Use proper database with encryption
   - Photos: Consider cloud storage (S3, CloudStorage) for production

3. **Authentication**
   - Current version has no authentication (demo purposes)
   - See technical guide for JWT authentication implementation
   - Implement role-based access control for production

## 🛠️ Technology Stack

### Frontend
- HTML5, CSS3, JavaScript (Vanilla)
- Tailwind CSS for styling
- Custom design system with safety-focused aesthetics

### AI Integration
- Anthropic Claude API (Sonnet 4)
- Vision API for photo analysis
- Natural language processing

### Backend (Optional)
- **Node.js**: Express + MongoDB
- **Python**: Flask/FastAPI + PostgreSQL
- **Serverless**: AWS Lambda + DynamoDB

## 📖 Usage Guide

### Reporting a Hazard

1. **Navigate to "Report Hazard" tab**
2. **Fill in basic information:**
   - Location (e.g., "Building A, Floor 3")
   - Your name
   - Hazard type (dropdown)
   - Severity level

3. **Describe the hazard:**
   - Type your description, or
   - Click "Get AI Help" for assistance

4. **Upload a photo (optional):**
   - Click to upload or drag & drop
   - Click "Analyze Photo with AI"
   - AI will auto-fill hazard type and severity

5. **Submit** - AI generates safety recommendations automatically

### Using the Dashboard

- View all submitted reports
- Filter by severity level
- See statistics (total, critical, high, medium)
- Each report shows AI-generated safety recommendations

### AI Assistant Chat

- Ask questions about safety procedures
- Get recommendations for specific scenarios
- Learn about hazard identification best practices

## 🎨 Customization

### Branding

Edit CSS variables in `index.html`:
```css
:root {
    --safety-orange: #FF6B00;    /* Primary brand color */
    --warning-yellow: #FFB800;   /* Warning indicators */
    --alert-red: #DC2626;        /* Critical alerts */
}
```

### Hazard Categories

Modify the hazard types in the HTML:
```javascript
<option value="Custom Category">Custom Category</option>
```

### AI Prompts

Customize AI behavior by editing prompts in the JavaScript sections.

## 🚀 Deployment Options

### Quick Deploy Buttons

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start)

### Manual Deployment

See [TECHNICAL_ARCHITECTURE.md](TECHNICAL_ARCHITECTURE.md) for detailed deployment guides:
- Node.js + MongoDB on Heroku/Railway
- Python + PostgreSQL on AWS/DigitalOcean
- Serverless on AWS Lambda
- Docker containerization
- Mobile app (React Native)

## 📊 Cost Estimation

### Small Team (10-50 users)
- **Hosting**: $0-20/month (Heroku free tier or Netlify)
- **Database**: $0-10/month (MongoDB Atlas free tier)
- **AI API**: $10-50/month (~500-2000 requests)
- **Total**: $10-80/month

### Enterprise (500+ users)
- **Hosting**: $50-200/month
- **Database**: $30-100/month
- **AI API**: $100-500/month
- **Total**: $180-800/month

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guidelines](CONTRIBUTING.md) first.

### Development Setup

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Make your changes
4. Commit (`git commit -m 'Add AmazingFeature'`)
5. Push (`git push origin feature/AmazingFeature`)
6. Open a Pull Request

### Reporting Issues

Found a bug? Have a feature request? [Open an issue](https://github.com/yourusername/safetywatch/issues)

## 📝 Roadmap

### Phase 1 (Current)
- ✅ Basic hazard reporting
- ✅ AI photo analysis
- ✅ Auto-categorization
- ✅ Safety recommendations
- ✅ Interactive dashboard

### Phase 2 (Planned)
- [ ] User authentication & roles
- [ ] Email notifications
- [ ] Mobile app (iOS/Android)
- [ ] Offline mode (PWA)
- [ ] Multi-language support

### Phase 3 (Future)
- [ ] Predictive analytics
- [ ] Integration with existing ERP systems
- [ ] Compliance reporting (OSHA, ISO)
- [ ] Real-time alerts
- [ ] Video hazard documentation

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Anthropic Claude** - AI capabilities
- **Tailwind CSS** - Styling framework
- **Font Awesome** - Icons (if using)
- Community contributors and testers

## 📞 Support

- **Documentation**: [Technical Architecture Guide](TECHNICAL_ARCHITECTURE.md)
- **Issues**: [GitHub Issues](https://github.com/yourusername/safetywatch/issues)
- **Discussions**: [GitHub Discussions](https://github.com/yourusername/safetywatch/discussions)
- **Email**: support@yourdomain.com

## ⚖️ Disclaimer

This software is provided as-is for demonstration and educational purposes. For production use in safety-critical environments, ensure proper testing, security audits, and compliance with relevant regulations (OSHA, ISO, etc.). The developers assume no liability for improper use or safety incidents.

---

**Made with ❤️ for workplace safety**

**Star ⭐ this repo if you find it useful!**
