# Turtlebot3 Navigations

Turtlebot3 package for autonomous navigation that uses the namespace `tb3`.

Tested on ROS Melodic Gazebo.


## Dealing with namespaces
When using namespaces and/or multiple robots, separate `yaml` files need to be created to reflect the new namespaced topics. These are the locations which need to be updated

- [**global_costmap_params**](./param/global_costmap_params.yaml)
  - 
- [**local_costmap_params**](./param/global_costmap_params.yaml)
  - 

To enable manual navigation via RVIZ, ensure the topics for the following are in the right namespace in your `rviz` config file:
- **Visualization Manager** :
  - `move_base_simple` in **Tools** -> `rviz/SetGoal`
  - `move_base/NavfnROS/plan` in **Display** -> `rviz/Path`

## Autonomous Mapping
The `explore_lite` launch file performs autonomous mapping of closed spaces. It uses the [explore_lite](http://wiki.ros.org/explore_lite) package, which can be installed as

```bash
sudo apt-get install ros-<DISTRO>-explore-lite
```