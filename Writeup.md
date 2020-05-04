## Write Up: 3D Motion Planning

<p align="center">
   
  <img width="805" height="593" src="https://user-images.githubusercontent.com/34810513/80971134-ed13cf80-8e39-11ea-8321-c2e53e64d603.jpg">
  
</p>

This Writeup.md considers the rubric points individually and describes how I addressed each rubric point in my implementation.  

---
### Writeup / README

#### 1. To provide a Writeup that includes all the rubric points and how I addressed each one.  

The current Writeup.md (markdown) file serves the purpose of addressing how I have dealt with the various tasks.

### Explaining the Starter Code

#### 1. Explaining the functionality of what's provided in `motion_planning.py` and `planning_utils.py`

This is my undertanding of the starter code:

1) The Drone initially spawns at the center of the map.
2) This is the global home by deafult. 
3) The center of the map (-north_offset, -east_offset)
is set as the starting point.
4) The goal is 10 meters to the north and 10 meters to the east of the starting point.
5) A path is calculated using A* algorithm and the waypoint is calculated.
6) The drone follows the waypoints and moves in a zigzag manner to the goal.

### Implementing Your Path Planning Algorithm

#### 1. Set your global home position
Here students should read the first line of the csv file, extract lat0 and lon0 as floating point values and use the self.set_home_position() method to set global home. Explain briefly how you accomplished this in your code.


And here is a lovely picture of our downtown San Francisco environment from above!
![Map of SF](./misc/map.png)

#### 2. Set your current local position
Here as long as you successfully determine your local position relative to global home you'll be all set. Explain briefly how you accomplished this in your code.


Meanwhile, here's a picture of me flying through the trees!
![Forest Flying](./misc/in_the_trees.png)

#### 3. Set grid start position from local position
This is another step in adding flexibility to the start location. As long as it works you're good to go!

#### 4. Set grid goal position from geodetic coords
This step is to add flexibility to the desired goal location. Should be able to choose any (lat, lon) within the map and have it rendered to a goal location on the grid.

#### 5. Modify A* to include diagonal motion (or replace A* altogether)
Minimal requirement here is to modify the code in planning_utils() to update the A* implementation to include diagonal motions on the grid that have a cost of sqrt(2), but more creative solutions are welcome. Explain the code you used to accomplish this step.

#### 6. Cull waypoints 
For this step you can use a collinearity test or ray tracing method like Bresenham. The idea is simply to prune your path of unnecessary waypoints. Explain the code you used to accomplish this step.



### Execute the flight
#### 1. Does it work?
It works!

### Double check that you've met specifications for each of the [rubric](https://review.udacity.com/#!/rubrics/1534/view) points.
  
# Extra Challenges: Real World Planning

For an extra challenge, consider implementing some of the techniques described in the "Real World Planning" lesson. You could try implementing a vehicle model to take dynamic constraints into account, or implement a replanning method to invoke if you get off course or encounter unexpected obstacles.


