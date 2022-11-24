<h1 align="center">Facial Recognition with OpenCV</h1>

&emsp;OpenCV is an open-source computer vision library supported by Intel. As a basic open-source project for computer vision, image processing and pattern recognition. It uses a face detector called Haar Cascade Classifier, which uses data stored in an XML file to determine the location of each local search image and detects it using its built-in function, which uses a Cascade Classifier trained on a target object to find rectangular regions in the image containing the target object and returns these regions as a sequence of rectangular boxes, with the final detection result stored in a variable.

&emsp;Haar features shown in the below image are used. They are just like convolutional kernels. Each feature is a single value obtained by subtracting sum of pixels under the white rectangle from sum of pixels under the black rectangle. 

<p align="center"><img src="lib/Haar_features.png"/>&nbsp;&nbsp;<img src="lib/Ex.1.png"/></p>

&emsp;Consider the image above on the right. The top row shows two good features. The first feature selected seems to focus on the property that the region of the eyes is often darker than the region of the nose and cheeks. The second feature selected relies on the property that the eyes are darker than the bridge of the nose. [1]

&emsp;Considering that the task we want to implement is relatively simple, the size of the dataset is relatively small, and the performance of Raspberry Pi is not enough for fast deep learning, so I used OpenCV-based face recognition. The QT library is used to develop the graphical interface under Raspbian (extended version of Debian), and the OpenCV image processing library is used as the basis to carry out various processes using the relevant functions provided in the library: image data are collected by the camera, face detection uses the trained Haar classifier to pattern match the collected images, and the detection results can be used for face image training and identity recognition.

&emsp; I have successfully built a car with a Raspberry Pi camera and hope to use convolutional neural networks in the future to achieve fully autonomous driving capabilities. Below I provided all the parts to build the car along with its workflow. 

<p align="center"><img src="lib/Parts.PNG" width=400px />&nbsp;&nbsp;<img src="lib/Workflow.PNG" width=400px /></p>

<h3 align="center">Simulations</h3>

<div align="center">
<table>
  <tr>
    <th>4 Predisents</th>
    <th>6 Presidents</th>
  </tr>
  <tr>
    <td> <p align="center"><img src="lib/sim1.gif" width=350px /></td>
    <td><img src="lib/sim2.gif" width=350px /></p></td>
  </tr>
</table>
</div>

<h2 align="center">Reference</h2>

[1]: [OpenCV: Cascade Classifier](https://docs.opencv.org/3.4/db/d28/tutorial_cascade_classifier.html)
