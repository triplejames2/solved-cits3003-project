Download Link: https://assignmentchef.com/product/solved-cits3003-project
<br>
The main project task

You are required to complete an implementation of a simple scene editor that allows a collection of objects to be arranged in a scene and various properties Of them to be changed, such as colour, shininess and texture. The specific items you have to implement are below, including sample videos.

Files provided

<ol start="2021">

 <li>Starting point – download the proj<u>ect-2021.zi</u>p file and extract somewhere safe. Inspect the skeleton file scene-start.cpp in the src subdirectory. Regardless Of your OS, this is the main file you should be able to edit to complete the project You will also need to edit the shader files in the res/shaders directory. Study the file, We will also keep a <u>liyg_lj.nk</u> to this file during the project phase to incorporate any student feedback to the instructions. The project requires you to use the mouse to move objects and light sources around. Click <u>here</u> if you need help to set up a 3 button mouse on the Mac.</li>

 <li>You will also have a zip file that contains many texture map files. This file can be downloaded <u>here </u>Note that, the provided files are for educational purpose only and cannot be publicly distributed The zip file contains a subdirectory named models-textures which should be placed in the res directory.</li>

 <li>The project will build all the dependencies you need from source (except for when using the lab pc’s or a mac, there it will use precompiled/OS provided libs for some or all as needed)</li>

</ol>

<h2>Project report</h2>

With your source code, each group must submit a project report that describes:

<ul>

 <li>For Which parts Of the project your solution works fine? Also mention the part(s) that you were unable to</li>

 <li>The steps you follo•.ved in building your program, focusing on the problems that you needed to solve in this process. This description can be brief.</li>

 <li>For those Who went beyond What is asked for in the project. you can use this document to also report the additional functionalitise.</li>

</ul>

There is no specific format of the report, and there are no explicit marks for this document. However, it has a very specific purpose. At your demo. you should expect your marker to have seen your report beforehand. Your report should be able to clearly show what worked in your solution (which you can later demonstrate), In your report, you can also take help from figures (e.g. screen shots) if you like Mention separately, what tasks you are unable to do. Do not use the report to give OS specific details. LJse a ReadMe file for that prupose. which can be as detailed as you like. Note that, the report is a necessary document for project submission. You may get heavily penalized for not submitting it, because your marker may not be able to assess your project accurately during a few minuts demo. Use this document wisely to secure the best grades and make your demo smootlm Only one report and one submission is required from each group.

<h2>Assessment Details</h2>

Your project has 100 marks and it Will be assessed based on correctness of the functionalities and coding (structure. clarity and appropriate use Of OpenGL). and your understanding reflected during the demonstration. Each task carries 10 marks. partial marks are possible with partially correct solutions.

<h2>Specific tasks that your scene editor should implement</h2>

Your scene editor needs to implement all the functionalities described in the items A to J below.

Dont panic if the videos provided alongside the items seem beyond what you have done in the labs. The project tasks have been chosen to cover all the relevant concepts Without requiring you to implement too much extra. Thus. much of the functionalities are already implemented in the skeleton code. and some of the tasks require similar code to what is in the skeleton code.

Also, you are allowed to improve upon the specification and implement some items differently, but you should explain in your report Why it is an improvement.

Although the videos provided below don’t have any audio, all the mouse actions were captured in the videos. We Suggest that you view each video in full Screen mode carefully. Please pay attention to the mouse icon shown inside the window.

<ul>

 <li>When the circle next to the mouse icon turns into red, it indicates that the left mouse button is held down _</li>

 <li>When the circle becomes green, it indicates that the middle mouse button is held down. When the wheel Of the middle mouse button is rolled, you should see an arrow and its direction.</li>

 <li>The right mouse button is reserved for bringing up the menu,</li>

</ul>

For your convenience, you can download the Zi<u>Q_file</u> (87MBl Of all the videos below.

<ol>

 <li>The skeleton code draws the ground, an initial mesh object and a sphere showing the position of a single point light source; however, it has the camera always facing the same way. You can move it forwards and backwards using the scroll wheel, via the viewOist variable, but there’s no way to move it otherwise. You should fix this problem in the code. The variables camRotUpAndOverCæg and camRoCSidewaysDeg are already set appropriately when moving the mouse with the left button down, or the middle button down (or shift • left button). Modify the display function so that the camera rotates around the centre point according to these variables, in the same way as the sample solution shown in the video below.</li>

</ol>

<table width="520">

 <tbody>

  <tr>

   <td width="520">A cameraRotate</td>

  </tr>

  <tr>

   <td width="520">Your scene editor should do the following:When the left mouse button is held down and dragged horizontally across the window, it should rotate the scene about the axis that is vertical to the ground plane.When the left mouse button is held down and dragged vertically up (or down) in the window, it should zoom into (or out of) the scene.+ Dragging the middle mouse button horizontally is the same as dragging the left button horizontally.+ Dragging the middle mouse button vertically up (or down) across the window should change the elevation angle of the camera looking at the ground plane. Correspondingly, this tilts the entire scene up (or down).See also the link here for some additional explanation.</td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Similarly, changing the location and scale of objects is already implemented, via the loc and scale members of the SceneObject structure, which is stored in the variable sceneObj s for each object in the scene. However, the angles array in this structure doesn’t affect what’s drawn, even though it is appropriately set to contain the rotations around the X, Y and Z axes, in degrees. Modify the drawMesh function so that it appropriately rotates the object when drawing it in the same way as the sample solution.</li>

</ol>

Note: The skeleton code also moves objects in different directions compared to the sample solution -you should also fix this (Hint: there is more than one way to do this).

<table width="520">

 <tbody>

  <tr>

   <td width="520">B objR0tateXYZ</td>

  </tr>

  <tr>

   <td width="520"> </td>

  </tr>

  <tr>

   <td width="520">As shown in the video, your scene editor should do the following:+ Dragging the left mouse button vertically across the window should rotate the current object about the x-axis (parallel to the ground plane and pointing to the right).Dragging the middle mouse button horizontally across the window should rotate the current object about the z-axis (parallel to the ground plane and pointing out of the screen).Dragging the left mouse button horizontally across the window should rotate the current object about the y-axis (vertical to the ground plane).</td>

  </tr>

 </tbody>

</table>

+ Dragging the middle mouse button vertically across the window should change the texture scale on the object.

Sometimes two of the rotations go the same way, as in the video below.

<table width="514">

 <tbody>

  <tr>

   <td width="514">B2 same rotation</td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Implement a menu item for adjusting the amounts of ambient, diffuse and specular light, as well as the amount of shine. Recall that the shine value needs to be able to increase to about 100 or so. Modify the materialMenu and makeMenuM functions so that they change the appropriate members of the SceneObj ect structure. The code to use these to affect the shading via the calculation for the light is already implemented in the skeleton code provided.</li>

</ol>

Follow the corresponding implementations of other similar menu items. Use the set ToolCa11backs function which has four arguments which are pointers to four float’s that should be modified when moving the mouse in the x and y directions while pressing the left button or the middle button (or shift + left button). After each callback function accepting a pair of (x,y) relative movements is a matrix which can be used to scale and rotate the effect of the mouse movement vector. See the calls to set ToolCa11backs in scene-start. cpp for example. The set Tool Callbacks function is defined in gnat i dread. h

<table width="520">

 <tbody>

  <tr>

   <td width="520">C materials</td>

  </tr>

  <tr>

   <td width="520">The sample video shows that+ the ambient or diffuse light of the object can be interactively changed by dragging the left mouse button horizontally or vertically;+ the specular light and amount of shine can be interactively adjusted by dragging the middle mouse button horizontally or vertically.+ the position of the light source can be modified by dragging the mouse button. For this functionality, you are suggested to use+ the left mouse button for changing the x- and z-coordinates+ the middle mouse button for changing the y-coordinates</td>

  </tr>

 </tbody>

</table>

of the light source’s position

<ol>

 <li>In the skeleton code, triangles are “clipped” (not displayed) if they are even slightly close to the camera. Fix the reshape callback function so that the camera can give more “close up” views of objects.</li>

</ol>

<table width="514">

 <tbody>

  <tr>

   <td width="514">D closeup</td>

  </tr>

  <tr>

   <td width="514">D closeup2</td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Also modify the reshape function, so that it behaves differently when the width is less than the height: basically whatever is visible when the window is square should continue to be visible as the width is decreased, similar to what happens if the window height is decreased starting with a square.</li>

</ol>

<table width="514">

 <tbody>

  <tr>

   <td width="514">E reshape</td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Modify the vertex shader so that the light reduces with distance – exactly how it reduces is up to you, but you should aim for the reduction to be noticeable without quickly becoming very dark, similar to the sample solution. This should apply to the first light, but the video shows a slightly different implementation so the second light was chosen from the menu to demonstrate the concept.</li>

</ol>

<table width="514">

 <tbody>

  <tr>

   <td width="514">F2 light reducing</td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Comment out the lighting calculations in the vertex shader and perform the lighting calculations in the fragment shader, so that the directions are calculated for individual fragments rather than for the vertices. This should have a very noticeable effect on the way the light interacts with the ground (especially when the ground has a plain texture map), since the ground only has vertices at the corners of a coarse grid.</li>

</ol>

<table width="514">

 <tbody>

  <tr>

   <td width="514">G light per frag</td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Generally specular highlights tend towards white rather than the colour of the object. Modify the shader code so that the specular component always shines towards white, regardless of the texture and the colour assigned to the object.</li>

</ol>

<table width="514">

 <tbody>

  <tr>

   <td width="514">H shine</td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Add a second light to both the C++ code and the shaders. The second light should be directional,</li>

</ol>

i.e., the direction that the light hits each surface is constant and independent of the position of the surface. In particular, use the direction from the second light’s location to the origin as the direction of the light. For example, moving the light source upward should increase the y-component of the direction of the light source, making the light source behave like the mid-day sun. Like the first light source, use sceneObj [2] to store the coordinates and colours of the second light, and make it similar to the first light, including placing a sphere at the coordinates of the light.

<table width="514">

 <tbody>

  <tr>

   <td width="514">I light2</td>

  </tr>

 </tbody>

</table>

<ol>

 <li>In your editor, allow (a) objects in the scene to be deleted, and (b) duplicated. (c) Add a spot light to the scene and allow its illumination direction to be changed interactively.</li>

</ol>