# Container running homeassistant with HACS pre-installed
ARG BUILD_FROM
FROM $BUILD_FROM

WORKDIR /config

# Rename the standard s6 homeassistant service to ha-guest
RUN mv /etc/services.d/home-assistant /etc/services.d/ha-guest

# Create the service directory for HACS installer
RUN mkdir -p /etc/services.d/hacs-installer
# Copy the run script and make it executable
COPY hacs-installer/run /etc/services.d/hacs-installer/run
RUN chmod +x /etc/services.d/hacs-installer/run

# Configure the entrypoint to be the s6-overlay init script
ENTRYPOINT [ "/init" ]
