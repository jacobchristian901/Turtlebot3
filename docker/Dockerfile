# Project ini TIDAK install ROS/Gazebo/TurtleBot3/Webots lagi — semua sudah
# ada di base image, jadi build project ini sangat cepat dan tidak menambah
# ukuran disk untuk dependensi yang sama.
FROM robotics-base:humble

USER root
RUN apt-get update && apt-get install -y --no-install-recommends \
    ros-humble-turtlebot3-cartographer \
    ros-humble-turtlebot3-teleop \
    ros-humble-nav2-map-server \
    ros-humble-tf2-tools \
    ros-humble-slam-toolbox \
    && rm -rf /var/lib/apt/lists/*

COPY docker/entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
USER dev
WORKDIR /ws
ENTRYPOINT ["/entrypoint.sh"]
CMD ["bash"]
