# 2. Create the Dockerfile for Your Ubuntu Container
# This Dockerfile (in app/Dockerfile) starts from the official Ubuntu image, installs any dependencies your project needs,
# and sets up an entrypoint to run your binaries. Customize the RUN and COPY steps based on your project's requirements
# (e.g., if your binaries are .deb packages, Python scripts, or compiled executables).

# Use a recent Ubuntu base image (e.g., 24.04 LTS for stability)
FROM ubuntu:24.04

# Set working directory
WORKDIR /app

# Install basic dependencies (customize as needed, e.g., for your project binaries)
RUN apt-get update && apt-get install -y \
    curl \
    wget \
    git \
    # Add more packages here, e.g., python3 if needed
    && rm -rf /var/lib/apt/lists/*

# Copy your project binaries/scripts into the image (assuming they're in the build context)
# If binaries are built externally, place them in app/binaries/ and COPY them here
#COPY binaries/ /app/binaries/

# Install your binaries (example: if they're executables, make them runnable)
#RUN chmod +x /app/binaries/your-main-binary

# Expose any ports your app needs (e.g., if it runs a server)
EXPOSE 8080
#EXPOSE 27017
#EXPOSE 7447

# Set the entrypoint to run your main binary/script
#ENTRYPOINT ["/app/binaries/your-main-binary"]
ENTRYPOINT ["/bin/bash"]
# Or use CMD if you want overridable commands: CMD ["/app/binaries/your-main-binary"]