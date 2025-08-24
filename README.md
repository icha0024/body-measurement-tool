# body-measurement-tool
AI-powered body measurement tool using pose detection. Recreated from a larger project - measures shoulder and waist width from photos with TensorFlow.js. No backend required.

## 📖 Project Background

This tool is a recreation of the body measurement system I developed as part of a larger  project. Due to branding requirements and IP policies, I was unable to retain the complete original codebase in my personal repository. 

This standalone version focuses specifically on the **body measurement functionality** - the core AI-powered measurement system that I designed and implemented. While the original project included additional features like user management, databases, and full web application infrastructure, this recreation captures only measurement logic and user interface.

## ✨ Features

- **AI-Powered Pose Detection** using TensorFlow.js and MoveNet model
- **Real-time Camera Capture** with countdown timer
- **Photo Upload Support** for analyzing existing images  
- **Automatic Body Measurements**:
  - Shoulder width
  - Waist width
- **Visual Landmarks** showing detected body points
- **Measurement History** with local storage
- **Responsive Design** for mobile and desktop

## 🚀 How to Use

1. **Clone or download** this repository
2. **Open `index.html`** in any modern web browser
3. **Allow camera permissions** when prompted (for camera mode)
4. **Choose your measurement method**:
   - **Camera**: Take a live photo with countdown
   - **Upload**: Select an existing photo from your device
5. **Enter your upper body height** (distance from slightly below waist to top of head)
6. **View your measurements** and save to history

## 💡 How It Works

The tool uses advanced computer vision to:
1. **Detect body pose** landmarks using Google's MoveNet model
2. **Identify key points** (shoulders, hips, nose) with confidence scoring
3. **Calculate pixel distances** between anatomical landmarks
4. **Scale measurements** using your provided upper body height as reference
5. **Display results** with visual confirmation of detected points

## 🛠️ Technologies Used

- **TensorFlow.js** - Machine learning framework
- **MoveNet** - Pose detection model
- **Bootstrap 5** - Responsive UI framework
- **Vanilla JavaScript** - Core application logic
- **HTML5 Canvas** - Image processing and landmark visualization
- **LocalStorage** - Client-side data persistence

## 🎯 Accuracy Tips

For best measurement accuracy:
- **Good lighting** with minimal shadows
- **Fitted clothing** to clearly show body outline
- **Stand straight** with arms slightly away from body
- **Full upper body visible** in frame (waist to head)
- **Stable camera/photo** without motion blur
- **Front-facing pose** perpendicular to camera

## 🔧 Technical Details

- **No backend required** - runs entirely in browser
- **Client-side processing** - your photos never leave your device
- **Cross-platform** - works on desktop and mobile browsers
- **Real-time inference** - measurements calculated instantly
- **Local data storage** - measurement history saved in browser

## 📋 Browser Compatibility

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+

*Requires a browser that supports WebRTC (for camera) and WebGL (for TensorFlow.js)*

## 🔒 Privacy

- **No data collection** - all processing happens locally
- **No internet required** after initial page load (model downloads once)
- **Photos not uploaded** - everything stays on your device
- **Local storage only** - measurements saved in your browser

## 📱 Mobile Support

The application is fully responsive and works on mobile devices. For best mobile experience:
- Use landscape orientation for camera mode
- Ensure good lighting
- Hold device steady during photo capture

## 🤝 Contributing

This is a personal portfolio project showcasing the measurement system I developed. While I'm not actively seeking contributions, feel free to fork the repository for your own experiments or learning purposes.

## ⚠️ Disclaimer

This tool is intended for general fitness tracking purposes. Measurements may vary based on photo quality, lighting conditions, and pose positioning. For medical or professional applications, please consult appropriate healthcare providers or use calibrated measurement tools.

---

*This project demonstrates computer vision and web development skills developed during my academic coursework in software engineering and AI applications.*