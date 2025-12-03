# ROS 2 Humble + Ubuntu 22.04
FROM osrf/ros:humble-desktop

ENV DEBIAN_FRONTEND=noninteractive

# Install basics
RUN apt update && apt install -y \
    python3-colcon-common-extensions \
    python3-pip \
    git \
    nano \
    && rm -rf /var/lib/apt/lists/*

# ROS entrypoint
COPY ./ros_entrypoint.sh /ros_entrypoint.sh
ENTRYPOINT ["/ros_entrypoint.sh"]
CMD ["bash"]
