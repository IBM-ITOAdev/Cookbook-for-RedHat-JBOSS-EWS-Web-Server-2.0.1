# Cookbook for RedHat JBOSS EWS (Web Server) 2.0.1  Content Pack

## Background:

The following was built for a customer using LA 132 and the bundled version logstash 1.5.3. This was tested using actual customer logfile samples. Links to vendor resources are provided as reference.

## Use:

1. Install LA 132 and the bundled logstash 1.5.3.
2. Copy the *-logstash.conf file to your logstash configuration directory. Keep in mind the LA bundled logstash version expects a certain location and filename by default.
3. Update the *-logstash.conf file based on your deployment. 
  - inputs to be used for ingestion approach (streaming via TCP, syslog, kafka, file, etc.
  - paths for your GROK patterns files
  - scala output configuration
  - others based on your environment and logfiles
4. Copy the *-GROK file to your logstash patterns directory. Update the logstash configuration to reflect this location.
5. Copy the *.header and *.props file to your $LAHOME/unity_content/DSVToolkit_v1.1.0.4/ directory.
6. Update the *.props file scalaHome: parameter based on your deployment.
7. Use the DSV Toolkit 'dsvGen.py' tool to build and deploy the DSV Content Pack.
8. Create a datasource in LA for each log type using your new DSV Content Pack.
9. Stream logs into LA using logstash.
10. Search!

## Resources: 

* Web: http://www.jboss.org/products/webserver/overview/
* Community: http://www.jboss.org/products/webserver/community/
* Docs: http://www.jboss.org/products/webserver/resources/
* Log Info: http://tomcat.apache.org/tomcat-7.0-doc/logging.html  (best I can tell logging is based on Apache/Tomcat)


