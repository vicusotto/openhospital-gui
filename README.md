[![Build Status](https://travis-ci.org/informatici/openhospital-gui.svg?branch=master)](https://travis-ci.org/informatici/openhospital-gui)
# OpenHospital-gui
OpenHospital 2.0 (ISF OpenHospital web version) - WIP

**OpenHospital-core**
You need the openhospital-core in order to run the gui.

* clone [openhospital-core](https://github.com/informatici/openhospital-core)
* follow the instructions in the related README.md

**How to build with Maven:**
_(requires Maven 3.2.5 or lesser installed and configured)_

    mvn clean install
    
**How to create the DataBase**:

You need a local (or remote) MySQL server where to run the script in mysql/db/ folder

    create_all_en.sql
	
For remote MySQL server you need to change IP (localhost) and PORT (3306) in rsc/applicationContext.properties:

    <property name="jdbcUrl" value="jdbc:mysql://localhost:3306/oh" />

**With docker compose**

Simply run (it will run on localhost:3306 or check the 'default machine with IP' configured by your Docker-Machine):

    docker-compose up 

**How to launch the software**:

Use scripts startup.sh (Linux) or startup.cmd (Windows) from `target/OpenHospital20` folder.
Set `target/rsc/database.properties` according with your MySQL Server or docker container's IP and PORT

    startup.cmd

**Other info**

Please read Admin and User manuals in doc/ folder

# How to contribute

Please read the OpenHospital [Wiki](https://openhospital.atlassian.net/wiki/display/OH/Contribution+Guidelines)

See the Open Issues on [Jira](https://openhospital.atlassian.net/issues/)
