# SLO Simply Smarter

## 1) Apply best practices Host Group and Management Zone

- [quickstart-ace-configurator](https://github.com/dynatrace-ace-services/quickstart-ace-configurator)

## 2) Import Dynatrace: Simply Smarter
 - For Saas and Managed, use the [bizops configurator](https://dynatrace.github.io/BizOpsConfigurator/index.html#prerequisites)  
 Prerequisite : create your [token](https://dynatrace.github.io/BizOpsConfigurator/index.html#prerequisites)
 
       begin
       use your *tenant** and **token** (don't care with Source)
       connect
       deploy 
       .../ALL
       Dynatrace_Simply Smarter
       next
       advanced (you can define the owenr = admin)
       done
       
 
 ![image](https://user-images.githubusercontent.com/40337213/210232428-7de19b44-579a-4979-9e4e-6b9ef61bcc7a.png)  
 - For OffLine environment, follow the process [here](/Import_Dynatrace_Simply_Smarter_for_OffLine_environment.pdf)
 
## 3) Import SLO: Simply Smarter
 - Use [monaco](https://dynatrace-oss.github.io/dynatrace-monitoring-as-code/) (with export NEW_CLI=1)

       git clone https://github.com/dynatrace-ace-services/slo-simply-smarter
       cd slo-simply-smarter
       wget https://github.com/dynatrace-oss/dynatrace-monitoring-as-code/releases/latest/download/monaco-linux-amd64
       mv monaco-linux-amd64 monaco
       chmod +x monaco
       export NEW_CLI=1
       export MyTenant={your-environment-id}.live.dynatrace.com or {your-domain}/e/{your-environment-id}
       export MyToken=yyyy
       
       ./monaco deploy -e=environments.yaml SLOSimplySmarter
       
 ## 4) Mapp Dashboards with SLO
  
