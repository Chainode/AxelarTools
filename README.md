# AxelarTools
## Monitoring Axelar Validator by using Grafana & Prometheus


## Scope

With this solution it will be possible to monitor both your Validator as well as the hardware your validator runs on. This will help you improve the overall health of your Validator as well as offer you proper insight into what happens in the Axelar network and with your machine at any point in time.  
Prometheus represents a monitoring solution for storing time series data like metrics. Grafana is another important tool which allows users to visualize the data stored in Prometheus and many more sources like Telegraf, etc. 

In combination with an Alertmanager it becomes a viable solution to monitor and improve the overall uptime and performance of your Validator.  Alertmanager can be used to define certain thresholds for which you will get alerted on Telegram, Discord, by SMS or many other options. Some example for possbile alerts: You can set your threshold for disk usage rate to 70% so that you will get alerted once that is reached in order to prepare for an upgrade for more disk space; low number of connected peers; validator is stuck (block height is not increasing over a period of time); validator is down and much more.  

## Prerequisites
* Enable export of tendermint metrics --> please check ExposeTendermintMetrics in this repo: https://github.com/Chainode/AxelarTools/blob/main/ExposeTendermintMetrics.md 
* Prometheus  --> please check InstallPrometheus in this repo: https://github.com/Chainode/AxelarTools/blob/main/InstallPrometheus.md  
* Node Exporter  --> please check guide InstallNodeExporter in this repo: https://github.com/Chainode/AxelarTools/blob/main/InstallNodeExporter.md
* Grafana  --> please check guide InstallGrafana in this repo: https://github.com/Chainode/AxelarTools/blob/main/InstallGrafana.md
* Grafana Pie Chart plugin  --> please check guide InstallGrafana in this repo: https://github.com/Chainode/AxelarTools/blob/main/InstallGrafana.md  

## Import Axelar Validator Dashboard into Grafana  
For this you will have to download the AxelarValidatorDashboard.json from this repo and then in Grafana go to *Dashboards* -> *Manage* -> *Import* -> *Upload JSON file* and select the AxelarValidatorDashboard.json to be uploaded.  
During the import, the AxelarValidatorDashboard.json Grafana dashboard will automatically search for Prometheus datasources that contain "Axelar", "axelar" or "axe" in their name.  
This can be changed once the dashboard was imported by going to "Dashboard Settings" -> "Variables" -> "datasource" variable -> here you will see a parameter "Instance name filter" where the regex condition for selecting the Prometheus source was defined.
As a next step you should make sure the right Prometheus connection has been selected and if necessary adapt the Dashboard. 


## Final Result 

![image](https://user-images.githubusercontent.com/53407923/136711152-a659f941-dffe-4a3d-a0f0-e422e1294288.png)  
![image](https://user-images.githubusercontent.com/53407923/136711175-7deea285-cc02-44e6-8997-78c8fac0e839.png)

