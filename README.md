# pythondeviceorientation
Flask/html program to draw the rotation in each axis for your android device

The application is a web-based tool that visualizes the rotation of a device in 3D space based on real-time gyroscope data. It uses the Device Motion API to capture the device's orientation and displays a simple 3D model (represented as a box) that rotates according to the device's movements. Below is a comprehensive description of the app, including its components, functionality, and how it works.

Overview of the Application

Purpose:

The application aims to demonstrate how a device's orientation can be visualized in a 3D space. It provides a visual representation of the device's rotation around the X, Y, and Z axes based on gyroscope data.
Technologies Used:
HTML: For the structure of the web page.
CSS: For basic styling of the page.
JavaScript: For handling device motion events and rendering the 3D model.
Three.js: A popular JavaScript library for creating and displaying animated 3D graphics in the browser.
Key Components

HTML Structure:

The HTML document includes a <head> section with meta tags, a title, and a link to the Three.js library. The <body> section is where the 3D rendering occurs.
Three.js Initialization:

The application initializes a Three.js scene, camera, and renderer. This setup is essential for creating and displaying 3D graphics.
A simple 3D box is created to represent the device. This box will be rotated based on the gyroscope data.
Device Motion Handling:
The application listens for devicemotion events, which provide real-time data about the device's rotation rates around the X, Y, and Z axes.
The gyroscope data is used to calculate the total rotation of the device by integrating the angular velocity over time.

nimation Loop:

The application includes an animation loop that continuously renders the scene and updates the rotation of the 3D model based on the integrated gyroscope data.
The rotation values are converted from degrees to radians (as required by Three.js) and applied to the 3D box.

Functionality

Real-Time Rotation Visualization:

As the user moves or tilts their device, the application captures the gyroscope data and updates the rotation of the 3D box in real-time. This allows users to see how their physical movements translate into 3D rotations.

User Interaction:

The application is designed to be interactive, responding to the device's movements without requiring any additional user input. Users can simply tilt or rotate their device to see the changes reflected in the 3D model.

Responsive Design:

The application is built to be responsive, adapting to different screen sizes and orientations. The canvas fills the entire browser window, providing an immersive experience.

How It Works

Initialization:

When the page loads, the Three.js scene, camera, and renderer are set up. A 3D box is created and added to the scene.
Listening for Device Motion:
The application listens for devicemotion events. When the device is moved, the event provides the gyroscope's rotation rates.

Calculating Rotation:

The application calculates the time difference between successive readings and integrates the angular velocity to update the total rotation angles for each axis.

Rendering the Scene:

The animation loop continuously renders the scene, updating the rotation of the 3D box based on the calculated rotation angles. This creates the visual effect of the box rotating in 3D space.

Displaying the Result:

The updated rotation is reflected in the 3D model, allowing users to see how their device's orientation changes in real-time.

Usage: Please create a template folder to store the index.html file under the folder that the python file resides.

