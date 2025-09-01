# AI-Based Video Creation Platform

A modern, AI-powered web application that automatically generates educational videos from text content, code, and topics. The platform uses natural language processing to summarize content and creates engaging presentations with audio narration.

## ✨ Features

- **AI-Powered Summarization**: Automatically summarizes long content using state-of-the-art NLP models
- **Presentation Generation**: Creates professional PowerPoint presentations from your content
- **Audio Synthesis**: Generates natural-sounding audio narration using text-to-speech
- **Video Creation**: Combines slides and audio into engaging videos
- **Modern UI/UX**: Beautiful, responsive interface with real-time progress tracking
- **Session Management**: Secure file handling with unique session IDs
- **Error Handling**: Comprehensive error handling and user feedback
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- FFmpeg installed on your system
- At least 4GB RAM (for AI models)

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd AI-Based-Video-Creation
   ```

2. **Install Python dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Install FFmpeg**
   
   **Windows:**
   - Download from [FFmpeg official website](https://ffmpeg.org/download.html)
   - Add to PATH environment variable
   
   **macOS:**
   ```bash
   brew install ffmpeg
   ```
   
   **Ubuntu/Debian:**
   ```bash
   sudo apt update
   sudo apt install ffmpeg
   ```

4. **Set up environment variables** (optional)
   ```bash
   # Create .env file
   echo "SECRET_KEY=your-secret-key-here" > .env
   ```

5. **Run the application**
   ```bash
   python app.py
   ```

6. **Open your browser**
   Navigate to `http://localhost:5000`

## 🏗️ Project Structure

```
AI-Based-Video-Creation/
├── app.py                 # Main Flask application
├── config.py              # Configuration settings
├── utils.py               # Utility functions
├── video_service.py       # Video generation service
├── requirements.txt       # Python dependencies
├── index.html            # Main web interface
├── style.css             # Styling and animations
├── README.md             # This file
└── temp/                 # Temporary files (auto-created)
```

## 🔧 Configuration

The application can be configured through the `config.py` file:

- **Video Settings**: Resolution, frame rate, quality
- **Audio Settings**: Language, speech rate, voice options
- **Model Settings**: AI model selection and parameters
- **File Limits**: Maximum content length and file sizes
- **Cleanup Settings**: Automatic cleanup intervals

## 📱 Usage

1. **Enter Content**: Fill in the topic, content, and code fields
2. **Generate Video**: Click "Generate Video" to start the process
3. **Monitor Progress**: Watch real-time progress through the step-by-step interface
4. **Download**: Once complete, download your generated video
5. **Cleanup**: Clean up temporary files when done

## 🎯 API Endpoints

- `GET /` - Main application interface
- `POST /generate-video` - Generate video from input data
- `GET /download/<session_id>/<filename>` - Download generated video
- `POST /cleanup/<session_id>` - Clean up session files
- `GET /status/<session_id>` - Check video generation status
- `GET /health` - Application health check

## 🛠️ Technical Details

### AI Models Used
- **Summarization**: Facebook BART Large CNN (via Hugging Face Transformers)
- **Text-to-Speech**: Google Text-to-Speech (gTTS)

### Video Processing
- **Format**: MP4 with H.264 codec
- **Resolution**: 1920x1080 (Full HD)
- **Frame Rate**: Configurable (default: 1 frame per 5 seconds)

### Security Features
- Session-based file handling
- Input validation and sanitization
- Secure file serving with path validation
- Rate limiting support

## 🔒 Security Considerations

- All user inputs are validated and sanitized
- Temporary files are stored in isolated session directories
- File access is restricted to prevent directory traversal attacks
- Session IDs use UUID4 for uniqueness and security

## 🚨 Troubleshooting

### Common Issues

1. **FFmpeg not found**
   - Ensure FFmpeg is installed and added to PATH
   - Restart your terminal after installation

2. **Out of memory errors**
   - Reduce the AI model size in config.py
   - Close other applications to free up RAM

3. **Video generation fails**
   - Check FFmpeg installation
   - Verify sufficient disk space in temp directory
   - Check application logs for detailed error messages

4. **Slow performance**
   - Use GPU acceleration if available (set device=0 in config)
   - Reduce video resolution in config.py
   - Optimize input content length

### Logs and Debugging

The application provides detailed logging. Check the console output for:
- Model loading status
- File processing steps
- Error details and stack traces
- Performance metrics

## 🔄 Future Enhancements

- [ ] Multiple video templates and themes
- [ ] Background music and sound effects
- [ ] Advanced video transitions and animations
- [ ] Multi-language support
- [ ] Cloud storage integration
- [ ] User authentication and project management
- [ ] Batch processing capabilities
- [ ] Real-time collaboration features

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

**RIYA CHAND** - Initial development and design

## 🙏 Acknowledgments

- Hugging Face for AI models
- Google for Text-to-Speech service
- FFmpeg for video processing
- Flask community for web framework
- Font Awesome for icons

## 📞 Support

If you encounter any issues or have questions:
1. Check the troubleshooting section above
2. Review the application logs
3. Create an issue in the repository
4. Contact the development team

---

**Happy Video Creating! 🎬✨**
