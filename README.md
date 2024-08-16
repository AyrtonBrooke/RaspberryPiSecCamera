# RaspberryPi Security Camera
Raspberry Pi Motion-Triggered Security Camera with Email Alerts
This project sets up a motion-triggered security camera using a Raspberry Pi. When motion is detected, the camera captures an image and immediately sends it via email as an alert. This is useful for home security, remote property monitoring, wildlife observation, and other applications where real-time notifications are crucial.

# Features:
Motion Detection: Uses the motion package to detect movement in the camera's field of view.
Automatic Image Capture: Captures the best image when motion is detected and saves it locally.
Email Notifications: Automatically sends the captured image to a specified email address for immediate alerting.
Low Bandwidth Usage: Unlike live streaming, this setup uses minimal bandwidth, making it ideal for low-connectivity environments.
Easy Setup: Simple configuration and setup on a Raspberry Pi with a camera module.

# Getting Started
Create email to recieve pictures

I created on Gmail

Go into settings to accept access to third party apps

Clone the Repository:
git clone https://github.com/AyrtonBrooke/RaspberryPiSecCamera.git

# Navigate to directory
cd pi-motion-camera-alert

# Install the motion package
sudo apt-get update.

sudo apt-get install motion.

Ensure Python and necessary libraries are installed.

# Configure Motion:
Edit the motion.conf file:
sudo nano /etc/motion/motion.conf

daemon: Set this to on to run motion as a daemon (background service).

output_pictures: best to save the best images when motion is detected.

target_dir: Specify the directory where images will be saved.

on_picture_save: Add the command to run your email script whenever an image is saved.

Save and Exit

# Run the Script
Start the motion service:
sudo service motion start

Move in front of the camera to test the setup.

# Customize
Modify the Python script to suit your specific email configuration or alerting needs.

# Contributions
Feel free to submit pull requests or open issues to improve the project.
