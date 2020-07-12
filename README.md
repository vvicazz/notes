## **tomcat remote debugging**
set JPDA_ADDRESS=8000  
set JPDA_TRANSPORT=dt_socket  
./catalina.bat jpda start  

## **jvm args**
-noverify -XX:TieredStopAtLevel=1 -XX:+AlwaysPreTouch
