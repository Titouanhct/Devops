FROM jenkins/jenkins:lts-jdk21

ENV JAVA_OPTS=-Djenkins.install.runSetupWizard=false

COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN jenkins-plugin-cli -f /usr/share/jenkins/ref/plugins.txt

ENV CASC_JENKINS_CONFIG=/var/jenkins_home/casc_configs/my_marvin.yml
COPY ./my_marvin.yml /var/jenkins_home/casc_configs/my_marvin.yml
COPY ./job_dsl.groovy /var/jenkins_home/init.groovy.d/job_dsl.groovy
