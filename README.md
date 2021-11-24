# Linxdot REST API
This repository acts as unofficial documentation of the Linxdot REST API.

## Webinterface
These findings were discovered in the javascript code of the current web interface of a Linxdot miner. The webinterface can be accessed by navigating to ```https://<your-linxdot-ip>```. However this interface communicates with the miner using REST.

  
## Acessing miner data
  Until now two data access url could be discovered. This information can be accessed without authentication.
  
  #### Helium Node Summary
  The helium node summary contains a lot of information about the node status. It can be accessed via
  ```
  https://<your-linxdot-ip>/summary
  ```
  TODO: List attributes and example data
  
  
  #### Helium Stats
  The helium stats contain information about the node status. It can be accessed via
  ```
  https://<your-linxdot-ip>/stats
  ```
  TODO: List attributes and example data
  
  
## Configure miner settings
The configuration of the miner is also done via REST. However this needs authentication.
TODO: Document the miner configuration

