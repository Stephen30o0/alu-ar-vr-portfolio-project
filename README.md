DEMO VIDEO - https://drive.google.com/file/d/1hjxdfW_xcWo67JGLgtLgcw40MQ45VNba/view?usp=sharing

✅ Assets
LabScope's virtual science lab includes carefully chosen assets that support curriculum goals, realistic practice, and accessibility for students in Sub-Saharan Africa.

🔧 Key 3D Assets and Their Justification:
Asset Name	Use in LabScope
Chemistry Lab Tools	Beakers, test tubes, pipettes, and burners are interactable to simulate experiments like flame tests, mixing solutions, and heating compounds.
Flame Test Station	Includes burners and metal salts (e.g., Na, Cu, Li) that change flame color—key for demonstrating chemical reactions students rarely see live.
Biology Dissection Setup	Dissection tray, virtual frog, scalpel, pins, and labels. Students can explore anatomy and follow guided instructions to identify organs.
Interactive Periodic Table	Clickable periodic table linked to in-lab simulations. Enables exploration of elements and understanding properties.
Physics-based Object Interactions	Designed to simulate weight, texture, and response of real materials when moved or combined—helps bridge theoretical and practical learning.
Virtual Notebook + HUD	Floating instructional panels and a virtual lab journal for students to receive feedback, take notes, and log experiment data.
Lab Environment (3D Room)	Immersive virtual classroom with stations, posters, and safe zones that replicate a real-world lab, aiding in environmental familiarity.

🧠 Hardware Integration (Detailed for Evaluation)
LabScope is designed for seamless integration with Meta Quest 3 to enable an accessible, controller-free or controller-enhanced experience. It supports both hand tracking and controller input for flexibility in low-infrastructure environments.

🕹️ Interaction Design:
Hardware	Function in LabScope
Meta Quest 3 Headset	Immersive visual and auditory experience for conducting experiments and exploring environments.
Hand Tracking	Enables users to pick up beakers, dissect the frog, rotate the periodic table, and interact naturally with equipment.
VR Controllers	Optional input method for more precise actions—ideal for tasks requiring stable or guided manipulation.
In-Lab Navigation	Gaze-based teleporting or joystick-based movement allows users to walk to different stations within the lab environment.
Voice Guidance (Optional Future Feature)	Contextual audio guides explain steps and safety instructions in the student’s local language.

🧰 Development Stack:
Engine: Unity (2022 LTS)

SDKs: Meta XR SDK, OpenXR Plugin

Interaction Toolkit: Unity XR Interaction Toolkit

Design Prototyping: Figma (VR interface mockups and object layout)

This setup ensures the app is optimized for standalone VR headsets (like Meta Quest 3) while remaining lightweight enough for broad deployment in schools with limited resources.





📦 1. Prerequisites
Before you begin, make sure you have the following tools installed:

Tool	Version	Purpose
Unity Hub	3.5+	To manage Unity installations and projects
Unity Editor	2022 LTS (e.g., 2022.3.X)	Compatible with XR plugins and long-term support
Meta XR Plugin for Unity	Latest	VR integration with Meta Quest
OpenXR Plugin	1.8+	For VR cross-compatibility
Android SDK & NDK	Included via Unity Hub	Required for building to Meta Quest
Meta Quest 3 Headset	Updated firmware	To test the VR application in a real environment
(Optional) SideQuest	Latest	To install the APK file onto Meta Quest manually

🔧 2. Clone the Project Repository
bash
Copy
Edit
git clone https://github.com/your-username/labscope-vr.git
cd labscope-vr
🧰 3. Open the Project in Unity
Launch Unity Hub.

Click Open, then select the cloned labscope-vr folder.

Open the project and allow Unity to load dependencies (may take a few minutes on first run).

🧱 4. Project Structure Overview
bash
Copy
Edit
labscope-vr/
│
├── Assets/
│   ├── VRInteractions/           # XR interaction logic
│   ├── LabScenes/                # Folders for Chemistry, Biology labs
│   ├── UI/                       # HUD, buttons, tooltips
│   ├── Models/                   # 3D assets (frog, tools, periodic table)
│   └── Scripts/                  # C# scripts for logic, assessments
│
├── ProjectSettings/
├── Packages/
├── README.md
└── main.unity                    # Launch scene
🔌 5. Setup XR Plugin Settings
Go to Edit → Project Settings → XR Plug-in Management

Enable OpenXR for Android platform

Under OpenXR → Features, enable:

Hand Tracking

Oculus Touch Controller Profile

🎯 6. Build and Deploy to Meta Quest 3
⚠️ Connect your Meta Quest 3 to your PC using USB-C and enable Developer Mode

Go to File → Build Settings

Switch platform to Android

Add main.unity to Scenes In Build

Set resolution and quality for VR

Click Build and Run or Build and use SideQuest to install APK

📁 7. Testing & Interaction
Use hand tracking or Oculus controllers

Interact with lab tools by grabbing, rotating, or selecting items

Use gaze or pointer for UI elements

Navigate between lab scenes using floating menu

🧪 8. Optional Tools
Figma: Prototype files for UI and layout are located in docs/Figma-mockups.pdf

GitHub Issues: Use for bugs and feature requests

Video Demo: See demo-video.mp4 in the root directory for a full walkthrough

✅ Troubleshooting Tips
Issue	Solution
Scene not loading	Ensure main.unity is added to Build Settings
Input not working	Check XR Interaction Toolkit setup and controller bindings
APK won’t install	Rebuild and ensure Developer Mode is enabled on Quest
