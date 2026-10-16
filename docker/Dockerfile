# Project ini TIDAK install ROS/Gazebo/TurtleBot3/Webots lagi — semua sudah
# ada di base image, jadi build project ini sangat cepat dan tidak menambah
# ukuran disk untuk dependensi yang sama.
FROM robotics-base:humble

COPY docker/entrypoint.sh /entrypoint.sh
USER root
RUN chmod +x /entrypoint.sh
USER dev

WORKDIR /ws
ENTRYPOINT ["/entrypoint.sh"]
CMD ["bash"]
