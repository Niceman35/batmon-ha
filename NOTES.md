## config.yaml
mqtt add on
* broker is exposed on host `core-mosquitto`
* https://developers.home-assistant.io/docs/add-ons/configuration/#options--schema
* https://github.com/hassio-addons/addon-zwavejs2mqtt/blob/main/zwavejs2mqtt/config.yaml
* https://github.com/hassio-addons/addon-zwavejs2mqtt/blob/d3549ff9d719bee4a770bba038ba3cfbb6bc72aa/zwavejs2mqtt/rootfs/etc/cont-init.d/configuration.sh


# RPI Dev
RaspiOS ships with python3 >= 3.9, so you just need to install pip3:
`sudo raspi-config` # set locale
`sudo apt update && sudo apt install -y python3-pip git`

```
cd batmon-ha
pip3 install -r requirements
```

```
echo "PATH=$PATH:/home/pi/.local/bin" >> ~/.bashrc
bleak-lescan
```

# Bluetooth Tools

Scan `bleak-lescan`
```
bluetoothctl 
connect C8:47:8C:F7:AD:B4
```

Explore BLE Device Services:
```
bleak/examples/service_explorer.py
```

