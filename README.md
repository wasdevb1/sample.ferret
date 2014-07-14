Ferret
======

This sample project contains a simple Servlet application called Ferret. Ferret listens for HTTP requests sent to `<host>:<port>/ferret[/*]`, and responds with information about the request and the server.

## Running in Eclipse

1. Download and install [Eclipse with the WebSphere Developer Tools](https://developer.ibm.com/wasdev/downloads/liberty-profile-using-eclipse/).
2. Create a new Liberty Profile Server. See [step 3](https://developer.ibm.com/wasdev/downloads/liberty-profile-using-eclipse/) for details.
3. Clone this repository.
4. Import the sample into Eclipse using *File -> Import -> Maven -> Existing Maven Projects* option.
5. Deploy the sample into Liberty server. Right click on the *ferret* sample and select *Run As -> Run on Server* option. Find and select the Liberty profile server and press *Finish*. 
6. Go to: [http://localhost:9080/ferret](http://localhost:9080/ferret)

## Running with Maven

This project can be build with [Apache Maven](http://maven.apache.org/). The project uses [Liberty Maven Plug-in](https://github.com/WASdev/ci.maven) to automatically download and install Liberty profile runtime from the [WASdev repository](https://developer.ibm.com/wasdev/downloads/). Liberty Maven Plug-in is also used to create, configure, and run the application on the Liberty server. 

Use the following steps to run the application with Maven:

1. To activate the automatic download and installation of Liberty runtime, you will first need to obtain the Liberty license code. To obtain this code read the current [Liberty license](http://public.dhe.ibm.com/ibmdl/export/pub/software/websphere/wasdev/downloads/wlp/8.5.5.2/lafiles/runtime//en.html) and look for the `D/N: <license code>` line. Set the `IBM_LIBERTY_LICENSE` environment property with the license code found in the Liberty license file:
    ```bash
    $ export IBM_LIBERTY_LICENSE=<license code>
    ```

2. Execute full Maven build. This will cause Liberty Maven Plug-in to download and install Liberty profile server.
    ```bash
    $ mvn clean install
    ```

3. To run the server with the Ferret sample execute:
    ```bash
    $ mvn liberty:run-server
    ```

Once the server is running, the application will be available under [http://localhost:9080/ferret](http://localhost:9080/ferret).

# Notice

© Copyright IBM Corporation 2014.

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
