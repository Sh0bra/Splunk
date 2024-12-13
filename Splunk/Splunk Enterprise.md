# Splunk Enterprise
This is my documentation on Splunk and using it as a SIEM in the Security Operations Center

## Learning Objectives
- Deploy Splunk in a production environment
- Monitor endpoints using Splunk Universal Forwarder
- Customizing indexes to manage proper workflow

# Installing Splunk

At our Data Center we are running RHEL 9 on a HP Server.  
For installing Splunk we will be following the [installation instruction for Linux](https://docs.splunk.com/Documentation/Splunk/9.3.2/SearchTutorial/InstallSplunk#Linux_installation_instructions).
At this time Splunk offers .rpm, .tgz, .deb files but for RHEL we will use .rpm.

1. Download the .rpm file from [Splunk](https://www.splunk.com/en_us/download/splunk-enterprise.html). <br>
- Alternatively you can run <br>
```
wget -O splunk-9.3.2-d8bb32809498.x86_64.rpm "https://download.splunk.com/products/splunk/releases/9.3.2/linux/splunk-9.3.2-d8bb32809498.x86_64.rpm"
```
 but keep in mind to change the version number if it gets updated.

2. In your terminal navigate to the folder you downloaded the file and run <br>
```
rpm -i splunk-9.3.2-d8bb32809498.x86_64.rpm
``` 
<br>

> Keep in mind the name of the .rpm file may differ from yours.

3. Navigate to the default folder that Splunk gets installed <br>
```
cd /opt/splunk
```

4. Navigate to the binary directory to where the splunk binary lives
```
cd bin
```

5. Run the splunk binary to start the server
```
./splunk start
```

6. Accept license and create username and password for server

7. Login to http://localhost:8000 with username and password
