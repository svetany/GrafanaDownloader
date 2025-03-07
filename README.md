## GrafanaDownloader
Download rendered panels from Grafana for given time interval  
Works with Grafana v6.4.4 on Java 8

### Arguments
```java
-start    Start of time interval  
-finish   End of time interval  
-config   Path to config file  
-out      Subfolder name for downloaded images  
```
### Start example
```java
java -jar GrafanaDownloader.jar -start 2020-02-20T20:00 -finish 2020-02-20T23:00 -config C:\User\config.txt -out Report
```
```python
### Config example
#Connection props  
grafana.protocol=http  
grafana.host=localhost  
grafana.port=3000  
grafana.login=admin  
grafana.password=admin  
grafana.token=eyJrIjoiajdWSzlkY2Z2Y0V5QjU0cmlkWU83S0tVVUIweE9VY00iLCJuIjoiYWRtaW4xIiwiaWQiOjF9  
  
#Metric props  
panels.count=3  
panels.height=500  
panels.width=1000  
  
#Env props  
java.timeMask=yyyy-MM-dd'T'HH:mm  
  
#Metric1 props  
metric1.dashboardName=local-util  
metric1.dashID=9b8LgEJZz  
metric1.panelId=2  
metric1.orgID=1  
metric1.output=test1.jpg  
  
#Metric2 props  
metric2.dashboardName=local-util  
metric2.dashID=9b8LgEJZz  
metric2.panelId=2  
metric2.orgID=1  
metric2.output=test2.jpeg  
  
#Metric3 props  
metric3.dashboardName=local-util  
metric3.dashID=9b8LgEJZz  
metric3.panelId=2  
metric3.orgID=1  
metric3.output=test3.png  
```
