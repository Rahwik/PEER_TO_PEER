# Peer-to-Peer Connection

This project enables real-time peer-to-peer video and audio communication between users using WebRTC and Agora RTM. The system handles video and audio streams with dynamic connection management to provide a seamless user experience.

---

## Features

### 1. **Real-Time Communication**
- High-quality video and audio transmission.
- Peer-to-peer connectivity using WebRTC for direct media exchange.

### 2. **Dynamic User Management**
- Users are dynamically notified when others join or leave the channel.
- Real-time connection updates to handle participants' presence.

### 3. **Interactive Controls**
- Toggle camera and microphone on/off.
- Dynamic UI updates for video frames based on user activity.

### 4. **Robust Connection Handling**
- Utilizes STUN servers for network traversal.
- Ice-candidate exchange for establishing reliable connections.

### 5. **Cross-Browser Compatibility**
- Built using modern web APIs for compatibility across major browsers.

---

## Technologies Used

1. **Agora RTM SDK**: Handles messaging and signaling between users.
2. **WebRTC**: Enables peer-to-peer media exchange.
3. **JavaScript**: Core scripting language for interactivity and control.
4. **HTML/CSS**: UI layout and styling.

---

## Setup Guide

### Prerequisites
- A valid Agora App ID.
- Modern web browser (Chrome, Firefox, etc.).

### Steps to Run

1. **Clone the Repository**
   ```bash
   git clone <repository_url>
   cd <repository_name>
   ```

2. **Edit Configuration**
   Update the `APP_ID` variable in the JavaScript code with your Agora App ID:
   ```javascript
   let APP_ID = "your_agora_app_id";
   ```

3. **Serve the Application**
   Use a local server to serve the files (e.g., Live Server or Python HTTP server):
   ```bash
   python3 -m http.server
   ```

4. **Access the Application**
   Open the application in your web browser:
   ```
   http://localhost:8000
   ```

5. **Join a Room**
   Provide a unique `room` ID in the URL to start or join a session:
   ```
   http://localhost:8000?room=room123
   ```

---

## How It Works

1. **Initialization**
   - The application initializes an Agora RTM client.
   - Users are authenticated and joined to the specified channel.

2. **Media Management**
   - Local video and audio streams are captured using the `getUserMedia` API.
   - Streams are dynamically displayed in the UI.

3. **Peer Connection**
   - A WebRTC `RTCPeerConnection` is established for each peer.
   - Ice candidates and session descriptions are exchanged using Agora RTM messaging.

4. **Dynamic Updates**
   - When a user joins, the app creates an offer to connect.
   - When a user leaves, the UI updates accordingly.

---

## Project Structure

```plaintext
project-root/
├── index.html        # Main HTML file
├── style.css         # Styling for the application
├── app.js            # Core JavaScript file for logic
└── README.md         # Project documentation
```

---

## UI Overview

### Main Interface
- **Local Video**: Displayed in a larger frame when no remote users are connected.
- **Remote Video**: Shown when another user joins the session.

### Controls
- **Camera Toggle**: Enable/disable video stream.
- **Mic Toggle**: Enable/disable audio stream.

---

## Future Enhancements

- **Screen Sharing**: Add support for screen sharing during calls.
- **Text Chat**: Integrate a text chat feature alongside video/audio.
- **Recording**: Enable session recording for later playback.
- **Improved UI/UX**: Refine design for better usability.

---

## Troubleshooting

### Common Issues

#### 1. **Black Screen in Video**
- Ensure the camera is properly connected.
- Check browser permissions for camera access.

#### 2. **Audio Not Working**
- Verify microphone access in browser settings.
- Ensure no other application is using the microphone.

#### 3. **Connection Issues**
- Check network connectivity.
- Ensure STUN server URLs are accessible.

---

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute as needed.

---

## Acknowledgments

- [Agora.io](https://www.agora.io) for the RTM SDK.
- WebRTC community for the peer-to-peer communication framework.

---

## Contact

For any queries or feedback, feel free to reach out:
- **Email**: rahul.3057.12@gmail.com
- **GitHub**: [your_github_profile](https://github.com/rahwik)

---

### Happy Coding! ✨

