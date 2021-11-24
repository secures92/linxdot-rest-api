# Linxdot REST API
This repository acts as unofficial documentation of the Linxdot REST API.

## Webinterface
These findings were discovered in the javascript code of the current web interface of a Linxdot miner. The webinterface can be accessed by navigating to ```https://<your-linxdot-ip>```. However this interface communicates with the miner using REST.

  
## Acessing miner data
  Until now two data access url could be discovered. This information can be accessed without authentication.
  
  ### Helium Node Summary
  The helium node summary contains a lot of information about the node status. It can be accessed via
  ```
  https://<your-linxdot-ip>/summary
  ```
  Example response:
  ```
  {
    "serial_number": "abcdef12", 
    "os_prefix": "linx", 
    "cpu_usage": 52.3, 
    "mem_used": 404, 
    "mem_total": 3743, 
    "swap_used": 0, 
    "swap_total": 0, 
    "storage_used": 5659, 
    "storage_total": 28216, 
    "temperature": 60, 
    "miner_height": 1100000, 
    "miner_listen_addr": "/ip4/XXX.XXX.XXX.XXX/tcp/44158", 
    "miner_listen_ok": true, 
    "hotspot_name": "some-miner-name", 
    "concentrator_model": "sx1302", 
    "region": "EU868", 
    "fw_version": "2021.11.23.0", 
    "ecc_sn": "ok", 
    "swarm_key_mode": false, 
    "address": "00000000000000000000000000000000000000000000000000", 
    "pub_key": "00000000000000000000 ... 0000000000000000000000000", 
    "eth_mac": "00:11:22:33:44:55", 
    "wlan_mac": "66:77:88:99:AA:BB", 
    "bt_mac": "CC:DD:EE:FF:00:11", 
    "uptime": 9343, 
    "time": 1637702568, 
    "last_panic": null, 
    "current_state": "lora_ready"
  }
  ```
  TODO: List and document attributes
  
  
  ### Helium Stats
  The helium stats contain information about the node status. It can be accessed via
  ```
  https://<your-linxdot-ip>/stats
  ```
  Example response:
  ```
  {
    "blockchain_height": "1,109,466", 
    "rewards_1d": 0.0, 
    "rewards_7d": 0.0, 
    "rewards_30d": 0.0, 
    "rewards_365d": 0.0, 
    "last_week": 0.0, 
    "oracle_price": 44.52, 
    "api_height": "1,109,466"
  }
  ```
  TODO: List and document attributes
  
  
## Configure miner settings
The configuration of the miner is also done via REST. However this needs authentication.
TODO: Document the miner configuration

