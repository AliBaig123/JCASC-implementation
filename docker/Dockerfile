
# Start with a specific Jenkins LTS image using Java 21
FROM jenkins/jenkins:2.568.3-lts-jdk21

# Copy the plugin list into the image
COPY --chown=jenkins:jenkins jenkins/plugins.txt /usr/share/jenkins/ref/plugins.txt

# Install the plugins listed in plugins.txt
RUN jenkins-plugin-cli \
    --plugin-file /usr/share/jenkins/ref/plugins.txt

# Copy the Jenkins Configuration as Code YAML file
COPY --chown=jenkins:jenkins jcasc/jenkins.yaml /usr/share/jenkins/ref/jenkins.yaml

# Tell the JCasC plugin where to find the configuration
ENV CASC_JENKINS_CONFIG=/usr/share/jenkins/ref/jenkins.yaml
