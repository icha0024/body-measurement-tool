# body-measurement-tool

AI-powered body measurement tool using pose detection. Measures shoulder and waist width from photos with TensorFlow.js MoveNet model. No backend required - runs entirely in the browser.

## 📖 Project Background

This tool is a recreation of the body measurement system I developed as part of a larger project. Due to branding requirements and IP policies, I was unable to retain the complete original codebase in my personal repository. 

This standalone version focuses specifically on the **body measurement functionality** - the core AI-powered measurement system that I designed and implemented. While the original project included additional features like user management, databases, and full web application infrastructure, this recreation captures the essential measurement logic and user interface.

## ✨ Features

- **AI-Powered Pose Detection** using TensorFlow.js and MoveNet SINGLEPOSE_LIGHTNING model
- **Camera Capture** with 5-second countdown timer
- **Photo Upload Support** with comprehensive file validation
- **Automatic Body Measurements**:
  - Shoulder width (distance between shoulder keypoints)
  - Waist width (distance between hip keypoints)
- **Visual Landmarks** showing detected body points with colored annotations
- **Measurement History** with local storage (saves last 50 measurements)
- **Robust Input Validation**:
  - File type validation (JPEG/PNG only)
  - File size limits (<10MB)
  - Image dimension requirements (>400x400px)
  - Height input bounds (50-250cm range)
  - Confidence scoring (>0.5 threshold for keypoints)
  - Realistic measurement bounds (20-200cm range validation)
- **Responsive Design** for mobile and desktop using Bootstrap 5

## 💡 How It Works

The tool uses computer vision with multiple validation layers:

1. **Input Validation**: Validates file format, size, dimensions, and height input ranges
2. **Pose Detection**: MoveNet SINGLEPOSE_LIGHTNING model detects body keypoints
3. **Quality Assurance**: Ensures nose, shoulders, and hips are detected with >50% confidence
4. **Scale Calculation**: Uses nose-to-hip pixel distance and provided height as reference
5. **Measurement Computation**: Calculates shoulder and waist widths in centimeters
6. **Bounds Checking**: Validates measurements fall within realistic ranges (20-200cm)
7. **Visualization**: Draws colored landmarks and measurement lines on canvas
8. **Storage**: Optionally saves validated results to browser's local storage

## 🛠️ Technologies Used

- **TensorFlow.js** - Machine learning framework for browser inference
- **MoveNet SINGLEPOSE_LIGHTNING** - Google's pose detection model
- **Bootstrap 5.3.0** - Responsive UI framework with utility classes
- **Font Awesome 6.0.0** - Icons for user interface elements
- **Vanilla JavaScript** - Core application logic and DOM manipulation
- **HTML5 Canvas** - Image processing and landmark visualization
- **WebRTC getUserMedia** - Camera access for live capture
- **LocalStorage API** - Client-side measurement history persistence
- **File API** - Image upload and validation handling

## 🔧 Technical Details

### Input Validation System
- **File format**: Strict JPEG/PNG validation with type checking
- **File size**: 10MB maximum limit with user feedback
- **Image quality**: Minimum 400x400px resolution requirement
- **Height input**: 50-250cm bounds for upper body measurements
- **Error handling**: Comprehensive user feedback for validation failures

### AI Model Performance
- **Model variant**: SINGLEPOSE_LIGHTNING for speed-accuracy balance
- **Keypoint validation**: Requires 5 specific body landmarks (nose, both shoulders, both hips)
- **Confidence threshold**: Minimum 0.5 score for reliable detection
- **Measurement validation**: 20-200cm realistic bounds checking with error messages

### Data Management
- **Privacy-first**: Complete client-side processing, no data transmission
- **History management**: Maintains last 50 measurements in localStorage
- **Error recovery**: Graceful handling of pose detection failures

## 📱 Browser Compatibility

Tested and verified on:
- ✅ Chrome 90+
- ✅ Firefox 88+  
- ✅ Safari 14+
- ✅ Edge 90+

**Requirements**: WebRTC support (camera access) and WebGL (TensorFlow.js acceleration)

## 🔒 Privacy & Security

- **No data collection** - zero telemetry or analytics
- **Offline capable** - works without internet after initial model download
- **Local processing** - photos and measurements never leave your device
- **Browser storage only** - all data saved locally
- **Input sanitization** - comprehensive validation prevents malformed data

## 📱 Mobile Support

Fully responsive design optimized for mobile devices:
- Touch-friendly interface with large interactive elements
- Responsive canvas sizing for various screen sizes
- Native mobile camera integration
- Portrait/landscape orientation support

## ⚠️ Limitations & Disclaimers

- **Intended for general fitness tracking** - not medical grade measurements
- **Measurement accuracy** depends on photo quality, lighting, and pose positioning
- **Single person detection** - designed for individual measurements only
- **Upper body focus** - requires waist-to-head visibility for accurate scaling
- **Browser dependency** - requires modern browser with WebGL support
