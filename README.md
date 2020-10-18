# Vulners-analyzer
 
This analyzer consists of 2 parts.
1. Checks network IOCs by Vulners Rst Threat Feed (including paid part)
2. Useful for vulnerability incidents to get information about vulnerabilities from Vulners database.

Vulners API key required.

## Setting up analyzer

~~~bash
$ git clone https://github.com/uchakin/Vulners-analyzer.git
$ cd Vulners-analyzer/Vulners
$ pip3 install -r requirements
~~~

After install the requirements you need to add Vulners folder to /Cortex-Analyzers/analyzers folder.
~~~bash
$ cp -R Path_where_you_dowloaded_Vulners/Vulners-analyzer/Vulners Path_to_Cortex-Analyzers/Cortex-Analyzers/analyzers/
~~~

## Setting up Vulners analyzer
Log into cortex with an account with the proper privileges then navigate ```Organization>Analyzers``` and click on Refresh analyzers button:
![cortex analyzer](screenshots/Cortex_vulners.PNG)​

After succesfully adding adding to Cortex, you need to enable it with Vulners API key:
![cortex analyzer](screenshots/Cortex_settings.PNG)​

Per default TheHive has no "CVE" Observable type, so we have to add this in the Admin settings:
![add observable](screenshots/theHive_add_cve.PNG)​

## Adding templates to TheHive

Log into TheHIVE with an account with the proper privilege level then navigate to ```>USER>Report templates```. 
![add template](screenshots/TheHive_templates.PNG)​

Add both short and long templates for Vulners analyzers:
![short template](screenshots/short_template.PNG)​

![long template](screenshots/long_template.PNG)​


### Testing Vulners analyzer (TheHive)

In the observables section add network IOCs to test.

The first one for network IOCs:
![short template](screenshots/iocs_long.PNG)​

![long template](screenshots/iocs_short.PNG)​

The second one for vulnerabilities:

![cve template](screenshots/animation.gif)​
