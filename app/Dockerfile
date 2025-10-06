FROM ubuntu:22.04

# Prevents interactive prompts during apt operations
ENV DEBIAN_FRONTEND=noninteractive

# Update package list and install basic tools (optional)
RUN apt-get update && apt-get install -y procps curl

# Keep the container alive forever
CMD ["tail", "-f", "/dev/null"]
