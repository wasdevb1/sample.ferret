Ferret [![Build Status](https://travis-ci.org/WASdev/sample.ferret.svg?branch=master)](https://travis-ci.org/WASdev/sample.ferret)
======

This sample project contains a simple Servlet application called Ferret. Ferret listens for HTTP requests sent to `<host>:<port>/ferret[/*]`, and responds with information about the request and the server.

## Running in Eclipse with Maven

1. Download and install [Eclipse with the WebSphere Developer Tools](https://developer.ibm.com/wasdev/downloads/liberty-profile-using-eclipse/).
2. Create a new Liberty Profile Server. See [step 3](https://developer.ibm.com/wasdev/downloads/liberty-profile-using-eclipse/) for details.
3. Clone this repository.
4. Import the sample into Eclipse using *File -> Import -> Maven -> Existing Maven Projects* option.
5. Deploy the sample into Liberty server. Right click on the *ferret* sample and select *Run As -> Run on Server* option. Find and select the Liberty profile server and press *Finish*.
6. Go to: [http://localhost:9080/ferret](http://localhost:9080/ferret)

## Running with Maven

This project can be built with [Apache Maven](http://maven.apache.org/). The project uses the [Liberty Maven Plug-in](http://github.com/WASDev/ci.maven) to automatically download and install the Liberty with Java EE Web Profile 7 runtime from [Maven Central](http://search.maven.org/#search%7Cga%7C1%7Ccom.ibm.websphere.appserver.runtime). The Liberty Maven Plug-in is also used to create, configure, and run the application on the Liberty server. 

Use the following steps to run the application with Maven:

1. Execute the full Maven build. The Liberty Maven Plug-in will download and install the Liberty server.
    ```bash
    $ mvn clean install
    ```

2. To run the server with the Ferret sample execute:
    ```bash
    $ mvn liberty:run-server
    ```

Once the server is running, the application will be available under [http://localhost:9080/ferret](http://localhost:9080/ferret).

Please refer to the [ci.maven](http://github.com/WASDev/ci.maven) repository for documentation about using the Liberty Maven Plug-in.

## Running with Gradle

This project can also be built and run with [Gradle](https://gradle.org/). The provided `build.gradle` file applies the [Liberty Gradle Plug-in](http://github.com/WASDev/ci.gradle) and is configured to automatically download and install the Liberty with Java EE Web Profile 7 runtime from [Maven Central](http://search.maven.org/#search%7Cga%7C1%7Ccom.ibm.websphere.appserver.runtime). The Liberty Gradle Plug-in has built-in tasks that can be used to create, configure, and run the application on the Liberty server.
  
Use the following steps to run the application with the Gradle wrapper (Windows machines use `gradlew.bat`):

1. Execute the full Gradle build. The Liberty Gradle Plug-in will download and install the Liberty server.
    ```bash
    $ ./gradlew clean build
    ```
    
2. To start the server with the Servlet sample execute:
    ```bash
    $ ./gradlew libertyStart
    ```
    
    Alternatively, execute the run command:
    ```bash
    $ ./gradlew libertyRun --no-daemon
    ```
    
Once the server has started, the application will be available under [http://localhost:9080/ferret](http://localhost:9080/ferret).

3. To stop the server, execute:
    ```bash
    $ ./gradlew libertyStop
    ```  

Note, if Gradle is properly installed, Gradle commands can be executed directly using `gradle` and wouldn't require `gradlew`.

Please refer to the [ci.gradle](http://github.com/WASDev/ci.gradle) repository for documentation about using the Liberty Gradle Plug-in.

## Deploying to Bluemix

Click the button below to deploy your own copy of this application to [Bluemix](https://bluemix.net).

[![Deploy to Bluemix](https://bluemix.net/deploy/button.png)](https://bluemix.net/deploy?repository=https://github.com/WASdev/sample.ferret.git)

# Notice

© Copyright IBM Corporation 2014, 2017.

# License

```text
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
````

[Liberty Maven Plug-in]: https://github.com/WASdev/ci.maven

