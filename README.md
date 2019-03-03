### References
**Building a world:** _*http://gazebosim.org/tutorials?tut=build_world*_ 
'<code>'
### Creating a world file
####1. Open a Gazebo simulation:
Click on <Edit> -> <Building Editor> and you should see the following page. Note there are three areas:
	**1. Platte:** You can choose models that you wish to add into the map here. \n
	**2. 2D View:** The only place you make changes to the map. \n
	**3. 3D View:** View only. \n
![p1](/images/p1.png)

####2. Import a floor plan
You may create a scene from scratch, or use an existing image as a template to trace over. On the **Platte**, click on '<import>' and selet a 2D map plan image in the shown prompt and click on **next**.
![p2](/images/p2.png)

To make sure the walls you trace over the image come up in the correct scale, you must set the image's resolution in pixels per meter _(px/m)_. To do so, click/release on one end of the wall. As you move the mouse, an orange line will appear as shown below. Click/release at the end of the wall to complete the line. Once you successfully set the resolution, click on "Ok" and the 2D map plan image you selected should show up in the 2D-View area.
![p3](/images/p3.png)

####3. Add & Edit walls
Select wall from **Platte**. On the **2D View**, click/release anywhere to start the wall. As you move the mouse, the wall's length is displayed. Click again to end the current wall and start an adjacent wall. Double-click to finish a wall without starting a new one. Double-clicking on an existing wall allows you to modify it. You can manipulate other models likewise. For more detailed instructions, please refer to _*http://gazebosim.org/tutorials?tut=build_world - automatic*_
![p4](/images/p4.png)

####4. Prepare a package
Before you save your world, you need to create a package for it so that you can use '<roslaunch>' to launch your world later!
Go to your catkin workspace
'<$ cd ~/catkin_ws/src>'
Create a package using the following command.
'<$ catkin_create_pkg ${your_package_name}>'
Open your package and create two folders **launch**, **worlds** and **models**.
'<$ cd ${your_package_name}>'
'<$ mkdir launch}>'
'<$ mkdir worlds>'
'<$ mkdir models>'

####5.Save your map
Once you finish editing the map, click on <file> -> <Exit Building Editor>. Please note that once you exit the editor, you are no longer able to make changes to the model.