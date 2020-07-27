# Remote-run-Java-template

The template for running java applications in the on the Remote run system. 



## Requirements

When submitting a Java request the current context of the executable will be packaged and sent to the server. When on the server the mvn exec plugging will be used to start the program. Because of this to have a your java project run successfully you need to:
1. Have the mvn exex plugin in your pom.xml. example:
```xml
  		 <plugin>
           <groupId>org.codehaus.mojo</groupId>
           <artifactId>exec-maven-plugin</artifactId>
           <version>1.4.0</version>
           <configuration>
             <mainClass>org.example.bip.bop</mainClass>
           </configuration>
         </plugin>
```
2. Have all dependences from maven (preferred) and/or saved in the project dir.
3. Everything you want returned after the run is complete has to be saved to the the ./save_data dir
4.  For compatibility: The  container this is run in is running openjdk-14 gpu accelerated with Nvidia cards using cuda-10.1 and cudnn-8.

## Usage

To execute the executable called Remote-run and follow the instructions on screen. If all the requirements above are met you can run whatever you want.