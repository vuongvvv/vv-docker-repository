FROM justb4/jmeter:latest

#Install JMeter Plugin
COPY cmdrunner-2.2.jar ${JMETER_HOME}/lib
COPY jmeter-plugins-manager-1.3.jar ${JMETER_HOME}/lib/ext
RUN java -cp ${JMETER_HOME}/lib/ext/jmeter-plugins-manager-1.3.jar org.jmeterplugins.repository.PluginManagerCMDInstaller
RUN ${JMETER_HOME}/bin/PluginsManagerCMD.sh install jpgc-casutg
RUN ${JMETER_HOME}/bin/PluginsManagerCMD.sh status