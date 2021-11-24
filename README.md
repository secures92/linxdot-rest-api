# Linxdot REST API
This repository acts as unofficial documentation of the Linxdot REST API.

## Webinterface
These findings were discovered in the javascript code of the current web interface of a Linxdot miner. The webinterface can be accessed by navigating to ```https://<your-linxdot-ip>```. However this interface communicates with the miner using REST. To access data no authentication is needed.
    
## Helium Node Summary
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

There is also the option to add the GET paramter ```quick=true``` to the url
```
https://<your-linxdot-ip>/summary?quick=true
```
If the quick option is used only the following parameters are updated (unconpleted list)
```
"cpu_usage"
"mem_used"
"mem_total"
"swap_used"
"swap_total"
"temperature"
"time"
...
```

## Helium Stats
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

## Helium Activity
The activity of the miner can be accessed via:
```
https://<your-linxdot-ip>/activity
```
It with a json array containing the last 10 activites of the miner.

Example response:
```
[
  {"block": 1110469, "time": 1637763272, "amount": "0.0553", "type": "rewards_v2"}, 
  {"block": 1110437, "time": 1637761513, "amount": "0.0493", "type": "rewards_v2"}, 
  {"block": 1110399, "time": 1637759510, "amount": "0.0555", "type": "rewards_v2"}, 
  {"block": 1110367, "time": 1637757733, "amount": "0.0186", "type": "rewards_v2"}, 
  {"block": 1110325, "time": 1637755386, "amount": "0.0156", "type": "rewards_v2"}, 
  {"block": 1110290, "time": 1637752807, "amount": "0.0314", "type": "rewards_v2"}, 
  {"block": 1110256, "time": 1637750146, "amount": "0.0058", "type": "rewards_v2"}, 
  {"block": 1110220, "time": 1637747946, "amount": "0.0061", "type": "rewards_v2"}, 
  {"block": 1110173, "time": 1637745337, "amount": "0.0148", "type": "rewards_v2"}, 
  {"block": 1110140, "time": 1637743479, "amount": "0.0322", "type": "rewards_v2"}
]
```
TODO: List and document attributes
  
## Configure miner settings
The configuration of the miner is also done via REST. However this needs authentication.
TODO: Document the miner configuration

