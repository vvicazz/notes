## **tomcat remote debugging**
set JPDA_ADDRESS=8000  
set JPDA_TRANSPORT=dt_socket  
./catalina.bat jpda start  

## **jvm args**
-noverify -XX:TieredStopAtLevel=1 -XX:+AlwaysPreTouch

## **java installation - ubuntu**
1. download jdk .deb file from oracle site
1. sudo dpkg -i jdk.deb
1. edit invironment sudo nano /etc/environment
   1. /usr/lib/jvm/jdk-11.0.7/bin
   1. JAVA_HOME="/usr/lib/jvm/jdk-11.0.7"
1. update alternatives
   1. sudo update-alternatives --install "/usr/bin/java" "java" "/usr/lib/jvm/jdk-11.0.9/bin/java" 0
   1. sudo update-alternatives --install "/usr/bin/javac" "javac" "/usr/lib/jvm/jdk-11.0.9/bin/javac" 0
   1. sudo update-alternatives --set java /usr/lib/jvm/jdk-11.0.9/bin/java
   1. sudo update-alternatives --set javac /usr/lib/jvm/jdk-11.0.9/bin/javac
1. verify
   1. update-alternatives --list java
   1. update-alternatives --list javac
   1. java -version
