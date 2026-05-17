FROM mcr.microsoft.com/devcontainers/python:3.12-bookworm

# Install udev (for serial port enumeration by MicroPico) and other tools
RUN apt-get update && apt-get install -y \
    udev \
    && rm -rf /var/lib/apt/lists/*

# Install Python tools
RUN pip install mpremote pyserial

# Give the default user access to serial devices
RUN usermod -aG dialout vscode