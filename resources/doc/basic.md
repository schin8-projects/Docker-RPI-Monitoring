```mermaid
flowchart TD

    grafana --> prometheus 

    subgraph Monitoring 
        direction TB 
        grafana[Grafana] 
        prometheus[Prometheus] 

    end 

    prometheus --> cadvisor 
    prometheus --> pjob
    prometheus --> node-exporter 

    subgraph Jobs 
        direction TB 
        pjob[Prometheus] 
        cadvisor
        node-exporter 
    end    
    
    

   

    
```