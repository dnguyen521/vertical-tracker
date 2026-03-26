A free, AI-powered vertical jump tracker that runs entirely in your browser — no app download, no sign-up, no cost.


What it does
Vert Tracker uses your camera and Google's MoveNet AI model to watch your feet in real time. It detects the exact moment you leave the ground and the moment you land, then calculates your jump height from your air time using physics.
Works with a live camera feed or by uploading a pre-recorded video.

Features

📷 Live camera tracking — point your phone or webcam at yourself and jump
🎥 Video upload — analyze slow-mo or recorded footage
📏 Jump height — displayed in both inches and centimeters
⏱ Air time — measured in seconds to 3 decimal places
🏆 Session stats — best jump, average height, total jumps
📋 Jump log — scrollable history of every jump with a visual bar chart
🤖 Runs 100% in the browser — no data is sent anywhere


How to use

Open the live demo link on your phone or computer
Allow camera access when prompted
Set up your camera so your full body is visible — side or front angle works best
Click Start Camera
Stand still for ~1.5 seconds while it calibrates the floor position
Jump! Your height and air time will appear instantly after each jump

For video upload:

Click the Upload Video tab
Select a video file (MP4, MOV, WebM)
Click Analyze Video


Tips for best results

Distance — stand 6–10 feet from the camera so your full body fits in frame
Lighting — make sure your feet and ankles are clearly visible, not in shadow
Background — a plain background helps the AI track you more accurately
Slow-mo video — uploading slow-motion footage gives the most precise results
Shoes — wearing bright or contrasting shoes can improve ankle detection


How it works
Vert Tracker uses Google's MoveNet Lightning pose detection model via TensorFlow.js, loaded directly in the browser — no server required.

Calibration — on startup, it samples your ankle position for ~1.5 seconds to establish the floor reference line
Takeoff detection — when your ankles rise above the floor threshold, the jump timer starts
Landing detection — when your ankles return to the floor level, the timer stops
Height calculation — uses the physics formula h = g·t² / 8 where t is air time and g is 9.81 m/s²
Running locally
No build tools or installs needed. Just open the file:
bash# Clone the repo
git clone https://github.com/duynguyen/vert-tracker.git

# Open in your browser
open index.html
Or drag index.html into any browser window.
