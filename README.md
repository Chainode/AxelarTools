# AxelarTools
## Monitoring Axelar Validator by using Grafana & Prometheus


## Scope

With this solution it will be possible to monitor both your Validator as well as the hardware your validator runs on. This will help you improve the overall health of your Validator as well as offer you proper insight into what happens in the Axelar network and with your machine at any point in time.  
Prometheus represents a monitoring solution for storing time series data like metrics. Grafana is another important tool which allows users to visualize the data stored in Prometheus and many more sources like Telegraf, etc. 

In combination with an Alertmanager it becomes a viable solution to monitor and improve the overall uptime and performance of your Validator.  Alertmanager can be used to define certain thresholds for which you will get alerted on Telegram, Discord, by SMS or many other options. Some example for possbile alerts: You can set your threshold for disk usage rate to 70% so that you will get alerted once that is reached in order to prepare for an upgrade for more disk space; low number of connected peers; validator is stuck (block height is not increasing over a period of time); validator is down and much more.  

