# Face Landmarks Detection with TensorFlow.js

This project demonstrates how to use TensorFlow.js to detect facial landmarks in real-time using the MediaPipe FaceMesh model. The application captures video from the user's webcam and overlays the detected facial landmarks on a canvas.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Code Explanation](#code-explanation)
- [Troubleshooting](#troubleshooting)

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/yourusername/facelandmarks-detection.git
    cd facelandmarks-detection
    ```

2. Install the dependencies:

    ```sh
    npm install
    ```

## Usage

1. Start the development server:

    ```sh
    npm start
    ```

2. Open your web browser and navigate to `http://localhost:3000`. The application will request access to your webcam and display the video feed with overlaid facial landmarks.

## Project Structure

facelandmarks-detection/
├── public/
│ └── index.html
├── src/
│ ├── App.css
│ ├── App.js
│ ├── index.js
│ └── utilities.js
├── .gitignore
├── package.json
└── README.md


## Dependencies

- `@tensorflow/tfjs-core`
- `@tensorflow/tfjs-backend-webgl`
- `@tensorflow-models/face-landmarks-detection`
- `react`
- `react-dom`
- `react-scripts`
- `react-webcam`

## Code Explanation

### App.js

This is the main React component. It initializes the webcam feed and the canvas, loads the face landmarks detection model, and periodically detects and draws facial landmarks.

### utilities.js

This file contains the `drawMesh` function, which is responsible for drawing the facial landmarks on the canvas. It uses the keypoints provided by the face landmarks detection model to draw dots and triangles on the detected face.

### Key Points

- **Webcam Initialization**: Uses the `react-webcam` component to capture video from the user's webcam.
- **TensorFlow.js Setup**: Initializes TensorFlow.js with the WebGL backend for optimal performance.
- **Model Loading**: Loads the MediaPipe FaceMesh model from TensorFlow.js.
- **Face Detection**: Periodically captures a frame from the webcam and uses the model to detect facial landmarks.
- **Drawing on Canvas**: Uses the `drawMesh` function to overlay the detected facial landmarks on the canvas.

## Troubleshooting

### Common Issues

- **Webcam Access**: Make sure your browser has permission to access the webcam. If you're running the application locally, use `localhost` instead of `127.0.0.1` to avoid mixed content issues.
- **Model Loading**: Ensure you have a stable internet connection to load the model from the CDN.

### Debugging Tips

- **Console Logs**: Use `console.log` to print debug information. Check the browser's developer console for any errors or warnings.
- **Canvas Dimensions**: Ensure the canvas dimensions match the video dimensions to properly overlay the facial landmarks.

## Contributing

Feel free to submit issues or pull requests if you have any improvements or fixes. Contributions are welcome!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
